# Use a firewall as a VPN fail-safe mechanism

If you simply add a VPN using common instructions, it generally "fails open". That means, if the VPN breaks down, 
because the connection is interrupted, traffic will be sent without the VPN. It is much safer when it "fails closed", 
meaning that when the VPN connection breaks down, the whole internet connection must be down as long as the VPN 
connection is not restored. If your [chosen VPN](vpn.md) does not include being able to 
set a kill switch, you can use your firewall as a fail-safe mechanism:

## Kill switch using pf

1. Get the IP address of the VPN gateway that the kill switch is intended for using the `host` command.
2. Get the network interface name connected to your default gateway and the subnet of the local network using the 
`route` command.
3. After connecting to the VPN, by running the command `ifconfig -a and searching for POINTOPOINT, find the interface used by the VPN:

```text
$ ifconfig -a | grep -i POINTOPOINT
utun0: flags=8051<UP,POINTOPOINT,RUNNING,MULTICAST> mtu 2000
```

4. Create a `killswitch.pf.conf` configuration file (The file can be created on the user $HOME directory and have any name):

```text
int_en1 = "[network interface name]"
vpn_utun1 = "[interface used by the VPN]"
vpn_ip = "[IP address of the VPN gateway]"

set block-policy drop
set ruleset-optimization basic
set skip on lo0

block all
block out inet6

# dns
pass quick proto {tcp, udp} from any to any port 53 keep state

# Allow broadcasts on internal interface
pass from any to 255.255.255.255 keep state
pass from 255.255.255.255 to any keep state

# Allow multicast
pass proto udp from any to 224.0.0.0/4 keep state
pass proto udp from 224.0.0.0/4 to any keep state

# Allow ping
pass on $int_en1 inet proto icmp all icmp-type 8 code 0 keep state

# Allow dhcp
pass on $int_en1 proto {tcp,udp} from any port 67:68 to any port 67:68 keep state

# Use only the vpn
pass on $int_en1 proto {tcp, udp} from any to $vpn_ip
pass on $vpn_utun1 all
```

5. Load the PF rules:

```text
$ sudo pfctl -Fa -f ~/killswitch.pf.conf -e
```

6. To disable:

```text
$ sudo pfctl -d
```

7. To load your system defaults (no kill switch):

```text
$ sudo pfctl -Fa -f /etc/pf.conf -e
```

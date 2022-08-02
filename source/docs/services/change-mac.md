# Change MAC address

A MAC address identifies the device connected to a network and allows the network to track, restrict or allow access 
based on it. Routers identify and assign static IP addresses based on the MAC addresses of devices. Before you try to 
change the MAC address, you need to know the value that you want to use.

Set the 2's place bit (the "locally administered" bit) in the first byte, to differentiate it from a guaranteed 
globally unique MAC address. Usually the first three bytes an unicast MAC address is an 
"Organizationally Unique Identifier" (OUI) that the IEEE assigned to the manufacturer of your Ethernet device. 
Manufacturers are required to make sure they keep the last 3 bytes unique. 

Avoiding all of that knowledge, the [MAC address generator tool](https://miniwebtool.com/mac-address-generator/) can 
generate a valid address for you.

If a specific MAC address, like `00:0a:95:9d:68:16`, is required:
```text
$ sudo ifconfig en0 00:0a:95:9d:68:16
```

To randomly generate new MAC address and assign it to `en0` network interface:

```text
$ openssl rand –hex6 | sed ‘s/(..)/1:/g; s/.$//’ | xargs sudo ifconfig en0 ether
```

When you restart your Mac computer, the Mac address reverts to the default. 

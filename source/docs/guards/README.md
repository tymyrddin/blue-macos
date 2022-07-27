# Introduction

There are many types of devices and mechanisms within the security environment to provide a layered approach of defense. 
This is so that if an attacker is able to bypass one layer, another layer stands in the way to protect the network. 
Two of the most popular and significant tools used to secure networks are firewalls and intrusion detection systems. 

## Choosing a firewall for a Mac

With a firewall, you can:

* Log hosts scanning services that aren't running.
* Limit the services that applications can connect to.
* Segregate the local network into trust segments (Local Area Network (LAN), DeMilitarised Zone (DMZ), and Internet).
* Redirect ports to the hosts providing the service (Network address translation (NAT)).

macOS has an [built-in firewall](https://support.apple.com/guide/mac-help/block-connections-to-your-mac-with-a-firewall-mh34041/mac), it is disabled by default, enable it with:

* Go to System Preferences -> Security & Privacy
* Click on the Firewall tab
* At the bottom of the window, click on the lock icon to enter your administrator password for changing the settings.
* Click the option to Turn On Firewall
* To configure the options for the firewall, click Firewall Options

The built-in firewall on your Mac only blocks inbound traffic. It does not allow you to control outbound connections. 
If you download a piece of malware, your Mac's firewall won't prevent it from connecting to the internet and sending 
out information. If you’d like to be more secure, install an additional firewall. 

* [Murus Lite](https://www.murusfirewall.com/) is an entry-stage firewall front end. It has inbound filtering and 
recording and can be used to safeguard applications. Although it is free, Murus Lite isn’t attempting to test or 
demonstrate. Instead, it is a fully-featured application that is a good beginning point for a new user.
* [Scudo](https://www.murusfirewall.com/scudo/) is a hybrid firewall for Mac that works as a combination of an outbound 
application-layer firewall and an inbound network-layer packet filter. The software offers enhanced protection to Mac’s network services from all the unwanted connections. It improves your privacy against remote computers trying to access your data through the network.
* [LuLu](https://objective-see.org/products/lulu.html) is a free, open source firewall that aims to block outgoing traffic unless it's explicitly approved by the user. Once installed, it will alert you about new or unauthorized attempts to create an outgoing network connection. Click the Allow or Block button to handle the connection.
* [Radio Silence](https://radiosilenceapp.com/) is the simplest firewall app for your Mac. After installation, the app automatically runs in the background without any menu bar icon or other visual indicators. Navigate to the Firewall tab and click the Block Application button. Once you add an app to the blacklist, it will no longer connect over the internet.
* [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html) is a host-based application firewall for Mac. The app provides detailed reports on processes, outgoing and incoming connections, ports, and protocols. It also shows the complete traffic history down to a one-minute interval time range. The Network Monitor shows a global map of the active connections from your system to the IP-derived or probable locations around the world in real-time. The left panel displays a list of apps sending and receiving data, while the right panel gives you a detailed summary.

## Choosing a HIDS for a Mac

Most of the [HIDS tools for macOS](ids.md) are File Integrity Agents (FIAs) and use Error Detection algorithms. A FIA 
monitors the integrity and state of the files and objects on a machine. It creates a hash of all files to be monitored. 
That snapshot is periodically checked against the current hash of the files. If it detects changes to those files, then 
it alerts the administrator that an unauthorised access or change has taken place. 

[OSSEC](ossec.md) monitors the checksum signatures of all the log files to detect possible interference and any 
attempts to get to the root account.

## Related attack trees

* [Scanning](attack-trees:docs/scanning/README)
* [Malware](attack-trees:docs/malware/README)
* [System](attack-trees:docs/system/README)
* [Network](attack-trees:docs/network/README)
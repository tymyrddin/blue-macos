# Introduction

There are many types of devices and mechanisms within the security environment to provide a layered approach of defense. 
This is so that if an attacker is able to bypass one layer, another layer stands in the way to protect the network. 
Two of the most popular and significant tools used to secure networks are firewalls and intrusion detection systems. 

## Choosing a firewall for a Mac

With a firewall, you can:

* Log hosts scanning services that aren't running.
* Limit the services that programs can connect to.
* Segregate the local network into trust segments (Local Area Network (LAN), DeMilitarised Zone (DMZ), and Internet).
* Redirect ports to the hosts providing the service (Network address translation (NAT)).

macOS has an [built-in firewall](https://support.apple.com/guide/mac-help/block-connections-to-your-mac-with-a-firewall-mh34041/mac), it is disabled by default, enable it with:

* Go to System Preferences -> Security & Privacy
* Vlick on the Firewall tab
* At the bottom of the window, click on the lock icon to enter your administrator password for changing the settings.
* Click the option to Turn On Firewall

If you’d like to be more secure, install a firewall. 

* [Murus Lite](https://www.murusfirewall.com/) is an entry-stage firewall front end. It has inbound filtering and 
recording and can be used to safeguard applications. Although it is free, Murus Lite isn’t attempting to test or 
demonstrate. Instead, it is a fully-featured application that is a good beginning point for a new user.
* [Scudo](https://www.murusfirewall.com/scudo/) is like a hybrid firewall for Mac that works as a combination of an outbound application-layer firewall and an inbound network-layer packet filter. The software offers enhanced protection to Mac’s network services from all the unwanted connections. It improves your privacy against remote computers trying to access your data through the network.

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
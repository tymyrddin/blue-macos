# Use a Tor proxy

## Tor proxy

Install:

    $ brew install tor

Start it: 

    $ tor

## Set network proxy settings via System Preferences

* Go to System Preferences > Network
* From Location dropdown at the top, select Edit Locations
* Create a new location by hitting the plus button and name it Tor. 
* Hitting Done will select the new location which is now ready to be configured.
* Go to Advanced > Proxies and activate SOCKS Proxy and add:

```text
SOCKS proxy server: localhost
Port: 9050
```
Now you can switch to this location from your menu bar under Location whenever you start up Tor. 
Switching to the Tor location routes all network traffic on your system through Tor. You have to repeat these steps 
for every network interface, ethernet, Wi-Fi.

## Notes

* If a government makes their own national internet, or routes traffic through specific servers to use deep packet inspection (DPI), running Tor may not provide security if the government is able to see the entire path. 
* Sometimes the Tor network is censored, and clients can't connect to it. An increasing number of censoring countries are using Deep Packet Inspection (DPI) to classify Internet traffic flows by protocol. While Tor uses bridge relays to get around a censor that blocks by IP address, the censor can use DPI to recognize and filter Tor traffic flows even when they connect to unexpected IP addresses. With pluggable transports, censorship against Tor can be bypassed.
* Not only that. If an attacker can see your traffic, and can see the website you're visiting, even with a path outside the adversary's control - they will still be able to correlate the traffic and learn you are visiting the website.
* If the same connection (the same set of relays) were to be used for a longer period of time a Tor connection could be vulnerable to statistical analysis, which is why the client software changes the entry node every ten minutes.


# Securing Network Communications
#### DEF CON for N00bs - Essential

## The Problem
The networks at DEF CON, both wired and wireless, should be considered extremely hostile at all times. Regardless of the threat actor (pranksters to black hats), this should be kept in mind with all gear with a radio. Cellular, WiFi, Ethernet, etc. are all under constant attack at this event.

### What can we do?
With all of this in mind, securing network communications at DEF CON may seem like a daunting task. However, there are some solutions which can be implemented with relative ease.

## VPN
First and foremost is setting up a VPN to secure your channel. For the uninitated, a Virtual Private Network (VPN) is capable of encrypting all network traffic between one sourcfe and another. It is possible to setup a VPN on all of your devices to protect their communications during the event.
For the purpose of this write-up, I am going to refer to OpenVPN as it is a FOSS project, and there are many ways to either implement it yourself, or to use a 3rd party hosted service. @hon1nbo personally recommends using PfSense in a cloud or self-hosted deployment, as it is easy to configure OpenVPN, has great firewall support, and is a great firewall / routing system to learn in general.

You will want to configure your OpenVPN deployment with a Full Tunnel, including DNS lookups, using an AES algorithm. This can be installed locally on your devices for communication. Ideally, you should use a prepaid hotspot or similar at the event to act as a buffer for your wireless radios. You can currently walk into a store and procure a prepaid hotspot with good ol' cash and without using real names through a few vendors in true DEF CON fashion. This will also enable you to not rely on the hotel at the event for internet.

Furthermore, with PfSense it is possible to run a fireall on your laptop using VMs that will isolate your trusted host or VMs from the Defcon networks.

Diagrams for both of these scenarios are provided.

Image references:

![WWAN Prepaid Hotspot](/images/wwan_prepaid_hotspot_vpn.jpg)

![Secure Laptop Architecture](/images/secure_laptop_wifi.jpg)

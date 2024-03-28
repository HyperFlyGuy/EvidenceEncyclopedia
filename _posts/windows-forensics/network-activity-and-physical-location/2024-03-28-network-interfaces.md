---
title: "Network Interfaces"
layout: post
permalink: /network-interfaces
categories: Network-Activity-and-Physical-Location
---
## Location and Format

The below registry keys will help us gather information on particular network interfaces.

- SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces
- SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkCards

## Purpose

The above registry keys will allow us to list available network interfaces and the last known configurations that they used.

## Forensic Uses

These keys will allow you to find the last known IP address, DHCP, and domain for both physical and virtual network adapters. There may be more historical data present in the various sub keys. The "NetworkCards" key will provide a more detailed view of network availability. Two caveats  about these two keys is that they are mapped via the interface GUID value and they are unlikely to provide a complete view of every connected network.

## Analysis Tools 



## Example Analysis

pending
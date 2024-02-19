---
title: "Network History"
layout: post
permalink: /network-history
categories: Network-Activity-and-Physical-Location
---
## Location and Format

There are many registry keys that will allow us to identify networks that the system has connected to. With many systems be portable you can expect these registry keys to contain a goldmine of information.

    - SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces
    - SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkCards
    - SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Signatures\Unmanaged
    - SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Signatures\Managed
    - SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Nla\Cache
    - SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Profiles

## Purpose

These keys will give us the ability to identify networks that a computer has connected to. Information that we may be able to get from these locations includes:

    - Domain name/Intranet Name
    - SSID
    - First/Last time connected
    - Gateway MAC Address

## Forensic Uses

The above registry keys are not neccessarily valuable on their own. However, when correlated together they offer you a near perfect picture of network activity. Only certain registry keys can be correlated, below you will find how they link together.

    - Interface info keys can be correlated to other keys via DhcpDomain value
    - Signature and Profile keys are correlated via the network ProfileGUID value

The network information from these keys will include VPN connections and the MAC Address of SSID for Gateway can assist with device geolocation(super cool!).Below we will provide the Network Profile NameType values:

    - 6 (0x06) = Wired
    - 23 (0x17) = VPN
    - 71 (0x47) = Wireless
    - 243 (0xF3) = Mobile Broadband

## Analysis Tools 

https://www.sans.org/tools/registry-explorer/

## Example Analysis

pending
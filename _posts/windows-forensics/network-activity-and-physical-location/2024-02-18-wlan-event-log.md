---
title: "WLAN Event Log"
layout: post
permalink: /wlan-event-log
categories: Network-Activity-and-Physical-Location
---
## Location and Format

There is a relatively new event log that will help us identify wireless network connections.

    -  WIN7+ - %SYSTEM ROOT%\System32\winevt\logs\Microsoft-Windows-WLAN-AutoConfig Operational.evtx

## Purpose

These event logs are a historical view of wireless network associations.

## Forensic Uses

Provides historical record of wireless network connections. SSID can be used to correlate and retrieve additional network information from Network History registry key
Relevant Event IDs:
 - 11000 – Wireless network association started
 - 8001 – Successful connection to wireless network
 - 8002 – Failed connection to wireless network
 - 8003 – Disconnect from wireless network
 - 6100 – Network diagnostics (System log)

## Analysis Tools 

- https://eventlogxp.com/

## Example Analysis

pending
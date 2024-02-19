---
title: "System Last Shutdown Time"
layout: post
permalink: /last-system-shutdown-time
categories: System-Information
---
## Location and Format

The registry keys that track the last time the system was shutdown are located at

    - SYSTEM\CurrentControlSet\Control\Windows (Shutdown Time)
    - SYSTEM\CurrentControlSet\Control\Watchdog\Display (Shutdown Count – WinXP only)

## Purpose

This registry key is the last time the system was shutdown. If the system is Windows XP the number of shutdowns will also be recorded.

## Forensic Uses

Being able to determine the last time that the system was shutdown can let us detect user behavior and system anomalies. It is important to realize that this key value is stored in Windows 64-bit FILETIME format.

## Analysis Tools 

https://www.sans.org/tools/registry-explorer/

## Example Analysis

pending
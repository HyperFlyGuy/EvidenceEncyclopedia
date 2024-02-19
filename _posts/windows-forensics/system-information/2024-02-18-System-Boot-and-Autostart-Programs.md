---
title: "System Boot and Autostart Programs"
layout: post
permalink: /boot-autostart-programs
categories: System-Information
---
## Location and Format

The registry keys below are often called "Autostart" locations. These registry keys are located at:

    - NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Run
    - NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\RunOnce
    - SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce
    - SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer\Run
    - SOFTWARE\Microsoft\Windows\CurrentVersion\Run
    - SYSTEM\CurrentControlSet\Services
         - If Start value is set to 0x02, then service application will start at boot (0x00 for drivers) 

## Purpose

Quite simply, system boot and autostart programs are lists of programs that will run when the system is booted or the user logs in.

## Forensic Uses

These keys are often abused by malware to establish persistence on a system. However, they can also be used to audit for software that is installed on the system that maybe shouldn't be (policy violation scenarios). This list is not exhaustive but it can allow us to catch some low hanging fruit. 

## Analysis Tools 

https://www.sans.org/tools/registry-explorer/

## Example Analysis

pending
---
title: "BAM and DAM"
layout: post
permalink: /bam-and-dam
categories: Application-Execution
---
## Location and Format

The Windows Background/Desktop Activity Moderator (BAM/DAM) are located in two SYSTEM registry keys **"SYSTEM\CurrentControlSet\Services\bam\state\UserSettings\<SID>"** and **"SYSTEM\CurrentControlSet\Services\dam\state\UserSettings\<SID>"** respectively.

## Purpose

The Windows BAM/DAM is a Windows service that controls the activity of background applications. It was introduced in Windows 10 as a new feature.

## Forensic Uses

The BAM/DAM will provide us with the full path of the executable along with last execution date and time. It is worth noting that BAM/DAM will only be updated if the executable is run locally on the system and excludes network shares or removable media. In addition to this console applications will not be tracked in BAM/DAM. After 7 days in the BAM/DAM entries will be removed on reboot.

## Example Analysis

pending
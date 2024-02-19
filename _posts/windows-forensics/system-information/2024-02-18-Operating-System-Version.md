---
title: "Operating System Version"
layout: post
permalink: /operating-system-version
categories: System-Information
---
## Location and Format

There are two registry keys that help us identify the Operating System Version. These keys are:

    - SOFTWARE\Microsoft\Windows NT\CurrentVersion
    - SYSTEM\Setup\Source OS 

## Purpose

These keys determine the operating system type, version, build number, and installation dates for the current installation and previous updates.

## Forensic Uses

Information about what can be found under each key is detailed below.

    - SOFTWARE\Microsoft\Windows NT\CurrentVersion
        - ProductName, EditionID – OS type
        - DisplayVersion, ReleaseId, CurrentBuildNumber – Version info
        - InstallTime – Installation time of current build (not original installation)

    - SYSTEM\Setup\Source OS (NOTE: these keys are created for each historical OS update)
        - ProductName, EditionID – OS type
        - BuildBranch, ReleaseId, CurrentBuildNumber – Version info
        - InstallTime – Installation time of this build version
        - Times present in names of Source OS keys are extraneous:
            - InstallTime = 64-bit FILETIME format (Win10+)
            - InstallDate = Unix 32-bit epoch format (both times should be equivalent)

## Analysis Tools 

https://www.sans.org/tools/registry-explorer/

## Example Analysis

pending
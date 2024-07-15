---
title: The Kusto Query Quick Reference
author: Hyper Fly Guy
date: 2024-06-27
category: Jekyll
layout: post
---

Content Coming Soon

### DCOM Hijacking Detection

    union DeviceFileEvents,DeviceProcessEvents,DeviceImageLoadEvents,DeviceProcessEvents
    | where (FolderPath contains "C:\\Program Files\\Common Files\\System\\UxTheme.dll" and InitiatingProcessFileName == "prevhost.exe")
    or (FolderPath contains "C:\\Program Files\\Windows NT\\Accessories\\XmlLite.dll" and InitiatingProcessFileName == "wordpad.exe")
    or (FolderPath contains "C:\\Windows\\System32\\oobe\\USERENV.dll" and InitiatingProcessFileName == "dllhost.exe")
    or (FolderPath contains "C:\\Program Files\\Common Files\\System\\Ole DB\\bcrypt.dll" and InitiatingProcessFileName == "dllhost.exe")
    or (FolderPath contains "C:\\Program Files\\Common Files\\Microsoft Shared\\ink\\DUI70.dll" and InitiatingProcessFileName contains "ShapeCollector.exe")
    or (FolderPath contains "C:\\Windows\\System32\\wbem\\wbemcomn.dll" and InitiatingProcessFileName == "unsecapp.exe")
    or (FolderPath contains "C:\\Windows\\System32\\wbem\\wbemcomn.dll" and InitiatingProcessFileName == "scrcons.exe")
    or (FolderPath contains "C:\\Windows\\System32\\WinBioPlugIns\\MFPlat.dll" and InitiatingProcessFileName == "svchost.exe")
    or (FolderPath contains "C:\\Program Files (x86)\\Windows Media Player\\ATL.dll" and InitiatingProcessFileName == "setup_wm.exe")
    or (FolderPath contains "C:\\Program Files (x86)\\Windows Media Player\\PROPSYS.dll" and InitiatingProcessFileName == "wmplayer.exe")
    | summarize count() by DeviceName, FileName

## Sources

https://www.kustoking.com/
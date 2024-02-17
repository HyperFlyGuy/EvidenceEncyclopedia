---
title: "Onedrive Artifacts"
layout: post
permalink: /onedrive-artifacts
categories: Cloud-Storage
---
## Location and Format

There are alot of locations that we need to be aware of if we are going to begin looking at cloud storage artifacts in general. We will try to be as clear and concise as possible when detailing them below. 
- Default Local File Storage:
-- %USERPROFILE%\OneDrive (Personal)
-- %USERPROFILE%\OneDrive - Company Name (Business)
- File Storage Folder Location Info:
-- NTUSER\Software\Microsoft\OneDrive\Accounts\Personal|Business1
- File Metadata:
-- %USERPROFILE%\AppData\Local\Microsoft\OneDrive\logs\Personal|Business1
--- SyncDiagnostics.log
--- SyncEngine “odl” logs
-- %USERPROFILE%\AppData\Local\Microsoft\OneDrive\settings\Personal|Business1
---  UserCid.dat

## Purpose

Onedrive is the cloud storage solution provided by Microsoft. It is integrated into the windows operating system, but before it can be used the user has to provide authentication through their Microsoft Cloud Account. 

## Forensic Uses

Examining cloud storage solutions can be overwhelming from a forensics perspective, which is complicated even further if the analysis is on a personal account. There are three key things that you need to understand when beginning your analysis.
- It is CRUCIAL to check the registry and confirm the local file storage location
- Metadata files (see above) are the meat and potatoes of your analysis. The syncdiagnostics.log will have more recent sync actions that have occurred. The .odl files are the standard format that Ondrive stores its logs in. Below is a github project that will assist in parsing the .odl files.
- Some files may only be stored in the cloud and will not be stored locally
It is also worth mentioning that deleted items will be stored in an online recycling bin for 30 days(personal) and 93 days(business). This gives us the possibility of some evidence recovery! If your business uses Microsoft 365 there are "Onedrive for Business Unified Audit Logs" that will provide 90 days of user activity logging.

## Analysis Tools 

https://github.com/Beercow/OneDriveExplorer

## Example Analysis

pending
---
title: "Win10 Timeline"
layout: post
permalink: /win10timeline
categories: Application-Execution
---
## Location and Format

The Windows 10 timeline artifact is located at **"C:\Users\USERPROFILE\AppData\Local\ConnectedDevicesPlatform\ACCOUNT-ID\ActivitiesCache.db"**

## Purpose

The Windows 10 timeline is a newer artifact and allows a user to travel back in time to view previous versions of files and windows. Depending on system settings your timeline artifact can go back up to 30 days! It is a feature that is accessible from the task view of the windows desktop. If you scroll down in task view you should begin to see previous versions of recently accessed files. This data is kept in the form of a sqlite database.

## Forensic Uses

The sqlite database format allows us to pivot around the data this artifact provides rather quickly. The timeline database provides us loads of information including:

    - Full path of executed application
    - Start time, end time, and duration
    - Items opened with an application
    - URLs visited 

**Please note that this feature was depreciated with Win11 but the database appears to still be present even in Win11.**

## Example Analysis

pending
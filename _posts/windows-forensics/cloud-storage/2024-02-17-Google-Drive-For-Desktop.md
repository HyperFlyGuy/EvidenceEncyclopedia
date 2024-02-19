---
title: "Google Drive For Desktop Artifacts"
layout: post
permalink: /google-drive-for-desktop-artifacts
categories: Cloud-Storage
---
## Location and Format

Similar to other cloud storage applications there are a few locations that you need to be aware of.

    - Local drive letter for virtual volume and account ID
        - NTUSER\Software\Google\DriveFS\Share\
    - Default local file cache
        - %USERPROFILE%\AppData\Local\Google\DriveFS\accountidentifier\content_cache
    - File metadata
        - %USERPROFILE%\AppData\Local\Google\DriveFS\accountidentifier\metadata_sqlite_db

## Purpose

Google Drive for Desktop is the new name for the merged Google Backup and Sync applications. It uses a virtual FAT32 volume named "My Drive" which is only accessible when the user is logged in.

## Forensic Uses

The assigned drive letter can allow us as analysts to tie folder and file access artifacts to Google drive. Similar to Onedrive, if you use Google Workspace you can use the admin reports that will provide 180 days of user activity logging! The metadata is stored in a sqlite database (metadata_sqlite_db) and it uses the protobuf format for many of the important fields.

## Analysis Tools 

pending

## Example Analysis

pending
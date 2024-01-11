---
title: "Userassist"
layout: post
permalink: /userassist
categories: Application-Execution
---

## Location and Format

The Windows Userassist information is located in the NTUSER.dat hive at **Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist\GUID\count**. All of the GUIDs in the UserAsist key are ROT13 encoded

## Purpose

The UserAssist key tracks the GUI-based applications that are run from the desktop in the launcher on the Windows System. This key is used by Windows to populate a user's start menu. This allows Windows to attempt to "predict" what the user will want to run based on how many times a program was previously ran.

## Forensic Uses

Forensicators use this registry as evidence of application execution. Due to the ROT13 encoding the data in the Userassist is not viewable in plaintext. However, there are well known tools that give us the ability to view this data. Once we have decoded this data we can expect to find the following:
-  Guid Key (ROT13 encoded)
-  Name (GUID Key decoded)
-  Counter for program execution
-  Last run time

Please note that in Windows versions lower than 7 the Counter starts at 5 by default. This is by design from Microsoft.

## Example Analysis

pending
---
title: "Last Visited MRU"
layout: post
permalink: /lastvisitedMRU
categories: Application-Execution
---
## Location and Format

The LastVisitedMRU registry key has different locations based on which version of the  Windows operating system you are running.

    - XP: NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedMRU
    - Win7: NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidMRU

## Purpose

The LastVisitedMRU tracks application use for the user along with the directory location for the file last used by the application. IT does not matter if the directories are hidden and can often allow us to find interesting directories.

## Forensic Uses

We get two very important pieces of information from this key. Firstly, applications that have been executed by the user. Secondly, the last place in the file system that those applications interacted with. This can lead to directories of note being identified.

## Example Analysis

pending
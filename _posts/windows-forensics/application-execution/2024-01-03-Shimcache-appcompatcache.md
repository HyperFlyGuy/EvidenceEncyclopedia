---
title: "Shimcache/AppCompatCache"
layout: post
permalink: /shimcache-appcompatcache
categories: Application-Execution
---

## Location and Format

The Windows Shimcache information is located in the SYSTEM hive at **SYSTEM\CurentControlSet\Control\SessionManager\AppCompatCache\AppCompatCache**. 

## Purpose

The Shimcache was designed to provided backwards compatibility to applications. It ensures that older applications are able to run on newer versions of Windows. Shimcache does this by applying properties to executables when they are run. These "properties" are known as shims.

## Forensic Uses

Shimcache has been a long time favorite of Forensicators as an artifact that corroborates execution. Shimcache is a crucial piece of evidence and you can expect the following information from it (Assuming Win7+):

    - File Path
    - Last Modified Date
    - Insert Flag

There are important facts about shimcache that you should be aware of before you begin analysis. First, The modification time of the shim cache entry does **not** indicate execution. The last modification date gives us the last time that the file content was changed (This causes an application to be re-shimmed). Secondly, if the modification time of the file and the modification time of the shimcache entry do not match it could indicate the time stomping occurred. Thirdly, Windows XP only tracks 96 entries and Win 7+ tracks 1024 entries. The Shimcache is rolling, meaning that once capacity is reached the older entries are overwritten by the newer ones. Lastly, the shimcache is present on servers and workstations alike (unlike prefetch).

## Analysis Tools 

- appcompatcacheparser.exe (https://github.com/EricZimmerman/AppCompatCacheParser)
- appcompatprocessor.py (https://github.com/mbevilacqua/appcompatprocessor)

## Example Analysis

pending
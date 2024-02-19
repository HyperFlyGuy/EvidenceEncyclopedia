---
title: "Capability Access Manager"
layout: post
permalink: /capabilityaccessmanager
categories: Application-Execution
---
## Location and Format

The Capability Access Manager is Located in both the SOFTWARE and NTUSER registry hives. The locations for these registry keys are:

    - SOFTWARE\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore
    - NTUSER\Software\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore

## Purpose

The Capability Access Manager is used to track application usage of the Microphone, Camera, along with other application specific settings. Essentiallly, it tracks what applications are allowed to use these devices. Think about that prompt you get when an application wants to use your microphone or camera.

    - HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore\webcam\
    - HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore\microphone\
    - HKEY_USERS\User\SOFTWARE\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore\webcam\
    - HKEY_USERS\User\SOFTWARE\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore\microphone\

Above is an example of some specific keys that you will find for various devices.

## Forensic Uses

With an understanding of the structure of this key it can aid us in answering three main questions.

- What app was using the microphone?
- When was the last session?
- How long was that last session?

These are relatively niche questions that can be asked but when investigating advanced cases it could turn up some interesting information. Microsoft applications are stored in the child keys, but any application that is not a Microsoft application will be stored in the "Nonpackaged child key".

## Example Analysis

pending
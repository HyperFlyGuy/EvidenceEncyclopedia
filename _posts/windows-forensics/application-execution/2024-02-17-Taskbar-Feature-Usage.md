---
title: "Task Bar Feature Usage"
layout: post
permalink: /taskbar-feature-usage
categories: Application-Execution
---
## Location and Format

The taskbar feature usage is located in the registry key at **"NTUSER\Software\Microsoft\Windows\CurrentVersion\Explorer\FeatureUsage"**

## Purpose

The name of this artifact largely describes itself and you can probably guess what it does! If you had guessed that it tracks feature bar usage then you would be right!

## Forensic Uses

There are a couple of ways to interpret the data that this registry key gives. However, first and foremost you must understand that it only tracks GUI applications and it does not include time stamps!

    - The "AppLaunch" sub-key tracks the data for pinned applications and allows us to show that the user was aware of the application. This data will persist even after an application is un-pinned.
    - The "AppSwitched" sub-key tracks the count of application focus, showing that the user had direct interaction with an application. This is not tied to pinned applications.

## Analysis Tools 

pending

## Example Analysis

pending
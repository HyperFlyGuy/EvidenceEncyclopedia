---
title: "Jumplists"
layout: post
permalink: /jumplists
categories: Application-Execution
---
## Location and Format

Jumplists artifacts are known as Automatic destinations and are located at **"USERPROFILE\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations"**

## Purpose

Jumplists are the list that you see when you right click on a Windows task bar item. The goal of the jumplist is to allow a user to quickly access recent or frequently used items. It was first introduced in Windows 7 and provides a wealth of meta data information for forensic investigators.

## Forensic Uses

A Jumplist file is named accourding to an application id. A list of these application ids can be found at *https://dfir.to/EZJumpList*. When we are examining jumplist files it is a safe assumption that the creation time of the jumplist file is the first time an item was added to the jumplist. This in turn is usually the first time an object was opened by an application. The modification time, similarly, is typically the last time an application opened an object. Another important note is that this is a user-centric artifact and allows us to map actions to a specific user.

## Example Analysis

pending
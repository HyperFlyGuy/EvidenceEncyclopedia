---
title: "Logon Event Types"
layout: post
permalink: /logon-event-types
categories: Account-Usage
---
## Location and Format

The Security Event Logs will give us the context needed to analyze certain logon events C:\Windows\System32\winevt\logs\Security.evtx"

## Purpose

Logon Event Types are able to provide us very specific information about a logon that has occurred. In addition to the date, time, user, hostname, and success/failure status. They also provideus the exact means in which a logon was attempted.

## Forensic Uses

Event ID 4624
Logon Type Explanation
2 = Logon via console
3 = Network Logon
4 = Batch Logon
5 = Windows Service Logon
7 = Credentials used to unlock screen; RDP session reconnect
8 = Network logon sending credentials (cleartext)
9 = Different credentials used than logged on user
10 = Remote interactive logon (RDP)
11 = Cached credentials used to logon
12 = Cached remote interactive (similar to Type 10)
13 = Cached unlock (similar to Type 7)

## Analysis Tools 



## Example Analysis

pending
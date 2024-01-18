---
title: "System Resource Usage Monitor (SRUM)"
layout: post
permalink: /srum
categories: Application-Execution
---
## Location and Format

The SRUM database is a newer artifact that was created after Win8+. It is located at **"C:\Windows\System32\SRU\
srudb.dat"**

## Purpose

The SRUM Database can record between 30-60 days of historical system performance. This includes applications that were ran, user accounts responsible for execution, network connections, and bytes sent/received per hour by an application!

## Forensic Uses

The SRUDB.dat is an ESE database that is one of the formats regularly used by Microsoft. It can allow us to discover application execution for various applications and users. The tables that are most useful for forensic purposes are:
- Network Data Usage
- Application Resource Usage
- Network Connectivity Usage

## Analysis Tools 

- ESEDatabaseView (https://www.nirsoft.net/utils/ese_database_view.html)


## Example Analysis

pending
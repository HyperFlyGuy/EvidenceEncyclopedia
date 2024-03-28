---
title: "SRUM (Network Activity)"
layout: post
permalink: /srum-network
categories: Network-Activity-and-Physical-Location
---
## Location and Format

The SRUM Database is present in Windows 8+ and resides at **"C:\Windows\System32\SRU\SRUDB.dat"**

## Purpose

The SRUM database records 30-60 days of historical System performance. This includes 

- Application Runs
- User Accounts Responsible
- Network Connections
- Bytes sent/recieved per application per hour

## Forensic Uses

The SRUDB is an ESE database, thus giving it many of the other benefits that databases offer in terms of data recovery. Three tables that are particular interesting to us are:

- {973F5D5C-1D90-4944-BE8E-24B94231A174} = Network Data Usage
- {d10ca2fe-6fcf-4f6d-848e-b2e99266fa89} = Application Resource Usage
- {DD6636C4-8929-4683-974E-22C046A43763} = Network Connectivity Usage

These tables record data once per hour in batches.

## Analysis Tools 



## Example Analysis

pending
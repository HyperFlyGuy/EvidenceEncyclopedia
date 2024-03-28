---
title: "Authentication Events"
layout: post
permalink: /authentication-events
categories: Account-Usage
---
## Location and Format

The goto resource for analyzing authentication events in a Windows system are the Windows Security Event Logs. These event logs are located at **"C:\Windows\System32\winevt\logs\Security.evtx"**

## Purpose

Authentication events allow us to identify where the authentication of credentials occurred. They are especially useful when trying to decipher local vs domain account usage.

## Forensic Uses

Authentication events are recorded on system that authenticated credentials. For instance, local accounts will be recorded on the workstation, while domain accounts will be recorded on the domain controller.

- Event ID Codes (NTLM protocol)
   - 4776: Successful/Failed account authentication
- Event ID Codes (Kerberos protocol)
   - 4768: Ticket Granting Ticket was granted (successful logon)
   - 4769: Service Ticket requested (access to server resource)
   - 4771: Pre-authentication failed (failed logon)

## Analysis Tools 



## Example Analysis

pending
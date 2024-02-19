---
title: "Run Dialog Usage"
layout: post
permalink: /rundialog
categories: Application-Execution
---
## Location and Format

The run dialog registry key is located in **"NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\RunMRU"**

## Purpose

This key was created to track the history of commmands entered into the run dialog box. This storage is done on a per user basis.

## Forensic Uses

We will be able to observe when the run dialog box was used by the user. The history of the run commands are in temporal order due to this being an MRU key.

## Example Analysis

pending
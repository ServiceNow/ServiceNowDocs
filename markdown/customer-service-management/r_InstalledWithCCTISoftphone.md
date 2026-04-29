---
title: Components installed with CTI Softphone
description: Several types of components are installed with CTI Softphone.Tables are added with activation of CTI Softphone.Script includes are added with activation of CTI Softphone.Business rules are added with activation of CTI Softphone.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Customer Service Management, Reference, Customer Service Management]
---

# Components installed with CTI Softphone

Several types of components are installed with CTI Softphone.

## Tables installed with CTI Softphone

Tables are added with activation of CTI Softphone.

|Table|Description|
|-----|-----------|
|User CTI Status|Stores the agent's availability status.|

## Script includes installed with CTI Softphone

Script includes are added with activation of CTI Softphone.

|Script include|Description|
|--------------|-----------|
|CTIAjaxUtility|Ajax class that provides helper functions to set and get user states, get incoming call context, log a call, and queue and dequeue a call.|

## Business rules installed with CTI Softphone

Business rules are added with activation of CTI Softphone.

<table id="table_jhr_czw_kt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Route available user for Incident Task

</td><td>

User CTI Status\[user\_cti\_status\]

</td><td>

Demo business rule to dequeue a call based on matching rules whenever an agent becomes available.

</td></tr></tbody>
</table>
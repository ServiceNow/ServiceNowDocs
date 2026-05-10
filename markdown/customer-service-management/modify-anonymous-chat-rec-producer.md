---
title: Modify the anonymous chat record producer
description: Modify the default anonymous chat record producer to gather the desired information from guest users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Anonymous chat, Administer, Customer Service Management]
---

# Modify the anonymous chat record producer

Modify the default anonymous chat record producer to gather the desired information from guest users.

## Before you begin

Role required: admin

## About this task

This record producer requests information from a guest user on the Consumer Service Portal and stores the information as a record in the Consumer Interaction table \(sn\_customerservice\_customer\_interaction\). The record is then used for routing the chat request.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Record Producers**.

2.  Click **What can we help you with?**.

3.  Modify the record producer as necessary, including the variables in the **Variables** related list.

    For more information, see [Create a record producer to log incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/t_CreateARecordProducer.md).

4.  Click **Update**.



---
title: Configure a learning system
description: Configure the learning system so that the schedule flow pulls learning content from the third-party system into a ServiceNow instance.
locale: en-US
release: australia
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administration tasks in Learning Core, Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Configure a learning system

Configure the learning system so that the schedule flow pulls learning content from the third-party system into a ServiceNow instance.

## Before you begin

Role required: learning\_admin

## Procedure

1.  Navigate to **Learning** &gt; **Administration** &gt; **Learning System Configuration**.

2.  Select the required learning source and set the **Active** field to true.

    |Field|Description|
    |-----|-----------|
    |Learning source|Record of the learning management system in Enterprise Service Management Integrations Framework.|
    |Active|Option to indicate that the source is available for use.|
    |Learning system|External learning management system to which the record is associated.|
    |Reassign completed course|Option to reassign the completed course.|
    |Support assign course|Option to indicate whether a particular external system allows a course assignment API.|
    |Sync course activity days|Option to specify the number of days that is considered for synchronizing course progress between the external learning management system and a ServiceNow application.|
    |Logo|Option to include a logo of the source.|

3.  Click **Update**.


**Parent Topic:**[Administration tasks in Learning Core](ln-administration.md)


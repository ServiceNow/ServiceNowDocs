---
title: Mark an update set complete in ServiceNow Studio
description: Mark an update set as Complete in ServiceNow Studio to enable your changes to be retrieved by other instances.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with update sets, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Mark an update set complete in ServiceNow Studio

Mark an update set as **Complete** in ServiceNow Studio to enable your changes to be retrieved by other instances.

## Before you begin

Role required: admin or delegated developer

## About this task

Only mark an update set as **Complete** when it’s ready to migrate. Once an update set is **Complete**, don’t change it back to **In progress**. Instead, create another update set for the rest of the changes.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the **Deployment** tab.

3.  Open the update set record you want to change.

4.  Change the **State** of the update set from **In progress** to **Complete**.


**Parent Topic:**[Working with update sets in ServiceNow Studio](../concept/working-with-update-sets-in-servicenow-studio.md)


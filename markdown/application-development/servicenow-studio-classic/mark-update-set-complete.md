---
title: Mark an update set complete in ServiceNow Studio
description: Mark an update set as Complete in ServiceNow Studio to make the changes available for retrieval by other instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/mark-update-set-complete.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 1
breadcrumb: [Update sets, App deployment in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Mark an update set complete in ServiceNow Studio

Mark an update set as **Complete** in ServiceNow Studio to make the changes available for retrieval by other instances.

## Before you begin

Role required: admin or delegated\_developer

## About this task

Mark an update set as **Complete** only when it is ready to migrate. After an update set is marked **Complete**, do not change the state back to **In progress**. Create a new update set for any remaining changes instead.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the **Deployment** tab.

3.  Open the update set record to change.

4.  Change the **State** of the update set from **In progress** to **Complete**.

    The update set is marked **Complete** and the changes are available for retrieval by other instances.


**Parent Topic:**[Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md)


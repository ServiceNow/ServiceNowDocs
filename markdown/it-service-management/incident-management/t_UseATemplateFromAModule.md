---
title: Create a module that uses incident template
description: Create a module to log an incident with pre-filled field values from an existing template.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Incident templates and record producers, Configure, Incident Management, IT Service Management]
---

# Create a module that uses incident template

Create a module to log an incident with pre-filled field values from an existing template.

## Before you begin

Role required: admin

## About this task

In the [Create incident template](t_CreateAnIncidentTemplate.md) topic, you have created the Bond Trade Access Denied template. In this topic, you can use the template with a module in the Self-Service application.

## Procedure

1.  Point to **Self-Service** and click the edit icon ![Edit icon](../../configurable-workforce-optimization-itsm/image/edit-icon.png).

2.  In the Modules related list, click **New**.

3.  On the form, fill in the fields.

    -   **Title**: `Bond Trading Access Denied`.
    -   **Order**: In the Module records list, view the order numbers and enter a number that is appropriate. For example, if the order number of **Homepage** is 50 and the order number of **Business Applications** is 52, and you want to place the new module between **Homepage** and **Business Applications**, enter the order number as 51.
    -   **Hint**: `Log an incident about the Bond Trade application`.
    Link Type section:

    -   **Link Type**: URL \(from Arguments:\)
    -   **Arguments**: `incident.do?sys_id=-1&sysparm_template=Bond Trading Access Denied`

        **Note:** This path deploys the template in the new incident record.

    ![Module using template to create incident](../image/incident-template-module.png)

4.  Click **Submit**.

    The new module appears in the Self-Service application.


## What to do next

Click the module to open a new incident record with the applied Bond Trading Access Denied template.

**Parent Topic:**[Incident templates and record producers](../concept/incident-templates-record-producers.md)

**Related topics**  


[Create incident template](t_CreateAnIncidentTemplate.md)

[Create a record producer to log incidents](t_CreateARecordProducer.md)

[Create a record producer using a template](t_CreateRecProducWithTempl.md)


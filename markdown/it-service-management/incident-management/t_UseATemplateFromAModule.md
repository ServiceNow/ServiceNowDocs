---
title: Create a module that uses an incident template
description: Create a module to log an incident with pre-filled field values from an existing template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/t\_UseATemplateFromAModule.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident templates and record producers, Configuring Incident Management, Incident Management, IT Service Management]
---

# Create a module that uses an incident template

Create a module to log an incident with pre-filled field values from an existing template.

## Before you begin

Role required: admin

## About this task

This example adds a module to the Self-Service application that uses the Bond Trading Access Denied template from [Create an incident template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/t_CreateAnIncidentTemplate.md).

## Procedure

1.  Point to **Self-Service** and select the edit icon \[Omitted image "edit-module.png"\] Alt text: Edit icon.

2.  In the Modules related list, select **New**.

3.  On the form, fill in the fields.

    -   **Title**: `Bond Trading Access Denied`.
    -   **Order**: In the Module records list, view the order numbers and enter an appropriate number. For example, if **Homepage** is 50 and **Business Applications** is 52, enter 51 to place the new module between them.
    -   **Hint**: `Log an incident about the Bond Trade application`.
    Link Type section:

    -   **Link Type**: URL \(from Arguments:\)
    -   **Arguments**: `incident.do?sys_id=-1&sysparm_template=Bond Trading Access Denied`

        **Note:** This path deploys the template in the new incident record.

    \[Omitted image "incident-template-module.png"\] Alt text: Module form with the link arguments that apply the Bond Trading Access Denied template

4.  Select **Submit**.

    The new module appears in the Self-Service application.


## What to do next

Select the module to open a new incident record with the applied Bond Trading Access Denied template.

**Parent Topic:**[Incident templates and record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-templates-record-producers.md)

**Related topics**  


[Create an incident template]()

[Create a record producer to log incidents]()

[Create a record producer using a template]()


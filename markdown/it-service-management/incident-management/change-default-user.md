---
title: Configure default user for auto-closing incidents
description: Change the default user who last updated an incident to the user you mention for auto-closing incidents.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Configure default user for auto-closing incidents

Change the default user who last updated an incident to the user you mention for auto-closing incidents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

2.  Open the **Autoclose Incidents** schedule job.

3.  In the **Job context**, add the following:

    ```
    fcRunAs=<user_name>
    fcScriptName=incident autoclose
    ```

    For example, if you add `fcRunAs=admin`, the code places **System Administrator** in the **Updated by** field.


**Parent Topic:**[Configuring Incident Management](../concept/incident-configuration.md)


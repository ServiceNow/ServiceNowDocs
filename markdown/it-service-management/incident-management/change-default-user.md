---
title: Configure the default user for auto-closing incidents
description: Specify the user that appears in the Updated by field when incidents are closed automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/change-default-user.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Configure the default user for auto-closing incidents

Specify the user that appears in the Updated by field when incidents are closed automatically.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

2.  Open the **Autoclose Incidents** scheduled job.

3.  In the **Job context** field, add the following lines:

    ```
    fcRunAs=<user_name>
    fcScriptName=incident autoclose
    ```

    For example, if you add `fcRunAs=admin`, the code places **System Administrator** in the **Updated by** field.


**Parent Topic:**[Configuring Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-configuration.md)


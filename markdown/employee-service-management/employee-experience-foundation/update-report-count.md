---
title: Update the report count based on eligible users
description: Update the direct and other report count by running a script execution job.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Organization chart in Employee Center Pro, Setup task management, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Update the report count based on eligible users

Update the direct and other report count by running a script execution job.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  On the scheduled jobs page, select the **Populate Manager Reportee Count Using Eligible Users** job.

    **Important:** If the [Domain Separation plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-plugin.md) is activated on your instance, select the **Populate Manager Reportee Count Using Eligible Users \[Domain Separated\]** job.

3.  On the scheduled script execution page, select **Execute Now**.


## Result

The report count is updated based on the [eligible users](config-eligible-users-orgchart.md) and is populated in the organization chart.

**Related topics**  


[Organization chart in Employee Center Pro](../concept/employee-profile-org-chart.md)


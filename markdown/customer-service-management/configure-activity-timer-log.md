---
title: Configure the activity timer log
description: Configure the activity timer log to appear on selected record pages in CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-activity-timer-log.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the activity timer log

Configure the activity timer log to appear on selected record pages in CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

The activity timer log feature automatically tracks the time that agents spend working on cases and interactions and provides detailed time reports. This feature is available on the following record pages:

-   CSM default record page
-   Front-line case page
-   CSM Interaction record page
-   CSM voice interaction record page
-   CSM centered chat interaction record page

## Procedure

1.  Install the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\).

2.  Assign the sn\_at.admin role to the appropriate users.

3.  Assign the sn\_at.agent role to the appropriate users.

4.  Configure the following UI Builder page properties.

<table id="table_d4c_1wd_cjc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**activity\_timer**

</td><td>

Enables the activity timer component in the workspace.-   True: Activity timer is active.
-   False: Activity timer is inactive.


</td></tr><tr><td>

**activity\_timer\_custom\_tables**

</td><td>

Specifies custom tables for the activity timer log feature.

</td></tr><tr><td>

**activity\_timer\_case\_type\_exclusion**

</td><td>

Specifies case types excluded from the activity timer log feature.

</td></tr></tbody>
</table>
**Related topics**  


[Activity timer log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-time-tracking.md)


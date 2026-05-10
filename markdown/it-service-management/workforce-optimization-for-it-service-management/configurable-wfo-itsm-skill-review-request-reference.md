---
title: Skill review request components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM installs roles and enables notifications when you install the application.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Skills Management, Workforce Optimization for ITSM, IT Service Management]
---

# Skill review request components in Workforce Optimization for ITSM

Workforce Optimization for ITSM installs roles and enables notifications when you install the application.

## Roles

|Role title \[name\]|Description|
|-------------------|-----------|
|Skill review manager \[sn\_wfo\_skillreview.manager\]|Grants administrative rights to create, read, update, and delete \(CRUD\) skill review request records.|
|Skill review user \[sn\_wfo\_skillreview.user\]|Grants administrative rights to create, read, or update skill review request records.|

## Notifications

Navigate to **All** &gt; **System Notifications** &gt; **Provider** &gt; **Notifications** to access the notifications below that are provided by default. For more information on adding notifications, see [Provider notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notification-provider.md)

<table id="table_nhy_chs_35b"><thead><tr><th>

Notification name

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Skill Request Pending Manager Review

</td><td>

When enabled, the manager receives a notification when their agent submits a skill review request to their manager for review.-   **Type:**string
-   **Default value:**true

</td></tr><tr><td>

Skill Request Reviewed

</td><td>

When enabled, the agent receives a notification when their manager submits a skill request that has been reviewed.-   **Type:**string
-   **Default value:**true

</td></tr><tr><td>

Skill Request Cancel

</td><td>

When enabled, if the agent or manager cancels the skill review request then the skill review request assignee will receive a notification.-   **Type:**string
-   **Default value:**true

</td></tr><tr><td>

Skill Request Pending User Review

</td><td>

When enabled, the agent receives a notification that their manager has submitted a skill request for the agent to review.-   **Type:**string
-   **Default value:**true

</td></tr></tbody>
</table>**Parent Topic:**[Skills Management in Workforce Optimization for ITSM](../concept/skills-management-wfo-itsm.md)


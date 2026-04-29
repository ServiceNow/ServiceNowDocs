---
title: Resolve and close an incident
description: When the service is restored by rectifying the issue that resulted for an incident, you can set the incident state as resolved. If the user is satisfied with the resolution, the user can close the incident or the incident is auto-closed after a certain time based on the incident auto-close properties.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Incident resolution and closure, Managing incidents, Incident Management, IT Service Management]
---

# Resolve and close an incident

When the service is restored by rectifying the issue that resulted for an incident, you can set the incident state as resolved. If the user is satisfied with the resolution, the user can close the incident or the incident is auto-closed after a certain time based on the incident auto-close properties.

## Before you begin

Role required:

-   For resolution: itil, list\_updater, sn\_incident\_write, or admin
-   For closure: itil\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident that you want to resolve and close.

3.  In the Resolution Information section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Resolved by|The user who resolved the issue and the date and time the incident was closed.|
    |Resolved|The date and time when the incident was resolved.|
    |Resolution code|Information to categorize resolved cases.|
    |Resolution notes|Document how an incident is resolved.|

4.  Click **Resolve**.

    The incident is in the resolved state.

5.  Click **Close Incident**.

    The incident is closed.

    **Note:** Even when an incident is closed or canceled, you can edit the following fields on the Incident form, if you have an admin role: **Subcategory**, **Service**, **Service Offerings**, **Description**, **Contact type**, **Watch list**, **Work notes list,** **Parent Incident**, **Problem**, **Change Request**, **Caused by Change**, **Resolved by**, **Resolved**, **Reassignment count**.


**Parent Topic:**[Incident resolution and closure](../concept/c_IncidentResolutionAndRecovery.md)


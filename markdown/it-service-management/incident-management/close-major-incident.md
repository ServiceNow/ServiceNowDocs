---
title: Close a major incident
description: You can close a major incident manually after validating the resolution and when the major incident is in the Resolved state.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Close a major incident

You can close a major incident manually after validating the resolution and when the major incident is in the **Resolved** state.

## Before you begin

-   Role required: major\_incident\_manager or admin
-   Major incident is in resolved state

## Procedure

1.  Navigate to **All** &gt; **Major Incidents** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the major incident that you want to close.

3.  Click **Close Incident**.

    **Note:**

    -   If you cancel an incident and the major incident state is in **Proposed** or **Accepted** state, the major incident state changes to **Canceled**.
    -   The incident auto-closure property **Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date** does not close any incident record that is accepted as a major incident. Users with the major\_incident\_manager or admin role must close a major incident manually, after validating the resolution and when the major incident is in the **Resolved** state.
    -   If an incident was promoted as a major incident, then an ESS user cannot resolve, close, or reopen the incident.

**Parent Topic:**[Working on major incident management](../concept/work-on-mim.md)


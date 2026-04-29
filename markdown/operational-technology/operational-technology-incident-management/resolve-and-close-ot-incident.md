---
title: Resolve and close an incident
description: When an issue is corrected, you can set the Operational Technology \(OT\) incident state to Resolved. If you're happy with the resolution, you can close the incident. The incident also auto-closes after a certain amount of time based on the incident auto-close properties.
locale: en-US
release: australia
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Resolve and close an incident

When an issue is corrected, you can set the Operational Technology \(OT\) incident state to **Resolved**. If you're happy with the resolution, you can close the incident. The incident also auto-closes after a certain amount of time based on the incident auto-close properties.

## Before you begin

Role required: sn\_ot\_incident\_write

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  Open the in-progress OT incident that you want to resolve and close.

3.  In the **Resolution Information** related list, fill in the following fields.

<table id="table_thj_lty_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resolution code

</td><td>

Information to categorize resolved cases.-   **Duplicate**

Incident is a duplicate of an existing incident and should be closed.

-   **Known error**

Incident was resolved by a solution from a known error.

-   **Resolved by caller**

Incident was resolved by the user who contacted the OT engineer for the issue.

-   **Resolved by change**

Incident was resolved with an OT change request.

For more information about OT change requests, see [Create a change request](create-ot-change-request.md).

-   **Resolved by problem**

Incident was resolved with a problem that identified the cause of the incident.

For more information about problems, see [Managing Problems](https://www.servicenow.com/docs/access?context=problem-mgmt-lifecycle&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

-   **Resolved by request**

Incident was resolved by an OT request.

For more information about OT requests, see [Create an Operational Technology request on the Industrial Workspace](../../operational-technology-request-management/task/create-ot-service-request-industrial-workspace.md).

-   **Solution provided**

Solution for the incident was provided that doesn't fit the other resolution codes.

</td></tr><tr><td>

Resolution notes

</td><td>

Describes how the incident was resolved.

</td></tr></tbody>
</table>4.  In the **State** field, select **Resolved**.

5.  Click **Update**.


**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)


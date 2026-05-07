---
title: Use Access Findings
description: You can use Access Findings to view the potential vulnerabilities that were discovered the last time access checks ran on your ServiceNow AI Platform.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access findings, Access Management]
---

# Use Access Findings

You can use Access Findings to view the potential vulnerabilities that were discovered the last time access checks ran on your ServiceNow AI Platform.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Access Management** &gt; **Access Findings**.

    **Note:** You can also select **Access Findings** from the Access Management Console.

2.  Select **Access Findings** from the options on the left to view the current findings.

    The page provides the following details:

<table id="table_o4n_vrn_bjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The record of the finding itself. Select this to view more details.

</td></tr><tr><td>

Check

</td><td>

The Access Check that found the issue.

</td></tr><tr><td>

Priority

</td><td>

The severity level of the finding. Severity is divided into the following priority levels:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low


</td></tr><tr><td>

Status

</td><td>

The current status of the finding.

</td></tr><tr><td>

Source

</td><td>

Where the issue was found in your instance.

</td></tr><tr><td>

Created

</td><td>

When the finding was created.

</td></tr></tbody>
</table>    The Findings list page is the primary workspace for triaging access findings.

    -   **Status tabs** -- Toggle between Open, Muted, and Resolved views. Each tab shows a count of findings in that state.
    -   **Filtering** -- Filter by priority level, check type, or other finding attributes.
    -   **Sorting** -- Sort by priority, date detected, status, or other columns.
    -   **Export** -- Export findings for offline review or reporting.
3.  Select each record to learn more about the vulnerability and detailed resolutions, including:

    -   Finding description and affected resource
    -   Priority level and the check that detected it
    -   Remediation guidance with documentation link
    -   Related Security Tasks
4.  Select any of the following remediation actions for managing the finding lifecycle:

<table id="table_yqw_xwn_bjc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mark as resolved

</td><td>

Mark a finding as resolved when the underlying misconfiguration has been corrected. Resolved findings move to the Resolved status tab.

 The system verifies resolution on the next scan -- if the misconfiguration is no longer detected, the finding stays resolved. If the misconfiguration is still present, the finding is automatically reopened.

</td></tr><tr><td>

Reopen

</td><td>

Restore a resolved finding to Open status. Use this if a resolved finding requires further investigation or if the remediation was incomplete.

</td></tr><tr><td>

Mute

</td><td>

Suppress a finding from the active findings list. Use this for known exceptions or accepted risks that do not require remediation. Muted findings: -   Move to the Muted status tab
-   Are excluded from the open findings count and the Overview donut chart
-   Remain visible in the Muted tab for audit purposes
-   Are not affected by auto-resolve or auto-reopen


</td></tr><tr><td>

Unmute

</td><td>

Restore a muted finding to open status. Use this when a previously accepted risk needs to be re-evaluated.

</td></tr><tr><td>

Create task

</td><td>

Create a Security Task \(`sn_vsc_security_task`\) from the finding to route remediation through your standard workflow.

 -   **Task type** is auto-populated based on the finding
-   **Description** is auto-populated with finding details
-   The created task is shown on the finding detail page
-   The related finding is shown on the task record
-   Multiple tasks can be created from the same finding if remediation requires coordination across teams


</td></tr></tbody>
</table>

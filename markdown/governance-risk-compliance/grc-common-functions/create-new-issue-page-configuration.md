---
title: Create a new Issue Page Configuration record
description: Create a new issue page configuration record in the Issue Page Configuration module in the classic user interface. The Issue Page Configuration module displays the configurations related to the Issues section in the landing pages of the workspaces. The newly created issue is displayed in the Issue overview landing page in the selected workspace.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Issue Page Configuration module, Landing Page Configurations module, Common GRC features, Governance, Risk, and Compliance]
---

# Create a new Issue Page Configuration record

Create a new issue page configuration record in the Issue Page Configuration module in the classic user interface. The Issue Page Configuration module displays the configurations related to the Issues section in the landing pages of the workspaces. The newly created issue is displayed in the Issue overview landing page in the selected workspace.

## Before you begin

Role required: sn\_grc.admin

## Procedure

1.  Navigate to **Landing Page Configurations** &gt; **Issue Page Configuration**.

2.  Click **New**.

    The Issue page configuration record is displayed.

3.  On the form, fill in the fields.

<table id="table_myj_3cq_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Configurable name of the workspace. This is the name of the tab that is displayed in the workspace.

</td></tr><tr><td class="sub-head" colspan="2">

Issues tab

</td></tr><tr><td>

Table

</td><td>

Name of the table used for configuring the issues that are displayed in the workspace. The **Filter** field displays the filter condition that you can configure and display the matching records.

</td></tr><tr><td class="sub-head" colspan="2">

Tracking tab

</td></tr><tr><td>

Policy exceptions

</td><td>

Option to display the policy exceptions under the Tracking section in the Compliance workspace.**Note:** On the Risk workspace, policy exceptions are by default not displayed.

</td></tr><tr><td>

Evidence requests

</td><td>

Option to display the evidence requests under the Tracking section in the Compliance workspace. This option is available only when the Advanced core plugin is installed in the instance.

</td></tr><tr><td class="sub-head" colspan="2">

Issue triage tab

</td></tr><tr><td colspan="2">

This tab is available only when the Advanced core plugin is installed in the instance.

</td></tr><tr><td>

Show issue triages

</td><td>

Option to display or hide the issue triages in the workspace.**Note:** For the Audit workspace, this option is inactive by default.

</td></tr><tr><td>

Table

</td><td>

Name of the table used for configuring the issue triages.

</td></tr><tr><td>

Filter

</td><td>

Filter condition that you can configure to display the matching records.

</td></tr><tr><td class="sub-head" colspan="2">

Observations tab

</td></tr><tr><td colspan="2">

This tab is available only when the Advanced Audit plugin is installed in the instance.

</td></tr><tr><td>

Show observations

</td><td>

Option to display or hide the audit observations in the workspace.**Note:** This option is by default selected for the Audit workspace.

</td></tr><tr><td>

Table

</td><td>

Name of the table used for the observation.

</td></tr><tr><td>

Field

</td><td>

Filter condition that you can configure and display the matching records.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

A new Issue Page Configuration record is created.

**Parent Topic:**[Issue Page Configuration module](../../grc-common-workspace/concept/issue-page-config-record.md)


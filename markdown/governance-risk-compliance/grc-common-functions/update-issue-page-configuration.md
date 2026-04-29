---
title: Update an Issue Page Configurations record
description: Update an existing Issue Page Configurations record in the classic user interface to update the issue page configurations that are displayed in the Issues overview landing page in the workspace. After modifying the configurations in the Issue Page Configuration record, the issues, issue triages, and tracking status of the issues are displayed for the users in the desired workspace.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Issue Page Configuration module, Landing Page Configurations module, Common GRC features, Governance, Risk, and Compliance]
---

# Update an Issue Page Configurations record

Update an existing Issue Page Configurations record in the classic user interface to update the issue page configurations that are displayed in the Issues overview landing page in the workspace. After modifying the configurations in the Issue Page Configuration record, the issues, issue triages, and tracking status of the issues are displayed for the users in the desired workspace.

## Before you begin

Role required: sn\_grc.admin

## Procedure

1.  Navigate to **Landing Page Configurations** &gt; **Issue Page Configurations**.

    The names of the available workspaces are listed in the Issue Page Configurations record.

2.  Select the workspace configuration record that you want to update.

    The Issue page configuration record for the selected workspace displays a list of the tabs. You can check the filter conditions for the selected table displayed in the respective tabs and update the fields if necessary.

    -   Name: Name of the tab that is displayed in the workspace.
    -   Issues: Configuration to be performed to display the issues widget in the workspace.
    -   Issue triage: Configuration to be performed to display the issue triage widget in the workspace.
    -   Tracking: Configuration to be performed to display the Policy exceptions and Evidence requests in the workspace.
    -   Observations: Configuration to be performed to display the audit observations in the workspace.
    ![Issue page configuration tabs](../../grc-common-workspace/image/issue-page-configuration-tabs.png "Issue page configuration tabs")

3.  In the **Issues** tab, check the filter conditions for the selected table and update the fields if necessary.

4.  In the **Issue** triage tab, check the filter conditions for the selected table.

5.  In the **Tracking** tab, select the **Policy exceptions** and **Evidence** options.

6.  In the **Observations** tab, select the **Show observations in the Audit workspace** option, and update the filter condition.

    The page displays the name of the table for observations \(sn\_audit\_advanced\_observation\) and the filter condition to be selected such as **Active is True**.

    **Note:** The Observations widget is displayed only in the Audit workspace.

7.  To update the issue page configuration record, click **Update**.


**Parent Topic:**[Issue Page Configuration module](../../grc-common-workspace/concept/issue-page-config-record.md)


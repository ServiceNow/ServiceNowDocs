---
title: Configure scanning properties per persona
description: You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine properties, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure scanning properties per persona

You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.

## TeamDev scanning properties

You can specify whether to scan TeamDev code pushes that are pending a review. You can also specify the requirements they must meet to be automatically approved or rejected.

If you use TeamDev as a method for pushing code, the Scan Engine can be used to scan code pushes that are pending a code review. You scan these pushes for findings, as well as define the conditions to automatically approve or reject code reviews.

**Note:** Code reviews must be enabled for TeamDev scanning to work properly. Additionally, admins must perform a one-time API configuration to enable TeamDev scanning. For more information, refer to [Register your instance](../task/register-your-instance.md).

Properties include:

-   **Automatically scan pushes pending Code Review** \(`auto_scan_team_dev_pushes`\)
-   **Automatically approve or reject pushes** \(`team_dev_auto_approve`\)
-   **Approval condition** \(`team_dev_approval_condition`\)

    **Note:** The default approval condition is `total_errors=0`. This means TeamDev code pushes with zero errors will be auto-approved.

-   **Code reviewer user** \(`team_dev_user`\)

## Users and administrators

This is a list that contains a record for each role given out in the system that is related to the Scan Engine.

## Team leads

The team and team leads defined here are able to view the Team Lead information in the Analytics Dashboard.

1.  To define teams and team leads, select **New**.
2.  Configure the following fields and settings.

    |Field/Setting|Description|
    |-------------|-----------|
    |Active|Determines if the Scan Engine Team Lead record is active.|
    |Team Name|Specify the name of the team as it will appear in reports within the Scan Engine.|
    |Team Lead|Identifies the team lead or manager of this group.|
    |My Team - Users|Specify the user or list of users that are part of this team.|
    |My Team - Groups|Specify the group or list of groups that are part of this team.|


## Set requirements for automatic approval or rejection

To automatically scan TeamDev code pushes when they are committed, configure the **Automatically Scan Pushes Pending Code Review** option:

1.  Enable **Automatically approve or reject pushes**.
2.  Add a Code reviewer user for additional tracking.

    You can see the table that will be used for checking scan results.

3.  Use the condition builder to specify the rules for how a code push is approved.

    If it does not meet these rules, it will be rejected.

    **Note:** By default, one condition is already set, which says that the total number of errors found must be zero.


You can add and configure additional filter conditions by selecting **Add filter condition**. You can also add and configure OR clauses by selecting **Add OR clause**.

**Note:** You can append filter conditions and OR clauses to existing conditions by selecting the **AND** or **OR** options next to them.


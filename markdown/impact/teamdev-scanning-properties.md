---
title: Configure Team Dev scanning properties
description: You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/teamdev-scanning-properties.html
release: brazil
topic_type: concept
last_updated: "2026-11-16"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Scan Engine properties, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Configure Team Dev scanning properties

You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.

You can specify whether to scan Team Dev code pushes that are pending a review, whether to approve or reject those pushes automatically, and whether developers can use Suite scans for applications.

If you use Team Dev as a method for pushing code, the Scan Engine can be used to scan code pushes that are pending a code review. You scan these pushes for findings, and you can choose to approve or reject code reviews automatically.

**Note:** Code reviews must be enabled for Team Dev scanning to work properly. Additionally, admins must perform a one-time API configuration to enable Team Dev scanning. For more information, refer to [Register your instance in My SN Instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/register-your-instance.md).

Properties include:

-   **Automatically scan pushes pending Code Review** \(`auto_scan_team_dev_pushes`\)
-   **Automatically approve or reject pushes** \(`team_dev_auto_approve`\). This option becomes available after you select **Automatically scan pushes pending Code Review**.
-   **Allow Suite scanning for Applications**. When selected, developers can choose between a Full scan and a Suite scan. A Suite scan runs only selected definitions for faster validation. A Full scan runs all active definitions. When cleared, only Full scans are available.

## Users and administrators

This is a list that contains a record for each role given out in the system that is related to the Scan Engine.

## Team leads

The team and team leads defined here can view the Team Lead information in the Analytics Dashboard.

1.  To define teams and team leads, select **New**.
2.  Configure the following fields and settings.

    |Field/Setting|Description|
    |-------------|-----------|
    |Active|Determines if the Scan Engine Team Lead record is active.|
    |Team Name|Specify the name of the team as it will appear in reports within the Scan Engine.|
    |Team Lead|Identifies the team lead or manager of this group.|
    |My Team - Users|Specify the user or list of users that are part of this team.|
    |My Team - Groups|Specify the group or list of groups that are part of this team.|


**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)


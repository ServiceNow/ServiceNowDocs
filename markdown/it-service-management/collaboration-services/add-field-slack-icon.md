---
title: Set up slack for a user or group
description: Set up slack from an incident to communicate and work together in channels with a user or a group.
locale: en-US
release: xanadu
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Slack integration - Incident Management, Collaboration services, IT Service Management]
---

# Set up slack for a user or group

Set up slack from an incident to communicate and work together in channels with a user or a group.

## Before you begin

Role required: admin

## About this task

To enable slack for the **Assignment group** field, ensure you have set up a slack channel for that group. For more information, refer [Associate existing slack channel with a group](setup-slack-assign-grp.md).

## Procedure

1.  Download the `Fix script to add Slack field decorators` update set to get the fix scripts from ServiceNow Store app.

2.  Import the update set file.

    For more information, refer [Import an update set](https://www.servicenow.com/docs/access?context=t_SaveAnUpdateSetAsAnXMLFile&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

3.  Navigate to **System Definition** &gt; **Fix Scripts**.

4.  Open the **Add Slack Field Decorator** fix script.

5.  In the **Scripts** field, edit the script to indicate the table and the field for which you want to enable the slack communication.

6.  Click **Run Fix Script**.

    The slack icon \(![Slack icon](../image/slack-icon.png)\) appears next to the following fields mentioned in the script.

    -   **Caller**
    -   **Assignment group**
    -   **Assigned to**
    Clicking the icon takes you to the direct message with the user on slack or slack channel for an assignment group.


**Related topics**  


[Open slack from an incident](open-slack-from-inci.md)


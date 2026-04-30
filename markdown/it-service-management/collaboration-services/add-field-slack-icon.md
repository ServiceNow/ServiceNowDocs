---
title: Set up slack for a user or group
description: Set up slack from an incident to communicate and work together in channels with a user or a group.
locale: en-US
release: zurich
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Collaboration services, IT Service Management]
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

    For more information, refer [Import an update set](https://www.servicenow.com/docs/access?context=t_SaveAnUpdateSetAsAnXMLFile&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

3.  Navigate to **System Definition** &gt; **Fix Scripts**.

4.  Open the **Add Slack Field Decorator** fix script.

5.  In the **Scripts** field, edit the script to indicate the table and the field for which you want to enable the slack communication.

6.  Click **Run Fix Script**.

    The Slack icon appears next to the following fields mentioned in the script.

    -   **Caller**
    -   **Assignment group**
    -   **Assigned to**
    Clicking the icon takes you to the direct message with the user on Slack or Slack channel for an assignment group.


-   **[Associate existing slack channel with a group](setup-slack-assign-grp.md)**  
Associate an existing slack channel to reach out to an assignment group from an incident. Assignment groups are a great way to contact all your stakeholders at once.

**Parent Topic:**[Configuring Collaboration services](../concept/configuring-collab-services.md)

**Related topics**  


[Open slack from an incident](open-slack-from-inci.md)


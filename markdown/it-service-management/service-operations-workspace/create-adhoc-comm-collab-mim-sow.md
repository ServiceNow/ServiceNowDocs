---
title: Create adhoc communication and collaboration using the Related record tab
description: Create adhoc communication and collaboration using the incident communication plan related list on the Related records tab of an incident record page.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Collaborate with stakeholders during a major incident, Managing a major incident record, Major Incident Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Create adhoc communication and collaboration using the Related record tab

Create adhoc communication and collaboration using the incident communication plan related list on the **Related records** tab of an incident record page.

## Before you begin

Role required: major\_incident\_manager, itil, ia\_admin, or admin

## Procedure

1.  On an incident record, select the **Related records** tab.

2.  In the related list, select the **Incident communications Plans** button to open a list of the existing communication plans associated with the incident record.

3.  Select **New** to create an incident communication plan.

    For more information on the form fields of an incident communication plan, see [Create adhoc incident communication plan from incident](../../incident-alert-management/task/t_CreateAnAlertFromAnIncident.md).

    The Incident communication plan record opens on a separate tab.

4.  On the Incident communication plan record, select the **Related records** tab.

5.  In the related links section, select **Incident Communication task**.

6.  Select **New** to create an incident communication task.

    For more information on the form fields of an incident communication task, see [Create adhoc incident communication task from Incident Communications Management](../../incident-alert-management/task/create-adhoc-inci-commu-task.md).

7.  On the Incident communication task record, add a communication channel.

    1.  Select the **More actions** \(![More action icon](../image/mim-more-action-icon.png)\) icon and then select **Add communication channel**.

    2.  On the pop-up window, select **Channel type**.

        The possible values are:

        -   Communication
        -   Collaboration
    3.  Select **Channel**.

        The possible values change depending on the selected **Channel type**:

        -   If **Channel type** is set to **Communication**, you can set one of the following values:
            -   DEX Desktop Assistant
            -   Email
            -   SMS
            -   Microsoft Teams
            -   Slack
            -   Slack notification
        -   If **Channel type** is set to **Collaboration**, you can set one of the following values:
            -   Sidebar discussion
            -   Conference
    4.  Select **Save**.

        The communication channel record opens on a separate tab.

    5.  On the communication channel record, fill in the required details based on the selected **Channel**.

        For more information on the form fields, see [Define a communication channel](https://www.servicenow.com/docs/access?context=create-comm-channel-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    6.  Select **Save**.


**Parent Topic:**[Collaborate with stakeholders during a major incident](collaborate-stakeholders-mim-sow.md)


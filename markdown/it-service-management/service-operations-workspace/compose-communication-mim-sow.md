---
title: Compose communications for incidents and major incidents
description: Compose communication messages for incidents and major incidents using communication channels such as email and SMS.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Communicating with stakeholders about incidents and major incidents, Managing a major incident record, Major Incident Management in Service Operations Workspace, Incident Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Compose communications for incidents and major incidents

Compose communication messages for incidents and major incidents using communication channels such as email and SMS.

## About this task

The **Communicate** tab displays the list of communication tasks with various options that are used to maintain communications with the stakeholders for an incident. For each communication task, you can view the following information:

-   Communication plan - Name of the communication plan.
-   Communication task – Name of the communication task.
-   Status – Status of the communication task.
-   Channels – Communication channel of the task, such as email or SMS.
-   Past due – Time duration since the due date has passed. This information is applicable for communication tasks that have a past due date in the overdue section.
-   Due in – Duration of time left until the due date.

## Before you begin

You must configure the communication plans and tasks in one of the following ways:

-   For major incidents, you must configure communication plans and tasks for Major Incident Management in Admin Center. For more information, see [Configure a communication plan in Major Incident Management](configure-comm-plan-mim-sow.md).
-   For incidents, you must activate and then configure communication plans and tasks in Task Communications Management. For more information, see [Task Communications Management](https://www.servicenow.com/docs/access?context=tcm-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: major\_incident\_manager, ia\_admin, itil, or admin

## Procedure

1.  On the incident record, select the **Communicate** tab.

    The **Communicate** tab displays the list of communication tasks based on the communications configured for major incidents or incidents.

2.  Select the communication task where you want to compose the communication message.

    **Note:** Select the communication task based on the due dates to avoid breaching of any due date for communications. For example, communication tasks from the Overdue section.

3.  On the communication task, select **Compose**.

    The communication task record opens on a new tab within the incident view with the configured communication channels, such as email and SMS.

    **Note:**

    -   Based on the channel selected on the communication task, any or all of the following sections are displayed:
        -   Email
        -   SMS
        -   SMS notification
        -   Microsoft Teams notification
        -   Slack
        -   Slack notifications
    -   For major incident SMS communications, you can select or change the SMS templates with any of the following user roles:
        -   major\_incident\_manager
        -   sn\_incident\_write user who has the required communication related roles
        -   ITIL user to whom the major incident is assigned
4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Email template|Email template used for composing the email.|
    |To|List of users to whom the email is sent.|
    |Cc|List of users to whom the email is sent as Cc.|
    |Bcc|List of users to whom the email is sent as Bcc.|
    |Subject|Subject of the email.|
    |Body|Content of the email.|
    |Attach file|Attachments for the email.|

    |Field|Description|
    |-----|-----------|
    |From|Number from which the message is sent.|
    |To|User to whom the message is sent.|
    |Message|Content of the message.|

    **Note:**

    -   Depending on the channel selected on the communication task, options such as email or SMS are displayed.
    -   SMS communication is sent to the recipient only if the recipient has a phone number linked to the recipient record.
5.  Select **Send**.


**Parent Topic:**[Communicating with stakeholders about incidents and major incidents](../concept/communicating-with-stakeholders-sow.md)


---
title: Compose communications for incidents and major incidents
description: Compose communication messages for incidents and major incidents using communication channels such as email and SMS.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Communicating about incidents and major incidents, Managing a major incident record, Major Incident Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Compose communications for incidents and major incidents

Compose communication messages for incidents and major incidents using communication channels such as email and SMS.

## About this task

The **Communicate** tab displays the list of communication tasks with various options that are used to maintain communications with the stakeholders for an incident. For each communication task, you can view the following information:

-   Communication plan - Name of the communication plan.
-   Communication task – Name of the communication task.
-   Status – Status of the communication task.
-   Channels – Communication channel of the task, such as DEX Desktop Assistant, email or SMS.
-   Past due – Time duration since the due date has passed. This information is applicable for communication tasks that have a past due date in the overdue section.
-   Due in – Duration of time left until the due date.

## Before you begin

You must configure the communication plans and tasks in one of the following ways:

-   For major incidents, you must configure communication plans and tasks for Major Incident Management in Admin Center. For more information, see [Configure a communication plan in Major Incident Management](configure-comm-plan-mim-sow.md).
-   For incidents, you must activate and then configure communication plans and tasks in Task Communications Management. For more information, see [Task Communications Management](https://www.servicenow.com/docs/access?context=tcm-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Role required: major\_incident\_manager, ia\_admin, itil, or admin

## Procedure

1.  On the incident record, select the **Communicate** tab.

    The **Communicate** tab displays the list of communication tasks based on the communications configured for major incidents or incidents.

2.  Select the communication task where you want to compose the communication message.

    **Note:** Select the communication task based on the due dates to avoid breaching of any due date for communications. For example, communication tasks from the Overdue section.

3.  On the communication task, select **Compose**.

    The communication task record opens on a new tab within the incident view with the configured communication channels, such as DEX Desktop Assistant, email and SMS.

    **Note:**

    -   Based on the channel selected on the communication task, any or all of the following sections are displayed:
        -   DEX Desktop Assistant
        -   Email
        -   SMS
        -   SMS notification
        -   Sidebar discussion
        -   Microsoft Teams notification
        -   Slack
        -   Slack notifications
    -   For major incident SMS communications, you can select or change the SMS templates with any of the following user roles:
        -   major\_incident\_manager
        -   sn\_incident\_write user who has the required communication related roles
        -   ITIL user to whom the major incident is assigned
4.  On the form, fill in the fields.

<table id="table_lcn_3ng_z1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email template

</td><td>

Email template used for composing the email.**Note:**

Selecting this field displays two sections of email templates. The first section contains the GenAI templates with corresponding Now Assist for ITSM icon \(![Now Assist for ITSM icon](../../now-assist-itsm/image/icon-now-assist-panel.png)\) and the second section contains the non GenAI templates. The GenAI email templates are displayed only if the following conditions exist:

-   Any GenAI variable is available in the email templates.
-   Now Assist for ITSM is installed and activated.
-   GenAI skills are enabled.
-   User has the required roles to execute the GenAI skills.


</td></tr><tr><td>

To

</td><td>

List of users to whom the email is sent.

</td></tr><tr><td>

Cc

</td><td>

List of users to whom the email is sent as Cc.

</td></tr><tr><td>

Bcc

</td><td>

List of users to whom the email is sent as Bcc.

</td></tr><tr><td>

Subject

</td><td>

Subject of the email.

</td></tr><tr><td>

Body

</td><td>

Content of the email.

</td></tr><tr><td>

Attach file

</td><td>

Attachments for the email.

</td></tr></tbody>
</table><table id="table_myv_m42_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To

</td><td>

List of recipients to whom the notification is sent.**Note:** The recipients can receive the notification message in DEX Desktop Assistant only if the DEX Desktop Assistant installed on their device.

</td></tr><tr><td>

Template

</td><td>

Template used for composing the notification message.**Note:** If any template is available, the **Title** and **Message** field is auto-populated. However, you can edit the content and post them.

</td></tr><tr><td>

Title

</td><td>

Title of the notification message.

</td></tr><tr><td>

Message

</td><td>

Content of the notification message.

</td></tr></tbody>
</table>    For more information on DEX Desktop Assistant, see [Use DEX Desktop Assistant](../../digital-end-user-experience/concept/use-dex-desktop-exp.md).

    |Field|Description|
    |-----|-----------|
    |From|Number from which the message is sent.|
    |To|User to whom the message is sent.|
    |Message|Content of the message.|

    **Note:**

    -   Depending on the channel selected on the communication task, options such as email or SMS are displayed.
    -   SMS communication is sent to the recipient only if the recipient has a phone number linked to the recipient record.
    -   For all supported channels such as email, SMS, or DEX Desktop Assistant, Major Incident Management allows notification to be sent to all users \(employees\) in the affected locations. You can use the demo recipient list available in the base system as part of the installed demo data installed. The affected locations list can be accessed from the Affected locations related list in the **Related records** tab of a major incident record. For more information, see [View and update incident information on the Overview tab in SOW](view-update-inc-overview-tab.md).
5.  Select **Send**.


**Parent Topic:**[Communicating with stakeholders about incidents and major incidents in SOW](../concept/communicating-with-stakeholders-sow.md)


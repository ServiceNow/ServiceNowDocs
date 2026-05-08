---
title: Example Activity Definition: Send email
description: The following is an example of Send email activity definition.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Activity Definitions, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Example Activity Definition: Send email

The following is an example of Send email activity definition.

## Basic

The basic details capture the name \(label\), application, description, table, and from all the applications it’s accessible from.

Add the Automation plan, Activity experience and submit. After submitting, edit the document to add more details against each tab.

## Automation Plan

The Automation Plan associates the backend action or subflows built using the flow designer. This example uses: **Send Email - ESCM Activity** subflow.

This subflow enables sending an email. It has the core logic to send an email. It has all the input fields and output fields defined.

All the input fields are shown within the automation plan section. Each input field can be enabled to be visible only for the admin, in the standard modal, in the standard modal and the configuration panel:

-   **Admin visibility only**: when set to admin, only admin can view it.
-   **Include in standard model**: when set to view in the standard modal, it appears only in the properties modal.
-   **Include in standard model and configuration panel**: when set to view in the standard modal and the configuration panel, it appears in the PAD configuration panel as well as in the properties modal. For more information, see Activity definitions

You can define the input fields at the time of activity definition itself, provided you don't have any need to change these values at the time of configuration. This helps the business process owner save time while configuring an activity within a process.

## Activity Experience

The activity experience tab defines how the activity card is rendered at run time. The base system provides the following experience types:

-   Approval
-   Catalog Item
-   Create Record
-   Instructional
-   Knowledge
-   List
-   Notification
-   Record

Based on the type of experience you select, the further fields are populated. For more information, refer the ServiceNow AI Platform documentation.

In this example, **Record** type is selected.

**Note:** For example, if you want to render a table, you can choose list as the experience type.

## Associated Record

Use this record to store the associated data pertaining to the current activity. This would capture the run time data, as well the status of the experience.

-   Associated table: Flow Data
-   Associated Record: VL
-   Experience status table: Flow Data
-   Experience Status record: VL

In this example, Flow data table is used to capture the run time data. The run time data can vary based on the use case. In this example, the run time data are fields like To, cc, Subject, and body. For each use case, a flow data definition needs to be created to define the type of the run time data.

1.  Navigate to the left pane and enter **sys\_flow\_data\_definition.list**. It displays the list of definitions created for the flow data table.

    ![This is an associate record](../image/data-def.png "Associate record")

2.  Open **Email - SCM Def** to view the definition related to this example.

    ![Email - SCM Def](../image/email-scm-def.png "Email - SCM Def")

    This flow data definition must be used by the subflow or the action that is associated with this activity definition \(Refer automation plan\) to capture the run time data.

    ![Automation Plan](../image/activity-send-email.png "Activity Definitions")

3.  In this example, open the subflow: **Send Email - ESCM Activity**. Under **Create Flow Data** step, the flow data definition you created is mapped against the **Definition** field. This flow data record is used across the subflow. In this example, the activity card status \(experience status\) is captured in the flow data table.

    ![Create Flow Data](../image/crete-flow-data.png "Send Email - ESCM Activity")


**Note:** If you want to capture the runtime data in a different table record other than flow data table, say for example in a response task. You can select the associated table as Response task table. The associated record should be set to response task record created by the subflow.

Similarly, experience status table captures the status of the activity card. In the base system, the state field of the flow data table is mapped to the activity card status. So, when flow data table is used to capture the experience status, it automatically updates the activity card status. You could also use a different table other than flow data table to capture the experience status.

For example, if you would want to map the response task status to the activity card status then that is possible. To do so:

1.  Navigate to **All** &gt; **Playbook Experiences**.

    ![Playbook Experiences](../image/playbook-exp.png "Playbook experiences")

2.  Open **SIR Playbook experience**.
3.  Open **Status Mapping** related list.

    ![SIR Playbook experience](../image/status-mapp.png "Playbook experience")

4.  Enter the **Response Task** against Experience Status Table field.
5.  Enter the **State** against Experience Status field.

    ![Playbook experience Status Mapping](../image/new-status-mapp.png "Experience Status")

6.  Click **Submit**. The record is created.

    ![Experience Status to Activity State](../image/status-mapping.png "Playbook Experience Status Mapping")

7.  Under Experience Status to Activity State, map the states of response task to activity card status.
8.  The left side shows the states of the Response Task, and the right side shows the activity card status.

    ![Playbook Experience Status to Activity State Map](../image/status-map.png "Playbook Experience Status Mapping")

9.  The mapping can be bi-directional. Under Activity State to Experience related list as well, map the statuses correctly. This step is the reverse of the previous step. In this case, the left side shows the activity card status, and the right side shows the response task status.

    ![Playbook Experience Activity State to Experience Status Map](../image/status-map-new-rcord.png "Playbook Experience Status Mapping")


## Details

-   Tag Line: Send Email
-   Icon: Envelope outline \(not shown in the user interface\)
-   Title: **Activity** &gt; **Activity Instance** &gt; **Label**. Here we have selected the activity instance’s label. This dot-walking will replace the label value as the title dynamically at run time.
-   Description: **Activity** &gt; **Activity Instance** &gt; **Description**. Here we have selected the activity instance’s description. This dot-walking will replace the label value as the title dynamically at run time.
-   Pending State Title: Send an email notification. This is the title when the activity is in Pending status.
-   Pending State Description: Prompts for confirmation of email subject and body before sending. This is the description of the activity card when the status is pending Record Fields: There are record fields selected in this example.

    Record Fields are comma-separated list of field names to display for the associated record in a name-value pair list. Data is pre-fetched on the server, dot-walking is supported and  **canRead\(\)** permissions are evaluated on each field.

-   Footer: There’s no footer defined for this example.

    Footer is a text in a gray area of the card footer. You can add any meaningful information to shown.

    ![Activity Definition - Send Email page](../image/details.png "Activity Definition - Send Email")


## Form

-   Form View: collect\_data
-   Form Fields:

This example uses collect\_data view to show the fields that must be presented to the user to enter inputs. Collect\_data view is a platform provided view corresponding to flow data table. Alternatively, you could leave Form View as empty, and select Vars from the list of values available against Form Fields. \(click the lock icon to open the list of available values\).

![Form](../image/form.png "Form view")

## Attachments

In this example:

-   Attachment Source is empty.
-   Attachment Read only not selected.

1.  Attachment Source - Drop down. What attachments to show on the card: Those attached to the Parent Record, the Associated Record, or none.
2.  Attachment Read only - True or False. Prevent the user from renaming or deleting the existing attachments.

![Activity Definition - Send Email page](../image/attach.png "Activity Definition - Send Email")

## Features

In this example,

-   Show SLA - Cleared
-   Show Checklist - Cleared
-   Is Automated - Cleared

Show SLA: True / False. Renders an SLA timer in the header of the card for the Associated Record. The SLA is chosen according to the SLA Configuration record specified in the Playbook configuration.

1.  Show Checklist  - True or False. Renders any checklist that is attached to the Associated Record. The checklist is editable and changes are saved without requiring a Declarative Action.
2.  Is Automated - True or False. If true, then the  **tagline**  and  **icon**  will be overridden with the text **Automated Task** and an automated icon.

![Activity Definition - Send Email Form page](../image/feaures.png "Activity Definition - Send Email Form")

## Playbook Actions in Activity Definition

This section has the actions that will be rendered on the activity card. This example has **Skip**, and **Send Email** as actions.

To add a new action to the activity card, you must create a record in the **Playbook Actions** related list present at the bottom of the page.

![Playbook Actions](../image/actions.png "Playbook Actions")

1.  Click **New**.
2.  Select existing activity action against Action Assignment field.
3.  Select **SIR Playbook Experience** against Playbook Experience field.

-   **[Create an Activity Action](steps-to-create-an-activity-action.md)**  
Following is procedure to create an activity action.

**Parent Topic:**[Activity Definitions](../concept/build-activities.md)


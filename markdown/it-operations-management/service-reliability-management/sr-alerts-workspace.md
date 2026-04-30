---
title: SRM alert workspace
description: The alert workspace contains various areas containing alert details and possible actions.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Exploring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# SRM alert workspace

The alert workspace contains various areas containing alert details and possible actions.

The base state of an alert in a configured system is open and unacknowledged.

**Alert forms**

**Note:** Managers or responders can assign individual alerts to someone without acknowledging the alert. The assigned responder is notified and can choose to acknowledge or reassign them.

The header contains the alert description and any tags as well as the **Save** button.

**Note:** Tags are imported from third-party integrations, such as Datadog, and attached to alerts. However, you can also create tags to categorize data and drive system logic in response or grouping rules or using the tag icon ![tag icon](../image/icon-sr-tag.png). For more information on creating and viewing tags, see [Manually create SRM tags](../task/sr-create-tags.md).

**Details tab**

The Details tab alert form contains not only the information related to the alert but options to search for further information and take actions.

This section contains three content panels: **Alert**, **Compose** and **Activity**, and the far right side panel containing **Attachments** and **Templates**.

**Note:** If there are existing templates, they are displayed but creating templates is not available in SRM.

**Note:** When an editable field is updated, notifications are sent based on user notification preferences.

<table id="id_iwk_z53_vyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Imported service associated with the alert, if available. You can edit this field from a list menu.**Note:** When you set a service, and that service has an assigned team, the assigned team of that service is automatically assigned to the incident.

Use the Information icon, , to view the service details.

</td></tr><tr><td>

Severity

</td><td>

Imported priority on the alert. You can edit this field. Choices are:

1.  Critical
2.  Major
3.  Minor
4.  Warning
5.  OK
6.  Clear

</td></tr><tr><td>

Source URL

</td><td>

Imported URL from the source of the alert.

</td></tr><tr><td>

State

</td><td>

Imported node on the alert.

</td></tr><tr><td>

Node

</td><td>

Team of the alert assignee. You can edit this field.

</td></tr><tr><td>

Acknowledged

</td><td>

Check box. Indicates whether the alert has been acknowledged or not. Acknowledgement doesn't automatically assign the alert.

</td></tr><tr><td>

Resource

</td><td>

Imported resource from the alert.

</td></tr><tr><td>

Updated

</td><td>

Date and time when the alert was last updated.

</td></tr><tr><td>

Configuration item

</td><td>

Imported asset associated with the alert.

</td></tr><tr><td>

Parent alert

</td><td>

The alert this alert is related to, if it is a related alert.

</td></tr><tr><td>

Task

</td><td>

Selectable task to associate with the alert.

</td></tr><tr><td>

Knowledge article

</td><td>

Select a knowledge article to associate with the alert.

</td></tr><tr><td>

Metric Name

</td><td>

Imported name of the metric associated with the alert.

</td></tr><tr><td>

Overall event count

</td><td>

Imported number of events associated with this alert.

</td></tr><tr><td>

Assigned to

</td><td>

Individual assigned to the alert. This assignee can be the person who acknowledged it or the one reassigned to it. You can edit this field.

</td></tr><tr><td>

Description

</td><td>

Imported description of the alert.

</td></tr><tr><td>

Message key

</td><td>

Identifier for multiple events related to the same alert. **Note:** If this value is empty on import, then it is generated from the **Source**, **Node**, **Type**, **Resource**, **Metric Name**, and **Service Id** field values.

</td></tr><tr><td>

Work notes

</td><td>

Add any relevant additional information.

</td></tr></tbody>
</table>**Secondary Alerts tab**

This tab contains any alerts associated with this alert.

Each record contains the following fields: \(You can refresh, edit columns, and filter the list\).

**Note:** All field values are imported from the related alert record.

|Field|Description|
|-----|-----------|
|Number|Related alert identifier.|
|Initial event time|Date and time when the event that triggered the related alert happened.|
|Short description|Short description of the related alert.|
|Impacted services|Services impacted by the related alert.|
|Severity|Severity of the related alert.|
|State|Related alert state.|

**Alert executions**

This tab contains any alerts management executions associated with this alert.

Each record contains the following fields: \(You can refresh, edit columns, and filter the list\).

|Field|Description|
|-----|-----------|
|Management rule|Rule associated with this alert.|
|Action name|Name of the action that the alert rule specified.|
|Link to execution|Link to executed actions.|
|Related Task|Task associated with the alert.|
|Log|Log file for the alert.|
|Automatic run|Whether executions are automatically running or not.|
|Created|Date and time the execution took place.|

**Probable root causes**

This tab contains any alerts associated with this alert.

Each record contains the following fields: \(You can refresh, edit columns, and filter the list\).

|Field|Description|
|-----|-----------|
|Root cause task|Task associated with the probable root cause.|
|Root cause alert|Alert associated with the probable root cause.|
|Configuration item|Asset associated with the probable root cause.|
|Description|Description of the probable root cause.|
|Type|Type associated with probable root cause.|
|Score|Scoring for the probable root cause.|

**Impacted services**

This tab contains any alerts associated with this alert.

Each record contains the following fields: \(You can refresh, edit columns, and filter the list\).

You can add a service to this alert using the **New** button.

<table id="id_f4w_n1j_vyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the impacted service for this alert.

</td></tr><tr><td>

Severity

</td><td>

Action icon that the alert rule specified.

</td></tr><tr><td>

Business Criticality

</td><td>

Icon shows whether the action executed successfully or not.

</td></tr><tr><td>

Service classification

</td><td>

Actions taken or error messages.

</td></tr><tr><td>

Managed by

</td><td>

Date and time the action was taken.

</td></tr><tr><td>

Owned by

</td><td>

Team member responsible for the service

</td></tr><tr><td>

Approval group

</td><td>

Team responsible for approvals.

</td></tr><tr><td>

Location

</td><td>

Geographical or physical location.

</td></tr><tr><td>

Operational status

</td><td>

Status of the service. Choices are:-   Operational
-   Non-Operational
-   Repair in Progress
-   DR Standby
-   Ready
-   Retired
-   Pipeline
-   Catalog

</td></tr></tbody>
</table>**Alert Insight CI Change Request**

This tab contains any CI change requests associated with this alert.

Each record contains the following fields: \(You can refresh, edit columns, and filter the list\).

With the itil role, you can add a change request to this alert using the **New** button. This is not implemented in SRM alone.

**Note:** For more detailed information on change requests, see [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

|Field|Description|
|-----|-----------|
|Name &amp; Description|ID and short description of the response rule that ran on this alert.|
|Short description|Short description of the change request associated with this alert.|
|Type|Type of change request.|
|State| |
|Planned start date|Date change is expected to start.|
|Planned end date|Date change is expected to be finished.|
|Assigned to|Team member the change request is assigned to.|

**Compose** panel

Work notes are added to the Activity timeline automatically. Add comments using the **Compose** text box. Notifications are sent for all updates based on user notification preferences.

**Activity** panel

Activity stream that contains all the system activity, comments, and work notes. You can filter, sort, expand or collapse all posts using the header icons. ![These are the buttons to filter, sort, expand, collapse, or select more actions.](../image/icon-sr-activity-header.png)

**Note:** The filter option includes **Post types**, **Field changes**, **Filter sets**, and **Flagged**. All choices are selected by default. Flagged entries are either all or none.

**Actions** panel

**Attachments** section is open by default. Click the ![Paper clip icon used for attachments.](../image/icon-sr-attachment.png) attachment icon to close.

On the **Attachments** panel, you can initially **Browse** your local hard drive for files.

Once you have added attachments, you can:

-   Sort attachments from newest to oldest, or vice versa using the Sort icon ![Sort icon.](../image/icon-sr-sort-attach.png).
-   Search for an attachment based on its name or extension

    **Note:** You must have two or more attachments to search.

    ![An image showing the search bar for attachments.](../image/sr-search-attach-field.png)

-   Upload a new attachment using the \(![Add icon](../image/icon-sr-add.png)\) icon
-   Download an existing attachment using the More actions icon \(![More actions icon](../image/icon-sr-more-actions-vertical.png)\) to the right of the attachment.
-   Remove an existing attachment using the More actions icon to the right of the attachment.
-   Rename an existing attachment using the More actions icon to the right of the attachment.

    ![When selecting More actions, you can select download, remove, or rename.](../image/sr-attach-menu.png)


**Template** panel

Open the Template panel using the Template icon ![Template icon.](../image/icon-sr-template.png).

**Note:** If there are existing templates, they are displayed but creating templates is not available in SRM.

See [Manually create an SRM template](../task/sr-create-template.md) to create your own templates.

**Collaboration** panel

Displays available Zoom meeting or Microsoft Teams or Slack channels to start or join.

To start or join a Zoom meeting:

**Note:** The Zoom integration and recognized IDs must be active in your instance. If Start Channel is unavailable, contact your administrator.

1.  Select **Start Zoom**.
    -   A meeting pop-up appears.
    -   Add participants.
    -   Select **Create Meeting**.
    -   The meeting is created, invitations are sent, and you join the meeting.

        **Note:** Any issues found when starting a meeting are shown in a banner message.

2.  Select **Join Meeting**
    -   **Sign in** to your Zoom account.
    -   You join the Zoom meeting.

Start or join a Microsoft Teams channel:

**Note:** The Microsoft Teams integration and recognized IDs must be active in your instance. If Start Channel is unavailable, contact your administrator.

1.  Select **Start Channel**.
    -   Sign in to your Microsoft Teams account.
    -   Select **Create**. You are redirected to the Microsoft Teams application.
    -   Back in the Collaboration column, the **Join Channel** button is activated.

        **Note:** Any issues found when joining a channel are shown in a banner message.

2.  Select **Join Channel** in the Collaboration panel in SRM.
3.  Sign into your Microsoft Teams account.

    You are taken to the channel in Microsoft Teams.


Start or join a Slack channel:

**Note:** The Slack integration and recognized IDs must be active in your instance. If Start Channel is unavailable, contact your administrator.

1.  Select **Start Slack**.
    -   Add participants in the Create a Slack channel pop-up.
    -   Select **Create**. You are redirected to the Slack application.
    -   Back in the Collaboration column, the **Join Slack** button is activated.

        **Note:** Any issues found when starting a channel are shown in a banner message.

2.  Select **Join Channel** in the Slack application window.
3.  Sign into you Slack account.

    You are taken to the Slack channel.


**Note:** When a Zoom meeting, Microsoft Teams, or Slack channel is created, details for the meeting or channel are posted as work notes to the timeline.

**Responders** tab

Add responders from the list menu and select the Add icon. Responders are notified based on their notification preferences.

**Parent Topic:**[Exploring Service Reliability Management](../concept/exploring-service-reliability-management.md)


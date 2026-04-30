---
title: SRM incident workspace
description: The incident workspace contains various panels containing incident details and possible actions.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Exploring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# SRM incident workspace

The incident workspace contains various panels containing incident details and possible actions.

The top header contains description information, tags, priority information, state, service, and assignment group.

**Note:** Tags are imported from third-party integrations and attached to incidents. However, you can also create tags to categorize data and drive system logic using the Tag icon ![Tag icon](../image/icon-sr-tag.png). For more information on creating and viewing tags, see [Manually create SRM tags](../task/sr-create-tags.md).

When selecting an incident, you are taken to an overview. This section contains three content panels: Summary, Activity, and Recommended actions.

**Note:** When an editable field is updated, notifications are sent based on user notification preferences.

In the Impact Summary, you will find the following information:

|Field|Description|
|-----|-----------|
|Configuration item|Name of and link to the configuration item associated with this incident.|

|Field|Description|
|-----|-----------|
|Configuration item|Name of and link to the configuration item associated with this incident.|
|Managed by|Team responsible for the incident.|
|Owned by|Incident owner.|
|Approval group|Team responsible for approvals.|
|Location|Geographical location of the incident if defined.|
|Operational status|Status of the incident.|
|Manually added.|Whether this incident was manually added or the result of an error budget policy.|

<table id="id_c1t_2ml_wyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the incident.

</td></tr><tr><td>

Number

</td><td>

Incident identifier.

</td></tr><tr><td>

Impact

</td><td>

Impact is a measure of the effect of an incident on business processes. Choices are:

-   1 - High
-   2 - Medium
-   3 - Low

</td></tr><tr><td>

Assignment group

</td><td>

Team assigned to the incident.

</td></tr><tr><td>

Priority

</td><td>

Priority is based on **Impact** and **Urgency**, and it identifies how quickly the incident should be addressed. Choices are:

-   High Impact = Critical Priority
-   Medium Impact = High Priority
-   Low Impact = Moderate

**Note:** See Priority Data Lookup rules below.

</td></tr><tr><td>

Category

</td><td>

Category of the incident. Choices are:

-   Inquiry/Help
-   Software
-   Hardware
-   Network
-   Database

</td></tr><tr><td>

Urgency

</td><td>

Urgency is a measure of how long the resolution can be delayed until an incident has a significant business impact.

</td></tr><tr><td>

Service

</td><td>

Affected service associated with the incident. You can edit this field from a list menu.**Note:** When you set a service, and that service has an assigned team, the assigned team of that service is automatically assigned to the incident.

</td></tr><tr><td>

Severity

</td><td>

Imported severity on the incident. Values P1–P5.

</td></tr><tr><td>

Configuration item

</td><td>

Asset associated with the incident.

</td></tr><tr><td>

Assigned to

</td><td>

Individual responsible for resolving the incident.

</td></tr><tr><td>

State

</td><td>

State of the incident. The state moves and tracks incidents through several stages of resolution.Choices are:

-   New
-   In Progress
-   Ob Hold
-   Resolved
-   Canceled

</td></tr><tr><td>

Watch list

</td><td>

Individuals interested in the incident. Subscribes them to notifications according to their preferences.

</td></tr><tr><td>

Resolution code

</td><td>

Code associated with the resolution.Choices are:

-   None \(default\)
-   Duplicate
-   Known error
-   No resolution provided
-   Resolved by caller
-   Resolved by change
-   Resolved by problem
-   Resolved by request
-   Solution provided

</td></tr><tr><td>

Resolution notes

</td><td>

Detailed information on the resolution. Resolution notes are posted to the **Activity** timeline.

</td></tr></tbody>
</table>**Note:** Priority is calculated according to the following sample data lookup rules:

|Impact|Urgency|Priority|
|------|-------|--------|
|1 - High|1 - High|1 - Critical|
|1 - High|2 - Medium|2 - High|
|1 - High|3 - Low|3 - Moderate|
|2 - Medium|1 - High|2 - High|
|2 - Medium|2 - Medium|3 - Moderate|
|2 - Medium|3 - Low|4 - Low|
|3 - Low|1 - High|3 - Moderate|
|3 - Low|2 - Medium|4 - Low|
|3 - Low|3 - Low|5 - Planning|

When a Service is deleted, its integrations, alerts, incidents, and automations are removed. This is not a recoverable action so consider deactivating the service instead.

The Related Records tab contains any alerts associated with this incident.

**Note:** All field values are imported from the related records and are not editable from SRM.

|Field|Description|
|-----|-----------|
|Number|Identifier for the related incident.|
|Short description|Brief description of the related incident.|
|Priority|Priority of the related incident.|
|State|State of the related incident.|
|Assigned to|Team member assigned to the related incident.|
|Assignment group|Team assigned to the related incident.|
|Service|Service associated with the related incident.|

|Field|Description|
|-----|-----------|
|Number|Identifier for the related alert.|
|Severity|Severity of the related alert.|
|Short description|Brief description of the related alert.|
|Acknowledged|Whether the related alert has been acknowledged or not.|
|Assigned to|Team member assigned to the related alert.|
|Configuration item|Asset associated with the related alert.|
|Parent|Primary alert associated with the related alert.|

|Field|Description|
|-----|-----------|
|Number|Identifier for the related changes associated with this incident.|
|Short description|Brief description of the related changes associated with this incident.|
|Type|Type of the recent changes associated with this incident.|
|State|State of the recent changes associated with this incident.|
|Planned start date|Date and time to begin changes associated with this incident.|
|Planned end date|Date and time to begin changes associated with this incident.|
|Assigned to|Team member responsible for the change request associated with this incident.|

|Field|Description|
|-----|-----------|
|Short description|Brief description of the change request associated with this incident.|
|Type|Type of the change request associated with this incident.|
|State|State of the change request associated with this incident.|
|Planned start date|Date and time to begin change request work associated with this incident.|
|Planned end date|Date and time change request work associated with this incident ended.|
|Assigned to|Team member responsible for the change request associated with this incident.|

**Postmortem tab**

About Postmortem owner:

-   If a Scribe has already been chosen in the Collaboration panel Responders list, they are automatically made the owner.
-   If there is more than one scribe then the first one assigned is chosen. Otherwise, you can select an owner from the list menu.
-   If a new scribe is added or an existing user persona is changed to Scribe, that user is made the owner.
-   If you manually remove an owner, no new owner is automatically selected.

Each section of the postmortem can be edited, excluded from a PDF, deleted, or reordered using drag-and-drop.

You can add new sections using the add icon ![Add icon.](../image/icon-sr-add.png).

For more detailed information on editing postmortems, see .

**Compose** panel

Work notes are added to the Activity timeline automatically. Visible to responders and above. Add comments using the **Compose** text box.

Comments are added to the Activity timeline automatically. Visible to everyone in SRM.

**Activity** section

Stream that contains all the system activity, and resolution notes. You can filter, sort, expand or collapse all posts using the header icons. ![Header icons.](../image/icon-sr-activity-header.png)

**Note:** The filter option includes **Post types**, **Field changes**, and **Filter sets**. All choices are selected by default. Flagged entries are either all or none.

![Activity section showing selected filters](../image/sr-incident-timeline-options.png)

**Actions** panel

**Note:**

The **Notifications**, **Agent assist**, **Expert on-call**, and **Email templates** panels are not currently supported in SRM.

**Attachments** section

Open the **Attachments** section using the Attachment icon ![Attachment icon](../image/icon-sr-attachment.png).

On the **Attachments** section, you can initially **Browse** your local hard drive for files.

Once you have added attachments, you can:

-   Search for an attachment based on its name or extension

    **Note:** You must have two or more attachments to search.

-   Upload a new attachment using the \(![Attachments](../image/icon-sr-add.png)\) icon
-   Download an existing attachment using the More actions icon \(![More actions icon.](../image/icon-more-options.png)\) to the right of the attachment.
-   Remove an existing attachment using the More actions icon to the right of the attachment.
-   Rename an existing attachment using the More actions icon to the right of the attachment.

    ![More actions icon.](../image/sr-attach-menu.png)


**Template** section

Open the **Template** panel using the Template icon ![Template icon](../image/icon-sr-template.png).

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


**Parent Topic:**[Exploring Service Reliability Management](../concept/exploring-service-reliability-management.md)


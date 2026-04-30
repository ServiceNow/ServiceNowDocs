---
title: Microsoft Exchange Online Spoke
description: The Microsoft Exchange Online spoke creates and manages calendar and mail in Microsoft Exchange Online. To create, manage, or delete users and groups, use the Microsoft Azure AD spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 12
keywords: [AI Agent, Agentic AI]
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Exchange Online Spoke

The Microsoft Exchange Online spoke creates and manages calendar and mail in Microsoft Exchange Online. To create, manage, or delete users and groups, use the Microsoft Azure AD spoke.

**Note:** User and group management can be done using Microsoft Azure AD only and not Microsoft Exchange Online spoke.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Exchange Online spoke v3.12.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Remote Tables \(com.glide.script.vtable\)
-   System Import Data Source \(com.glide.system\_import\_data\_source\)
-   iHub Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported version

Microsoft Graph REST API v1.0

## Spoke module

The Microsoft Exchange Online spoke adds the Microsoft Exchange Online application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Events|Displays the list of events in Microsoft Exchange Online.|
|Subscriptions|Displays the list of subscriptions in Microsoft Exchange Online.|
|Webhook Registry|Displays the list of webhook registries of Microsoft Exchange Online.|
|Calendars|Displays a list of calendars in Microsoft Exchange Online.|
|Calendar Events Transform Data|Displays the list of records from the data source.|

## Spoke flows

The Microsoft Exchange Online spoke provides sample flows in the published state to demonstrate automating renewing subscriptions. Available sample flows include:

|Flow|Description|
|----|-----------|
|Renew Subscriptions|Retrieves all the subscription records and renews the subscriptions if a renewal is required, based on the expiration time. If any subscription has its status marked as 'Being deleted', then its record is deleted and isn’t considered for renewal.|

## Spoke subflows

The spoke provides subflows in the Published state to integrate with the Microsoft Exchange Online service. These subflows can be used as part of other subflows and flows.

<table id="table_flk_32k_npb"><thead><tr><th>

Category

</th><th>

Subflows

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Webhook management

</td><td>

Check Event Subscription

</td><td>

Checks if a webhook subscription with specified event resource, or notification URL and change type exists.

</td></tr><tr><td>

Create or Update Subscription Record

</td><td>

Checks if the specified subscription record exists in Microsoft Exchange Online and updates the subscription record if it exists. If the subscription record doesn’t exist, a new subscription record is created.

</td></tr><tr><td>

Create or Update Subscriptions for Resources

</td><td>

Checks for the subscriptions for the specified resources. If the subscription for the specified resources don’t exist, then new subscriptions are created.**Note:** This subflow is available only when the Workplace Calendar Synchronization plugin is already installed.

</td></tr><tr><td>

Delete Subscription

</td><td>

Deletes the specified subscription when the specified subscription is related only with the specified application.

</td></tr><tr><td>

Recreate Removed Subscription

</td><td>

Recreates a removed webhook subscription using the details from the related subscription record.

</td></tr><tr><td>

Subscription Lifecycle Management

</td><td>

Manages the lifecycle of a webhook subscription.

</td></tr><tr><td rowspan="9">

Calendar Management

</td><td>

Calendar Synchronization

</td><td>

Synchronizes the calendar by retrieving events from the Exchange Online Calendar Events Transformed Data table and adding the retrieved events to the Microsoft Exchange Online Events table. It creates a subscription if a valid subscription doesn’t exist for the user's specified calendar.

</td></tr><tr><td>

Create or Update Event Record

</td><td>

Checks for the specific existing event record and updates with the specified properties. If the specified event record does not exist, a new event record is created.

</td></tr><tr><td>

Delete Calendar Scheduling Event

</td><td>

Deletes the specified event in Microsoft Exchange Online and the related records from events tables, related attachments, related records from event attendees and event to subscription m2m tables.

</td></tr><tr><td>

Delete Event Record

</td><td>

Deletes the specified event record from events tables and the related attachments, related records from event attendees and event to subscription m2m tables.

</td></tr><tr><td>

Event Lifecycle Management

</td><td>

Retrieves the event details and updates the records in event, attendees, event to subscription m2m tables accordingly.

</td></tr><tr><td>

Look up and Update Attachments to Event Record

</td><td>

Retrieves the attachments of a specific event record from Microsoft Exchange Online and updates them.

</td></tr><tr><td>

Look up and Update Calendar Scheduling Change

</td><td>

Retrieves the event details of a specified event record and updates them.

</td></tr><tr><td>

Sync up Events

</td><td>

Synchronizes the calendar view based on the data from the Exchange Online Calendar Events Transformed Data table.

</td></tr><tr><td>

Update Calendar Scheduling Event

</td><td>

Updates the properties of an event object in Microsoft Exchange Online and the related record in the events table.

</td></tr></tbody>
</table>**Note:**

-   Use the Microsoft Exchange Online Webhook Registry table to generate a callback URL and store the secret value \(Client state\) for webhook subscriptions.
-   Make sure that webhook subscription is stored in the Microsoft Exchange Online Subscriptions table with the Status field set to Active.

## Spoke actions

The Microsoft Exchange Online spoke provides actions to automate calendar and mail tasks when an incident is created in the ServiceNow instance.

|Category|Action|Description|
|--------|------|-----------|
|Calendar Management|Copy Attachment to Calendar Event|Copies a ServiceNow attachment to an Exchange calendar event.|
|Create Calendar Event|Creates an event in the user's default calendar and specifies the time zone for the start and end times of the event.|
|Create Recurring Calendar Events|Creates a recurring event in the user's default calendar and specifies the time zone for the start and end times of the event.|
|Delete Attachment|Deletes the specified attachment in the specified event.|
|Delete Calendar Event|Deletes a calendar event.|
|Find Meeting Times|Retrieves meeting times and locations based on the availability of the meeting organizer and attendees for the specified time and locations.|
|Look up Attachments by Event ID|Retrieves all the attachments in the specified event.|
|Look up Calendar by ID|Retrieves the calendar details for the specified ID.|
|Look up Calendar Events by User ID|Retrieves the list of event objects in the user's mailbox.|
|Look up Calendar View Stream|Retrieves the list of meeting entries for the specified User ID for the specified time period.|
|Look up Calendars Stream|Retrieves details of the calendars of all the users.|
|Look up Event by ID|Retrieves the calendar event details for the specified ID.|
|Look up Schedules|Retrieves the list of schedules.|
|Look up Out of Office Settings|Retrieves the details of the out-of-office settings for the specified recipients.|
|Look up Time Zones|Retrieves details of all the available time zones.|
|Update Calendar Event|Updates the properties of an event object.|
|Mail Management|Delete Message|Deletes the message in a user's inbox or from a custom folder.|
|Look Up Mail Folders by User ID|Retrieves all the mail folders for a specified User ID.|
|Look Up Messages by Mail Folder ID|Retrieves all the messages in a mail folder.|
|Look Up Messages by User ID|Retrieves all the messages in the inbox folder of the user.|
|Send Mail|Sends an email with the message subject and message body to the specified list of recipients.|
|Set Mailbox Auto Reply|Sets the user’s auto-reply message for the given time period.|
|Webhook Management|Look up Subscription by ID|Retrieves details of the webhook subscription for the specified ID.|
|Look up Subscriptions Stream|Retrieves details of all webhook subscriptions.|
|Renew Webhook Subscription|Renews the subscription of the specified webhook.|
|Subscribe Webhook|Creates a webhook subscription for the specified resource.|
|Unsubscribe Webhook|Deletes the specified webhook subscription.|
|Mailbox Management|Create MailBox|Creates mailboxes and user accounts simultaneously.|
|Delete MailBox|Deletes or disables mailboxes and user accounts simultaneously.|
|Enable MailBox|Enables a mailbox in Microsoft Exchange Online. The mailbox can be in an archived state.|
|Look up MailBox|Retrieves the list of mailboxes.|
|User Management|Look up Relevant Users Stream|Retrieves a stream of users who are most relevant to the specified user, based on collaboration and organizational context. Relevance is determined by the user's communication and collaboration patterns, and business relationships.|

Permissions required to run these actions are:

|Category|Action|Permission type|Permissions \(from least to most privileged\)|
|--------|------|---------------|---------------------------------------------|
|Calendar Management|Copy Attachment to Calendar Event|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Create Calendar Event|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Create Recurring Calendar Events|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Delete Attachment|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Delete Calendar Event|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Find Meeting Times|Delegated \(work or school account\)|Calendars.Read, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Not supported.|
|Application|Not supported.|
|Look up Attachments by Event ID|Delegated \(work or school account\)|Calendars.Read|
|Delegated \(personal Microsoft account\)|Calendars.Read|
|Application|Calendars.Read|
|Look up Calendar by ID|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Application|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Look up Calendar Events by User ID|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Application|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Look up Calendar View Stream|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Application|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Look up Calendars Stream|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read, Calendars.Read.Shared, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadBasic, Calendars.Read, Calendars.Read.Shared, Calendars.ReadWrite|
|Application|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Look up Event by ID|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read|
|Delegated \(personal Microsoft account\)|Calendars.ReadBasic, Calendars.Read|
|Application|Calendars.ReadBasic, Calendars.Read|
|Look up Schedules|Delegated \(work or school account\)|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Not supported.|
|Application|Calendars.ReadBasic, Calendars.Read, Calendars.ReadWrite|
|Look up Out of Office Settings|Delegated \(work or school account\)|Mail.Read, Mail.Read.Shared|
|Delegated \(personal Microsoft account\)|Mail.Read|
|Application|Mail.Read|
|Look up Time Zones|Delegated \(work or school account\)|User.Read, User.ReadBasic.All|
|Delegated \(personal Microsoft account\)|User.Read|
|Application|User.Read.All|
|Update Calendar Event|Delegated \(work or school account\)|Calendars.ReadWrite|
|Delegated \(personal Microsoft account\)|Calendars.ReadWrite|
|Application|Calendars.ReadWrite|
|Mail Management|Delete Message|Delegated \(work or school account\)|Mail.ReadWrite|
|Delegated \(personal Microsoft account\)|Mail.ReadWrite|
|Application|Mail.ReadWrite|
|Look Up Mail Folders by User ID|Delegated \(work or school account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Delegated \(personal Microsoft account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Application|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Look Up Messages by Mail Folder ID|Delegated \(work or school account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Delegated \(personal Microsoft account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Application|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Look Up Messages by User ID|Delegated \(work or school account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Delegated \(personal Microsoft account\)|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Application|Mail.ReadBasic, Mail.Read, Mail.ReadWrite|
|Send Mail|Delegated \(work or school account\)|Mail.Send|
|Delegated \(personal Microsoft account\)|Mail.Send|
|Application|Mail.Send|
|Set Mailbox Auto Reply|Delegated \(work or school account\)|MailboxSettings.ReadWrite|
|Delegated \(personal Microsoft account\)|MailboxSettings.ReadWrite|
|Application|MailboxSettings.ReadWrite|
|Mailbox Management|Create MailBox|These actions uses powershell cmdlets and hence doesn’t requires API permissions.|
|Delete MailBox|
|Enable MailBox|
|Look up MailBox|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Microsoft Exchange Online calendar management AI agent|Automates workflows related to the calendar within Microsoft Exchange Online such as calendar event management, attachment handling, and time zone look ups.|
|Microsoft Exchange Online room management AI agent|Automates workflows related to the room management within Microsoft Exchange Online such as 'Look up Rooms Stream'.|
|Microsoft Exchange Online metadata retrieval management AI agent|Automates workflows related to the room metadata management within Microsoft Exchange Online such as looking up room metadata and time zone metadata.|
|Microsoft Exchange Online meeting scheduler AI agent|Automates calendar management tasks within Microsoft Exchange Online. It enables users to find the available meeting time slots and create the meetings accordingly.|
|Microsoft Exchange Online mail manager|Automates mail management tasks within Microsoft Exchange Online such as look up mail folders and messages, delete messages, and set mailbox auto-replies.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Microsoft account requirements

The Microsoft Exchange Online spoke needs registering an application using the Microsoft Azure portal to generate OAuth 2.0 tokens.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Microsoft Exchange Online spoke](../task/setup-ms-exch-ol.md#).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use PowerShell. Make sure that Power Shell with EXO V2 module is installed. This module is required for executing the Mailbox management actions. Use the connection record associated with the Mailbox alias to configure where actions run as well as set MID Server selection attributes. For more information about the MID Server, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


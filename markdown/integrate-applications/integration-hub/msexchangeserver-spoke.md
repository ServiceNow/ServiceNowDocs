---
title: Microsoft Exchange Server Spoke
description: The Microsoft Exchange Server spoke creates and manages address list, mailbox, and calendar events in Microsoft Exchange mail system.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Exchange Server Spoke

The Microsoft Exchange Server spoke creates and manages address list, mailbox, and calendar events in Microsoft Exchange mail system.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Exchange Server spoke v2.5.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - PowerShell \(com.glide.hub.action\_step.powershell\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

-   Exchange Server 2016 installed on Windows Server 2016

    **Note:** The Create Calendar Event For User and Lookup Room Availability actions are supported only on Exchange Server 2013.

-   Exchange Server 2013 installed on Windows Server 2012 R2

This spoke may be compatible with the earlier versions of Microsoft Exchange Server.

## Spoke requirements

Powershell remoting must be enabled on the target Exchange Server. For more information about the Microsoft Exchange Server, see [Exchange Server documentation](https://docs.microsoft.com/en-us/exchange/exchange-server?view=exchserver-2019).

## Spoke flows

The Exchange Server spoke provides sample flows to demonstrate automating the Exchange Server tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Pull From Subscriptions|Uses the Look up Items From Subscription ID subflow to periodically retrieve the modified items in an active subscription and saves the details in the ServiceNow instance.|
|Look up Calendar Item from Item ID Flow|Uses the Look up Items From Subscription ID subflow to display the details of the modified items in a subscription in the Subscription to Events Mapping module.|
|Renew Subscription|Uses the Renew Subscription subflow to renew subscription.|

**Note:** Subscriptions are valid for 24 hours and flows renew the subscriptions periodically. If there are failures with the third-party applications, subscriptions will not be renewed. That is, **Active** is set to **False**. In the event of failure, you should use the create subscription flow to create a subscription.

## Spoke subflows

The Exchange Server spoke provides sample subflows to demonstrate automating the Exchange Server tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Look up Items From Subscription ID|Saves the details of the modified items in a subscription to the Event to Subscription Mapping table.|
|Create Subscription|Creates a subscription for the specified mailbox and adds it to the Subscription table. If the subscription already exists, the subflow adds the application details to the subscription record.|
|Renew Subscription|Renews a subscription for the given mailbox.|

## Spoke actions

The Microsoft Exchange Server spoke provides actions to automate address list, mailbox, and calendar event tasks.

<table id="table_rfs_y41_vhb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="10">

Address List Management

</td><td>

Create Address List Using Included Recipients

</td><td>

Creates a new address list in Exchange Server using the **Included Recipients** field.

</td></tr><tr><td>

Create Address List Using Recipient Filter

</td><td>

Creates a new address list in Exchange Server using the **Recipient** field.

</td></tr><tr><td>

Delete Address List

</td><td>

Deletes the required address list on a required Exchange Server.

</td></tr><tr><td>

Get Address List Details

</td><td>

Retrieves the details of a required address list on a required Exchange Server.

</td></tr><tr><td>

Look Up Address List

</td><td>

Retrieves the address list details on a required Exchange Server using a search query.

</td></tr><tr><td>

Look up Address List Details

</td><td>

Retrieves details of the specified address list by identity.

</td></tr><tr><td>

Move Address List

</td><td>

Moves an address list to another location in the address hierarchy.

</td></tr><tr><td>

Synchronize Address List

</td><td>

Refreshes email clients with the latest details, for a required address list in Exchange Server.

</td></tr><tr><td>

Update Address List Using Included Recipients

</td><td>

Updates details and recipients of a required address list using a the **Included Recipients** field.

</td></tr><tr><td>

Update Address List Using Recipient Filter

</td><td>

Updates details and recipients of a required address list details using the **Recipient Filter** field.

</td></tr><tr><td rowspan="11">

Mailbox Management

</td><td>

Create Calendar Event For User

</td><td>

Creates a calendar event in Exchange Server. Calendar event can be either a meeting or appointment.**Note:**

-   This action is supported only on Exchange Server 2013.
-   This action uses the Exchange\_https connection and credential alias.

</td></tr><tr><td>

Create Mailbox

</td><td>

Creates mailboxes and user accounts simultaneously.

</td></tr><tr><td>

Delete Mailbox

</td><td>

Deletes a mailbox in Exchange Server.

</td></tr><tr><td>

Disable Mailbox

</td><td>

Disables a mailbox in Exchange Server.

</td></tr><tr><td>

Enable Mailbox

</td><td>

Enables a mailbox in Exchange Server.

</td></tr><tr><td>

Look up Calendar by Event ID

</td><td>

Retrieves the list of calendar events.

</td></tr><tr><td>

Look up Mailbox

</td><td>

Retrieves mailbox properties for a given mailbox in Exchange Server.

</td></tr><tr><td>

Look up Room Availability

</td><td>

Retrieves the availability response for a given array of room objects.

</td></tr><tr><td>

Update Mailbox

</td><td>

Updates the properties of a mailbox in Exchange Server.

</td></tr><tr><td>

Set Mailbox Auto Reply

</td><td>

Schedules the auto-reply for a given mailbox in Exchange Server.

</td></tr><tr><td>

Lookup Room Mailboxes

</td><td>

Retrieves all the room mailboxes in Exchange Server.

</td></tr><tr><td rowspan="6">

Meeting Management

</td><td>

Look up Meeting Suggestions

</td><td>

Retrieves the meeting suggestions for the specified mailboxes.

</td></tr><tr><td>

Update a Calendar Meeting

</td><td>

Updates an existing calendar event that has already been created. While updating the meeting, in addition to saving the modified appointment item to the calendar folder, the updated meeting request is sent to all attendees.

</td></tr><tr><td>

Look up Meetings Stream

</td><td>

Retrieves details of the user's meetings within the specified start and end times.

</td></tr><tr><td>

Look up Folder ID

</td><td>

Retrieves Folder ID of the required folder.

</td></tr><tr><td>

Delete Calendar Event for User

</td><td>

Deletes the specified existing calendar event. The update is sent to all attendees.

</td></tr><tr><td>

Look up User Availabilities

</td><td>

Retrieves the availability response for a given mailbox.

</td></tr><tr><td rowspan="3">

Subscription Management**Note:** The Exchange Server spoke supports the calendar events only.

</td><td>

Create Subscription

</td><td>

Creates a new subscription for given mailbox.

</td></tr><tr><td>

Look up Calendar Item from Item ID

</td><td>

Retrieves the calendar information for the given calendar ID.

</td></tr><tr><td>

Look up Events by Subscription ID

</td><td>

Retrieves the latest changes in the calendar folder for the subscription since the last watermark.

</td></tr><tr><td rowspan="5">

Attachment Management

</td><td>

Copy Attachment to Event Record

</td><td>

Copies an calendar event’s attachment to the specified record in the ServiceNow instance.

</td></tr><tr><td>

Create Attachment

</td><td>

Adds attachment to an event.

</td></tr><tr><td>

Delete Attachment

</td><td>

Deletes an attachment associated with the provided Attachment ID.

</td></tr><tr><td>

Delete Attachments from Event Record

</td><td>

Deletes one or more attachments associated with the specified event record.

</td></tr><tr><td>

Look up Attachment by Attachment ID

</td><td>

Retrieves the specified attachment.

</td></tr></tbody>
</table>## Spoke modules

The Exchange Server spoke adds a Microsoft Exchange Server Spoke module to your ServiceNow instance. Data is these modules is populated when the associated flows are executed:

|Module|Description|
|------|-----------|
|Subscriptions|Displays details of the subscriptions in Exchange Server. Data is populated in this module when the Create Subscriptions and Renew Subscriptions subflows are executed.|
|Events|Displays details of the events in Exchange Server. Data is populated in this module when the Look up Calendar Item from Item ID flow is executed.|
|Event Attendees|Displays details of the event attendees in the events. Data is populated in this module when the Look up Calendar Item from Item ID flow is executed.|
|Subscription to Events Mapping|Displays details of the subscriptions and events. Data is populated in this module when the Look up Items From Subscription ID subflow is executed.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

Two connection and credential aliases are created when the Microsoft Exchange Server spoke is activated, Exchange and Exchange\_https.

**Note:**

-   The Exchange\_https alias is supported only on Exchange Server 2013.
-   The Exchange\_https alias is required to use the Create Calendar Event For User and Lookup Room Availability actions.

For information about setting up the spoke, see [Set up the Microsoft Exchange Server spoke](../task/setup-msexchange.md#).

## MID Server requirements

Your instance must have a MID Server set up and configured to run PowerShell 2.0. Use the connection record associated with the Microsoft Exchange alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


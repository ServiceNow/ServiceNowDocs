---
title: Vonage Spoke
description: Manage communications through calls, SMS, and WhatsApp by using the Vonage account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Vonage Spoke

Manage communications through calls, SMS, and WhatsApp by using the Vonage account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Vonage spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for Vonage for these versions, but may be compatible with later versions:

-   Messages API version v1
-   Voice API version v1

## Spoke requirements

-   Admin access to Vonage account and [Vonage API Dashboard](https://dashboard.nexmo.com/).
-   Record the values of **API key** and **API Secret**. You can access these values from the Vonage API Dashboard. For more information, see the [Authentication](https://developer.nexmo.com/concepts/guides/authentication) page in the [Vonage API Developer](https://developer.nexmo.com/documentation) documentation site.
-   Record and save the value of the **Signature Secret**. You can access this value in the [Account Settings in Vonage API Dashboard](https://dashboard.nexmo.com/settings). For more information, see the [Authentication](https://developer.nexmo.com/concepts/guides/authentication) page in the [Vonage API Developer](https://developer.nexmo.com/documentation) documentation site.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Vonage spoke provides sample subflows to demonstrate automating Vonage tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Vonage SMS Webhook|Processes the SMS requests from Vonage.|
|Vonage Voice Webhook|Processes the voice requests from Vonage.|
|Vonage WhatsApp Webhook|Processes the WhatsApp requests from Vonage.|

To customize the default subflow, you must a create a copy of the sample subflow and customize the subflow as per your requirement. While customizing subflows, you must ensure that the subflows are configured to avoid infinite loops.

## Spoke triggers

Use triggers in the Vonage spoke to subscribe to the required events. The endpoint enables webhooks to connect with your ServiceNow instance. You can configure the flows to execute only when the specified trigger conditions are met. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Call Management|Voice Ringing|Trigger is initiated when a call is made from Vonage and the number is Ringing.|
|Voice Answered|Trigger is initiated when a call is made from Vonage and the call is Answered.|
|Voice Completed|Trigger is initiated when a call is made from Vonage and the call is Completed.|
|SMS Management|SMS Delivered|Trigger is initiated when an SMS is sent from Vonage to a number.|
|SMS Failed|Trigger is initiated when an SMS is sent from Vonage and it fails.|
|SMS Accepted|Trigger is initiated when a message has been accepted for delivery, but has not yet delivered.|

For information about setting up the triggers for the Vonage spoke, see Setup the trigger for vonage spoke.

## Spoke actions

The Vonage spoke provides actions to automate Vonage tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Management

</td><td>

Get Account Balance

</td><td>

Retrieves the current balance of the Vonage account.

</td></tr><tr><td rowspan="14">

Call Management

</td><td>

Play DTMF tone into Call

</td><td>

Plays DTMF \(Dual-tone multi-frequency\) tones into an active call

</td></tr><tr><td>

Attach Recording To ServiceNow Record

</td><td>

Attaches a call recording to the target ServiceNow record.

</td></tr><tr><td>

Create Outbound Call

</td><td>

Creates an outbound call to a phone number.

</td></tr><tr><td>

Generate NCCO

</td><td>

Constructs a Nexmo Call Control Objects \(NCCO\) that is used in Create an Outbound Call action.

</td></tr><tr><td>

Generate Connect NCCO

</td><td>

Generates a Nexmo Call Control Object \(NCCO\) that defines how to connect an outbound call to endpoints such as a phone number or WebSocket.

</td></tr><tr><td>

Generate Notify NCCO

</td><td>

Generates a Nexmo Call Control Object \(NCCO\) that defines a notify action for an outbound call.

</td></tr><tr><td>

Generate Transfer NCCO

</td><td>

Generates a Nexmo Call Control Object \(NCCO\) that defines how to transfer an active call.

</td></tr><tr><td>

Look Up Call Details

</td><td>

Retrieves the details of the specified call.

</td></tr><tr><td>

Look up Calls

</td><td>

Retrieves details of the specified calls.

</td></tr><tr><td>

Play Audio into Call

</td><td>

Plays an audio file into an active call.

</td></tr><tr><td>

Play Text to Speech into Call

</td><td>

Plays text-to-speech into an active call.

</td></tr><tr><td>

Stop Playing Audio into Call

</td><td>

Stops playing an audio file into an active call.

</td></tr><tr><td>

Stop Text to Speech In Call

</td><td>

Stops text-to-speech into an active call.

</td></tr><tr><td>

Update Call

</td><td>

Updates the status of an active call.

</td></tr><tr><td>

Number Management

</td><td>

Look up Numbers

</td><td>

Retrieves all the inbound numbers associated with the Vonage account.

</td></tr><tr><td rowspan="3">

RCS Management**Note:** If you are upgrading from an earlier version of the spoke, make sure to generate a new JWT token in your existing credential record before using this category actions.

</td><td>

Send RCS Card Message

</td><td>

Sends an RCS \(Rich Communication Services\) card message to a specified phone number.

</td></tr><tr><td>

Send RCS Media Message

</td><td>

Sends an RCS \(Rich Communication Services\) media message to a specified phone number.

</td></tr><tr><td>

Send RCS Text Message

</td><td>

Sends an RCS \(Rich Communication Services\) text message to a specified phone number.

</td></tr><tr><td>

SMS Management

</td><td>

Send SMS

</td><td>

Sends an SMS \(Short Message Service\) to a phone number.

</td></tr><tr><td rowspan="5">

WhatsApp Management**Note:** If you are upgrading from an earlier version of the spoke, make sure to generate a new JWT token in your existing credential record before using this category actions.

</td><td>

Send Contacts

</td><td>

Sends contacts to a WhatsApp number.

</td></tr><tr><td>

Send Location

</td><td>

Sends geographic coordinates of a location to a WhatsApp number.

</td></tr><tr><td>

Send Media Message

</td><td>

Sends a media message to a WhatsApp number.

</td></tr><tr><td>

Send Text Message

</td><td>

Sends a text message to a WhatsApp number.

</td></tr><tr><td>

Send Text Message Using Template

</td><td>

Sends a text message using the template to a WhatsApp number.

</td></tr></tbody>
</table>## Spoke module

Bi-directional webhooks can be set up to be notified about the required events. Routing policy defines conditions that must be met to notify the ServiceNow instance. These conditions are based on the events in Vonage that you want to be notified about. When the conditions are met, routing policy triggers the associated subflow, which in turn automates the Vonage tasks. By default, the Vonage Spoke application is available and has the following modules:

-   Vonage Webhook Registries
-   Vonage WebHook Routing Policies

Use the Vonage Webhook Registries module to assign a token and provide the API path. You must generate a Callback URL here and provide this URL in Vonage. Default routing policies are provided as a reference in the Vonage WebHook Routing Policies module. Customize these routing policies as per your requirement. The routing policy supports these fields:

-   Keywords
-   Call Direction
-   Call Status
-   Event Type
-   From
-   SMS Status
-   SMS Text
-   To
-   WhatsApp Message Status
-   WhatsApp Text
-   Show Related Fields

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Two connection and credential aliases are available along with the Vonage spoke:

|Vonage alias|Description|
|------------|-----------|
|VonagePrimary|Required for the actions that manage SMS, number, and account.|
|Vonage|Required for the actions that manage calls and WhatsApp.|

For information about setting up the spoke, see [Set up the Vonage spoke](../task/setup-vonage-spoke.md#).


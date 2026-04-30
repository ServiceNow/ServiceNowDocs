---
title: Vonage Spoke
description: Manage communications through calls, SMS, and WhatsApp by using the Vonage account from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Vonage Spoke

Manage communications through calls, SMS, and WhatsApp by using the Vonage account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Vonage spoke v1.1.5 is the latest version.

## Supported versions

This spoke was built for Vonage for these versions, but may be compatible with later versions:

-   Messages API version v0.1
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

## Spoke actions

The Vonage spoke provides actions to automate Vonage tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Get Account Balance|Retrieves the current balance of the Vonage account.|
|Call Management|Play DTMF tone into Call|Plays DTMF \(Dual-tone multi-frequency\) tones into an active call|
|Attach Recording To ServiceNow Record|Attaches a call recording to the target ServiceNow record.|
|Create Outbound Call|Creates an outbound call to a phone number.|
|Generate NCCO|Constructs a Nexmo Call Control Objects \(NCCO\) that is used in Create an Outbound Call action.|
|Get Call Details|Retrieves the details of the specified call.|
|Look up Calls|Retrieves details of the specified calls.|
|Play Audio into Call|Plays an audio file into an active call.|
|Play Text to Speech into Call|Plays text-to-speech into an active call.|
|Stop Playing Audio into Call|Stops playing an audio file into an active call.|
|Stop Text to Speech In Call|Stops text-to-speech into an active call.|
|Update Call|Updates the status of an active call.|
|Number Management|Look up Your Own Numbers|Retrieves all the inbound numbers associated with the Vonage account.|
|SMS Management|Send SMS|Sends an SMS \(Short Message Service\) to a phone number.|
|WhatsApp Management|Send Contacts|Sends contacts to a WhatsApp number.|
|Send Location|Sends geographic coordinates of a location to a WhatsApp number.|
|Send Media Message|Sends a media message to a WhatsApp number.|
|Send Text Message|Sends a text message to a WhatsApp number.|
|Send Text Message Using Template|Sends a text message using the template to a WhatsApp number.|

## Spoke module

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

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Two connection and credential aliases are available along with the Vonage spoke:

|Vonage alias|Description|
|------------|-----------|
|VonagePrimary|Required for the actions that manage SMS, number, and account.|
|Vonage|Required for the actions that manage calls and WhatsApp.|

For information about setting up the spoke, see [Set up the Vonage spoke](../task/setup-vonage-spoke.md#).


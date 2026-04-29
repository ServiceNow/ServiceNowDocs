---
title: Twilio Spoke
description: Use the Twilio spoke to send SMS, make voice calls, create conference calls, manage calls, manage short codes, notify services, and messaging services.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Twilio Spoke

Use the Twilio spoke to send SMS, make voice calls, create conference calls, manage calls, manage short codes, notify services, and messaging services.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Twilio spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for Twilio Base version 2010-04-01, Twilio Messaging version v1, and Twilio Notify version v1, but may be compatible with later versions.

## Spoke requirements

-   Twilio account.
-   **AccountSid** and **AuthToken** of the account to create a Basic Auth credential.
-   The following plugins are installed when you install the Twilio spoke.
    -   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
    -   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
    -   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

See [Twilio documentation](https://www.twilio.com/docs) for instructions on creating an account.

## Spoke actions

The Twilio spoke provides actions to automate sending SMS, making voice calls, and creating conference calls when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Create Application|Creates an application resource in a Twilio account.|
|Delete Application|Deletes an application resource from a Twilio account.|
|Get Application|Retrieves the required application resource.|
|Look Up Accounts|Retrieves the account resources in a Twilio account. The list includes the account and its sub-account resources.|
|Look Up Applications|Retrieves the application resources in a Twilio account.|
|Update Application|Updates properties of an application resource in a Twilio account.|
|Call Management|Dequeue Call|Removes a call from a queue.|
|Get Call|Retrieves the required call resource.|
|Get Incoming Phone Number|Retrieves the incoming phone number resource.|
|Hang Up Call|Ends a call in progress.|
|Look Up Incoming Phone Numbers|Retrieves the incoming phone number resources in a Twilio account.|
|Make a Call With Recording|Places a call to a phone number and records the call.|
|Make a Call Without Recording|Places a call to a phone number and doesn't record the call.|
|Modify Call|Modifies a call in progress.|
|Mute Or Unmute Participant|Mutes or unmutes a participant resource in a conference call.|
|Remove Participant From Conference Call|Removes a participant resource from a conference call.|
|Update Incoming Phone Number|Updates properties of an incoming phone number resource in a Twilio account.|
|Messaging Service Management|Add Phone Number To Messaging Service|Adds a phone number resource to the messaging service.|
|Add Short Code To Messaging Service|Adds a short code resource to the messaging service.|
|Create Messaging Service|Creates a new messaging service resource in a Twilio account.|
|Delete Messaging Service|Deletes a messaging service resource from a Twilio account.|
|Look Up Messaging Service Phone Numbers|Retrieves the phone number resources in a messaging service.|
|Look Up Messaging Service Short Codes|Retrieves the short code resources associated with a messaging service.|
|Look Up Messaging Services|Retrieves the messaging service resources in a Twilio account.|
|Remove Phone Number From Messaging Service|Removes a phone number resource from a messaging service.|
|Remove Short Code From Messaging Service|Removes a short code resource from a messaging service.|
|Notification Service Management|Create Notify Service|Creates a new notify service resource in a Twilio account.|
|Delete Notify Service|Deletes a notify service resource from Twilio account.|
|Look Up Notify Services|Retrieves the notify service resources in a Twilio account.|
|Short Code Management|Get Short Code|Retrieves a short code resource.|
|Look Up Short Codes|Retrieves the short code resources of a Twilio account.|
|Reset Short Code|Resets the short code resource.|
|Update Short Code|Updates properties of a short code resource in a Twilio account.|
|Text Messaging|Send Bulk SMS|Sends an SMS to multiple phone numbers.|
|Send SMS|Sends an SMS to a phone number.|

**Note:** To receive information about Status Callbacks, you must configure webhooks in Twilio. See [Twilio documentation](https://www.twilio.com/docs) for instructions on creating and configuring webhooks.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** Three connection and credential alias records are needed for the Twilio spoke. One each for Twilio Base, Twilio Notify, and Twilio Messaging. Each alias should be associated with the respective Twilio API.

For information about setting up the spoke, see [Set up Twilio spoke](../task/setup-twilio.md#).


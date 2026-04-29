---
title: Plivo Spoke
description: Enable communications with your customers using the Plivo platform from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Plivo Spoke

Enable communications with your customers using the Plivo platform from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Plivo spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for Plivo API version v1, but may be compatible with later versions.

## Spoke requirements

-   Admin access to the Plivo console.
-   **AUTH ID** and **AUTH TOKEN**. You can find these vales in the dashboard of your Plivo account. For more information, see [Authentication](https://www.plivo.com/docs/account/api/request#authentication) in the [Plivo documentation](https://www.plivo.com/docs/).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Plivo spoke provides sample subflows to demonstrate automating the Plivo tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Plivo Call Handler|Manages calls associated with the Plivo account.|
|Plivo SMS Handler|Manages SMS associated with the Plivo account.|

While customizing subflows, you must ensure that the subflows are configured to avoid infinite loops.

**Note:**

-   You must configure webhooks to use the spoke subflow. See [Set up a bi-directional webhook for the Plivo spoke](../task/setup-plivo-webhook.md#) for information regarding setting up and configuring the webhook.
-   The sample subflow runs as a user by default. The subflow can be configured to run as system.

## Spoke actions

The Plivo spoke provides actions to automate the Plivo tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Application Management|Create Application|Creates an application.|
|Delete Application|Deletes an application.|
|Get Application|Retrieves details of an application.|
|Look up Applications|Retrieves list of all application IDs.|
|Update Application|Updates details of an application.|
|Call Management|Get Call|Retrieves Call Detail Record\(CDR\) of the call.|
|Hang Up Call|Ends an ongoing call or cancel a queued outbound call.|
|Look up Call|Retrieves details of the specified call.|
|Make Call|Initiates an outbound call.|
|Start Recording Call|Starts recording an ongoing outbound call.|
|Stop Recording Call|Stops all the ongoing recordings for the specified call UUID.|
|Conference Management|Get Conference|Gets details of a conference.|
|Hang Up Conference|Hangs up all ongoing conferences in your account.|
|Hang Up Member|Hangs up a member in a conference.|
|Kick Member|Disconnects a member in a conference.|
|Look up Conferences|Retrieves a list of all conferences that are ongoing on your account.|
|Mute Member|Mutes members in a conference.|
|Unmute Member|Unmutes members in a conference.|
|SMS Management|Get Message|Retrieves the details of the specified message.|
|Look up Message|Retrieves the details of the messages.|
|Send Bulk SMS|Sends SMS to the multiple numbers.|
|Send SMS|Sends the SMS to the specified number.|

## Spoke module

Webhooks can be set up to be notified about the required events. Routing policy defines conditions that must be met to notify the ServiceNow instance. These conditions are based on the events in Plivo that you want to be notified about. When the conditions are met, routing policy triggers the associated subflow, which in turn automates the Plivo tasks.

Webhooks require separate setup and can be used independently without using the spoke actions. The Plivo spoke adds the Plivo Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Plivo Webhook Registries|Create and view the Plivo webhooks in ServiceNow.|
|Plivo Webhook Routing Policy|Create and view the routing policies for the Plivo webhooks in ServiceNow. You can also customise the conditions in the routing policies as per your requirement.|

Use the Plivo Webhook Registries module to register a Plivo webhook. You must generate a Callback URL and provide this URL in your Plivo account.

Routing policies and subflows support these Plivo fields:

-   Keywords
-   Call Event
-   Caller Name
-   Event Type
-   SMS Text
-   To Number
-   Show Related Fields

Create routing policy in the Plivo WebHook Routing Policies module and specify conditions as per your requirement. See [Set up a bi-directional webhook for the Plivo spoke](../task/setup-plivo-webhook.md#) for information regarding setting up and configuring the webhooks.

## Spoke user roles

The Plivo spoke provides a Plivo Admin \(sn\_plivo\_spoke.Plivo\_Admin\) role.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Plivo spoke](../task/plivo-setup.md#).


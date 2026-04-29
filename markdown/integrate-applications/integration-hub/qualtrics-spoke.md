---
title: Qualtrics Spoke
description: Integrate ServiceNow instance with Qualtrics. Manage web-based survey distribution in Qualtrics from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Qualtrics Spoke

Integrate ServiceNow instance with Qualtrics. Manage web-based survey distribution in Qualtrics from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Qualtrics spoke v1.3.0 is the latest version.

## Supported versions

This spoke was built for Qualtrics v3, but may be compatible with later versions.

## Spoke requirements

Qualtrics account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Qualtrics spoke provides sample flows to demonstrate automating the Qualtrics tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

<table id="table_rmj_jbc_gnb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create distribution when incident is closed

</td><td>

Creates a distribution for a survey and sends the survey to the incident caller, when an incident is closed.

</td></tr><tr><td>

Look up Contact by Email

</td><td>

Retrieves details of the customer and the customer score. That is, customer value and customer satisfaction, which can be high or low based on the configured decision policy.

</td></tr><tr><td>

Upsert Contact or Consumer to Qualtrics

</td><td>

Updates details of the existing consumer records or creates consumer record in Qualtrics.This flow is triggered when a record in created or updated in the Contacts and Consumers module of your ServiceNow instance.

 When a record is created the Contacts and Consumers module of your ServiceNow instance, the Upsert Contact or Consumer to Qualtrics flow is triggered and creates the record in Qualtrics. Also, Reference ID that is generated in Qualtrics, is updated in the Contacts and Consumers module of your ServiceNow instance.

</td></tr></tbody>
</table>## Spoke subflows

The Qualtrics spoke provides sample subflows to demonstrate automating Qualtrics tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Look up Contact in Mailing List|Retrieves the look up ID of the specified contact.|
|Look up Mailing List by Name|Retrieves ID of the mailing list for the specified name.|
|Look up Message by Name|Retrieves ID of the message for the specified name.|
|Look up Survey by Name|Retrieves ID of the survey with the specified name.|

## Spoke actions

The Qualtrics spoke provides actions to automate Qualtrics tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_vmj_jbc_gnb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Contact Management

</td><td>

Create Contact

</td><td>

Creates a contact in the specified directory.

</td></tr><tr><td>

Look up Contact by Email

</td><td>

Retrieves contacts in a directory of the required email address.

</td></tr><tr><td>

Look up Contact Distribution Email History Stream

</td><td>

Retrieves the distribution email history for the specified contact in a directory.

</td></tr><tr><td>

Look up Contact Distribution Response Histories Stream

</td><td>

Retrieves a list of distribution response history for a specified contact in a directory.

</td></tr><tr><td>

Look up Contacts Stream

</td><td>

Retrieves a list of contacts from a directory.

</td></tr><tr><td>

Update Contact

</td><td>

Updates the specified contact details in the specified directory.

</td></tr><tr><td rowspan="3">

Distribution Management

</td><td>

Create Distribution

</td><td>

Creates a distribution for a survey.

</td></tr><tr><td>

Look up Distribution Links Stream

</td><td>

Retrieves a list of distribution links for an existing distribution of the specified survey.

</td></tr><tr><td>

Look up Distributions Stream

</td><td>

Retrieves a list of distributions for a survey.

</td></tr><tr><td>

Library Management

</td><td>

Look up Library Messages Stream

</td><td>

Retrieves a list of messages in a library.

</td></tr><tr><td rowspan="4">

Mailing List Management

</td><td>

Create Contact in Mailing List

</td><td>

Creates a directory contact in a specified mailing list.

</td></tr><tr><td>

Look up Contact in Mailing Lists Stream

</td><td>

Retrieves a contact from a mailing list in the specified directory.

</td></tr><tr><td>

Look up Mailing Lists

</td><td>

Retrieves a list of mailing lists in a directory.

</td></tr><tr><td>

Remove Contact from Mailing List

</td><td>

Removes a contact from the specified mailing list.

</td></tr><tr><td rowspan="2">

Metadata Retrieval

</td><td>

Look up Directories Metadata

</td><td>

Retrieves the metadata of a list of directories within a brand.**Note:** Ensure that this action is always used along with relevant actions that use dynamic inputs.

</td></tr><tr><td>

Look up Libraries Metadata

</td><td>

Retrieves a list of libraries.**Note:** Ensure that this action is always used along with relevant actions that use dynamic inputs.

</td></tr><tr><td>

Survey Management

</td><td>

Look up Surveys

</td><td>

Retrieves a list of surveys available to the user.

</td></tr><tr><td rowspan="3">

Event Subscription Management

</td><td>

Create Subscription

</td><td>

Creates an event subscription.

</td></tr><tr><td>

Look up Subscription by Subscription ID

</td><td>

Retrieves all event subscriptions.

</td></tr><tr><td>

Look up Subscriptions Stream

</td><td>

Retrieves all event subscriptions.

</td></tr></tbody>
</table>## Spoke modules

The Qualtrics spoke provides these modules.

|Module|Description|
|------|-----------|
|Contacts and Consumers|Create, view, and modify the contact and consumer records. When a record is created or updated here, the Upsert Contact or Consumer to Qualtrics flow is triggered.|
|Qualtrics Score Mapping Answers|View the score mapping answers.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Qualtrics spoke](../task/setup-qualtrics.md#).


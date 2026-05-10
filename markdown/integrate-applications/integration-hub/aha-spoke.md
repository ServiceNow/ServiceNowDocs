---
title: Aha! Spoke
description: Manage Aha! accounts using your ServiceNow instance. Analyze data usage for Aha! and reclaim idle accounts.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Aha! Spoke

Manage Aha! accounts using your ServiceNow instance. Analyze data usage for Aha! and reclaim idle accounts.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Aha! spoke v1.8.0 is the latest version.

## Spoke requirements

Aha! admin role

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Aha! spoke provides a sample flow, Upsert Aha Ideas to:

-   Check if an idea is created in the Aha Ideas \[sn\_aha\_spoke\_aha\_ideas\] table in ServiceNow instance. If an idea record is created, the flow creates the idea record in Aha! and updates the value of auto-generated ID ServiceNow instance.
-   Check if an existing idea has been updated and synchronizes the details updates in Aha!.

You can also create a copy of the flow and customize it according to your requirement.

## Spoke subflows

The Aha! spoke provides a sample subflow, Process Aha webhooks to create and update records in Aha!, and save the records' information in the Aha Feature \[sn\_aha\_spoke\_feature\_aha\] table.

## Spoke actions

The Aha! spoke provides actions to automate Aha! tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Feature Management|Create Feature|Creates features in the specified release.|
|Look up Features Associated with Objects Stream|Retrieves information about features within the specified objects.|
|Look up Features Stream|Retrieves information about the required features.|
|Update Feature|Updates details of the required feature.|
|Idea Management|Create Idea Vote|Creates an idea vote with the provided details.|
|Create Idea|Creates an idea with the provided details.|
|Look up Idea by ID|Retrieves information about the required idea.|
|Look up Ideas Associated with Product Stream|Retrieves information about ideas in the specified product.|
|Look up Ideas Stream|Retrieves information about the required ideas.|
|Look up Ideas Votes Stream|Retrieves information about the required idea endorsements.|
|Look up Ideas with String Stream|Retrieves information about the required ideas.|
|Update Idea Vote|Updates details of the required idea vote.|
|Update Idea|Updates details of the required idea.|
|Product Management|Create Product|Creates a product.|
|Create Task|Creates a task.|
|Look up Personas Stream|Retrieves information about the required personas.|
|Look up Product by ID|Retrieves information about the specified product.|
|Look up Products Stream|Retrieves information about the required products.|
|Look up Tasks Associated with Object Stream|Retrieves information about the tasks that are associated with the specified API.|
|Look up Tasks Stream|Retrieves information about the tasks.|
|Update Product|Updates details of the specified product.|
|Update Task|Updates details of the required task.|
|Release Management|Create Epic|Creates epics in the required release.|
|Create Release|Creates a release with the provided details.|
|Create Release Phase|Creates a release phase in the specified release.|
|Look up Epic Associated with Objects Stream|Retrieves information about the epics that are associated with the specified API.|
|Look up Epics Stream|Retrieves information about the required epics.|
|Look up Release Phases Stream|Retrieves information about the required release phases.|
|Look up Release Phases With Releases Stream|Retrieves information about the releases phases in the specified release.|
|Look up Releases Associated with Objects Stream|Retrieves information about the releases that are associated with the specified API.|
|Update Epic|Updates details of the required epic.|
|Update Release|Updates details of the required release.|
|Update Release Phase|Updates details of the required release phase.|
|Strategy Management|Create Goal|Creates a goal with the provided details.|
|Create Initiative|Creates an initiative with the provided details.|
|Create Persona|Creates a persona with the provided details.|
|Look up Goals Associated with Objects Stream|Retrieves information about the goals that are associated with the specified API.|
|Look up Goals Stream|Retrieves information about the required goals.|
|Look up Initiatives Associated with Objects Stream|Retrieves information about the initiatives that are associated with the specified API.|
|Look up Initiatives Stream|Retrieves information about the required initiatives.|
|Update Goal|Updates details of the required goal.|
|Update Initiative|Updates details of the required initiative.|
|Update Persona|Updates details of the required persona.|
|User Management|Create Users|Creates a user in the specified product.|
|Deactivate User|Deactivates the specified user account.|
|Look up User Associated with Product Stream|Retrieves information about the users that are associated with the specified product.|
|Look up Users Stream|Retrieves details of all members in an account.|
|Update Users|Updates details of the specified user.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Spoke modules

The Aha! spoke adds the Aha! Spoke application to your ServiceNow instance. The Aha! Spoke application includes these modules:

<table id="table_hmw_12m_q5b"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ideas

</td><td>

Contains details of the idea records and enables users to create ideas. When an idea is created here, the Upsert Aha Ideas flow is triggered. This flow creates an idea record with the provided details in Aha! and updates the value of auto-generated ID in ServiceNow instance.To create ideas from ServiceNow instance:

1.  Navigate to **Aha! Spoke** &gt; **Ideas**.
2.  Click **New**.
3.  On the form, provide all the required details except **ID**. Value of **ID** is populated after this record in Aha!.
4.  Click **Submit**.

</td></tr><tr><td colspan="2">

Webhook

</td></tr><tr><td>

Feature Records

</td><td>

Contains details of the feature records in the Aha Remote Feature \[sn\_aha\_spoke\_st\_aha\_features\_remote\] table. Once the webhook is set up and configured, the feature records are retrieved from Aha! and saved in the Aha Remote Feature \[sn\_aha\_spoke\_st\_aha\_features\_remote\] table.

</td></tr><tr><td>

Webhook Registries

</td><td>

Contains details about the webhook registry records.

</td></tr><tr><td>

Webhook Routing Policies

</td><td>

Contains details about the webhook routing policy records. One routing policy is available with the spoke to create and update records in Aha!, and save the records' information in the Aha Feature \[sn\_aha\_spoke\_feature\_aha\] table.

</td></tr><tr><td colspan="2">

Remote Table

</td></tr><tr><td>

Features

</td><td>

Contains records about the Aha! features. Data displayed here is retrieved from the Aha Remote Feature \[sn\_aha\_spoke\_st\_aha\_features\_remote\] table.

</td></tr></tbody>
</table>## Spoke triggers

Use triggers in the Aha! spoke to subscribe to the required events. The endpoint enables webhooks to connect with your ServiceNow instance. You can configure the flows to execute only when the specified trigger conditions are met. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Default|Comment Added|Trigger initiates when a comment is added to a feature in Aha! workspace.|
|Field Change|Trigger initiates when a field is changed in Aha! workspace.|
|Feature Management|Feature Created|Trigger initiates when a feature is created in Aha! Workspace.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

For information about setting up the spoke, see [Create an Aha! OAuth2 application](../task/create-aha-oauth2-authentication.md) and [Set up ServiceNow instance for Aha!](../task/setup-servicenow-instance-to-authorize-aha.md).


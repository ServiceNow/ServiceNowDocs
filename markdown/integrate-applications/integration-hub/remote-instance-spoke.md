---
title: ServiceNow Remote Instance Spoke
description: Integrate your local and remote ServiceNow instances to export, import, and manage records from your local instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# ServiceNow Remote Instance Spoke

Integrate your local and remote ServiceNow instances to export, import, and manage records from your local instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription on the local instance where it will be installed. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

ServiceNow Remote Instance spoke v2.2.8 is the latest version.

## Supported versions

This spoke was built for the Orlando version and later.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke requirements

Ensure that the spoke users have only the required minimum permissions to access data in ServiceNow tables. Do not assign elevated privilege roles to users of this spoke unless very much required. This practice ensures controlled access to data.

**Note:** The terms remote instance and local instance are used in these contexts:

-   Local instance: This is the ServiceNow instance from which the communication is initiated and established.
-   Remote instance: This is the ServiceNow instance with which the local instance communicates.

## Spoke actions

The ServiceNow Remote Instance spoke provides actions to export, import, and manage records when events occurs in your local ServiceNow instance. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Change request Management

</td><td>

Export Change Request Record

</td><td>

Exports a change request record to a remote instance from the local instance.

</td></tr><tr><td>

Import Change Request Record

</td><td>

Imports a record from the Change Request table of the remote instance to the local instance.

</td></tr><tr><td rowspan="2">

Incident Management

</td><td>

Export Incident Record

</td><td>

Exports an Incident record to a remote instance from the local instance.

</td></tr><tr><td>

Import Incident Record

</td><td>

Imports a record from Incident table of the remote instance to the local instance.

</td></tr><tr><td rowspan="2">

Problem Management

</td><td>

Export Problem Record

</td><td>

Exports a Problem record to a remote instance from the local instance.

</td></tr><tr><td>

Import Problem Record

</td><td>

Imports a record from Problem table of the remote instance to the local instance.

</td></tr><tr><td rowspan="4">

Table Management

</td><td>

Look Up Fields By Remote Table

</td><td>

Retrieves all the fields from the given remote table.

</td></tr><tr><td>

Look Up Local Import Set Tables

</td><td>

Retrieves information about the given local import set table.

</td></tr><tr><td>

Look Up Remote Import Set Tables

</td><td>

Retrieves information about the given remote import table.

</td></tr><tr><td>

Look Up Remote Tables

</td><td>

Retrieves information about the given remote table.

</td></tr><tr><td rowspan="3">

Attachment Management

</td><td>

Copy Attachment From Remote Instance

</td><td>

Copies the required attachment from the remote instance.**Note:** You must select the required attachment using data pills only.

</td></tr><tr><td>

Copy Attachment To Remote Instance

</td><td>

Copies the required attachment to the remote instance.**Note:** You must select the required attachment using data pills only.

</td></tr><tr><td>

Look Up Local Attachments Names

</td><td>

Retrieves name of the required attachment.

</td></tr><tr><td rowspan="8">

Case Management

</td><td>

Export Case as Incident

</td><td>

Exports a case record as an incident record to a remote instance from the local instance.

</td></tr><tr><td>

Export Case Record

</td><td>

Exports a case record to the remote instance from the local instance.

</td></tr><tr><td>

Export Case Task Record

</td><td>

Exports a Case Task record to the remote instance from the local instance.

</td></tr><tr><td>

Export Incident as Case

</td><td>

Exports an incident record as a case record to the remote instance from the local instance.

</td></tr><tr><td>

Import Case as Incident

</td><td>

Imports a record from the case table of the remote instance as an incident record to the local instance.

</td></tr><tr><td>

Import Case Record

</td><td>

Imports a record from the Case table of the remote instance to the local instance.

</td></tr><tr><td>

Import Case Task Record

</td><td>

Imports a record from the Task table of the remote instance to the local instance.

</td></tr><tr><td>

Import Incident as Case

</td><td>

Imports a record from the Incident table of the remote instance as a case record to the local instance.

</td></tr><tr><td rowspan="10">

Record Management

</td><td>

Create or Update Remote Record

</td><td>

Creates a record or updates an existing record in the remote instance.

</td></tr><tr><td>

Create or Update Remote Record Using Import Set

</td><td>

Creates a record in the remote import set.

</td></tr><tr><td>

Create Remote Record

</td><td>

Creates record in remote instance.

</td></tr><tr><td>

Delete Remote Record

</td><td>

Deletes record in remote instance.

</td></tr><tr><td>

Export Record Using Import Set

</td><td>

Exports a record from the selected local table to a remote instance.

</td></tr><tr><td>

Get Remote Record

</td><td>

Retrieves the required record information from the remote instance.

</td></tr><tr><td>

Import Record Using Import Set

</td><td>

Imports a record from table in the remote instance to the local instance.

</td></tr><tr><td>

Look Up Remote Record

</td><td>

Retrieves the required record from the remote Instance.

</td></tr><tr><td>

Look Up Remote Records

</td><td>

Retrieves multiple records from the remote instance table.

</td></tr><tr><td>

Update Remote Record

</td><td>

Updates the required record in the remote instance.

</td></tr></tbody>
</table>**Note:** The **Company** field is required to import or export records using the default transform maps. However, users can modify the transform maps as per their requirement. Also, use the import sets when working with integration involving data transfer.

## Spoke transform maps

The ServiceNow Remote Instance spoke provides sample transform maps in active state and associated sample target tables to demonstrate using transform maps to save the remote ServiceNow instance data in your local ServiceNow tables. You can use these sample transform maps and target tables as reference to create transform maps as per your requirement.

For more information, see [Transform maps](../../../script/server-scripting/concept/c_CreatingNewTransformMaps.md).

**Note:**

-   By default, the sample transform maps uses **sys\_id** as the coalesce field. You can customise the transform map script as per your requirement to change the coalesce field.
-   By default, the export and import actions use the spoke tables. You can change this to use different import sets.
-   The time zones may be different in your ServiceNow instances. Ensure that you customise flows accordingly.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Two connection and credential aliases are required for this spoke; one for the local instance and other for the remote instance. For information about setting up the spoke, see [Set up the ServiceNow Remote Instance spoke](../task/setup-rem-instance.md#).


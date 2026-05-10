---
title: Utility Actions Spoke
description: Create file attachments and zip attachments in your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Utility Actions Spoke

Create file attachments and zip attachments in your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Utility Actions spoke v1.3.1 is the latest version.

## Supported versions

This spoke is compatible with ServiceNow instance of Australia and later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Utility Actions spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

Default

</td><td>

Add File to Zip

</td><td>

Adds the file to list of files to be zipped.

</td></tr><tr><td>

Append to Delimited File

</td><td>

Creates a file line record, corresponding to a row in the delimited file.

</td></tr><tr><td>

Append to File

</td><td>

Creates a file line record, corresponding to a line in the file to be created.

</td></tr><tr><td>

Begin File

</td><td>

Creates a file record, to which the actual file would be attached.

</td></tr><tr><td>

Begin Zip

</td><td>

Creates a file set record, to which the zip file would be attached.

</td></tr><tr><td>

Build File

</td><td>

Generates the file and attaches it to the file record specified.

</td></tr><tr><td>

Build Zip

</td><td>

Generates the zip file and attaches it to the file set record specified.**Note:** This action requires at least one MID Server with the IntegrationHub Utilities capability.

</td></tr><tr><td rowspan="4">

Spoke Util Actions

</td><td>

Convert Record to Object

</td><td>

Converts the specified record into an object.

</td></tr><tr><td>

Convert Record to Array of Objects

</td><td>

Converts the given list of records to an array of objects.**Note:** Flow designers must have read access to the sys\_dictionary and sys\_db\_object tables to use this action as the table schema is being populated from these tables.

</td></tr><tr><td>

Generate Encoded Query

</td><td>

Generates encoded query with the provided name and value pairs. The output encoded query can be used with any field that is of the type, dynamic template. For example, the encoded query output of the Generated Encoded Query action, can be given as an input for Additional Fields in the Create Issue action.

</td></tr><tr><td>

Look up Latest Comment on Record

</td><td>

Retrieves the latest comment from the required record in ServiceNow instance.The output comment is in the form of a string.

</td></tr></tbody>
</table>## Spoke module and tables

The Utility Actions spoke includes these tables:

<table id="table_okz_1by_qlb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

File \[sn\_utility\_spoke\_file\]

</td><td>

Information about every file that has been created. The associated file is attached to the record.**Note:** You must specify **Schema** if you specify **Delimited File** for **File Type**.

</td><td>

-   File Name
-   File Type
-   Schema

</td></tr><tr><td>

File Line \[sn\_utility\_spoke\_file\_line\]

</td><td>

Information about each row in delimited file.

</td><td>

-   File
-   Line Content

</td></tr><tr><td>

File Mapping \[sn\_utility\_spoke\_file\_mapping\]

</td><td>

Information about files mapped to a ZIP file. For example, if four files are zipped to a ZIP file, four records are created in this table for each file.

</td><td>

-   File
-   File Set

</td></tr><tr><td>

File Schema \[sn\_utility\_spoke\_file\_schema\]

</td><td>

Information regarding the delimited files.

</td><td>

-   Schema Name
-   Columns
-   Delimiter
-   Has Header
-   Quoted

</td></tr><tr><td>

File Set \[sn\_utility\_spoke\_file\_set\]

</td><td>

Information about the zip files. The associated ZIP file is attached to the record.

</td><td>

Zip File Name

</td></tr></tbody>
</table>The Utility Actions spoke adds the IntegrationHub Utilities application to your instance and includes the File Schemas module. The module displays records from the File Schema table.

Auto Flush data retention policies are available for the File and File Set tables. By default, the system retains data in the spoke tables, except the File Schema table, up to 7 days.

**Note:**

-   Auto Flush data retention policies don't apply to records in the File Schema table.
-   When the file records in the File table are deleted, the corresponding file line records in the File Line table are also deleted.
-   When the file set records in the File Set table are deleted, the corresponding file mapping records in the File Mapping table are also deleted.

To modify the data retention policy, change the value of **Age in seconds** in the Auto Flush form of the required table. For more information, see [Autoflush form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-auto-flush.md).

## Connection and credential alias requirements

This spoke doesn't require configuration of connection and credential alias. For information about setting up the spoke, see [Create schema](../task/create-schema.md).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

**Note:**

-   The Build Zip action in the spoke requires at least one MID Server with the capability IntegrationHub Utilities or ALL. To set up and configure the MID Server, user must have the role sn\_utility\_spoke.utility\_actions\_admin role.
-   [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md) with **Value** as `*.service-now.com`.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


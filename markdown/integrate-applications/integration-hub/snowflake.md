---
title: Snowflake Spoke
description: Manage data warehousing capabilities of Snowflake directly from your ServiceNow instance. You can create, delete, search, records, execute queries, and perform other data manipulation tasks in Snowflake from your ServiceNow instance.Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-08-19"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Snowflake Spoke

Manage data warehousing capabilities of Snowflake directly from your ServiceNow instance. You can create, delete, search, records, execute queries, and perform other data manipulation tasks in Snowflake from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Snowflake spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Snowflake v2, but may be compatible with later versions.

## Spoke requirements

Snowflake account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Workflow Studio - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Flow Designer - Flow Engine \(com.glide.hub.flow\_engine\)
-   Flow Designer Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Snowflake spoke provides actions to automate Snowflake data manipulation tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_p5w_f4x_c2c"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

Record Management

</td><td>

Create Record

</td><td>

Creates a record in the Snowflake tables with the specified details using the INSERT statement.

</td></tr><tr><td>

Delete Records

</td><td>

Deletes the specified records in the Snowflake tables using the DELETE statement.

</td></tr><tr><td>

Execute Custom Query

</td><td>

Runs the custom query in the Snowflake database using a custom statement and retrieves the result.

</td></tr><tr><td>

Look up Columns

</td><td>

Retrieves a list of columns from the Snowflake table.**Note:** Make sure that your Snowflake Service Account has access privilege to the columns that you want to fetch.

</td></tr><tr><td>

Look up Records

</td><td>

Runs the SELECT statement and retrieves the matching records from Snowflake tables.

</td></tr><tr><td>

Look up Tables

</td><td>

Retrieves a list of tables from the specified database and specified warehouse in Snowflake.**Note:** Make sure that your Snowflake Service Account has access privileges to the tables that you want to fetch.

</td></tr><tr><td>

Update Records

</td><td>

Updates the specified records in the Snowflake tables using the UPDATE statement.

</td></tr></tbody>
</table>
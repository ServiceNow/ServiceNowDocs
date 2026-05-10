---
title: Create a data source similar to Telecom core data source
description: Set up a schema-compliant data source in the connector’s application scope to simulate telecom data and ensure successful testing and validation of the Telecom Discovery Builder framework ETL before integrating with live device data.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Discovery Builder, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Create a data source similar to Telecom core data source

Set up a schema-compliant data source in the connector’s application scope to simulate telecom data and ensure successful testing and validation of the Telecom Discovery Builder framework ETL before integrating with live device data.

## Before you begin

Role required: admin

Ensure the following:

-   Access to the TSOM Core application and its data sources.
-   Switch to the connector’s application scope.
-   Have a sample payload that conforms to the Telco Generic Schema \(optional, but recommended for testing\).

## About this task

When duplicating the Telecom Discovery Builder framework ETL into a Service Graph Connector \(SGC\) application scope, you must first create a data source that replicates the exact structure of the TSOM Core data source. This duplicated data source provides the required schema and structure for testing and validating the ETL before connecting it to live telecom data.

The Telecom Discovery Builder framework expects data that conforms to the Telco Generic Schema, as defined in the Telecom Core. Duplicating the original TSOM data source ensures:

-   Schema alignment during ETL duplication.
-   A valid import set structure for testing.
-   Separation of core and connector scopes for customization and upgrade safety.

When to create a data source similar to the TSOM Core data source:

-   Before duplicating the Telecom Discovery Builder framework ETL.
-   When you want to run a test load using simulated or placeholder telecom data.
-   When preparing the connector’s application scope for ingestion configuration.

The following screenshot can help you understand to fill the field values while you create the data source.![Create data source user interface](../images/datasource.png)

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Find the **Generic Schema Multi Source v2** or a similar baseline source provided with TSOM Core.

3.  Open the TSOM Core data source record and copy the script from the **Data Loader** field.

4.  Create a data source by clicking **New**.

5.  On the form, fill in the fields

    For more information, see [Create a Custom \(Load by Script\) type data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/create-custom-type-data-source.md).

6.  In the **Type** field, select **Custom \(Load by Script\)**.

7.  Select the **Data in single column** field.

8.  In the **Data Loader** field, paste the copied script.

9.  Select **Submit**.

    The data source is created.

10. To test load the data source:

    1.  Click Test Load 20 Records \(or similar\) to generate an import set.

    2.  Ensure that records are created without errors.

    3.  Confirm that classes like Logical Composite, Network Gear, or Port appear in the staging table.


## What to do next

After the data source is created and tested:

-   Use it as the import source when duplicating the Telco Generic ETL.
-   Replace it with the actual connector-specific data source once simulation and validation are complete.

**Related topics**  


[Standardized JSON common data set to support all service graph connectors](../concept/overview-of-standardized-json-common-data-set.md)

[Duplicate the Telecom Discovery Builder framework ETL into a connector scope](duplicate-the-generic-etl-to-use-a-specific-connector.md)


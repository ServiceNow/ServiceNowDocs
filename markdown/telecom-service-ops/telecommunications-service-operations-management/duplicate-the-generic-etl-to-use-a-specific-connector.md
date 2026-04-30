---
title: Duplicate the Telecom Discovery Builder framework ETL into a connector scope
description: The Telecom Discovery Builder framework ETL enables Service Graph Connector \(SGC\) teams to rapidly adopt a standardized, schema-compliant data ingestion pipeline without building ETL logic from scratch.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure Telecom Discovery Builder, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Duplicate the Telecom Discovery Builder framework ETL into a connector scope

The Telecom Discovery Builder framework ETL enables Service Graph Connector \(SGC\) teams to rapidly adopt a standardized, schema-compliant data ingestion pipeline without building ETL logic from scratch.

## Before you begin

Role required: admin

Ensure that:

-   The Telecom Core plugin is activated and the Telco Generic ETL v2 \(automatically installed\) is available.
-   You have admin access to IntegrationHub ETL Studio.
-   You have created a temporary data source in the connector’s application scope. After creating a temporary data source, you can duplicate the Generic ETL into your connector’s application scope to customize and extend it for your specific use case.

## About this task

Duplicating the Telco Generic ETL allows you to:

-   Reuse standardized ETL mappings across multiple connectors.
-   Customize ETL behavior without altering the original baseline provided by the Telecom Service Operations Management \(TSOM\) Core.
-   Align with the Telco Generic Schema for consistency and TNI compliance.
-   Save time and reduce errors by working with a tested and proven ETL framework.

The following screenshot can help you duplicate the ETL Transform Map.![Duplicate ETL Transform Map user interface displaying field information to duplicate the Telco Generic Schema V2 to Nokia NSP ETL.](../images/createduplicate.png)

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub ETL**.

2.  On the **IntegrationHub ETL** page, select the connector's application scope.

    **Note:** For example, **Service Graph Connector for Nokia NSP**.

3.  Expand the CMDB Application Telco Generic Schema and select **Telco Generic Schema** record.

4.  Click **Duplicate**.

    The Duplicate ETL Transform Map page appears.

5.  Configure the duplicated ETL transform map

    1.  In the **Duplicate From** field, ensure Telco Generic Schema is selected.

    2.  Select an existing CMDB Application or click **Add new...** to add a new CMDB Application.

    3.  For a new CMDB Application, enter the CMDB application name \(for example, Nokia NSP Generic ETL v2\)

    4.  In the **Discovery Source** field, select the import set.

    5.  In the **Name** field, enter a name for the duplicate ETL.

    6.  In the **Description** field, enter a description for the duplicate ETL.

    7.  Select the data source that is used for the duplicate ETL transform map.

        **Note:** This needs to be different than the existing default Data Source that is attached to the Telco Generic Schema ETL. For more information, see [Create a data source similar to Telecom core data source](create-a-data-source-similar-to-tsom-core-data-source.md).

    8.  Enable **Auto-pull a new import set** option to automatically pull data into a new import set.

    9.  In the **Preview Size Override** field, set a custom preview size for testing and validation.

6.  Select **Create Duplicate**.

    A duplicate ETL of Telco Generic ETL is created.

7.  Open the duplicated ETL record and review the mappings and settings.


## What to do next

1.  Test the duplicated ETL \(optional but recommended\):
    -   Run a test load or a simulation using the temporary data source.
    -   Verify that import sets are processed successfully, CIs are created according to the Telco Generic Schema, and relationships are established properly.
2.  After successful duplication and testing:
    -   Update the ETL’s data source configuration to point to the actual production data source \(for real device data\).
    -   Deploy the connector integration into a test or production environment.
    -   Monitor import runs to validate that inventory data is ingested into the CMDB correctly.

**Related topics**  


[Update the data source of the connector](update-data-source-of-the-connector.md)


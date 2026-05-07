---
title: Define a Workflow Data Fabric table data source
description: Enable data collection and analysis from external tables by integrating the Data Context Engine with Workflow Data Fabric to generate actionable insights.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Define a table data source, Define the data source, Set up the Data Context Engine, Customer success, Customer Success Management, Customer Success Management]
---

# Define a Workflow Data Fabric table data source

Enable data collection and analysis from external tables by integrating the Data Context Engine with Workflow Data Fabric to generate actionable insights.

## Before you begin

-   Workflow Data Fabric plugin must be installed and configured. See [Activate Zero Copy Connector Hub](https://www.servicenow.com/docs/access?context=activate-zcc-hub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for details.
-   The Workflow Data Fabric table must have been created. See [Create a data fabric table](https://www.servicenow.com/docs/access?context=create-data-fabric-table-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for details.
-   Role required: sn\_acct\_lc.customer\_success\_application\_admin

## About this task

Access external data through the Workflow Data Fabric tables and analyzed it using the Data Context Engine. This data is available in real-time using a zero-copy model and synced only when queried. See [Managing zero copy connections](https://www.servicenow.com/docs/access?context=managing-connections-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for details.

## Procedure

1.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources**and select **Create New**.

2.  Select **Table** in the **Source** field.

3.  In the **Source table** field, select a Workflow Data Fabric.

4.  On the Data Source Form, fill in the remaining fields.

    For a description of the field values, see [Define a table data source](account-lifecycle-define-data-source-table.md) page.

5.  Select **Submit** to create the data source.


## Total licenses used quarterly

To get the total number of licenses used this quarter across accounts and products from a Workflow Data Fabric table, select:

-   Source table: df\_usage\_information
-   Conditions: Timestamp between last quarter and today
-   Group by: Account, Product
-   Aggregation: Sum
-   Source Reference: sold\_product
-   Source reference resolver: Specify the mapping between the **Account** and **Product** combination and the **Sold Product** table in the script as follows:

    -   `var account = groupByFieldValueMap[account]`
    -   `var product = groupByFieldValueMap[product]`
    **Note:** You must update the **Source reference resolver** script to specify field mappings only when the **Group By** field contains:

    -   Two fields \(maximum allowed\).
    -   A non-reference field.
    -   An external field.

## What to do next

After defining the data source, the next step is to configure the context engine mapper. See [Configure the Context Engine Mapper](../concept/account-lifecycle-define-context-engine-mapper.md) for details.


---
title: Configure the Context Engine Mapper
description: After you have defined the data source, use the Context Engine Mapper to specify the record in the context table for which it is applicable.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up the Data Context Engine, Customer success, Configure, Customer Success Management]
---

# Configure the Context Engine Mapper

After you have defined the data source, use the Context Engine Mapper to specify the record in the context table for which it is applicable.

The Context Engine Mapper is a framework that establishes mappings between source entities and their corresponding context entities, enabling the resolution of context-specific records based on given sources such as resolving engagements from customer accounts.

You can use the Context Engine Mapper to determine which fields will be used to categorize data collected by the [Data Context Engine](account-lifecycle-setup-metric-data.md). This mapping ensures that data is organized and analyzed based on designated breakdown fields such as account type, engagement status, or sold products.

**Note:** You can set up the context engine to map the source and target tables using one of the following methods:

-   Related table: Use the mapping rule `related table[query_field] = source table[source_field]`. In every record in the **Source table**, the **Source field** value is matched with the `Query field` in the Related table.
-   Script: If a script is defined, it takes precedence over the table based mapping. The script checks the **Source Field** and the ID of the record to determine the appropriate context based on the resolving context table.
-   Metric based: Mapping logic can vary depending on the data source used for metrics and measurements. Can be used for more granular and context specific mappings.

1.  Login as a user with the `sn_acct_lc.customer_success_agent` role.
2.  Navigate to **All** &gt; **Data Context Engine** &gt; **Context Engine Mappers** &gt; **Create New**.
3.  Enter the following details:

<table id="table_oxx_g3l_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

This can be:-   Global: For each record in the source table, the source field value is matched against the query field in the supporting related table. If a match is found, the associated values from the resolving context field are returned as mapped context records.
-   Metric based: This type is used to enable mapping specific to certain data sources or conditions. The mapping logic can vary depending on the data source used and provides enhanced filtering and flexibility.


</td></tr><tr><td>

Source table

</td><td>

Select the source table to which the data source is to be mapped. This table is related to the attribute selected in the Breakdown field in the Data Source table. For example, if you selected `Account` in the Breakdown field, select the Customer Account table here.

</td></tr><tr><td>

Source field

</td><td>

The specific field in the source table that contains the data to be mapped.

</td></tr><tr><td>

Supporting related table

</td><td>

The related table that will be used to connect the source and context tables.

</td></tr><tr><td>

Query field

</td><td>

Select the field that is used to query or dot walk the `Supporting related table` to map data from the `Source table` to the `Context table`.

</td></tr><tr><td>

Metric list

</td><td>

If **Type** is **Metric based**, select a data source from the list. If a data source listed here is used for a specific source or target table, this mapping takes precedence over the Global mapping.

</td></tr><tr><td>

Resolving context table

</td><td>

The target table where resolved context records are stored.

</td></tr><tr><td>

Resolving context field

</td><td>

The target field where the mapped data will be stored.

</td></tr><tr><td>

Resolving table conditions \(Optional\)

</td><td>

You can use additional conditions, such as field level filters, to narrow down the results from the resolving context table based on specific criteria.

</td></tr><tr><td>

Script

</td><td>

If you cannot query the context table through dot walking, you can define a script that uses the Source field and returns an array of possible context fields.

</td></tr></tbody>
</table>    **Note:** If a script is defined for a **Metric based** mapper, it overrides:

    -   Supporting related table
    -   Resolving table conditions
    The script returns an array of context record IDs based on the conditions defined.

4.  Select **Submit** to save the context mapping.
5.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources**.

    ![Metric data collection data source](../image/account-lifecycle-data-source.png)

6.  Open the data source you had created earlier and select **Publish**.

    Data will now be collected according to the defined schedule and the context engine data record is created and stored in the **Context Engine Data** table.


The following examples show how to set up the different types of mapping:

-   **Related table \(Global\)**

    ![Context engine mapping with related table](../image/account-lifecycle-context-engine-mapping-1.png)

-   **Metric Based Type**

    ![Metric based mapping](../image/account-lifecycle-context-engine-mapping-3.png)

-   **Script**

    ![Context engine mapping with script](../image/account-lifecycle-context-engine-mapping-2.png)



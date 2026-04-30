---
title: Set up the context engine mapper
description: After you have defined the data source, the next step is to specify the record in the context table for which it is applicable.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup the data context engine, Configure customer success, Customer success, Customer Success Management]
---

# Set up the context engine mapper

After you have defined the data source, the next step is to specify the record in the context table for which it is applicable.

1.  Login as a user with the `sn_acct_lc.ale_success_agent` role.
2.  Navigate to **All** &gt; **Data Context Engine** &gt; **Context Engine Mappers** &gt; **Create New**.
3.  Enter the following details:

    |Field|Description|
    |-----|-----------|
    |Source table|Select the source table to which the data source is to be mapped. This table is related to the attribute selected in the Breakdown field in the Data Source table. For example, if you selected `Account` in the Breakdown field, select the Customer Account table here.|
    |Source field|The specific field in the source table that contains the data to be mapped.|
    |Supporting related table|The related table that will be used to connect the source and context tables.|
    |Query field|Select the field that is used to query or dot walk the `Supporting related table` to map data from the `Source table` to the `Context table`.|
    |Resolving context table|The target table for mapping the data source.|
    |Resolving context field|The target field where the mapped data will be stored.|
    |Script|If you cannot query the context table through dot walking, you can define a script that uses the Source field and returns an array of possible context fields.|

    **Note:** You can set up the context engine to map the source and target tables using one of the following methods:

    -   Related table: Use the mapping rule `related table[query_field] = source table[source_field]`. In every record in the **Source table**, the **Source field** value is matched with the `Query field` in the Related table.
    -   Script: The script checks the **Source Field** and the ID of the record to determine the appropriate context based on the resolving context table.
    The following examples show how you can set up the mapping.

    -   **Example with Related table**

        ![Context engine mapping with related table](../image/account-lifecycle-context-engine-mapping-1.png)

    -   **Example with script**

        ![Context engine mapping with script](../image/account-lifecycle-context-engine-mapping-2.png)

4.  Click **Submit** to save the context mapping.
5.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources**.

    ![Metric data collection data source](../image/account-lifecycle-data-source.png)

6.  Open the data source you had created earlier and click **Publish**.

    Data will now be collected as per the defined schedule and the context engine data record is created and stored in the **Context Engine Data** table.



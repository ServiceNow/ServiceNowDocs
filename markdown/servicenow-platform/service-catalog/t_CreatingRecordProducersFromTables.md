---
title: Create record producers from tables
description: You can create Service Catalog record producers directly from a table record.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Record Producer, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create record producers from tables

You can create Service Catalog record producers directly from a table record.

## Before you begin

Role required: admin

## About this task

To create a record producer from a table record:

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** and open the table record.

    **Note:** When using a workflow with a Record producer, set the condition to Run the workflow.

2.  Under **Related Links**, click **Add to Service Catalog**.

3.  Complete the **Name**, **Short Description**, and **Category** fields as you would for service catalog items.

4.  Use the list to select the fields and the order in which you want them to appear.

5.  To use container variables, select **\|- container start -\|** and **\|- container end -\|**.

    ![](../image/CreateRecordProducersFromTables.png)

6.  Click **Save and Open** to open the record producer and define additional options.

    Alternatively, click **Save** to return to the table record.

    -   A record producer is created with these values:
        -   **Table name**: table record opened in step 1
        -   **Name**, **Short Description**, and **Category**: information entered in step 3
    -   A variable is created for each of the selected fields with these values:
        -   **Name**: Column name of the field
        -   **Type**: Variable type that corresponds to the field type
        -   **Order**: Position selected in the slushbucket \(for example, 100 for the first field and 200 for the second field\)
        -   **Question**: Column label of the field
    -   If the field type is **Choice**, a corresponding question choice is created for each field choice.
    -   The new record producer is added to the **Record Producers** related list on the table record.

**Parent Topic:**[Record Producer](../concept/c_RecordProducer.md)

**Related topics**  


[Create a record producer](t_DefRecProdInSCat.md)

[Populate record producer data and redirect users](../concept/c_PopulatingRecordData.md)


---
title: Custom \(Load by Script\) type data source
description: Use a custom script to store any type of incoming data in the import set table.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data sources, Import sets, Imports, Creating integrations with applications]
---

# Custom \(Load by Script\) type data source

Use a custom script to store any type of incoming data in the import set table.

When you select a **Type** of **Custom \(Load by Script\)** for your data source, the **Data Loader** field appears. The **Data Loader** field is a JavaScript field where you can enter a script to fetch data and insert it into the import set table using the **import\_set\_table** input parameter. For example, you can enter a script to get data from a REST API or a file attachment.

The **Data Loader** script loads the data. You can also **Enable parallel loading** to use a script to partition the data into smaller sections, then load them in parallel. Parallel loading can enable your integrations to finish in less time and create less of an impact on other tasks.

**Note:** With parallel loading, you must be running a concurrent import and the **Partition Method** for the import must be set to **Custom size**. For more information see, [Schedule a data import](../task/t_ScheduleADataImport.md).

## Data Loader script

The data loader script has the following input parameters.

-   `import_set_table`: The import set table referred to in the Data Source record. The data is inserted into this table.
-   `data_source`: The data source referred to in the Data Source record.
-   `import_log`: The log that records information about data import activity.
-   `last_success_import_time`: The last time this data source was run successfully.
-   `partition_info`: The partitioning information for the data. Used for parallel loading.

The import\_set\_table parameter has the following methods:

-   `addColumn(label, maxLength)`: Adds a string-type column to the import set table.
-   `addJSONColumn(label, maxLength)`: Adds a JSON-type column to the import set table.
-   `addXMLColumn(label, maxLength)`: Adds an XML-type column to the import set table.
-   `insert(rowData)`: Inserts a map \(key = column name, value = column value\) in the import set table.
-   `getMaximumRows()`: Returns `20` when you select **Test load 20 records**. In every other case, returns `-1`.

## Data Loader example

![Data Loader example showing a script that inserts data into the import set table.](../image/custom-data-source.png)

## Parallel loading script

The parallel loading script has the following input parameters.

-   `parallel_job_loader`: The Parallel Jobs \[sys\_parallel\_job\] table.
-   `data_source`: The data source referred to in the Data Source record.
-   `import_log`: The log that records information about data import activity.

The parallel\_job\_loader parameter has the `add(partitionInfo)` method, which adds the partition information to the Parallel Jobs \[sys\_parallel\_job\] table.

## Parallel loading example

![Parallel loading script example.](../image/parallel-loading-script.png)

## Parallel loading properties and status

If a job gets stuck in a **Running** state for more than 600 minutes, it's automatically put back into a **Pending** state. You can modify the amount of time a parallel job is allowed to be stuck in a running state with the **com.glide.system\_parallel\_job\_inactive\_time\_minutes** property.

If a parallel job can't complete after two tries, the job is set to **Error**. You can modify the number of tries before having an error state with the **com.glide.system\_parallel\_job\_max\_retry\_count** property. The **com.glide.system\_parallel\_job\_auto\_retry** property can be set to false to disable auto retry.

You can check the status of your current parallel import tasks by navigating to **All** &gt; **System Import Sets** &gt; **Advanced** &gt; **Concurrent Import Sets**, selecting your job, and viewing the Parallel Jobs tab.

## Script auto-complete

As you type the script, the script auto-complete displays the available options, as shown in this example.

![Data Loader auto-complete](../image/data-loader-auto-complete.png)


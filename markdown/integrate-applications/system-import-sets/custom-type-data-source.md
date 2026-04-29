---
title: Custom \(Load by Script\) type data source
description: Use a custom script to store any type of incoming data in the import set table.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Custom \(Load by Script\) type data source

Use a custom script to store any type of incoming data in the import set table.

When you select a **Type** of **Custom \(Load by Script\)** for your data source, the **Data Loader** field appears. The **Data Loader** field is a JavaScript field where you can enter a script to fetch data and insert it into the import set table using the **import\_set\_table** input parameter. For example, you can enter a script to get data from a REST API or a file attachment.

The **Data Loader** script loads the data. You can also **Enable parallel loading** to use a script to partition the data into smaller sections, then load them in parallel. Parallel loading can enable your integrations to finish in less time and create less of an impact on other tasks. Parallel jobs are usually processed immediately. If you need to delay a job, you can configure a delay in the Data Loader script.

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
-   `last_success_import_time`: The last time this data source was run successfully.

The parallel\_job\_loader parameter has the `add(partitionInfo)` method, which adds the partition information to the Parallel Jobs \[sys\_parallel\_job\] table.

## Parallel loading example

In this example, the parallel loading script partitions the data into smaller sections to be loaded in parallel. The Data Loader script loads the data into the import set table and adds a new partition to process data after a 120-second delay.

![Parallel loading script example.](../image/parallel-loading-script.png)

## Parallel loading delays, status, and properties

For most parallel jobs, data is available when the Data Loader script runs, so you don’t need to add any parallel jobs to the Data Loader script.

In cases where the data might not be immediately available, you can create an additional parallel job with a delay in the Data Loader script. When the Data Loader script runs, the parallel job is scheduled to run after the amount of time specified by the delay.

When adding parallel jobs to the Data Loader script, avoid repetitive loops. You can avoid repetitive loops by specifying a constraint. In the previous example, the parallel job in the Data Loader script uses the constraint  `(partition.start < 1000)`. Delays are measured in seconds.

You can check the status of your current parallel import tasks by going to the Concurrent Import Sets \[sys\_concurrent\_import\_set\] table, selecting your job, and viewing the Parallel Jobs tab.

Delayed jobs may show as **Pending** depending on the delay’s length of time. Parallel jobs are processed from the event queue, so you can also view your jobs by going to the Events \[sysevent\] table and filtering by **\[Queue\] \[is\] \[impex\_parallel\_job\_queue\]**.

If a job gets stuck in a **Running** state for more than 600 minutes, it's automatically put back into a **Pending** state. You can modify the amount of time a parallel job is allowed to be stuck in a running state with the **com.glide.system\_parallel\_job\_inactive\_time\_minutes** property.

If a parallel job can't complete after two tries, the job is set to **Error**. You can modify the number of tries before having an error state with the **com.glide.system\_parallel\_job\_max\_retry\_count** property. The **com.glide.system\_parallel\_job\_auto\_retry** property can be set to false to disable auto retry.

## Script auto-complete

As you type the script, the script auto-complete displays the available options, as shown in this example.

![Data Loader auto-complete](../image/data-loader-auto-complete.png)


---
title: Add a dataset
description: Add the data from a table to a data catalog as a dataset through generative AI by using the Now Assist Data Kit application. Adding a dataset is required to create and publish a data collection.
locale: en-US
release: xanadu
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2024-10-15"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Add a dataset

Add the data from a table to a data catalog as a dataset through generative AI by using the Now Assist Data Kit application. Adding a dataset is required to create and publish a data collection.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  On the **Data catalog** tab, select **Add New**.

3.  On the Choose data form, select the import type, table, and column.

    There’s an option to add columns, such as group notes and comments. These columns aren’t stored in the incident table but in a separate table. You can add these columns by using a script.

4.  Select Add a filter if needed.

5.  Review the records and select **Save &amp; next**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the dataset.|
    |Category|Category that the dataset is in.|
    |Dataset description|Description of the dataset.|
    |Dataset source type|Dataset source that you can select from the drop-down menu.|

7.  Add tags to identify the dataset.

8.  Navigate to the Data governance section and select each check box.

9.  Select **Add dataset**.

    The dataset is added to the catalog.


## What to do next

After your dataset is added to the data catalog, you can choose to create a smaller dataset by creating a derived dataset or adding a ground truth to your existing data set. For more information, see [Create a derived dataset](create-derived-dataset.md) or [Add a ground truth to each dataset record](add-ground-truth.md).


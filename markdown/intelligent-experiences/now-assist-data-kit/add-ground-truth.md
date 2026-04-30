---
title: Add a ground truth to each dataset record
description: Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can do this task by using the Now Assist Data Kit application.
locale: en-US
release: xanadu
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2024-10-16"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Add a ground truth to each dataset record

Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can do this task by using the Now Assist Data Kit application.

## Before you begin

Role required: sn\_data\_kit.admin, sn\_data\_kit.analyst

## About this task

After you successfully add a derived dataset to the data catalog, a pop-up window opens and then you can select **Add ground truth.**

## Procedure

1.  Select how you want to add the ground truth for the records in your dataset.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Currently, Add manually is supported.|
    |Ground truth type|Type.|
    |Ground truth guideline|Guidelines for labelers and linguists who manually add the ground truth.|
    |Column name|Name.|

3.  Select **Confirm**.

    A new Record detail page opens.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Form label|Incident record number.|
    |State|Time of the record creation.|
    |Summarization|Manual entry of the ground truth.|

    You can manually enter the ground truth and rate the ground truth. These options appear in a separate column in the dataset record.

5.  Select **Save and next**

    The ground truth column is added in a separate column in the dataset. Use the Add to data collection pop-up window to combine similar records from different datasets.

6.  Add the dataset to an existing collection by selecting **Add to data collection**.

    1.  Enter the data collection name, description, data collection category, and relevant tags.

    2.  To create a new data collection, slide the toggle bar.

7.  Select **Next**.

    A new data collection page populates.

8.  Select the Choose columns form and then select the columns that you want to add to the data collection.

9.  Select the Choose records form and select how you want to sample the dataset again \(manually or sampling method\).

    For a random sample, select **Run** to preview the record. Choose a sampling method, and select **Run** to preview the record.

    The selected records are added to the data collection.

10. Select the data collection to preview the records.

11. Select**Publish** to make the data available for validation.

    When you publish a collection, the data freezes curation and makes the dataset available for use through ServiceNow SDK.

12. Select **Confirm** to make your collection available.

    The data collection is published and available in Mobile SDK for evaluation.



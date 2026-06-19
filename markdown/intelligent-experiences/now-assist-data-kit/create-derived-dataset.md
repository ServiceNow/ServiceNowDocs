---
title: Create a derived dataset
description: Create a smaller, derived dataset from an existing dataset using Now Assist Data Kit. Use derived datasets to isolate specific records for focused ground truth labeling or evaluation without modifying the original dataset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/create-derived-dataset.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Create a derived dataset

Create a smaller, derived dataset from an existing dataset using Now Assist Data Kit. Use derived datasets to isolate specific records for focused ground truth labeling or evaluation without modifying the original dataset.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**, and open an existing dataset in the **Datasets** tab.

2.  Select the **Create derived dataset** button at the top of the **Records** list.

3.  In the **Add dataset info** section, fill in the fields.

    \[Omitted image "nadk-derived-dataset.png"\] Alt text: Create derived dataset form

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the derived dataset.|
    |Dataset description|Description of the derived dataset. This field is pre-populated with a reference to the parent dataset.|
    |Tags|Keywords to help identify and search for the dataset.|

4.  In the **Choose records** section, select a selection method and choose the records to include.

    A minimum of 10 records must be selected before you can create the dataset.

    -   **Manual Selection**: Select the check box next to each record you want to include.
    -   **Sampling Selection**: Select a sampling method from the drop-down menu, enter a number in the sample size box, and select **Run** to preview the sampled records.
5.  Select **Create dataset**.

    The derived dataset is added as a separate dataset.


## What to do next

After you have created the derived dataset, you can add ground truth to its records. For more information, see [Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/add-ground-truth.md).


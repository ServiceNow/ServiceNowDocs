---
title: Add a ground truth to each dataset record
description: Add a ground truth to each record in a dataset. A ground truth is an expected correct output for a given record. During evaluation in Now Assist Skill Kit, your custom skill's actual output is compared against the ground truth to measure accuracy and identify areas for improvement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/add-ground-truth.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Add a ground truth to each dataset record

Add a ground truth to each record in a dataset. A ground truth is an expected correct output for a given record. During evaluation in Now Assist Skill Kit, your custom skill's actual output is compared against the ground truth to measure accuracy and identify areas for improvement.

## About this task

Ground truth content should match your custom skill's output type. For a summarization skill, enter an ideal paragraph-length summary as the ground truth. For a content generation skill, enter the expected output text. The closer your ground truth examples are to real, high-quality outputs, the more meaningful your evaluation results will be.

## Before you begin

Role required: sn\_data\_kit.admin, sn\_data\_kit.analyst

The **Create ground truth guidelines** button is controlled by a system property that is not enabled by default. Before you begin, verify that the `sn_data_kit.enable_ground_truth` system property exists on your instance and is set to `true`. If the property does not exist, create it:

1.  Navigate to **All** &gt; **System Properties** &gt; **System Properties**.
2.  Select **New**.
3.  Fill in the following fields and select **Submit**:
    -   **Name**: `sn_data_kit.enable_ground_truth`
    -   **Type**: String
    -   **Value**: true

**Note:** Create this property in the Global application scope. If you create it in the wrong scope, the button doesn't appear.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**, and open an existing data set in the **Datasets** tab.

2.  Select the **Create ground truth guidelines** button.

3.  On the form, fill in the fields.

<table id="table_irk_ttk_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

-   Manual


</td></tr><tr><td>

Ground truth type

</td><td>

-   Summarization
-   Content generation
-   Other


</td></tr><tr><td>

Instructions

</td><td>

Guidelines for labelers and linguists who manually add the ground truth.

</td></tr><tr><td>

Column type

</td><td>

If you chose AI generated ground truth, select the column type.-   String
-   Number
-   JSON


</td></tr><tr><td>

Column label

</td><td>

The name of the column that is added for the ground truth in the dataset.

</td></tr></tbody>
</table>4.  Select **Confirm**.

    A new Record detail page opens.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Form label|Incident record number.|
    |State|Time of the record creation.|
    |Summarization|Manual entry of the ground truth.|

    You can manually enter the ground truth and rate the ground truth. These options appear in a separate column in the dataset record.

6.  Select **Save and next**

    The ground truth column is added in a separate column in the dataset. Use the Add to data collection pop-up window to combine similar records from different datasets.

7.  Add the dataset to an existing collection by selecting **Add to data collection**.

    1.  Enter the data collection name, description, data collection category, and relevant tags.

    2.  To create a data collection, slide the toggle bar.

8.  Select **Next**.

    A new data collection page populates.

9.  Select the Choose columns form and then select the columns that you want to add to the data collection.

10. Select the Choose records form and select how you want to sample the dataset again \(manually or sampling method\).

    For a random sample, select **Run** to preview the record. Choose a sampling method, and select **Run** to preview the record.

    The selected records are added to the data collection.

11. Select the data collection to preview the records.

12. Select**Publish** to make the data available for validation.

    When you publish a collection, the data freezes curation and makes the dataset available for use through ServiceNow SDK.

13. Select **Confirm** to make your collection available.

    The data collection is published and available in ServiceNow SDK for evaluation.



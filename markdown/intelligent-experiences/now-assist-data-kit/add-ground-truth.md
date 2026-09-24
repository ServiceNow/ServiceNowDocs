---
title: Add a ground truth to each dataset record
description: Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can do this task by using the AI Data Kit application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/add-ground-truth.html
release: brazil
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Add a ground truth to each dataset record

Add a ground truth, which is the real-world data that is used to train and test AI models to each dataset record. You can do this task by using the AI Data Kit application.

## Before you begin

Role required: sn\_data\_kit.admin, sn\_data\_kit.analyst

## Procedure

1.  After you create a data set, select **Create ground truth guidelines**.

2.  On the form, fill in the fields.

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
</table>3.  Select **Confirm**.

    A new Record detail page opens.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Form label|Incident record number.|
    |State|Time of the record creation.|
    |Summarization|Manual entry of the ground truth.|

    You can manually enter the ground truth and rate the ground truth. These options appear in a separate column in the dataset record.

5.  Select **Save and next**

    The ground truth column is added in a separate column in the dataset.


## What to do next

To combine this dataset with others and make the records available for evaluation, see [Create a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/create-data-collection.md).


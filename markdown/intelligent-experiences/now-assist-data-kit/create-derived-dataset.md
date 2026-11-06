---
title: Create a derived dataset
description: Create a smaller dataset from an existing dataset by selecting records manually or by random sampling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 2
keywords: [derived dataset, random sampling, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Create a derived dataset

Create a smaller dataset from an existing dataset by selecting records manually or by random sampling.

## Before you begin

Role required: sn\_data\_kit.admin

## About this task

A derived dataset contains copies of the records that you choose from another dataset. The original dataset doesn't change. A smaller dataset lets you evaluate a skill without processing every record.

If the original dataset was created from an instance table, the derived dataset keeps the access controls of that table.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Datasets** tab, select the dataset that contains the records that you want.

    If the dataset isn't listed, select **View all datasets**.

3.  On the dataset page, select **Create derived dataset**.

4.  In the Add dataset Info section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the derived dataset. Required. The name must contain at least one letter or number, and it can include underscores, hyphens, and spaces.|
    |Dataset description|Description of the derived dataset. By default, it names the dataset that the records come from.|
    |Tags|Keywords for the dataset.|

5.  In the Choose records section, select a selection method.

    |Selection method|Action|
    |----------------|------|
    |**__Manual Selection__**|Select the check box for each record that you want to include.|
    |**__Sampling Selection__**|In the **Sample size** field, enter the number of records to include, and then select **Run**. **Random Sampling** is the only sampling method. The sampled records appear in the records list.|

    The Selected records count at the top of the page shows how many records the derived dataset will include.

    You can't filter records in this section. To create a dataset of records that match specific conditions, add a dataset from an instance table and use a filter. For details, see [Add a dataset from an instance table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-dataset-instance-table.md).

6.  Select **Create dataset**.

    For sampling selection, **Create dataset** isn't available until you run the sample.

    The page for the derived dataset opens. Its state changes from In progress to Active when the records are copied. The copied records have new record IDs.


## What to do next

After the derived dataset is Active, you can [scan it for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md), [add ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md), or [add it to a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md).


---
title: Create a data collection
description: Combine one or more datasets into a data collection, choosing the columns and records to include. Then, publish the collection so that you can use it to evaluate a skill in AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/create-data-collection.html
release: brazil
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Create a data collection

Combine one or more datasets into a data collection, choosing the columns and records to include. Then, publish the collection so that you can use it to evaluate a skill in AI Skill Kit.

## Before you begin

Role required: sn\_data\_kit.admin

At least one dataset must exist. To learn more, see [Add a dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/add-dataset.md).

## About this task

A data collection is the object that AI Skill Kit uses to evaluate a skill. A collection can combine records from more than one dataset.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the **An overview of your data assets** section, select the **Datasets** tab.

3.  Select the dataset that contains the records that you want.

4.  At the top of the dataset page, select **Add to data collection**.

    -   To create a collection, enter the data collection name, description, and relevant tags.
    -   To add the dataset to an existing collection, clear the **Create Data Collection** check box. Then select the collection from the **Available data collection** field.
5.  Select **Confirm**.

6.  Select **Next**.

    The **Add to data collection** page displays.

7.  On the **Choose columns** form, select the columns that you want to add to the data collection.

8.  In the **Choose records** section, select a selection method.

    |Selection method|Action|
    |----------------|------|
    |**__Manual Selection__**|Select the check box for each record that you want to include. If you don't select any records, all records in the dataset are added to the collection.|
    |**__Sampling Selection__**|In the **Sampling Method** field, select **Random Sampling**. In the **Sample size** field, enter the number of records to include, and then select **Run**. The sampled records appear in the records list.|

9.  At the bottom of the page, select **Add to data collection**.

    For sampling selection, this button is available only after you run the sample.

10. Select the data collection to preview the records.

11. Select **Publish** to make the data available for evaluation.

    When you publish a collection, the collection freezes curation and becomes available for use through AI Skill Kit.

12. Select **Confirm** to make your collection available.

    The data collection is published.


## What to do next

Select the published data collection in AI Skill Kit and run the evaluation.


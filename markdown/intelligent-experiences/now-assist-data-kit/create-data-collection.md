---
title: Create a data collection
description: Combine one or more datasets into a data collection, choosing the columns and records to include. Then, publish the collection so that you can use it to evaluate a skill in AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 2
keywords: [data collection, random sampling, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Create a data collection

Combine one or more datasets into a data collection, choosing the columns and records to include. Then, publish the collection so that you can use it to evaluate a skill in AI Skill Kit.

## Before you begin

At least one dataset must exist. To learn more, see .

Role required: sn\_data\_kit.admin

## About this task

A data collection is the object that AI Skill Kit uses to evaluate a skill. A collection can combine records from more than one dataset.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Datasets** tab, select the dataset that contains the records that you want.

    If the dataset isn't listed, select **View all datasets**.

3.  At the top of the dataset page, select **Add to data collection**.

    -   To create a collection, enter a name in the **Data collection name** field. Optionally, enter a description, and add tags by typing each tag and pressing Enter.
    -   To add the dataset to an existing collection, turn off the **Create data collection** toggle. Then select the collection from the **Available data collection** field.
4.  Select **Confirm**.

    The Add to data collection page opens, with a Choose columns section and a Choose records section.

5.  In the Choose columns section, select the columns that you want to add to the data collection, and then select **Save &amp; next**.

6.  In the Choose records section, select a selection method.

    |Selection method|Action|
    |----------------|------|
    |**__Manual selection__**|Select the check box for each record that you want to include. If you don't select any records, all records in the dataset are added to the collection.|
    |**__Sampling selection__**|In the **Sample size** field, enter the number of records to include, and then select **Run**. **Random sampling** is the only sampling method. The sampled records appear in the records list.|

7.  At the bottom of the page, select **Add to data collection**.

    For sampling selection, this button is available only after you run the sample.

    Adding a dataset to a collection changes the dataset's state to Published. You can't edit or delete the records in a published dataset.

    The data collection page opens.

8.  Select **Publish data collection**.

    When you publish a collection, the collection freezes curation and becomes available for use through AI Skill Kit.

9.  Select **Confirm** to make your collection available.

    The data collection is published.


## What to do next

Select the published data collection in AI Skill Kit and run the evaluation.

You can also use a published data collection as the source for a labeling project, which adds ground truth to its records. Labeling projects can only use published collections. For details, see [Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md).


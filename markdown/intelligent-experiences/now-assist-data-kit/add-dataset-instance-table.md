---
title: Add a dataset from an instance table
description: Create a dataset from records in an instance table by choosing the columns to include and the conditions that select the records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/add-dataset-instance-table.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 3
keywords: [dataset, instance table, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Add a dataset from an instance table

Create a dataset from records in an instance table by choosing the columns to include and the conditions that select the records.

## Before you begin

Read access to the source table is required. The AI Data Kit roles don't grant it.

Role required: sn\_data\_kit.admin

## About this task

A dataset must contain at least 1 and no more than 10,000 records. Use the filter to keep the number of records within that range.

Dataset records keep the access controls of the source table. Anyone who views the records in the dataset must also be able to read the source table.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Datasets** tab, select **Create dataset**.

3.  In the Choose data section, select **Import data from Instance table**.

4.  In the **Table** field, select the table that contains the records that you want.

5.  In the **Columns** field, select the columns to include in the dataset.

6.  To add a column whose values are stored in another table, such as work notes, select **Add column via scripting** and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Display name of the column. Required.|
    |Name|Internal name of the column. Required.|
    |Type|Data type of the column values. The default is String.|
    |Script|Script that returns the column value for each record. The `current` parameter is the GlideRecord object for the record being processed. The editor includes a commented sample that adds work notes.|

    Scripted columns don't appear in the dataset preview.

7.  To limit the records that are included, select **Edit filter condition** and build the filter conditions.

    After you close the dialog box, the filter appears as an encoded query, such as `state=6`.

8.  Review the records in the Preview dataset section.

    If the preview shows no records, check your filter conditions. Also confirm that you can read the source table, because the preview shows no records without read access.

9.  Select **Continue**.

10. In the Add dataset info section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the dataset. Required.|
    |Description|Description of the dataset that helps you and others find it later.|
    |Source type|Read-only.|
    |Tags|Keywords for the dataset. Press Enter after each tag.|

11. In the Data governance section, select the **I'm assuring to use data responsibly for AI Evaluation** check box.

    **Add data** isn't available until you select this check box.

12. Select **Add data**.

    The dataset page opens with a state of In progress. Adding the records can take a few minutes. When it finishes, the state changes to Active.

    If a message says that a dataset must contain from 1 to 10,000 records, select **Back** and adjust the filter conditions.


## What to do next

After the dataset is Active, you can [scan it for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md), [create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md), [add ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md), or [add it to a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md).


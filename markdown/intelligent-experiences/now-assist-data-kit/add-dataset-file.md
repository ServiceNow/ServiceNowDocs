---
title: Add a dataset from a file
description: Create a dataset by importing records from a CSV or Excel file on your computer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/add-dataset-file.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 2
keywords: [dataset, import, CSV, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Add a dataset from a file

Create a dataset by importing records from a CSV or Excel file on your computer.

## Before you begin

Role required: sn\_data\_kit.admin

## About this task

You can import a CSV or XLSX file of up to 1,024 MB. The first row of the file must contain the column names. The file can contain up to 10,000 rows, including the header row, so a file can hold up to 9,999 records.

**Important:**

Records that you import from a file don't inherit access controls from any table, even if the data was originally exported from one. Anyone with an AI Data Kit role can view the records. Before you upload a file, remove any data that not everyone with an AI Data Kit role should see.

The original file is stored with the dataset, including any columns that you don't select.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Datasets** tab, select **Create dataset**.

3.  In the Choose data section, select **Import data from my computer**.

4.  To see the expected file layout, select **Download sample file**.

5.  In the Choose file section, select **Add file** and choose the file on your computer.

6.  In the Upload a file dialog box, review the **Title** and select **Upload**.

    The title names the uploaded file, not the dataset, and it's filled in from the file name. You name the dataset later.

7.  In the Define Columns section, select the check box for each column to include, and select a data type for each column.

    The columns come from the first row of the file. To select all columns, select the check box next to **Columns**.

    The data type is String by default.

8.  Select **Validate and Preview**.

    The Preview Dataset section shows the records with the columns that you selected. Column labels are generated from the column names in the file.

9.  Review the preview, and then select **Continue**.

    **Continue** isn't available until you validate the file.

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


## What to do next

After the dataset is Active, you can [scan it for sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md), [create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md), [add ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-ground-truth.md), or [add it to a data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-data-collection.md).


---
title: Add a dataset
description: Add the data from a table to a data catalog as a dataset through generative AI by using the Now Assist Data Kit application. Adding a dataset is required to create and publish a data collection.
locale: en-US
release: yokohama
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Add a dataset

Add the data from a table to a data catalog as a dataset through generative AI by using the Now Assist Data Kit application. Adding a dataset is required to create and publish a data collection.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  Navigate to Discover datasets and select **Get started**.

3.  On the **Datasets** tab, select **New**.

4.  Select where to curate data from.

    -   I'll import data from Instance table
    -   I'll import data from my computer
5.  On the Choose data form, select the table and columns.

    There’s an option to add columns, such as work notes and comments. These columns aren’t stored in the incident table but in a separate table. You can add these columns by using a script.

6.  Select Add a filter if needed.

7.  Review the records and select **Continue**.

8.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the dataset.|
    |Dataset description|Description of the dataset.|

9.  Add tags to identify the dataset.

10. Navigate to the Data governance section and select each check box.

    ![Data governance options for Now Assist Data Kit](../image/image/nadk-data-governance.png)

    -   I'm assuring to use data responsibly for AI Evaluation
    -   Scan for personally identifiable or information sensitive data before creating datasets. You can turn this off if you prefer.

        **Note:** If you opt in, your data is scanned for sensitive data like names or email addresses using [vault service](https://www.servicenow.com/docs/bundle/yokohama-platform-security/page/administer/general/concept/privacy-landing-page.html). After the scan, records will be highlighted and give you an option to anonymize them. You can also choose to scan the dataset after it is generated.

11. Select **Generate dataset**.

    The dataset is added to the data assets.


## What to do next

After your dataset is added to the data catalog, you can choose to create a smaller dataset by creating a derived dataset or adding a ground truth to your existing data set. For more information, see [Create a derived dataset](create-derived-dataset.md) or [Add a ground truth to each dataset record](add-ground-truth.md).


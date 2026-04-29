---
title: Add a dataset
description: Add the data from a table to a data catalog as a dataset through generative AI by using the Now Assist Data Kit application. Adding a dataset is required to create and publish a data collection.
locale: en-US
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
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

    If a column does not appear as a possible selection, then the field is not a supported data type. For example, Watch List fields are the glide\_list datatype, which is not supported, so Watch List is not a selectable field.

6.  Select **Add column via scripting** if you have columns, such as work notes or comments, that aren't stored in the table.

    This is an example script for adding worknotes.

    ```
    (function generate(current) {
    //Current is the Gliderecord object of current record.
    // //Sample script for adding worknotes
    // var gr = new GlideRecord("sys_journal_field");
    // gr.addQuery('name', current.getTableName());
    // gr.addQuery('element_id', current.getUniqueValue());
    // gr.query();
    // var records = [];
    // while (gr.next()) {
    //     var obj = {
    //         "value": gr.getValue("value"),
    //         "type": gr.getValue("element"),
    //         "created": gr.getValue("sys_created_on"),
    //         "created_by": gr.getValue("sys_created_by")
    //     };
    //     records.push(obj);
    // }
    // return records;
    })(current);
    ```

7.  Select **Edit filter condition**.

8.  Review the records and select **Continue**.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the dataset.|
    |Dataset description|Description of the dataset.|

10. Add tags to identify the dataset.

11. Navigate to the Data governance section and select each check box.

    ![Data governance options for Now Assist Data Kit](../image/nadk-data-governance.png)

    -   I'm assuring to use data responsibly for AI Evaluation
    -   Scan for personally identifiable or information sensitive data before creating datasets. You can turn this off if you prefer.

        **Note:** If you opt in, your data is scanned for sensitive data like names or email addresses using [vault service](https://www.servicenow.com/docs/bundle/yokohama-platform-security/page/administer/general/concept/privacy-landing-page.html). After the scan, records will be highlighted and give you an option to anonymize them. You can also choose to scan the dataset after it is generated.

12. Select **Generate dataset**.

    Fields of any data type are stored as strings when converted to a data asset.

    The dataset is added to the data assets.


## What to do next

After your dataset is added to the data catalog, you can choose to create a smaller dataset by creating a derived dataset or adding a ground truth to your existing data set. For more information, see [Create a derived dataset](create-derived-dataset.md) or [Add a ground truth to each dataset record](add-ground-truth.md).


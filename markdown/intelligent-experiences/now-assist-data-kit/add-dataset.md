---
title: Add a dataset
description: Import data from a ServiceNow table or a local file into Now Assist Data Kit as a dataset. Datasets are the foundation of data collections, which you publish for use in custom skill evaluation in Now Assist Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/add-dataset.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Add a dataset

Import data from a ServiceNow table or a local file into Now Assist Data Kit as a dataset. Datasets are the foundation of data collections, which you publish for use in custom skill evaluation in Now Assist Skill Kit.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  On the **Datasets** tab, select **Create dataset**.

3.  On the **Choose data** page, select how you want to import data.

    -   **Import data from Instance table**
    -   **Import data from my computer**
4.  Select the table and columns.

    If a column does not appear as a possible selection, the field is not a supported data type. For example, Watch List fields are the glide\_list datatype, which is not supported, so Watch List is not a selectable field.

5.  Select **Add column via scripting** to include columns stored in other tables, such as comments or work notes.

    This is an example script for adding work notes.

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

    **Note:** Additional columns are not included in the dataset preview.

6.  Select **Edit filter condition** to filter which records are included in the dataset.

7.  Review the dataset preview and select **Continue**.

8.  On the **Add dataset info** page, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Dataset name|Name of the dataset.|
    |Description|Description of the dataset.|
    |Source type|The origin of the dataset data. This field is automatically populated based on your import selection.|
    |Tags|Keywords to help identify and search for the dataset. Press Enter after each tag to add it.|

9.  In the **Data governance** section, select the check boxes.

    \[Omitted image "nadk-data-governance.png"\] Alt text: Data governance options for Now Assist Data Kit

    -   I'm assuring to use data responsibly for AI Evaluation
    -   Scan for personally identifiable or information sensitive data before creating datasets. You can turn this off if you prefer.

        **Note:** If you opt in, your data is scanned for sensitive data like names or email addresses using [vault service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/privacy-landing-page.md). After the scan, records will be highlighted and give you an option to anonymize them. You can also choose to scan the dataset after it is generated.

10. Select **Add data**.

    Fields of any data type are stored as strings when converted to a data asset.

    The dataset is added to the data catalog.


## What to do next

After your dataset is added, you can create a derived dataset or add a ground truth to your existing dataset. For more information, see [Create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md) or [Add a ground truth to each dataset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/add-ground-truth.md).

**Important:** Datasets cannot be edited or deleted after creation. Before generating a dataset, verify your table selection, filter conditions, and column choices.


---
title: Create a field for data extraction
description: Set up fields as part of your use case. Document Intelligence uses fields to identify and extract data from documents. Fields can be grouped to help DocIntel extract data from documents with tables, check box lists, and other logical groupings of fields.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up document extraction use cases, Configuring Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Create a field for data extraction

Set up fields as part of your use case. Document Intelligence uses fields to identify and extract data from documents. Fields can be grouped to help DocIntel extract data from documents with tables, check box lists, and other logical groupings of fields.

## Before you begin

Role required: sn\_docintel.manager

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

2.  Select a use case in the list.

3.  Go to the **Fields** tab and select **Define your fields**.

    If you have already defined one or more fields and you want to add another field, select **New field**.

4.  Select the type of data that you want to extract from the document.

    You can choose one of the following types of data to extract:

    -   **Single field**

        Single fields are used to extract a single piece of information in the document. For example, a document number or a customer name.

    -   **Check box list**

        Check box lists are used to extract a check box or a group of check boxes. Each check box can be checked or cleared.

    -   **Table**

        Tables are used to extract lists or tables of information. A table can have multiple columns. The number of list items or table rows doesn’t have to be known in advance.

    -   **Single field group**

        Single field groups are used to extract values that are grouped in the document. For example, a location with an address, city, and country. Only one item can be extracted for a single field group, as opposed to the multiple rows extracted for a table.

    A form displays based on the data type you selected.

5.  On the form, fill in the fields.

    The type of form depends on the type of field that you selected in the previous step.

    -   [Single field form](../reference/single-field-form.md)
    -   [Single field group form](../reference/single-field-group-form.md)
    -   [Check box list form](../reference/check-box-list-form.md)
    -   [Table form](../reference/table-form.md)
6.  Select **Save**.


## Result

The system added the new fields to the Fields list associated with the use case.


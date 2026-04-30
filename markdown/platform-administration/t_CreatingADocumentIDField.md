---
title: Document ID field
description: You can create document ID fields to reference any record on any table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Document ID field

You can create document ID fields to reference any record on any table.

## Before you begin

Role required: personalize\_dictionary

## About this task

In comparison, a reference field references a record on a specific table. To reference records from any table, two fields need to work together—one to store the table reference and another to store the record reference.

You can select the document ID type when creating a new field.

## Procedure

1.  Navigate to the form view for the table.

2.  Right-click the header and select **Configure** &gt; **Form Layout**.

3.  Create a field to store the table name and click **Add**.

    -   **Name**: Any label \(for example, `Model table`\)
    -   **Type**: String
4.  Create a field to store the record reference and click **Add**.

    -   **Name**: Label for your document ID field \(for example, `Model ID`\)
    -   **Type**: Document ID
5.  Click **Save**.

6.  Right-click the form header and select **Configure** &gt; **Dictionary**.

7.  Open the dictionary entry for the document ID field.

8.  Under **Related Links**, click **Advanced view**.

9.  In the **Dependent** field, enter the column name of the table reference field \(for example, `u_model_table`\).

10. In **Attributes**, add the **show\_all\_tables** dictionary attribute to display system tables.

11. Click **Update**.When users click the reference lookup for the document ID field, a dialog appears that allows them to select the table and then the record. The sys\_id of the selected record is stored in the document ID field and the table name is stored in the table reference field.

12. [Configure the form](../../form-administration/concept/configure-form-layout.md#) to remove the table reference field.

    ![Document ID](../image/DocumentID1.png)


**Related topics**  


[Configuring the form layout](../../form-administration/concept/configure-form-layout.md#)

[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)


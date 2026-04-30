---
title: Prepare to left-pad number fields in custom tables
description: Before you configure left padding of number fields on a custom table or a table that does not extend the task table, you must prepare business rules and script includes.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Record numbering, Add and customize a field in a table, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Prepare to left-pad number fields in custom tables

Before you configure left padding of number fields on a custom table or a table that does not extend the task table, you must prepare business rules and script includes.

## Before you begin

Role required: admin

## Procedure

1.  Duplicate the base system business rule named **Pad Numbers**: Click **Insert and Stay**.

    If **Insert and Stay** is not available on your instance, create a new business rule and manually copy all field values from Pad Numbers.

2.  Give the business rule a new name and change the script field to read as follows:

    ```
    padCurrentCategory();
    function padCurrentCategory() {
    var target = new GlideRecord(current.category+"");
    if (!target.isValidField("u_number") || target.isValidField("number")) return;
    var nm = new UNumberManager();
    nm.padTableNumbers(current.category, current.maximum_digits);
    }; 
    ```

3.  Save the changes.

4.  Duplicate the base system script include named NumberManager.

5.  Change the following two lines as indicated:

    ```
    105: currentNumber = records.u_number.toString();
    117: records.u_number = prefix + currentNumber;
    ```

6.  Name the new script include `UNumberManager` and save your changes.

    You can now continue with the process of configuring left-padding and renumbering records.


-   **[Configure left padding of a system number in a table](t_RenumberingRecords.md)**  
You can configure the left padding of the system numbers on a table. For example, pad the **Number** field on an Incident, Problem, or Change Request.

**Parent Topic:**[Record numbering](../concept/c_ManagingRecordNumbering.md)


---
title: Relabel a column
description: Sometimes, two different tables may have fields of the same name that are both important \(such as two tables with a sys\_updated\_on field\). For clarity, relabel one of the fields.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Database view creation, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Relabel a column

Sometimes, two different tables may have fields of the same name that are both important \(such as two tables with a sys\_updated\_on field\). For clarity, relabel one of the fields.

## Before you begin

Role required: admin.

## About this task

To create clear reports, relabel the fields on the Database View \[sys\_db\_view\] table without changing the names of the fields.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Language File**.

2.  Select **New**.

3.  Fill in the form as follows:

    |Name|Description|
    |----|-----------|
    |Table|Name of the database view|
    |Label|Display label|
    |Plural|Plural form of the display label|
    |Element|Name of the field on the database view in the format variable prefix\_fieldname. For example, you may enter inc\_name to indicate the Name field on the Incident table. **Variable prefix** is a required field when you define the tables in a database view.|

4.  Select **Submit**.


**Parent Topic:**[Database view creation](c_CreatingDatabaseViews.md)

**Previous topic:**[Specify a field to return](../concept/c_SpecifyAFieldToReturn.md)

**Next topic:**[Specify the number of records to return](../concept/c_SpecifyTheNumberOfRecordsToReturn.md)


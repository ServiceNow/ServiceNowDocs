---
title: Configure due dates for supplier cases
description: Configure due dates for different case types so that the Due date field is auto-populated when you create supplier cases.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage supplier cases from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure due dates for supplier cases

Configure due dates for different case types so that the **Due date** field is auto-populated when you create supplier cases.

## Before you begin

Role required: sn\_slm.admin

## About this task

Although the **Due date** field is auto-populated for a supplier case type, you can always update this field as required.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Default Due Dates for Cases**.

    The Decision Builder opens and displays the Decision table for configuring the default due dates.

    |Case type|Default due date|
    |---------|----------------|
    |Onboard new supplier|30|
    |Supplier support request|3|
    |General inquiry|3|
    |Banking information change request|3|
    |Supplier information change request|3|
    |Supplier location change request|3|
    |Enroll new supplier user|3|
    |Account access request|3|
    |Supplier issue|3|
    |Document change request|3|
    |Conduct a risk assessment|3|
    |Conduct a tiering risk assessment|3|
    |Request supplier contact|3|
    |Offboard supplier contact|3|
    |Primary contact elevation|3|

2.  Under the Default due date column, select a row next to the case type row and enter a positive number.

    The number that you enter for a case type is auto-populated in the **Due date** field the next time you create a supplier case of that case type.

    For example, let's say that you enter 3 as the due date for the case type General enquiry. If you create a General enquiry case on September 12, the due date will be in three days from this date; that is, September 15.

3.  Select **Save**.


**Parent Topic:**[Manage supplier cases from the Source-to-Pay Workspace](../concept/managing-cases.md)


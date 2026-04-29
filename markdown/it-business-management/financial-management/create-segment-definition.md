---
title: Create a segment definition - Legacy
description: Define segments to be used with cost and budget models.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Segments - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a segment definition - Legacy

Define segments to be used with cost and budget models.

## Before you begin

Role required: budget\_admin or cost\_transparency\_admin

## About this task

You can create more than one segment in the same transaction table with different filter conditions. For example, create one segment for vendors in the core\_company table where the **Vendor** field is **true**, and another segment for customers in the same table where the **Vendor** field is **false**.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Administration** &gt; **Segments**.

    You can also create a new segment from the **Segment Definition** tab on the workbench.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Segment name|Descriptive name for the new segment.|
    |Transactional table|Database table for transaction data to associate with the segment.|
    |Primary field|Field in the transactional table to serve as the primary source of information for the segment.|
    |Used by Cost Allocation|Check box to make the segment available for financial modeling.|
    |Used by Budgeting|Check box to make the segment available for financial planning.|
    |Condition|Conditions that can be set to filter the records.|
    |Fiscal effective start|Fiscal start period to filter the records in allocation setup for that fiscal period. Used by Financial Modeling.|
    |Fiscal effective end|Fiscal end period to filter the records in allocation setup for that fiscal period. Used by Financial Modeling.|

4.  Set a fiscal validity for the segment to include only valid records for allocation.

    To view all the accounts in all fiscal periods, specify the fiscal effective start and end date as 'none'.

    1.  Example 1: Consider 'server' as a segment.

        To filter valid servers for allocation, set the fiscal start date as the install date and set the fiscal end date as the decommissioned date.

    2.  Example 2: To view only active projects for a fiscal period, use active start and end dates in the projects table.

5.  Click **Submit**.


**Parent Topic:**[Segments - Legacy](../concept/segments.md)


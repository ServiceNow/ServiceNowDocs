---
title: Define an allocation unit
description: Allocation unit records define the capacity and usage of a business service.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use business services with expenses, Cost Management, Strategic Portfolio Management]
---

# Define an allocation unit

Allocation unit records define the capacity and usage of a business service.

## Before you begin

Role required: financial\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Config** &gt; **Allocation Units**.

2.  Select a record to edit or select **New**.

    **Note:** Selecting the name of the configuration item will display the CI record, not the Allocation Units.

    |Field|Description|
    |-----|-----------|
    |Configuration Item|Select the Business Service to define allocation units for.|
    |Total Units|The total number of units of expense available to allocate. A unit is a generic measurement which can represent anything. Should match the cost center relationship unit. What units represent can be recorded in the **Unit Type** field. Using the Total units option may result in unallocated expenses if there are unallocated business service units. Using the Allocated unit option always results in 100% expense allocations.|
    |Allocated Units|How many of the total units are allocated. Populated by script.|
    |Available Units|How many of the total units are unallocated. Populated by script.|
    |Updated|When the units were last updated.|
    |Unit Type \(added by configuring the form\)|Used to record what the units represent \(e.g. seats, licenses, Gigabytes, and so on\).|


**Parent Topic:**[Use business services with expenses](../concept/c_UseBusinessServicesWithExpenses.md)


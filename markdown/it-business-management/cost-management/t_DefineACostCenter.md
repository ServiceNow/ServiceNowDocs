---
title: Define a cost center
description: Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities, and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.
locale: en-US
release: yokohama
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use business services with expenses, Cost Management, Strategic Portfolio Management]
---

# Define a cost center

Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities, and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.

## Before you begin

Role required: financial\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Config** &gt; **Cost Center**.

2.  Select a record to edit or select **New**.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the cost center.|
    |Account Number|An account number associated with the cost center, if one exists.|
    |Code|A code associated with the cost center, if one exists.|
    |Location|A reference to the location of the cost center.|
    |Manager|A reference to the user who manages the cost center.|
    |Valid from|The date that the cost center is valid from.|
    |Valid to|The date that the cost center is valid to.|

    |Field|Description|
    |-----|-----------|
    |Service|A reference to a Business Service.|
    |Cost Center|The cost center to apply the relationship to. If reached through the related list, it should already be related to the appropriate cost center.|
    |Allocation Percentage|Feature not yet implemented.|
    |Allocation Type|A choice list. Should be **Units**.|
    |Allocation Units|The number of units that the cost center is using. This is measured using the same type of unit used to define the total capacity of the business service in the allocation unit record. This number will be used to update the number of allocated units in the allocation unit record. It will also be used to determine the amount of expenses to allocate to the cost center based on the percentage of business service used versus the total capacity.|


**Parent Topic:**[Use business services with expenses](../concept/c_UseBusinessServicesWithExpenses.md)


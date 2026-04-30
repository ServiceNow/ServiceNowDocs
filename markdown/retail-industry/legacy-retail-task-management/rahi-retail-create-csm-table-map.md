---
title: Create a CSM Table Map for Retail Task Management Core
description: Create a CSM table map to create multi-store case configurations for use with your service definitions.
locale: en-US
release: yokohama
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Retail Task Management, Retail Task Management, Retail]
---

# Create a CSM Table Map for Retail Task Management Core

Create a CSM table map to create multi-store case configurations for use with your service definitions.

## Before you begin

Role required: admin

Scope required: Retail Task Management Core.

## About this task

![Retail multi-store record CSM table map creation form.](../image/rahi-retail-csm-table-map.png)

In the preceding example, Retail Case is both the parent and child case type for this table mapping. This means that for parent cases of type Retail Case, child cases will also be of this type.

## Procedure

1.  Navigate to **All** and search for **csm\_table\_map.do**

    ![All search menu to navigate to the CSM mapping table.](../image/rahi-retail-csm-table-all.png)

2.  Press enter.

3.  In **CSM Table Map**, enter a mapping name.

4.  In **Source Table**, select the desired parent table for your multi-store cases.

5.  In **Target Table**, select the desired child table type for your multi-store cases.

6.  Select **Submit**.


## Result

Service definitions leveraging the multi-store case creation capability are now enabled through utilization of the Multiple case creation config field.

Once this mapping has been created, use the field mapping to define which fields are mapped from the parent to child case. This mapping should occur, at a minimum, for the following fields:

-   Description
-   Short description
-   Priority


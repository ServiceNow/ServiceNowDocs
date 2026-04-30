---
title: Create segments for linear assets
description: Create segments for linear assets to assign work orders to the segments. You can also create maintenance plans for the segments.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create segments for linear assets

Create segments for linear assets to assign work orders to the segments. You can also create maintenance plans for the segments.

## Before you begin

Linear segments are parts of a linear asset. When creating a linear segment, you must enter values for any two of the following fields and the value for the third field is populated automatically. For example, when you enter the start and end markers, the **Length** field is automatically filled in. Similarly, entering the start marker and length populates the **End marker** field.

-   Start marker
-   End marker
-   Length

If you enter start marker or end marker on the map, markers must be within 10 feet from the linear asset line. This value can be customized by changing the value of the asset\_property **com.eam.linear\_segment\_marker\_boundary**.

For details on creating work orders and maintenance plans, see [Create a work order for an enterprise asset](create-eam-work-order.md) and [Create a maintenance plan for your enterprise assets](create-eam-maintenance-plan.md).

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise asset estate** &gt; **Linear assets**.

2.  Open the linear asset record on which you want to add segments.

3.  Select the Linear segments related list.

4.  Select **New**.

5.  On the form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the linear segment.|
    |**Linear asset type**|The linear asset type of the linear asset|
    |**Linear asset**|The linear asset that the segment belongs to.|
    |**State**|The current state of the linear asset.|
    |**Description**|A brief description of the linear segment.|
    |**Location**|Location of the linear asset.|
    |**Start marker**|Start point of the linear segment.|
    |**End marker**|End point of the linear segment.|
    |**Length**|The length of the linear segment.|
    |**Length unit**|The unit the length of the linear segment is measured in.|

6.  Select **Save**.

    The linear segments appear in the Linear segments related list.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)


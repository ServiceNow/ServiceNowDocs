---
title: Submit an enterprise asset move order through the Service Catalog
description: Use the ServiceNow Service Catalog to submit a move order so that you can move in-use or consumed enterprise assets between locations.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Submitting an enterprise asset move order, Managing enterprise asset move orders, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Submit an enterprise asset move order through the Service Catalog

Use the ServiceNow® Service Catalog to submit a move order so that you can move in-use or consumed enterprise assets between locations.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or end user

**Note:** The sn\_eam.enterprise\_asset\_manager role can submit move orders for any enterprise assets within a deployment. The end user role can submit move orders for only assigned enterprise assets.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Enterprise Asset Lifecycle**.

2.  From the list of available Enterprise Asset Lifecycle catalog items, select **Asset Move Order**.

3.  On the Catalog item to initiate an asset move order form, fill in the fields.

<table id="table_rtm_3vk_bxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requested for

</td><td>

User who the move order is being submitted for. If you specify a user in this field, the move order can include enterprise assets that are assigned only to that user.

</td></tr><tr><td>

Assignment group

</td><td>

Group that you want to assign the move order to.

</td></tr><tr><td>

Assigned to

</td><td>

User who you want to assign the move order to.

</td></tr><tr><td>

Move date

</td><td>

Date on which you want to move the enterprise assets.

</td></tr><tr><td>

From location

</td><td>

Location that you want to move the enterprise assets from.

</td></tr><tr><td>

To location

</td><td>

Location that you want to move the enterprise assets to.

</td></tr><tr><td>

Asset\(s\)

</td><td>

Enterprise assets that you want to include in the move order. You can select from any of the enterprise assets that reside in the location specified in the **From location** field.**Note:** If you select an enterprise asset that contains any child assets, all child assets are also included in the move order.

</td></tr><tr><td>

Notes/Special Instructions

</td><td>

Additional notes or instructions for the move order.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Submitting an enterprise asset move order](../concept/submitting-enterprise-asset-move-order.md)


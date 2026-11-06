---
title: Submit an enterprise asset move order through the Service Catalog
description: Use the ServiceNow Service Catalog to submit a move order so that you can move in-use or consumed enterprise assets between locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/enterprise-asset-management/submit-enterprise-asset-move-order-service-catalog.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Submitting an enterprise asset move order, Managing enterprise asset move orders, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Submit an enterprise asset move order through the Service Catalog

Use the ServiceNow® Service Catalog to submit a move order so that you can move in-use or consumed enterprise assets between locations.

## Before you begin

Role required: none

**Note:** If you have the sn\_eam.enterprise\_asset\_manager role, you can include any eligible enterprise asset in a move order. If you have any other role, you can include only enterprise assets that are assigned to, managed by, or owned by the user specified in the **Requested for** field of the move order.

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

User who the move order is being submitted for.

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

Enterprise assets that you want to include in the move order. Consider the following points when selecting these enterprise assets:

-   If you have the sn\_eam.enterprise\_asset\_manager role, you can select from any of the enterprise assets that reside in the location specified in the **From location** field.
-   If you have any role other than the sn\_eam.enterprise\_asset\_manager role, you can select from only the enterprise assets that meet the following criteria:
    -   Reside in the location specified in the **From location** field.
    -   Are assigned to, managed by, or owned by the user specified in the **Requested for** field.
-   If you select an enterprise asset that contains any child assets, all child assets are also included in the move order.


</td></tr><tr><td>

Notes/Special Instructions

</td><td>

Additional notes or instructions for the move order.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Submitting an enterprise asset move order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/enterprise-asset-management/submitting-enterprise-asset-move-order.md)


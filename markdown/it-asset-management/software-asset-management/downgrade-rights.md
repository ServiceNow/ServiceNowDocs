---
title: Downgrade Rights
description: The concept of downgrading licenses is built into the Software Asset Management plugin feature. Downgrading rights is the process of having acquired the rights to the latest version of software but using the rights to license earlier versions of the same software.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Downgrade Rights

The concept of downgrading licenses is built into the Software Asset Management plugin feature. Downgrading rights is the process of having acquired the rights to the latest version of software but using the rights to license earlier versions of the same software.

Downgrade rights are added at the software model level.

The Software Asset Management Content Service generates downgrade rights. The downgrade rights correspond to a discovery map. The **Download software content: Downgrade Rights** scheduled job that runs weekly, gets the downgrade rights from the Software Asset Management Content Service and pushes the data to the Downgrade Rights \[samp\_dmap\_downgrade\_model\] table.

Another scheduled job, **SAM- Create downgrades/upgrades for a software entitlement**, picks up the information from the \[samp\_dmap\_downgrade\_model\] table. The table propagates the next version and the downgrade rights on the existing software models and their corresponding entitlements.

If there’s no software model corresponding to a discovery map, when populating the Downgrade Rights \[samp\_sw\_downgrade\_model\] table, a new software model is automatically created.

If the discovery map corresponding to the software model has downgrade rights, the Downgrade Rights related list is automatically populated with a hierarchical list of downgraded versions of the software.

Once downgrade rights are created and saved in the Downgrade Rights tables, \[samp\_sw\_downgrade\_model\] and \[samp\_downgrade\_model\], the downgrade rights can't be deleted. However, you can deactivate the downgrade rights.

If you delete a software model, all records corresponding to the software model in the Downgrade Rights \[samp\_sw\_downgrade\_model\] table are automatically deleted.

Downgrade rights are supported across products for the same publisher, which helps in effectively managing product name changes. When a product is renamed, it's treated as two products. For example, if the product Captivate is renamed to Illustrator, both Captivate and Illustrator are considered distinct products. You can manually add software model downgrade rights from Illustrator to Captivate either in the software model form or in the software entitlement form.

The system doesn’t permit creating duplicate downgrade rights; either through the scheduled job or manually in the Software Model and Entitlement form layout. If you try to create duplicate downgrade rights on software models or on entitlements, an error message appears informing you that the downgrade model exists. If they have the same values in all the following fields, downgrade rights are considered to be duplicates.

-   **Publisher**
-   **Product**
-   **Version condition**
-   **Version**
-   **Edition condition**
-   **Edition**
-   **Platform**
-   **Language**
-   **Software install condition**
-   **Named User Type**- is displayed only for SAP products.

If you already have duplicate downgrade rights from previous Software Asset Management Professional releases, then those duplicate downgrade rights aren't modified or deleted.

If you try to create a duplicate downgrade right for an inactive downgrade right, an error message appears. The error message informs you that an inactive downgrade right exists and you can reactivate it.

![Downgrade rights](../image/mmasset0021314-discovery-map-horizontal.png)

Downgrade rights aren’t available for the following license metrics mentioned in the metric groups:

**Note:** Downgrade rights aren't supported for the User Subscription license metric regardless of the metric group.

<table id="table_grv_gg3_xfc"><thead><tr><th>

Metric group

</th><th>

License metric

</th></tr></thead><tbody><tr><td>

SAP

</td><td>

-   Engine Measurement
-   Named User

</td></tr><tr><td>

Consumption

</td><td>

SaaS Consumption

</td></tr><tr><td>

Concurrent Licenses

</td><td>

-   Floating
-   Token
-   Network

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)


---
title: Add a custom software product in Software Asset Management classic
description: If a software product does not exist in the Software Library, you can add a custom product. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Add a custom software product in Software Asset Management classic

If a software product does not exist in the Software Library, you can add a custom product. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.

## Before you begin

Role required: sam\_admin

## About this task

The product and publisher combination is used during discovery model normalization. If the custom product exists, a message is shown.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Custom Products** and create a new record \(see table for field descriptions\).

<table id="table_fdn_2pd_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_xgr_fd1_nfb"><td>

Publisher

</td><td>

Publisher of the custom software product. If it does not exist, a new one can be created on the Publisher field Companies lookup list.

</td></tr><tr id="row_xfx_fd1_nfb"><td>

Product

</td><td>

Name of the custom software product.

</td></tr><tr id="row_add_gd1_nfb"><td>

Subscription software

</td><td>

Option that indicates that the software has a subscription.

</td></tr><tr id="row_btp_gd1_nfb"><td>

Product type

</td><td>

Product type of the custom software product.-   Child: A subcomponent of main software \(not licensable\).
-   Driver: A software product that controls a device.
-   Licensable: A software product that is licensable.
-   Not Licensable: A software product that is not licensable.
-   Patch: A software product designed to update, fix, or improve an existing computer program.
-   Unknown: A software product that is unknown.


</td></tr><tr id="row_r5x_gd1_nfb"><td>

Product classification

</td><td>

Official UNSPSC classification.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option that excludes the custom product details from being shared with [Software Asset Management Content Service](../concept/c_SAMContentService.md) if opted in.

</td></tr><tr id="row_nch_hd1_nfb"><td>

Active

</td><td>

Option that indicates the rule is active.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)


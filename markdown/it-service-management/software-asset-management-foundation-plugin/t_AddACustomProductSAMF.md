---
title: Add a Software Asset Management Foundation plugin custom software product
description: You can add a custom product if a software product does not exist in the Software Library. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management Foundation plugin Administration, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Add a Software Asset Management Foundation plugin custom software product

You can add a custom product if a software product does not exist in the Software Library. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.

## Before you begin

Role required: sam\_admin

## About this task

The product and publisher combination is used during discovery model normalization. If the custom product already exists, a message is shown.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Custom Software Products** and create a new record \(see table for field descriptions\).

<table id="table_fdn_2pd_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Publisher of the custom software product. If it does not exist, a new one can be created on the Publisher field Companies lookup list.

</td></tr><tr><td>

Product

</td><td>

Name of the custom software product.

</td></tr><tr><td>

Product type

</td><td>

Product type of the custom software product.-   Child: A subcomponent of main software \(not licensable\).
-   Driver: A software product that controls a device.
-   Licensable: A software product that is licensable.
-   Not Licensable: A software product that is not licensable.
-   Patch: A software product designed to update, fix, or improve an existing computer program.
-   Unknown: A software product that is unknown.


</td></tr><tr><td>

Product classification

</td><td>

Official UNSPSC classification.

</td></tr><tr><td>

Active

</td><td>

Check box for activating the rule.

</td></tr></tbody>
</table>
**Parent Topic:**[Software Asset Management Foundation plugin Administration](../concept/c_SAMAdministrationSAMF.md)


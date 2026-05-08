---
title: Add a software pattern normalization rule
description: You can add a pattern normalization rule to normalize specific software products in your environment based on a common pattern.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Add a software pattern normalization rule

You can add a pattern normalization rule to normalize specific software products in your environment based on a common pattern.

## Before you begin

Role required: sam\_admin

## About this task

**Note:** When creating a pattern normalization rule for custom products and publishers, create the custom product and company records first.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Pattern Normalization Rules** and create a new record \(see table for field descriptions\).

<table id="table_gb1_jgm_ty"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Specify a unique name for pattern normalization rule.

</td></tr><tr><td>

Discovered publisher contains

</td><td>

Specify text to search for in the software publisher field.

</td></tr><tr><td>

Discovered product contains

</td><td>

Specify text to search for in the product field.

</td></tr><tr><td>

Active

</td><td>

Option that activates the rule.

</td></tr><tr><td>

Discovered publisher is empty

</td><td>

Option that includes products that have an empty publisher field \(the rule applies to discovery models where the publisher is unknown\).

</td></tr><tr><td class="sub-head" colspan="2">

Normalized Attributes

</td></tr><tr><td>

Publisher

</td><td>

Specify the normalized name of the publisher of the software.

</td></tr><tr><td>

Product

</td><td>

Specify the normalized name of the product.

</td></tr><tr><td>

Edition

</td><td>

Specify the product edition.

</td></tr><tr><td>

Product type

</td><td>

Choose the product type.-   Child: A subcomponent of main software \(not licensable\).
-   Driver: Software product that controls a device.
-   Licensable: Software product that is licensable.
-   Not Licensable: Software product that is not licensable.
-   Patch: Software product designed to update, fix, or improve an existing computer program.


</td></tr><tr><td>

Version

</td><td>

Specify the version of the product.

</td></tr><tr><td>

Platform

</td><td>

Choose the platform.-   Windows
-   macOS
-   UNIX


</td></tr><tr><td>

Language

</td><td>

Choose the language.-   Dutch
-   English
-   French
-   German
-   Italian
-   Spanish


</td></tr></tbody>
</table>2.  Once the rule is created, to apply the rule so applicable discovery models are normalized without delay, click the **Apply Rule** related link.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)


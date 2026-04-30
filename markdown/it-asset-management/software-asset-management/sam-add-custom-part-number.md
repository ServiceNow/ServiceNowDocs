---
title: Add a custom part number
description: You can add a custom part number to resolve an entitlement import error that occurs when a part number does not exist in the Software Library.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Add a custom part number

You can add a custom part number to resolve an entitlement import error that occurs when a part number does not exist in the Software Library.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Custom Part Numbers** and create a new record \(see table for field descriptions\).

<table id="table_fdn_2pd_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher part number

</td><td>

Manufacturer product code.

</td></tr><tr><td>

Entitlement definition

</td><td>

Discovery map associated with the part number. -   Publisher
-   Product
-   Version
-   Edition
-   Language
-   Platform


</td></tr><tr><td>

License type

</td><td>

Specifies whether the rights grant full access to the software or if they are being upgraded from a previous version of the software. -   Full
-   Upgrade


</td></tr><tr><td>

License metric

</td><td>

The license metric that will be used during reconciliation to determine how software rights are consumed.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option that excludes the custom product details from being shared with [Software Asset Management Content Service](../concept/c_SAMContentService.md) if opted in.

</td></tr></tbody>
</table>
**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)


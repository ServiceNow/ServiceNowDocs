---
title: Normalization statuses
description: Description of normalization statuses for discovery models.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Normalization statuses

Description of normalization statuses for discovery models.

When a discovery model is normalized, it is normalized to the version and full version. However, if the discovery model is partially normalized or publisher normalized, then the discovery model won't be updated to full version. If the discovery model is manually normalized, you can decide if you want it normalized to version and full version.

Normalization status can have six different results:

<table id="table_eg4_myc_cjb"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Normalized

</td><td>

A discovery model is fully normalized based on publisher, product, version fields. No fields are editable.Under specific conditions, certain fields that are typically read-only can be edited. If edited, the status changes to **Manually Normalized**.

 If only publisher and product fields are discovered, but the product type is Not Licensable, Child, Driver, or Patch, the status is **Normalized**.

</td></tr><tr><td>

Partially Normalized

</td><td>

A discovery model is partially normalized based on publisher and product fields only. In this case, the version field is editable and once that information is added the normalization status is changed to **Manually Normalized**.

</td></tr><tr><td>

Publisher Normalized

</td><td>

A discovery model that is partially normalized based on the publisher field alone. In this case, the version and product fields are editable, and once that information is added, the normalization status is changed to **Manually Normalized**.

</td></tr><tr><td>

Match Not Found

</td><td>

The normalization process could not match any of the three key fields of the discovery model with a rule in the Software Library. In this case, all key fields are editable and once the information is added the normalization status is changed to **Manually Normalized**.**Match Not Found** status could occur if a normalization rule for the software does not exist.

 For example, if the organization created custom software specific to the organization.

</td></tr><tr><td>

Manually Normalized

</td><td>

A discovery model is manually normalized when key fields in a **New**, **Match Not Found**, **Partially Normalized**, or **Publisher Normalized** discovery model are filled in manually.

</td></tr><tr><td>

New

</td><td>

The software discovery model has not yet run through the normalization process.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)


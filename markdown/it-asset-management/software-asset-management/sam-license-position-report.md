---
title: Software license compliance position
description: The Software Asset Management License Position report shows compliance details for each software model in a single list.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software license compliance position

The Software Asset Management License Position report shows compliance details for each software model in a single list.

You can view and export the software model compliance list for your environment to understand your license position.

Two license metric results are generated if a software model has two entitlements, one with a perpetual SA license type and the other with a subscription license type. One license metric result where active maintenance is true and the other where the active maintenance is false. In such a scenario, two license position reports are generated, one with active maintenance true and the other one with active maintenance false.

A single license position report is generated if there are any unlicensed installations. A single license position report is also generated if there are any unlicensed subscriptions. If both are present, two license position reports are generated.

![License compliance position report showing compliance details for each software model](../image/sw-license-compliance-position.png "License compliance position report")

<table id="table_jf1_vk2_cdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software publisher

</td><td>

Software publisher of the software model.

</td></tr><tr><td>

Software product

</td><td>

Software product of the software model.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td></tr><tr><td>

Software model status

</td><td>

Compliance status of the software model.-   Compliant \(indicated with a green dot\)
-   Not Compliant \(indicated with a red dot\)

</td></tr><tr><td>

License metric

</td><td>

License metric of the software model.

</td></tr><tr><td>

Total spend

</td><td>

Total cost of rights owned.

</td></tr><tr><td>

Rights owned

</td><td>

Sum of all active rights.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights allocated in use and not allocated in use.

</td></tr><tr><td>

Rights needed

</td><td>

Rights needed to cover the number of unlicensed installs.

</td></tr><tr><td>

Rights available

</td><td>

Rights owned less rights used.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Number of unlicensed software installations that are not covered by any entitlements.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the least number of rights needed.

</td></tr><tr><td>

Potential savings

</td><td>

Estimated savings from reclaiming unused installs.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Total cost of unused rights.

</td></tr><tr><td>

Software model

</td><td>

Software model name.

</td></tr></tbody>
</table>The License Position Report form also contains **Group** and **Subgroup** fields that specify the group and subgroup on which reconciliation was run.

**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)


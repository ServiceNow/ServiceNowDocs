---
title: Data center infrastructure allocation failure cases
description: Allocation failures occur when devices, rack constraints, or CMDB records don't meet the requirements for placement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-failure-cases.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Data center infrastructure allocation failure cases

Allocation failures occur when devices, rack constraints, or CMDB records don't meet the requirements for placement.

## Allocation failure cases

-   Each device listed in the request must exist as a hardware configuration item in the CMDB, with a matching equipment model record that includes a rack unit count. If any device or its equipment model is not found, the allocation fails. Work notes list which records are missing.
-   A write-back to the CMDB is blocked by a platform rule. In this case the run is reported as a failure even if a placement was found.
-   If no single rack can accommodate a device, the allocation fails even if the combined capacity across multiple racks is sufficient.
-   If splitting is not allowed and no single rack fits the full request, the allocation fails.
-   No rack units or devices are specified in the short description and description of the change request.
-   The placement policy can't be interpreted and the allocation can't proceed. A warning appears in the **Decisions** section of the work notes.
-   No rack — or combination of racks when splitting is allowed — can satisfy the rack unit, power, weight, contiguous space, or temperature constraints.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)


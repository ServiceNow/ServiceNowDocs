---
title: Map all OT devices within a subnet
description: An OT admin can trigger automated mapping of all OT devices within a selected subnet.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automatically map all OT devices, Automated mapping of OT devices to the Equipment Model, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Map all OT devices within a subnet

An OT admin can trigger automated mapping of all OT devices within a selected subnet.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_write

## Procedure

1.  Navigate to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Subnet Mapping**.

2.  From the OT Subnet Mapping list, open the OT subnet mapping record whose devices you want to map.

    **Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

3.  Ensure that the Site and Equipment Model Entity fields are correctly completed.

4.  Select the **Map OT devices in this subnet** UI Action to automatically map all OT devices in this site with IP addresses in the selected OT subnet.


## Result

If there are OT devices in the selected site with IP addresses that fall in the selected IP range, all devices in the site are mapped for the OT subnet. After the mapping is triggered, you can view the mapping results by selecting the link available in the information message from the list view.

**Parent Topic:**[Automatically map all OT devices to an equipment model entity](automatedly-map-all-ot-assets.md)


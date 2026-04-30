---
title: Automatically map all OT devices to an equipment model entity
description: An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated mapping of OT devices to the Equipment Model, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Automatically map all OT devices to an equipment model entity

An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_admin

## Procedure

1.  Navigate to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Subnet Mapping**.

2.  Select **Map all OT devices** to execute the Map OT Device flow.


## Result

OT devices are automatically mapped to the Equipment Model Entities listed on all active OT subnet mapping records. After the mapping is triggered, you can view the mapping results by selecting the link available in the information message from the list view.

**Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

-   **[Map all OT devices within a subnet](map-all-ot-assets-within-subnet.md)**  
An OT admin can trigger automated mapping of all OT devices within a selected subnet.

**Parent Topic:**[Automated mapping of OT devices to the Equipment Model](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


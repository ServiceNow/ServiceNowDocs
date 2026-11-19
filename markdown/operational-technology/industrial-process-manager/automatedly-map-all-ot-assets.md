---
title: Automatically map all OT devices to an equipment model entity
description: An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/industrial-process-manager/automatedly-map-all-ot-assets.html
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Automatically map all OT devices to an equipment model entity

An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/operational-technology-manager.md)
-   [Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_admin

## Procedure

1.  Navigate to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Subnet Mapping**.

2.  Select **Map all OT devices** to execute the Map OT Device flow.


## Result

OT devices are automatically mapped to the Equipment Model Entities listed on all active OT subnet mapping records. After the mapping is triggered, you can view the mapping results by selecting the link available in the information message from the list view.

**Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

-   **[Create a new OT subnet mapping record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/create-a-new-ot-subnet-mapping-record.md)**  
Create a new OT subnet mapping to associate with an equipment model entity.
-   **[Map all OT devices within a subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/map-all-ot-assets-within-subnet.md)**  
An OT admin can trigger automated mapping of all OT devices within a selected subnet.
-   **[Map OT devices to equipment model entities from the Equipment Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/map-ot-devices-in-iw.md)**  
Map Operational Technology \(OT\) devices to equipment model entities from the Equipment Model Manager in the Industrial Workspace.
-   **[Map an individual OT device to an equipment model entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/automatedly-map-ot-assets-to-isa-entities.md)**  
Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.

**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/automate-mappings-between-ot-assets-and-equipment-model-entity.md)


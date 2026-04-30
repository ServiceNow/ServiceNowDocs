---
title: Configure the OT Subnet Mapping scheduled flow
description: Configure the OT device mapping flow to automatically map OT devices to sites and equipment model entities.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Configure the OT Subnet Mapping scheduled flow

Configure the OT device mapping flow to automatically map OT devices to sites and equipment model entities.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: admin

## About this task

The OT device mapping flow can be set to run on a scheduled basis to automatically map OT devices for all active OT subnet mapping records.

## Procedure

1.  Navigate to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Subnet Mapping Scheduled Flow**.

2.  Activate site mapping:

    1.  Open the Set Flow Variables section.

    2.  Check the box next to **Run Auto Assign Site** and select **Save**.

3.  To schedule the flow to run on a regular basis, select the link in the Trigger section to define the interval.

4.  In the header, select **Activate** to activate the scheduled execution of the OT device mapping flow.

    After activation, this flow can run on a scheduled basis to automatically map OT devices for all active OT subnet mapping records on an instance.

    **Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.


**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


---
title: View OT subnet mappings
description: View all mapped OT subnets assigned to an equipment model entity.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# View OT subnet mappings

View all mapped OT subnets assigned to an equipment model entity.

## Before you begin

Roles required:

-   sn\_ot\_amazing\_write, cmdb\_ot\_isa\_editor, and cmdb\_ot\_viewer or
-   sn\_ot\_amazing\_admin, cmdb\_ot\_isa\_editor, and cmdb\_ot\_viewer

## Procedure

1.  Navigate to the Equipment Model Manager using one of these options:

    -   Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.
    -   Navigate to **All** &gt; **Industrial Workspace**. Select the Equipment model \(![image.equipment-model-manager-button]\) icon.
2.  From the Equipment model view, select the site, or expand the equipment model hierarchy to select the entity that you want to view mappings for.

3.  In the entity form, select the **Mapped OT subnets** related list tab.

    The mapped OT subnets show as active or inactive. Only active OT subnets will be included in the scheduled flow. For more information, see [Configure the OT Subnet Mapping scheduled flow](run-ot-subnet-mapping-scheduled-job.md).

4.  To view the OT subnets that are used for mapping at the OT device level, select the **OT Subnets** related list in an OT device record.


## What to do next

[Create a new OT subnet mapping record](create-a-new-ot-subnet-mapping-record.md)

**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


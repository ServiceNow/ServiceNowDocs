---
title: Assign the user criteria for Can Read access to a site
description: Assign the user criteria to a site to define which users can read or view the equipment model entities that belong to the selected site.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assign or remove access for non-admins, Configure, Industrial Process Manager, Operational Technology]
---

# Assign the user criteria for Can Read access to a site

Assign the user criteria to a site to define which users can read or view the equipment model entities that belong to the selected site.

## Before you begin

Role required: cmdb\_ot\_isa\_admin or admin

## About this task

You can assign the user criteria for Can Read access in two locations:

-   From the Equipment Model Entity View Access table
-   From the Can Read Equipment Models related list in a site record

## Procedure

1.  Navigate to either the table or related list.

    |Location|Navigation path|
    |--------|---------------|
    |**Equipment Model Entity View Access Table**|**All** &gt; **Equipment Model - ISA** &gt; **User Criteria - Can Read**|
    |**Can Read Equipment Models related list**|**All** &gt; **Equipment Model - ISA** &gt; **Sites** and open a site record. Select the Can Read Equipment Models related list.|

2.  Create a record by selecting **New**.

3.  In the **Site** field, select the equipment model site record that you need.

4.  In the **User Criteria** field, select the user criteria to define which users can read or view the selected site's equipment model entities.

    **Note:** If a user has the cmdb\_ot\_viewer role, the user can also view the Operational Technology \(OT\) devices that are assigned to the selected site.

    If a user has a cmdb\_ot\_editor role, the user can edit the OT devices that are assigned to the selected site.

5.  Select **Submit**.


**Parent Topic:**[Assign or remove equipment model site access for non-administrators](create-user-criteria-for-equipment-model-entity-site-users.md)


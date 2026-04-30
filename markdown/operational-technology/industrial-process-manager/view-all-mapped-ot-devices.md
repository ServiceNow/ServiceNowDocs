---
title: View all mapped OT devices
description: View a list of all the Operational Technology \(OT\) devices that are mapped to an equipment model entity.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# View all mapped OT devices

View a list of all the Operational Technology \(OT\) devices that are mapped to an equipment model entity.

## Before you begin

Role required: sn\_ot\_amazing\_write or sn\_ot\_amazing\_admin

## About this task

When you open a parent record in the CI Relationships table, you can view the Mapped OT Devices related list. The related list is a rolled up view that shows all the devices mapped with children ISA equipment model entities after you open the parent ISA equipment model entity. It contains the records that represent a mapping between an equipment model entity and a device.

## Procedure

1.  To view the mapped OT devices in the Industrial Workspace, complete the following actions.

    1.  Navigate to the Industrial Workspace.
    2.  Select the Equipment model \(![Equipment model icon in the Industrial Workspace to access the Equipment Model Manager](../../mftg-manufacturing-process-mgr/image/equip-model-manager-button.png)\) icon.
    3.  Open the equipment model entity that you want to view the mapped devices for.
    4.  Select the **Mapped OT Devices** tab.

        **Note:** The **Mapped Equipment Model Entity** column notes the equipment model entity that the device is mapped to. You can map a device to more than one equipment model entity.

2.  To view the mapped OT devices on the ServiceNow AI Platform, navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Mapped OT Devices**.

    This list contains all the devices that are mapped with different equipment model entities. The **Automates by :: Automates** CI relationship is applied to the parent and child entities.

    In this list, you can use the **Mapped Equipment Model Entity** column to identify the equipment model entity the device is mapped to. For more information on how to add a column to a list, see [Personalize a list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=zurich&pubname=zurich-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US).


**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


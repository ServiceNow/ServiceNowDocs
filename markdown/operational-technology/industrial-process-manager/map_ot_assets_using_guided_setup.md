---
title: Configure Automated Mapping of OT devices using guided setup
description: Use the Industrial Process Manager guided setup to automatically map OT devices to the ISA equipment model entity.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Configure Automated Mapping of OT devices using guided setup

Use the Industrial Process Manager guided setup to automatically map OT devices to the ISA equipment model entity.

## Before you begin

Role required: admin

## About this task

If you have the admin role, you can use the Industrial Process Manager Guided Setup to walk you through mapping OT devices to the ISA equipment model entity. You can map OT devices for the sites that you have access to.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup**.

2.  Select **Get Started** for the Industrial Process Manager application.

3.  Select the **Automatically Map OT Devices** task.

4.  Select the following task tabs, then select **Configure** to complete the configuration tasks.

<table><thead><tr><th align="left" id="d93188e103">

Task

</th><th align="left" id="d93188e106">

Purpose

</th></tr></thead><tbody><tr><td id="d93188e112">

**Import OT Subnets**

</td><td>

Upload a spreadsheet of OT subnets to import subnets from network management platforms.

</td></tr><tr><td id="d93188e121">

**Add Sites**

</td><td>

Add a site to each OT subnet so that OT devices with IP addresses matched with the OT subnet record can be mapped to that site automatically.

</td></tr><tr><td id="d93188e130">

**Add Equipment Model Entities**

</td><td>

Add an equipment model entity to the OT subnet record to automatically associate an OT device with the equipment model entity.

</td></tr><tr><td id="d93188e139">

**Select Discovery Source\(s\)**

</td><td>

Configure the following OT subnet-mapping system properties to limit the discovery sources that OT subnet mapping considers.-   sn\_otsm.map\_all\_ot\_devices.all\_discovery\_sources
-   sn\_otsm.map\_all\_ot\_devices.discovery\_sources


</td></tr><tr><td id="d93188e158">

**Test Mappings**

</td><td>

Validate assigned mappings of individual OT devices, individual OT subnets, multiple selected OT subnets, or all active OT subnets.

</td></tr><tr><td id="d93188e167">

**Activate and Schedule**

</td><td>

Activate the scheduled flows to run scheduled mapping of all OT devices regularly. There are two subflows that you can trigger individually:-   Subflow to assign sites to OT devices
-   subflow to map OT devices to a site


</td></tr></tbody>
</table>
**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)

**Related topics**  


[Guided Setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


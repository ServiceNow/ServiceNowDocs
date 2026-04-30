---
title: Automated mapping of OT devices to the Equipment Model
description: Automate mapping of OT devices to the production process.​
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Automated mapping of OT devices to the Equipment Model

Automate mapping of OT devices to the production process.​

When OT managers experience vulnerabilities or need to manage workflow involving OT devices, the context of how the OT device connects to the production process it automates is critical to prioritizing work. ​ ​Automatic mapping of OT devices to ISA equipment model entities enables the view of device-to-process relationships​.

**Note:** Only one subnet range per site is supported. Two different sites can have the same subnet; for example, 192.168.101.0/24. But multiple subnets of the same range are **not** supported for the same site. It is recommended that you use manual mapping in this scenario.

## Key benefits

-   Upload and store OT subnets from authoritative sources \(such as NetDB or Firewalls\) as records in a ServiceNow ​ instance.
-   Automate assignment of OT devices to ISA entity using IP addresses and OT subnet
-   Minimize issues with reuse of private IP address ranges across multiple sites​

Industrial networks use subnets to divide the private IP address space with a single subnet often aligned to a part of the production process, or the equipment model entity. For example: A canning line runs on a 192.168.101.0/24 network in which all the equipment was programmed by the integrator. The IPs used by the control systems, or OT devices, are often hard coded into the automation software used to run the line. If the subnet maps to the canning line in the Atlanta site, a manager can automatically map a detected PLC with IP 192.168.101.66 to the canning line.

The mapping feature relates each subnet to an equipment model entity, enabling you to automatically map OT devices to the subnets associated with the equipment model entity based on the IP address that was reported upon import from an OT Certified integration or ServiceNow® [Discovery for OT](../../mftg-manufacturing-oper-tech-mgr/concept/discovery-for-operational-technology.md).​

A system administrator can import OT subnet mapping records. An ISA administrator can automatically create mappings of subnets to equipment model entities through a scheduled job flow. An ISA Editor can manually create mappings of an individual OT device on-demand.

## Automated mapping feature personas

The automated mapping feature is aimed at the following personas.

<table id="table_ivx_4nv_xbc"><thead><tr><th>

Persona

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System Admin

</td><td>

The System Administrator performs these tasks:-   Imports data into the OT subnet to Equipment Model Entity Mapping table
-   Activates, schedules, or manually triggers the OT Subnet Mapping scheduled flow

</td></tr><tr><td>

ISA Admin

</td><td>

The ISA admin manually triggers the Map all OT devices UI action from the OT Subnet Mapping list view.

</td></tr><tr><td>

ISA Editor

</td><td>

The ISA editor performs these tasks:-   Manually creates and updates OT subnet mapping entries for specific sites
-   Maps individual OT devices to an equipment model entity from an OT device record
-   Maps multiple OT devices to an equipment model entity from an OT subnet mapping record

</td></tr></tbody>
</table>## Plugins

Enabling the mapping feature requires the following plugins:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

If the required plugins are installed, an ISA administrator can access the subnet mapping feature from the Industrial Process Manager application menu.

-   **[Workflow for the automated mapping feature](../concept/workflow-automated-dynamic-mapping-feature.md)**  
The Industrial Process Manager includes an automated flow for the automated mapping feature.
-   **[Configure Automated Mapping of OT devices using guided setup](map_ot_assets_using_guided_setup.md)**  
Use the Industrial Process Manager guided setup to automatically map OT devices to the ISA equipment model entity.
-   **[Automatically map all OT devices to an equipment model entity](automatedly-map-all-ot-assets.md)**  
An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.
-   **[View OT devices not assigned to a site](view-ot-devices-not-assigned-to-a-site.md)**  
View the list of Operational Technology \(OT\) devices that aren't assigned to a site.
-   **[View unmapped OT devices](view-unmapped-ot-devices.md)**  
View a list of Operational Technology \(OT\) devices with IP addresses that aren't mapped to any equipment model entity.
-   **[Map an individual OT device to an equipment model entity](automatedly-map-ot-assets-to-isa-entities.md)**  
Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.
-   **[Configure the OT Subnet Mapping scheduled flow](run-ot-subnet-mapping-scheduled-job.md)**  
Configure the OT device mapping flow to automatically map OT devices to sites and equipment model entities.
-   **[View OT subnet mappings](view-ot-subnet-to-equip-model-mappings.md)**  
View all mapped OT subnets assigned to an equipment model entity.
-   **[Create a new OT subnet mapping record](create-a-new-ot-subnet-mapping-record.md)**  
Create a new OT subnet mapping to associate with an equipment model entity.
-   **[View all mapped OT devices](view-all-mapped-ot-devices.md)**  
View a list of all the Operational Technology \(OT\) devices that are mapped to an equipment model entity.
-   **[System properties used by the OT subnet mapping feature](../reference/system-properties-used-by-automated-mapping-feature.md)**  
An Amazing Admin can view and configure the system properties that support the OT subnet mapping feature.
-   **[Automated mapping components installed when Industrial Process Manager and Operational Technology Manager are both installed](../reference/components-installed-with-manufacturing-process-manager-integration-with-operational-technology.md)**  
Several types of automated mapping components will be installed with activation of the Industrial Process Manager when Operational Technology Manager is also active, including tables, system properties, and scheduled flows.

**Parent Topic:**[Managing equipment models](../../mftg-manufacturing-process-mgr/task/managing-equipment-models-after-data-import.md)


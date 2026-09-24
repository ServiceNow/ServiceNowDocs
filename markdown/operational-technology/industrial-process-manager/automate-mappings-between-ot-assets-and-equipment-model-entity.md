---
title: Automated Mapping Across Zone-based IP Network Groups
description: Automate mapping of Operational Technology \(OT\) devices to the production process using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature.​
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/automate-mappings-between-ot-assets-and-equipment-model-entity.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Automated Mapping Across Zone-based IP Network Groups

Automate mapping of Operational Technology \(OT\) devices to the production process using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature.​

When OT managers experience vulnerabilities or must manage workflow involving OT devices, the context of how the OT device connects to the production process it automates is critical to prioritizing work. ​ ​Automatic mapping of OT devices to ISA equipment model entities enables the view of device-to-process relationships​.

**Note:** Only one subnet range according to site is supported. Two different sites can have the same subnet; for example, 192.168.101.0/24. But multiple subnets of the same range are **not** supported for the same site. It is recommended that you use manual mapping in this scenario.

## Key benefits

-   Upload and store OT subnets from authoritative sources \(such as NetDB or Firewalls\) as records in a ServiceNow ​ instance.
-   Automate assignment of OT devices to ISA entity using IP addresses and OT subnet.
-   Minimize issues with reuse of private IP address ranges across multiple sites​.
-   Use discovered subnets in copy-paste networks to help uniquely identify OT devices for mapping.

Industrial networks use subnets to divide private IP address space, with each subnet aligned to a production process or equipment entity. For example, a canning line runs on a 192.168.101.0/24 network where all equipment was programmed by the integrator. IPs for control systems and OT devices are hard-coded into the automation software. When the subnet maps to a canning line in the Atlanta site, detected PLCs with IPs like 192.168.101.66 are automatically mapped to that line.

The mapping feature relates each subnet to an equipment model entity. You can map OT devices to associated subnets based on imported IP addresses from OT-certified integrations or Discovery for Operational Technology.

## Types of mapping

The following types of mapping are supported in the AMAZING feature.

<table id="table_ugv_pp2_h3c"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Network

</td><td>

Subset of IP addresses in a subnet.**Note:** IP network mapping isn't supported in a copy-paste network.

</td></tr><tr><td>

IP Range

</td><td>

Entire subnet, in CIDR notation**Note:** IP range mapping isn't supported in a copy-paste network.

</td></tr><tr><td>

Discovered Subnet

</td><td>

Discovered subnet in your OT network.**Note:** Discovered subnet mapping is supported in a copy-paste network.

</td></tr></tbody>
</table>## Using discovered subnets to uniquely identify devices

Copy-paste networks create difficulty uniquely identifying OT devices and mapping them to equipment model entities. At some sites, the same IP subnet range applies to multiple equipment model entities, causing ambiguity about device mapping. Configure the discovered subnet to identify unique devices and their equipment model entities for more accurate mapping. By using discovered subnets with the AMAZING feature, you can uniquely identify OT devices in a copy-paste network. The logic is as follows:

1.  When OT device data is populated from a Service Graph Connector, the subnet and managed network must be populated in the IP Address \[cmdb\_ci\_ip\_address\] table using the **Netmask** and **Network partition identifier** fields. The **Network partition identifier** field is important to the mapping process because it's always unique to an OT device.
2.  The **Discovered subnet** and **Managed network** fields must also be populated in the OT device data for mapping to continue.

The AMAZING feature retrieves all configuration items \(CIs\) associated with a particular site. The IP address details, including the **Netmask** and **Network partition ID** fields, are obtained. Using the IP address details, the feature determines the discovered subnet then checks if the selected subnet and the managed network match the discovered subnet. If a match is found, the **Automated by :: Automates** relationship is established between the CI and the equipment model entity to effectively map the OT device to the correct entity.

The discovered subnets live in the OT Discovered Subnets \[sn\_ot\_discovered\_subnet\] table available with the Industrial Core. This table leverages the following attributes to help refine OT device mapping accuracy:

-   CIDR
-   Discovered Managed Network
-   Site

For more information about Industrial Core, see [Industrial Core plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/industrial-core-plugin.md).

You can also manually create a discovered subnet. For more information, see the [Create an OT discovered subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/create-ot-discovered-subnet.md).

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

-   [Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/operational-technology-manager.md)
-   [Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/industrial-process-manager-overview.md)
-   [Industrial Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/industrial-core-plugin.md)

If the required plugins are installed, an ISA administrator can access the subnet mapping feature from the Industrial Process Manager application menu on the ServiceNow AI Platform.

-   **[Workflow for the automated mapping feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/workflow-automated-dynamic-mapping-feature.md)**  
The Industrial Process Manager includes an automated flow for the automated mapping feature.
-   **[Configure Automated Mapping of OT devices using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/map_ot_assets_using_guided_setup.md)**  
Use the Industrial Process Manager guided setup to automatically map OT devices to the ISA equipment model entity.
-   **[Configure the OT Subnet Mapping scheduled flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/run-ot-subnet-mapping-scheduled-job.md)**  
Configure the OT device mapping flow to automatically map OT devices to sites and equipment model entities.
-   **[Automatically map all OT devices to an equipment model entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/automatedly-map-all-ot-assets.md)**  
An Operational Technology \(OT\) Amazing admin can trigger automated mapping of all OT devices to the appropriate ISA equipment model entity.
-   **[Create an OT discovered subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/create-ot-discovered-subnet.md)**  
Create an Operational Technology \(OT\) discovered subnet to use during OT subnet mapping to help identify OT devices and assign them to the correct equipment model entity.
-   **[View OT devices not assigned to a site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/view-ot-devices-not-assigned-to-a-site.md)**  
View the list of Operational Technology \(OT\) devices that aren't assigned to a site.
-   **[View unmapped OT devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/view-unmapped-ot-devices.md)**  
View a list of Operational Technology \(OT\) devices with IP addresses that aren't mapped to any equipment model entity.
-   **[View OT subnet mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/view-ot-subnet-to-equip-model-mappings.md)**  
View all mapped OT subnets assigned to an equipment model entity.
-   **[View all mapped OT devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/view-all-mapped-ot-devices.md)**  
View a list of all the Operational Technology \(OT\) devices that are mapped to an equipment model entity.

**Parent Topic:**[Managing equipment models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/managing-equipment-models-after-data-import.md)


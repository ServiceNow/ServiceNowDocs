---
title: Mapping Nokia Altiplano CIs and Relationships in CMDB
description: Use the Service Graph Connector for Nokia Altiplano to map discovered physical and logical network resources to telecom-aligned Configuration item \(CI\) classes in the CMDB. The connector supports consistent service modeling, visibility into chassis-level components, and automation of logical and physical relationships.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure Nokia Altiplano SGC, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Mapping Nokia Altiplano CIs and Relationships in CMDB

Use the Service Graph Connector for Nokia Altiplano to map discovered physical and logical network resources to telecom-aligned Configuration item \(CI\) classes in the CMDB. The connector supports consistent service modeling, visibility into chassis-level components, and automation of logical and physical relationships.

To confirm accurate CI classification and insertion, the connector uses the Robust Transform Engine \(RTE\) and Identification and Reconciliation Engine \(IRE\).

The connector classifies and relates discovered CIs using telecom-specific models based on device type, function, and chassis structure. This helps maintain a clean and normalized CMDB across vendors. Discovered model names from Nokia Altiplano are automatically transformed into ServiceNow standard model identifiers and categories for slot and subslot components.

## CI mapping and relationships

The following tables describe how Altiplano CIs are represented in the CMDB and how they relate to each other across physical and logical layers.

|CI Type|CMDB Table|Description and Relationships|
|-------|----------|-----------------------------|
|OLT CI|`cmdb_ci_optical_line_terminal`|Represents the OLT device. Contains Slot CIs and Logical Network Interface CIs.|
|ONU/ONT CI|`cmdb_ci_optical_network_terminal` or `cmdb_ci_optical_network_unit`|Represents ONU or ONT devices. The class is determined by the system property `sn_sgc_altiplano.onu_ci_class`. Contains Network Interface CIs.|
|Slot CI|`cmdb_ci_container_slot`|Represents main chassis slots. Contained by OLT CIs. Contains Interface Card CIs \(for example, LT/NT, PSU, fan\). Model transformations are applied in the data source. For more information, see the above-mentioned Model transformation for slot and subslot CIs table.|
|Subslot CI|`cmdb_ci_container_subslot`|Represents subcomponents within interface cards \(for example, cages for SFPs\). Contained by LT/NT cards. Contains transceiver card CIs. For more information, see the above-mentioned Model transformation for slot and subslot CIs table.|
|Interface Card CI|`cmdb_ci_interface_card`|Represents LT/NT cards, transceivers, and control units. Can contain subslots and network interfaces.|
|Network Interface CI|`cmdb_ci_ni_interface`|Represents both physical \(for example, PON, Ethernet\) and logical \(for example, VLAN\) ports. Contained by interface cards or ONU/ONT CIs. Logical ports are related to physical ports using Members::Member of.|
|Logical Connection CI|`cmdb_ci_ni_logical_path`|Represents logical paths such as PON or VLAN between OLT and ONU. Defined with Port A and Port Z attributes referencing terminating Network Interface CIs. VLAN paths consume PON paths.|
|IP Address CI|`cmdb_ci_ip_address`|Represents discovered IP addresses for OLTs. Owned by the corresponding OLT CI.|

## Key Relationship Examples

-   Containment relationships
    -   OLT CI → contains Slot CI
    -   Slot CI → contains Interface Card CI
    -   Interface Card CI → contains Subslot CI
    -   Subslot CI → contains transceiver Interface Card CI
    -   ONU/ONT CI → contains Network Interface CIs
-   Interface relationships:
    -   Logical Connections -&gt; terminated by Network Interfaces
    -   Network Interfaces -&gt; members of Network Interfaces
-   Logical path relationships:
    -   VLAN path \(parent\) → consumes → PON path \(child\)
    -   Logical paths → terminate at → Network Interface CIs via Port A and Port Z
-   Ownership: IP Address CI → owned by OLT device

## Supported models

1.  Network equipment models \(sn\_ent\_nw\_equipment\_model\)
    -   The supported OLT is Nokia Lightspan MF-2, by default the model name is Nokia MF-2
    -   ONU/ONT models are manufacturer + ONU/ONT. The system property sn\_sgc\_altiplano.onu\_ci\_class defines if ONU or ONT will be used.
    -   If the model wasn’t found in the model table, a new model is created in the CI, and the CI will be created as Network gear
2.  Equipment holder models: \(sn\_ent\_nw\_holder\_model\)
    -   Slots models: "Traffic Slot", "FAN Slot", "Power Slot"
    -   Subslots models: "SFP Subslot"
    -   The used model name can be customized by the customer through the Altiplano extension point \(sn\_sgc\_altiplano.AltiplanoCustomizedModels\)
    -   If the model wasn’t found in the model table, a new model is created in the CI.
3.  Network card models \(sn\_ent\_nw\_card\_model\)
    -   Card models are found by the model name, manufacturer, and model number discovered from the Altiplano API
    -   If the model wasn’t found in the model table, a new model is created in the CI.
4.  Network Interface Models: \(sn\_ent\_nw\_interface\_model\).
    -   Ethernet ports models are found by the "port bandwidth" column in the Network Interface table \(sn\_ent\_nw\_interface\_model\). the port bandwidth of the port CI is located by the discovered port speed in the Bandwidth table \(bandwidth\)
    -   PON physical ports models: PON Access Interface, PON Network Interfaces
    -   Logical ports models: ENET Interface, VLAN Interface, LAG Interface, PON Logical Interface
    -   If the model wasn’t found in the model table, the reference to the "Model ID" will remain empty.
5.  Logical network connection models \(sn\_ent\_logical\_nw\_connection\_model\)
    -   PON Access Path
    -   VLAN Path
    -   If the model wasn’t found in the model table, the reference to the Model ID will remain empty.

**Note:**

-   If the connector cannot match a discovered equipment to an existing model in the product model table the CI is created as `Network Gear` by default.
-   If demo data is installed, default models are created for OLT, ONU, ONT, Slots, Subslots, Cards, Network Interfaces, and Logical connections.
-   Equipment and Equipment holder model names can be customized using an extension point

## Model transformation for slot and subslot CIs

During ingestion, specific discovered model names are mapped to predefined CMDB model identifiers to confirm consistent slot categorization. The transformation logic is embedded in the SGC data source script and applies to the Nokia Altiplano source.

Slot components such as fan, power, and traffic slots are mapped to the `Slot` category in the CMDB. Subslot components such as SFP cages or synthetic subslots are mapped to the `Subslot` category in the CMDB.

|Source|Discovered Model Name|Target CMDB Model ID|Model Category|
|------|---------------------|--------------------|--------------|
|Altiplano|slot-fan|Fan Slot|Slot|
|Altiplano|slot-lt|Traffic Slot|Slot|
|Altiplano|cage|SFP Subslot|Subslot|
|Altiplano|slot-nt|Traffic Slot|Slot|
|Altiplano|synthetic nt-slot|SFP Subslot|Subslot|
|Altiplano|slot-psu|Power Slot|Slot|

## CI relationship structure

The following infographics describes the CI relationships.

![CI relationships structure](../images/ci-relationships.png)![CI relationship structure](../images/ci-relationship-diagram.png)

## Example: OLT to ONU Structure

The following structure enables end-to-end traceability from OLT through its hardware layers to the connected ONU and associated logical paths.

```
OLT (cmdb_ci_optical_line_terminal)
├── Slot
│   ├── Interface Card (LT/NT)
│   │   ├── Subslot
│   │   │   └── Interface Card (Transceiver)
│   │   │       └── Network Interface (PON port)
├── Logical Connections (PON/VLAN) → Connected to →
└── ONU/ONT (cmdb_ci_optical_network_terminal)
    └── Network Interface (ONT port)

```


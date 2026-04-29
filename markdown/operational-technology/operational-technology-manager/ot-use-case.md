---
title: Operational Technology and CSDM tables
description: Operational Technology manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Operational Technology.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Implementing the CSDM framework for Operational Technology, Configure, Operational Technology Manager, Operational Technology]
---

# Operational Technology and CSDM tables

Operational Technology manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Operational Technology.

## CSDM tables managed by Operational Technology

There are three primary categories of tables managed by Operational Technology \(OT\):

-   Operational Technology devices: Configuration items found on an OT \(ICS or PCN\) network.
-   ISA equipment model entity: Industrial process automated by OT devices.
-   OT system service: Creates other control systems, such as a distributed control system \(DCS\).

The numbers in this figure correspond to the CSDM tables managed by Incident Management.

![CSDM tables managed by Operational Technology Service Management.](../image/tables-used-by-ot.png)

## CSDM tables used by Operational Technology

1.  OT devices:
    1.  Configuration Item classes were created for Operational Technology hardware classes \(cmdb\_ci\_ot\) by extending hardware. See [Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for details.
    2.  Any CI Class \(any relevant existing hardware class as well as new OT classes can be designated as OT devices by adding OT device details using the OT Device Details \(cmdb\_ot\_entity\) reference to the cmdb\_ot\_entity table. OT Device Details include OT-specific characteristics like Purdue Level and OT device type.
    3.  OT device types describe the function of any CI that automates an industrial or production process. The cmdb\_ot\_entity\_type table describes these functions or roles.

        As shown here, a single OT device is represented by at least two records: one CI and one OT entity record. The device can contain six or more records in up to six tables \(for example, if the CI has more than one IP and MAC address\).

        ![OT table schema.](../image/ot-table-schema.png)

2.  Equipment model entities:
    1.  The equipment model entity class extends the Calculated Application Service and is used to:
        1.  Represent the site of any OT device or equipment model entity. A record in the Equipment Model Entity table \(cmdb\_ci\_ot\_isa\_entity\) without a parent is considered a site.
        2.  Represent the ISA equipment model entity for a part of the production process.
    2.  You can use equipment model templates \(isa\_entity\_template\) to further describe the relationships between equipment model entities found in an industrial environment.
        1.  Levels \(isa\_entity\_level\) describe the hierarchical level of the equipment model entity. For the default ISA-95 template, the levels shown here \(area, work center, and work units\) are included in the base system.
        2.  Level types \(isa\_entity\_type\) describe the type of process represented by the equipment model entities at a given level. For the default ISA-95 template, the types shown here \(process cell, production unit, production line, and storage zone\) are included in the base system.

            ![OT equipment model entity types.](../image/ot-equip-model-entity-types.png)

3.  OT system service:
    1.  The OT system service class extends the Calculated Application Service and is used to create the OT system service
    2.  The OT system service can then be associated with equipment model entities, technical services for software applications, and business offerings.
    3.  The OT system service can be related to the following items:
        -   OT devices that are part of the OT system service
        -   Equipment model entities that the OT system service manages

CSDM includes relationship types \(specific to Operational Technology\) that more accurately distinguish how OT devices and equipment model entities relate to each other:

-   **Producer for::Consumer of**: Describes the production process \(material flow\) between equipment model entities.
-   **Contains Element::Element of**: Describes the hierarchical relationship between equipment model entities.
-   **Automated by::Automates**: Describes the relationship between an OT device and an equipment model entity that the OT device automates.
-   **Detects::Detected by**: Describes which Network Intrusion Detection System \(NIDS\) class \(cmdb\_ci\_nids\) detected an OT device on an OT network.
-   **Owns::Owned by**: Describes the relationship when an OT Control Module is owned by an OT Control System \(PLC, DCS, and so on\)

The following dependency maps show the relationships between OT devices and equipment model entities:

![Contains Element::Element of — Describes the hierarchical relationship between equipment model entities.](../image/ot-element-elementof-relation.png)

![Producer for::Consumer of — Describes the production process material flow between equipment model entities.](../image/ot-producer-consumer-relation.png)

## Products that add value to Operational Technology

When you use OT with any of the following ServiceNow products, you increase the value you get from OT.

-   **Discovery for Operational Technology**

    Discovery for Operational Technology provides details about IT-classed hardware and software CIs and can be configured to provide additional OT device context like Purdue Level and Site on a per-OT schedule basis. Discovery for OT is part of the Operational Technology Manager product.

-   **Industrial Process Manager**

    When OT devices are assigned to an equipment model entity, **automated by::automates** relationships are created between them. This can be done manually in the Industrial Workspace or using the relationship between OT subnets and equipment model entities using the Automatic Mapping Across Zone-based IP Network Groups \(AMAZING\) feature in the OT Subnet Mapping menu item.

-   **Operational Technology Vulnerability Response**

    When vulnerable item \(VIT\) records are created by importing records from an OT-certified integration with a third-party security platform, OT devices are associated with the VIT. This enables both of the following capabilities:

    -   Risk calculation based on the criticality of the mapped equipment model entity.
    -   Assignment of VITs to the appropriate local team for remediation via site-based assignment groups.
-   **Operational Technology Incident Management**

    Incident Management for OT runs separately from IT for most OT devices. OT incident records enable site-based access and views to issues that are related to OT devices.

-   **Operational Technology Change Management**

    OT change requests enable changes to OT devices or industrial equipment configurations.

-   **Operational Technology Knowledge Management**

    Operational Technology Knowledge Management enables you to capture information about your OT system in knowledge articles that are related to OT incidents.

-   **Operational Technology Request Management**

    Enables you to access the OT Service Catalog to request OT catalog items and fulfill them based on the defined flows. OT workers can then create and submit an OT request from a catalog item, which helps provide a consistent experience and facilitates cross-functional requests.


## Products that benefit from Operational Technology

-   **IT Service Management \(ITSM\)**

    Services have the context of the site, production process, and OT devices, along with the information and technologies layered beneath them.

-   **Information Technology Operations Management \(ITOM\)**

    Understands the business context for the production processes along with the OT device hardware and software being managed.

-   **Security Operations**

    Understands the business context for the production processes as well as OT device hardware and software being secured.

-   **Governance, Risk, and Compliance \(GRC\)**

    Auditors can better leverage production process flows and related Information objects. This helps auditors understand the design-time data sensitivity for scoping audits, measuring risks, and managing audit activities.

-   **Asset Management**

    Manages the impact of the software and hardware life cycle process on the production processes.


**Parent Topic:**[Implementing the CSDM framework for Operational Technology](../concept/ot-use-case-product-view.md)


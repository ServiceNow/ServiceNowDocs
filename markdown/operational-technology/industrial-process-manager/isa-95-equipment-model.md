---
title: ISA-95 equipment model
description: The ISA-95 equipment model is an industry standard for organizing industrial facilities and their production equipment. Use it to define hierarchical equipment structures with distinct levels and type options at each level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/operational-technology/industrial-process-manager/isa-95-equipment-model.html
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# ISA-95 equipment model

The ISA-95 equipment model is an industry standard for organizing industrial facilities and their production equipment. Use it to define hierarchical equipment structures with distinct levels and type options at each level.

## ISA-95 standard

The ISA-95 equipment model represents an industry standard for describing industrial facilities and their production equipment. With this model, you can create a hierarchical structure that maps your equipment model entities and define different equipment types at each hierarchical level.

By applying an ISA-95 template, you can complete these tasks:

-   Map your equipment model entities and create a hierarchical structure.
-   Create multiple equipment models for multiple industrial sites.
-   Assign users to each site so you can manage their access to equipment model information for specific sites. For example, you can designate that users in Atlanta can access only the Atlanta site information but not the data for a site in Michigan. For more information, see [Manage equipment model site access for non-administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/industrial-process-manager/create-user-criteria-for-equipment-model-entity-site-users.md).

## Equipment model hierarchy

The ISA-95 equipment model consists of four hierarchical levels, starting at the site level. Each level represents a distinct organizational unit within your industrial facility:

|Level|Name|Description|
|-----|----|-----------|
|1|Site|A physical facility or plant.|
|2|Area|A sub-facility or department within a site.|
|3|Work Center|A section within an area.|
|4|Work Unit|A specific unit or section within a work center.|

Equipment model entity records are stored in the Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table.

## Work Center types

The Work Center level \(Level 3\) has four type options. Each type serves a specific function within your manufacturing facility:

-   **Process Cell**

    An area within a manufacturing facility dedicated to a particular stage of production. It includes all necessary equipment such as programmable logical controllers \(PLCs\), sensors, and actuators to automate and monitor processes. Process cell data is collected for control, quality monitoring, and diagnostics.

    **Example:** A robotic welding cell in an automotive factory.

-   **Production Unit**

    A group of process cells that perform related manufacturing operations. It coordinates process cell activities and manages material and data flow.

    **Example:** A car manufacturing plant production unit might include cells for welding, painting, assembling, and packaging.

-   **Production Line**

    A sequence of process cells or production units that manufacture a product from start to finish. It provides overall control and monitoring, and coordinates activities across all cells and units. It also manages the entire process from raw materials to finished goods.

    **Example:** An automotive assembly line where parts are assembled into a complete vehicle.

-   **Storage Zone**

    A designated area for storing raw materials, work-in-progress items, or finished goods. Inventory management systems maintain material flow and availability.

    **Example:** A warehouse for raw materials before production or finished goods awaiting shipment.


## Work Unit types

The Work Unit level \(Level 4\) has three type options. Work units exist beneath work centers and represent the most granular level in the equipment model:

-   **Unit**

    A generic work unit designation for operational purposes.

-   **Work Cell**

    A designated area where grouped machines and resources work together to complete a specific task or process efficiently.

-   **Storage Unit**

    A designated space or structure for keeping specific equipment, materials, or products.

    **Example:** A car manufacturing plant uses storage units for car paint, electrical accessories, and raw steel.


The following graphic shows the standard ISA-95 default template delivered when you install the Industrial Process Manager.

\[Omitted image "ot-equip-model-entity-types.png"\] Alt text: Equipment model entity example for the site Atlanta

**Parent Topic:**[Explore Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/industrial-process-manager/exploring-manufacturing-process-mgr.md)


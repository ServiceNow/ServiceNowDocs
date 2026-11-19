---
title: ISA-95 equipment model
description: The ISA-95 equipment model is an industry standard that represents an industrial facility and the production equipment in it. Describe the equipment model entities in your facilities by defining an equipment model template with different levels and level types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/industrial-process-manager/isa-95-equipment-model.html
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 3
breadcrumb: [Explore, Industrial Process Manager, Operational Technology]
---

# ISA-95 equipment model

The ISA-95 equipment model is an industry standard that represents an industrial facility and the production equipment in it. Describe the equipment model entities in your facilities by defining an equipment model template with different levels and level types.

With this template, you can:

-   Map your equipment model entities. With this map, you create a hierarchical structure.
-   Create multiple equipment models for multiple industrial sites.
-   Assign users to each site so that you can manage their access to the equipment model information for specific sites. For example, you can designate that users in Atlanta can access only the Atlanta site information but not the data for a site in Michigan. To learn more, see [Assign or remove equipment model site access for non-administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/create-user-criteria-for-equipment-model-entity-site-users.md).

The equipment models start at the site level and contain a detailed hierarchical structure that describes each industrial site. You can apply an equipment model template to structure this data in a hierarchical sequence.

Equipment model entity records are located in the Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table. For more information about managing your equipment model entity, see [Managing equipment models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/managing-equipment-models-after-data-import.md).

The following graphic shows the standard ISA-95 default template delivered when you install the Industrial Process Manager.

-   The subordinate levels under a site represent the door assembly area, its own subordinate work centers, and work units.

    A work cell is a designated area within a manufacturing facility where a group of resources are strategically arranged to work together and complete a specific task or process efficiently. A work center includes people, machinery, and equipment.

-   The Work Centers and Work Unit levels each have level types. In this model, there are four different level types for the Work Center level:
    -   Process Cell: An area within a manufacturing facility dedicated toward a particular stage of production. It includes all necessary equipment such as programmable logical controllers \(PLCs\), sensors, and actuators to automate and monitor processes. Process cell data is collected for control, quality monitoring, and diagnostics.

        For example, a robotic welding cell in an automotive factory.

    -   Production Unit: A group of process cells that perform related manufacturing operations. It coordinates process cell activities and manages material and data flow.

        For example, a car manufacturing plant production unit might include cells for welding, painting, assembling, and packaging.

    -   Production Line: A sequence of process cells or production units that manufacture a product from start to finish. It provides overall control and monitoring, and coordinates activities across all cells and units. It also manages the entire process from raw materials to finished goods.

        For example, an automotive assembly line where parts are assembled into a complete vehicle.

    -   Storage Zone: A designated area for storing raw materials, work-in-progress items, or finished goods. Inventory management systems maintain material flow and availability.

        For example, a warehouse for raw materials before production or finished goods awaiting shipment.

    -   Storage Unit: A designated space or structure for keeping specific equipment, materials, or products.

        For example, a car manufacturing plant uses storage units for car paint, electrical accessories, and raw steel.


\[Omitted image "ot-equip-model-entity-types-atlanta.png"\] Alt text: Equipment model entity example for the site Atlanta

**Parent Topic:**[Exploring Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-process-manager/exploring-manufacturing-process-mgr.md)


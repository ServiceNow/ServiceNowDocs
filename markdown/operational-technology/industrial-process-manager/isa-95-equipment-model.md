---
title: ISA-95 equipment model
description: The ISA-95 Equipment Model is an industry standard that represents an industrial facility and the production equipment in it. You can describe the Equipment Model entities in your facilities by defining an equipment model template that has different levels and level types.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Industrial Process Manager, Operational Technology]
---

# ISA-95 equipment model

The ISA-95 Equipment Model is an industry standard that represents an industrial facility and the production equipment in it. You can describe the Equipment Model entities in your facilities by defining an equipment model template that has different levels and level types.

With this template, you can do the following actions:

-   Map your equipment model entities. With this map, you create a hierarchical structure.
-   Create multiple equipment models for multiple industrial sites.
-   Assign users to each site so that you can manage their access to the equipment model information for specific sites. For example, you can designate that users in Atlanta can access only the Atlanta site information but not the data for a site in Michigan. To learn more, see [Assign or remove equipment model site access for non-administrators](../task/create-user-criteria-for-equipment-model-entity-site-users.md).

The equipment models start at the site level and contain a detailed hierarchical structure that describes each industrial site. You apply an equipment model template to structure this data in a hierarchical sequence.

The following graphic is an example of the standard ISA-95 default template that is delivered to you when you install the Industrial Process Manager. This graphic is a representation of a facility in Atlanta that manufactures cars.

-   The subordinate levels below a site represent the door assembly area, its own subordinate work centers, and work units.

    A work cell is a designated area within a manufacturing facility where a group of resources are strategically arranged to work together and complete a specific task or process efficiently. A work center includes people, machinery, and equipment.

-   The Work Centers and Work Unit levels each have level types. In this model, there are four different level types for the Work Center level:
    -   Process Cell: A process cell is a specific area within a manufacturing facility dedicated toward a particular stage of production. It includes all necessary equipment such as programmable logical controllers \(PLCs\), sensors, and actuators to automate and monitor processes. Process Cell data is collected for control, quality monitoring, and diagnostics.

        For example, a robotic welding cell in an automotive factory.

    -   Production Unit: A production unit is a group of process cells that work together to perform related manufacturing operations. In a production unit, you can coordinate the activities of process cells, manage material and data flow, optimize processes, and maintain quality.

        For example, in a car manufacturing plant, a production unit might include cells for welding, painting, assembling, and packaging.

    -   Production Line: A production line is a sequence of process cells or production units that manufacture a product from start to finish. A production line provides overall control and monitoring, coordinate activities of all cells and units, manage the entire process from raw materials to finished goods.

        For example, an automotive assembly line where parts are assembled into a complete vehicle.

    -   Storage Zone: A storage zone is a designated area for storing raw materials, work-in-progress items, or finished goods. A storage zone requires inventory management systems to maintain efficient material flow and availability.

        For example, a warehouse for storing raw materials before production or finished goods that are waiting for shipment.

    -   Storage Unit: A storage unit in an industrial site refers to a designated space or structure used for keeping specific equipment, materials, or products.

        For example, in a car manufacturing plant there are designated storage units to store car-paint, electrical accessories, and raw steel.


![Equipment model template example.](../image/equipment-model-template.png "Equipment model template example")

**Parent Topic:**[Exploring Industrial Process Manager](exploring-manufacturing-process-mgr.md)


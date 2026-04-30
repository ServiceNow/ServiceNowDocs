---
title: ISA-95 equipment model
description: The ISA-95 Equipment Model is an industry standard that represents an industrial facility and the production equipment in it. You can describe the Equipment Model entities in your facilities by defining an equipment model template with different levels and level types.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Explore, Industrial Process Manager, Operational Technology]
---

# ISA-95 equipment model

The ISA-95 Equipment Model is an industry standard that represents an industrial facility and the production equipment in it. You can describe the Equipment Model entities in your facilities by defining an equipment model template with different levels and level types.

With this template, you can do the following actions:

-   Map your equipment model entities. With this map, you create a hierarchical structure.
-   Create multiple equipment models for multiple industrial sites.
-   Assign users to each site so that you can manage their access to the equipment model information for specific sites. For example, you can designate that users in Atlanta can access only the Atlanta site information but not the data for a site in Michigan. To learn more, see [Assign or remove equipment model site access for non-administrators](../task/create-user-criteria-for-equipment-model-entity-site-users.md).

The equipment models start at the site level and contain a detailed hierarchical structure that describes each industrial site. You apply an equipment model template to structure this data in a hierarchical sequence.

The following graphic is an example of the standard ISA-95 default template that is delivered to you when you install the Industrial Process Manager. This graphic is a representation of a facility in Atlanta that manufactures cars.

-   The subordinate levels below a site represent the door assembly area, its own subordinate work centers, and work units.
-   The Work Centers and Work Unit levels each have level types. In this model, there are four different level types for the Work Center level:
    -   Process Cell
    -   Production Unit
    -   Production Line
    -   Storage Zone

![Equipment model template example.](../image/equipment-model-template.png "Equipment model template example")

**Parent Topic:**[Exploring Industrial Process Manager](exploring-manufacturing-process-mgr.md)


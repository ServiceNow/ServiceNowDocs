---
title: How CSDM concepts map to CMDB tables
description: The objects in the conceptual CSDM framework must map to the physical model objects \(CIs and CI class tables\) in the CMDB. You can navigate in the platform to see dictionary attributes.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# How CSDM concepts map to CMDB tables

The objects in the conceptual CSDM framework must map to the physical model objects \(CIs and CI class tables\) in the CMDB. You can navigate in the platform to see dictionary attributes.

![Conceptual-to-physical mapping CSDM to CMDB.](../image/csdm-data-to-table-mapping.png)

Business Application data belongs in the cmdb\_ci\_business\_app table, and not in the cmdb\_ci\_app table.

**Note:** Business services and Technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-portfolio-management/SPM2-taxonomy.md).

## Life Cycle Stage inheritance for Business Application records

Business Application records define a restricted set of Life Cycle Stage values that are intended to reflect application planning and usage, such as Ideation, Design, Operational, and End of Life. These life cycle definitions are configured using the life\_cycle\_control table specifically for the cmdb\_ci\_business\_application class. When you view or edit a Business Application record, however, additional Life Cycle Stage values such as Deploy and Inventory might also appear. These stages are not defined directly for Business Application, but are inherited from parent CI classes \(for example, cmdb\_ci\) through the aggregation-based inheritance model that is used by life\_cycle\_control. In this model, life cycle definitions from the current CI class are combined with life cycle definitions from all parent classes in the CMDB class hierarchy. Child classes therefore extend parent life cycle definitions rather than overriding them. As a result, Business Application records can display Life Cycle Stage values that are applicable to infrastructure or hardware CIs but might not be semantically meaningful for applications. This behavior is expected and working as designed.

In contrast, in sys\_choice inheritance definitions in child tables override the values in parent tables.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

**Related topics**  


[CSDM resources](../reference/csdm-resources.md)


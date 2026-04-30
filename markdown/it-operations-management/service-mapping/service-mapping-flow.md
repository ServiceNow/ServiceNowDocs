---
title: Service Mapping flow
description: Learn about high-level tasks users having different roles perform in Service Mapping.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 4
breadcrumb: [Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping flow

Learn about high-level tasks users having different roles perform in Service Mapping.

In Service Mapping, users collaborate to map, review, and monitor organization application services.

**Note:** For a complete list of Service Mapping roles, see [Components installed with Service Mapping](../reference/components-installed-with-service-mapping.md).

A typical Service Mapping workflow has the following stages:

1.  The administrator performs basic obligatory configurations to set up Service Mapping. See [Configuring Service Mapping](service-mapping-setup.md) for more details.
2.  The administrator maps organization application services in bulk. In addition, the administrator may map some application services individually. See [Map multiple application services suggested by classic Service Mapping](../task/map-business-services-in-bulk.md) for more information about mapping services in bulk.
3.  The administrator fixes application service errors in bulk, as described in [Fix application service errors in bulk](../task/fix-bus-serv-errors-by-category.md).
4.  The administrator reviews the results of the initial mapping, resolving errors in individual application services. See [Fix errors in individual application service maps](../task/fix-or-ignore-errors-business-service-map.md) for more details.
5.  The administrator sends fixed application services to the application service owner for review. See [Send application service maps for review](../task/send-business-service-for-review.md) for more information.
6.  The service instance owner checks that the service instance maps are complete and all major components comprising it are correctly represented. If necessary, the owner leaves comments, referred to as reject messages, on service instance maps for the Service Mapping administrator to implement. See [Review application service maps](../task/review-service-map.md).
7.  The administrator uses the feedback from the application service owner to fine-tune the application service maps, and then resends them to the owner for review. For more information about fine-tuning an application service map, see [Fine-tune application services to implement owner requests](../task/review-implement-business-service-maps.md).
8.  If the revised service instance maps are satisfactory, the service instance owner approves them. If not, the owner requests further fixes, which the administrator must address. See [Review application service maps](../task/review-service-map.md).
9.  The administrator finalizes the application services by configuring access and setting advanced attributes, such as criticality. To learn more, see [Application service completion](advanced-business-service-definitions.md).
10. After the service instance definition is complete, the Service Mapping user can view application service maps. To learn more about maintaining the application services using Service Mapping, see [Application service analysis and maintenance using classic Service Mapping](c_SvcPlanningAndAnalysisUsingMaps.md).

![Service Mapping flow](../image/SMMapFlow.png "Service Mapping flow")

In addition to these tasks, there may be a need to customize patterns that Service Mapping uses to discover devices and applications forming application services. Users must have the pd\_admin role to customize patterns. In the base system, the service\_mapping\_admin role contains the pd\_role. Customizing patterns requires basic knowledge of programming.

**Parent Topic:**[Exploring Service Mapping](service-mapping-get-started.md)

**Related topics**  


[Control user access to application services](../task/control-user-access-to-business-services.md)


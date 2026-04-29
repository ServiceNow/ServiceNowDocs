---
title: Review and approval of application service maps
description: After the Service Mapping administrator maps IT services and fixes errors in them, the administrator and the owner collaborate to review and approve the service maps. The review and approval process is available only for discovered and manually created service instances.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Review and approval of application service maps

After the Service Mapping administrator maps IT services and fixes errors in them, the administrator and the owner collaborate to review and approve the service maps. The review and approval process is available only for discovered and manually created service instances.

You must have Service Mapping enabled to map or review service instances.

Users who perform review and approval have the roles of a Service Mapping administrator and an Service Mapping administrator is responsible for mapping, fixing, and maintaining application services. The service instance owner checks that the service instance maps are complete and all major components comprising it are correctly represented. If necessary, the owner leaves comments, referred to as reject messages, on service instance maps for the Service Mapping administrator to implement.

The review and approval process is performed in the following stages:

1.  After the initial mapping of service instances, the administrator fixes errors and sends individual service instances for review. The system creates a service process task assigned to the service instance owner and sends an email notification about it.
2.  The service instance owner checks that the service instance maps are complete and all major components comprising it are correctly represented. If necessary, the owner leaves comments, referred to as reject messages, on service instance maps for the Service Mapping administrator to implement. The service process task assigned to the owner closes. The system sends an email notification to the administrator that the owner posted comments.
3.  The administrator receives the email notification, views owner requests and implements them.
4.  The administrator resends the service instance maps for review. The system again creates a service process task assigned to the service instance owner and sends an email notification about it.
5.  If the revised service instance maps are satisfactory, the service instance owner approves them. If not, the owner requests further fixes, which the administrator must address.

To see documentation for a review phase, click the relevant box in the diagram.

![Approval flow for individual application services](../image/ApproveBSFlow.png)

The process of application service review may take some time as it requires making changes and repeatedly running the mapping process on the application service. Typically, it takes several iterations to arrive at the desired result.

Once the owner approves an application service, the application service status changes to Approved and it appears in the list of completed application services on the **Home** page.

-   **[Send application service maps for review](send-business-service-for-review.md)**  
After you map an application service, send it to the application service owner for review to make sure that the map is accurate.
-   **[Review application service maps](review-service-map.md)**  
As the application service owner for the application service map, you receive an email notification that the application service map is assigned to you for review. Review mapping results for correctness and either provide your feedback or approve the application service map. The review and approval process is available only for discovered and manually created service instances.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)


---
title: Application service completion
description: After an application service is reviewed and approved, you can define attributes that enhance its discovery, reflect its importance, and control access to it.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service completion

After an application service is reviewed and approved, you can define attributes that enhance its discovery, reflect its importance, and control access to it.

There are several configurations you must perform to complete definition of an application service.

![Complete application service definition as part of the Service Mapping workflow](../image/SMMapFlowCompleteBS.png "Service Mapping workflow")

-   **[Define criticality for application services](../task/define-criticality-for-business-services.md)**  
For each service instance, select a criticality level that reflects how important it is to your organization operations.
-   **[Group application services](../task/organizing_services-into-groups.md)**  
Organize application services by groups to perform actions simultaneously on multiple services, and to control user access to services. You can use Event Management to track service health by service groups.
-   **[Control user access to application services](../task/control-user-access-to-business-services.md)**  
Assign user roles to service groups to grant users access to application services in your organization. Your organization may restrict access to some services for security or secrecy reasons.
-   **[Schedule a top-down discovery by Service Mapping](../task/t_CreateDiscoSchedForCITypes.md)**  
After Service Mapping discovers configuration items \(CIs\) belonging to your service instance for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs. For example, you may create custom discovery schedules to avoid redundant stress on the infrastructure.
-   **[Service definition transfer from one instance to another](transfer-service-definitions.md#)**  
Save time and effort by exporting definitions of service instances from the source instance and importing these definitions into the target instance. You can use this method to copy definitions of service instances only of the discovered type.

**Parent Topic:**[Application service mapping using classic Service Mapping](c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](../task/map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](../task/map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](../task/import-business-services-csv.md)

[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

[Fix application service errors in bulk](../task/fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](../task/fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](../task/business-service-approval.md)

[Fine-tune application services to implement owner requests](../task/review-implement-business-service-maps.md)

[Application service analysis and maintenance using classic Service Mapping](c_SvcPlanningAndAnalysisUsingMaps.md)


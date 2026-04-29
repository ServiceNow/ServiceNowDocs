---
title: Application service mapping using classic Service Mapping
description: You can perform initial mapping of multiple or single application services in your organization using a method that best suits you.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service mapping using classic Service Mapping

You can perform initial mapping of multiple or single application services in your organization using a method that best suits you.

You can map application services after you complete the Service Mapping setup.

![Initial mapping of business services as part of the Service Mapping workflow](../image/SMMapFlowDiscoverBulk.png "Service Mapping workflow")

A typical organization has hundreds of application services. Mapping each of them individually can be time and effort consuming. With Service Mapping, you can map most IT services in bulk. Mapping multiple application services at once is very effective, but is not precise. You may need to individually map application services omitted during bulk mapping.

A discovery method depends on how you have been managing your application services prior to mapping them and what information about them you gathered:

-   [Map multiple application services suggested by classic Service Mapping](../task/map-business-services-in-bulk.md)

    Service Mapping uses load balancers on your network to identify possible application services \(candidates\). You can map all or selected candidate in bulk, creating multiple application services in a single operation. This method suits your organization if you do not have much information about application services.

-   [Map application services using tags with classic Service Mapping](../task/map-service-tag.md)

    If your organization uses tags for asset management, you can use these tags to map service instances. Unlike other mapping methods, tag-based mapping does not require configuring credentials or providing users with elevated rights. You can effectively use tags to map multiple service instances.

-   [Map multiple application services from a CSV file using classic Service Mapping](../task/import-business-services-csv.md)

    This method suits you if your organization has performed cross-organization mapping and analysis and collected some information about planned service instances. If so, you can organize the collected information in a specific order and save it as a CSV file. Service Mapping extracts information from this file and creates potential service instances referred to as service candidates.

-   [Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

    You can map individual, single application services one by one by defining attributes for each service instance. Use this mapping method for application services Service Mapping cannot discover during bulk mapping. You must know or plan to find out application service attributes necessary for mapping.


-   **[Map multiple application services suggested by classic Service Mapping](../task/map-business-services-in-bulk.md)**  
You can map multiple application services identified and suggested by Service Mapping in a single operation. This method suits your organization if you do not have much information about application services.
-   **[Map application services using tags with classic Service Mapping](../task/map-service-tag.md)**  
Use tags that help categorize and organize configuration items \(CIs\) in your organization to map application services. Tag-based mapping doesn't require configuring credentials or providing users with elevated rights.
-   **[Map multiple application services from a CSV file using classic Service Mapping](../task/import-business-services-csv.md)**  
This method suits you if your organization has performed cross-organization mapping and analysis and collected some information about planned service instances. If so, you can organize the collected information in a specific order and save it as a CSV file. Service Mapping extracts information from this file and creates potential service instances referred to as service candidates.
-   **[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)**  
In addition to mapping application services in bulk, you can map individual, single application services by defining attributes for each application service. Use this mapping method if you already know or are planning to find out application service details. You must have Service Mapping enabled to map or review application services.
-   **[Fix application service errors in bulk](../task/fix-bus-serv-errors-by-category.md)**  
Service Mapping classifies errors by their root cause, for example, missing credentials or task timeout. For a fast and efficient process, fix errors belonging to the same category in bulk.
-   **[Fix errors in individual application service maps](../task/fix-or-ignore-errors-business-service-map.md)**  
You can address discovery issues in each application service map individually.
-   **[Review and approval of application service maps](../task/business-service-approval.md)**  
After the Service Mapping administrator maps IT services and fixes errors in them, the administrator and the owner collaborate to review and approve the service maps. The review and approval process is available only for discovered and manually created service instances.
-   **[Fine-tune application services to implement owner requests](../task/review-implement-business-service-maps.md)**  
As an administrator, you tweak and fine-tune maps based on comments from the application service owner.
-   **[Application service completion](advanced-business-service-definitions.md)**  
After an application service is reviewed and approved, you can define attributes that enhance its discovery, reflect its importance, and control access to it.
-   **[Application service analysis and maintenance using classic Service Mapping](c_SvcPlanningAndAnalysisUsingMaps.md)**  
Service Mapping creates maps to help you see the architecture and organization of application services. These maps are useful for planning change or migration, as well as analyzing the continuity and availability of services.

**Parent Topic:**[Using Service Mapping](using-service-mapping.md)


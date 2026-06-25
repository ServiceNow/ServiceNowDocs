---
title: Application service analysis and maintenance using classic Service Mapping
description: Service Mapping creates maps to help you see the architecture and organization of application services. These maps are useful for planning change or migration, as well as analyzing the continuity and availability of services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/c\_SvcPlanningAndAnalysisUsingMaps.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service analysis and maintenance using classic Service Mapping

Service Mapping creates maps to help you see the architecture and organization of application services. These maps are useful for planning change or migration, as well as analyzing the continuity and availability of services.

The maps are useful in the following cases:

-   **Planning the migration of an entire service instance or its segments**

    Use the map to see which configuration items \(CIs\) need relocating or which CIs become redundant.

-   **Planning the upgrade or replacement of a CI**

    Check the map to see what other CIs are affected when the CI is non-operational during maintenance. You can assess and plan the downtime or make provisions to avoid the downtime.

    Because the same CI may be used for multiple application services, check the CI using the Dependency Views application. With this application, you can see all application services that a CI belongs to.

-   **Analyzing a service instance for high availability and continuity**

    Use the map to identify CIs crucial for the service performance. Decide if you want to fortify these CIs by creating clusters.

-   **Troubleshooting application services**

    Use the map to understand the impact of an issue and determine which CI is causing the problem.


-   **[Application service maps in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_UndestandMaps.md)**  
Maps offer you a visualization of data on configuration items \(CIs\) comprising application services, and relations and connections between these CIs.
-   **[View CI attributes in an application service map in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_ViewCIDetails.md)**  
An application service map displays attributes for each configuration item \(CI\) that is part of the application service, as well as for the application service itself. The attributes come from the CMDB.
-   **[View CI connection attributes in an application service map in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/view-connector-properties.md)**  
You can view attributes of connections between configuration items \(CIs\).
-   **[View the change history of application services in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_ViewCIChanges.md)**  
You can view the changes made to an application service as a whole and to the individual configuration items \(CIs\) comprising the service. Change history is useful for maintenance, planning, or troubleshooting procedures.
-   **[Compare two versions of an application service in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CompareBS.md)**  
You can see a summary of application service changes at a glance by comparing two versions of an application service. This feature is useful for checking the application service status before and after a certain change or problem.
-   **[View dependent application services in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/view-linked-services.md)**  
Check which application services depend on an application service and open maps for dependent application services.
-   **[View contained application services in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/view-contained-services.md)**  
A contained application service is a reference included into another, dependent application service. You can open the contained service map directly from within the dependent service map.
-   **[Check CI dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CheckWhatBusinessServicesCIPartOf.md)**  
You can see if a particular configuration item \(CI\) is part of other application services and check if it depends on other CIs.
-   **[View the network or storage path in classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CheckNtwrkStrgPath.md)**  
You can drill down to see objects behind a connection on a map for troubleshooting service performance or maintaining your network. This feature is not available for manually created services or for services on instances using Edge Encryption.
-   **[View the list of CIs belonging to an application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/view-ci-list.md)**  
View a complete list of CIs that make up an application service, including CIs not shown on the application service map: tracked configuration files, endpoints, processes, and network devices.
-   **[Convert application service maps into PDFs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/convert-service-into-pdf.md)**  
You may want to create a PDF for a map to share information about the service content with other people. PDFs are especially useful during the review and approve process for application services discovered by Service Mapping.
-   **[Modify view for an application service map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/modify-map-view.md)**  
Customize a map view to display relevant information and increase clarity.

**Parent Topic:**[Application service mapping using classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping]()

[Map application services using tags with classic Service Mapping]()

[Map multiple application services from a CSV file using classic Service Mapping]()

[Map a single application service using classic Service Mapping]()

[Fix application service errors in bulk]()

[Fix errors in individual application service maps]()

[Review and approval of application service maps]()

[Fine-tune application services to implement owner requests]()

[Application service completion]()


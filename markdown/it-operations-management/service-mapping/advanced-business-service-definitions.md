---
title: Application service completion
description: After an application service is reviewed and approved, you can define attributes that enhance its discovery, reflect its importance, and control access to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/advanced-business-service-definitions.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service completion

After an application service is reviewed and approved, you can define attributes that enhance its discovery, reflect its importance, and control access to it.

There are several configurations you must perform to complete definition of an application service.

\[Omitted image "SMMapFlowCompleteBS.png"\] Alt text: Complete application service definition as part of the Service Mapping workflow

-   **[Define criticality for application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/define-criticality-for-business-services.md)**  
For each service instance, select a criticality level that reflects how important it is to your organization operations.
-   **[Group application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/organizing_services-into-groups.md)**  
Organize application services by groups to perform actions simultaneously on multiple services, and to control user access to services. You can use Event Management to track service health by service groups.
-   **[Control user access to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/control-user-access-to-business-services.md)**  
Assign user roles to service groups to grant users access to application services in your organization. Your organization may restrict access to some services for security or secrecy reasons.
-   **[Schedule a top-down discovery by Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CreateDiscoSchedForCITypes.md)**  
After Service Mapping discovers configuration items \(CIs\) belonging to your service instance for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs. For example, you may create custom discovery schedules to avoid redundant stress on the infrastructure.
-   **[Service definition transfer from one instance to another](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/transfer-service-definitions.md)**  
Save time and effort by exporting definitions of service instances from the source instance and importing these definitions into the target instance. You can use this method to copy definitions of service instances only of the discovered type.

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

[Application service analysis and maintenance using classic Service Mapping]()


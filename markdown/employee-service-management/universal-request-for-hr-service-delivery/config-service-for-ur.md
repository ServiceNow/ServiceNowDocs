---
title: Configure service to use Universal Request
description: Configure the Universal Request application with any service to manage requests across multiple services under one unified request. Using Universal Request integrated with your service helps deliver a seamless employee experience in your organization.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Configure service to use Universal Request

Configure the Universal Request application with any service to manage requests across multiple services under one unified request. Using Universal Request integrated with your service helps deliver a seamless employee experience in your organization.

-   **[Configure mappings](../task/ur-transfer-map-config.md)**  
Configure the target table and field mappings to create a department level ticket and to set the fields according to the field mappings.
-   **[Create a service set](../task/ur-create-service-set.md)**  
Create your service set \(department\) name in the Universal Request \(UR\) application to use the UR capabilities for a specific service set in your organization. Service sets are the various departments in your organization.
-   **[Create your service-specific assignment groups](../task/ur-create-grp-service.md)**  
Set up your service-specific groups and assign the necessary roles and users. The users in the group inherit the roles of the group, so you do not have to assign roles to each user separately.
-   **[Assign assignment group to service sets](../task/ur-assign-groups-service-set.md)**  
After creating your service-specific assignment groups, assign them to the service sets. Assigning assignment groups to the various departmental service sets facilitates in automatically routing universal requests to the right agents \(assignment group\) within a specific department \(service set\).
-   **[Create your service for Universal Request](../task/ur-register-service.md)**  
Register your service name for your service specific table and associate it with a service set \(department\) to use the Universal Request capabilities for a specific service in your organization.
-   **[Assign assignment group to your service](../task/assign-group-to-service.md)**  
After creating the services for your service set \(department\), assign the assignment groups to the services in the service sets to enable agents to transfer tickets to the appropriate routing group.
-   **[Create service specific UI actions](../task/ur-create-service-UIactions.md)**  
Create a UI action or modify an existing one to enable your service to create department tickets under a universal request.
-   **[Register application administration enabled scoped application](../task/ur-service-scoped-administration.md)**  
If your application is an application admin enabled scoped application, register the application with Universal Request \(UR\) to make your application’s service and service set data available for the Universal Request application to work.
-   **[Remove UR administrator role from system administrator](../task/remove-admin-role-ur.md)**  
To secure your information from undue access, after system configuration, ensure that only the Universal Request \(UR\) administrator \[sn\_uni\_req.ur\_admin\] role has access to sensitive information.
-   **[Create a business rule for your service](../task/ur-create-busrule-service.md)**  
Create a business rule on the service table to attach the newly created department ticket with a universal request.
-   **[Create a business rule to automatically create universal request](../task/ur-create-brule-omnichannel.md)**  
Create a before insert business rule on the service table to automatically create a universal request when a ticket is raised from any of the available channels.
-   **[Create extension points for departments](../task/create-extn-points-ur-service.md)**  
Create a scripted extension point to create your department specific primary ticket during cross-department ticket transfers. Using extension point enables you to create a primary ticket type as per the extension point definition.
-   **[Create an extension point for post-processing of transfers](../task/create-extension-points-ur-transfers.md)**  
Create a scripted extension point to perform additional actions after the cross-department transfer of a primary ticket in the Universal Request application. You can change the sample extension point to copy any additional information from the previous primary ticket's child entities.
-   **[Unified ticket experience setting](unified-ticket-experience.md)**  
Set up your service to provide your employees with a unified and consistent ticket experience. This setup automatically creates a universal request when requests are raised from an interaction record, email, or record producer.
-   **[Universal Request state mapping](../task/ur-state-mapping.md)**  
All workflows consist of states, transitions, and reasons. Map your service-specific states to the Universal Request states to provide a better user experience during request state transition.

**Parent Topic:**[Setting up and configuring Universal Request](setup-configure-ur.md)


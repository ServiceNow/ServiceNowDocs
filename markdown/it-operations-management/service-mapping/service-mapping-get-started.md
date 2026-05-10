---
title: Exploring Service Mapping
description: Service Mapping discovers all service instances in your organization and builds a comprehensive map of all devices, applications, and configuration profiles used in these service instances.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Mapping, ITOM Visibility, IT Operations Management]
---

# Exploring Service Mapping

Service Mapping discovers all service instances in your organization and builds a comprehensive map of all devices, applications, and configuration profiles used in these service instances.

Video: Service Mapping Overview

This video provides an overview of Service Mapping on the ServiceNow AI Platform.

## Who uses Service Mapping

Service Mapping enables IT departments of companies, organizations, and cloud companies providing platform as a service to create a service-aware view of infrastructure.

## How do you use Service Mapping

A service instance is a set of interconnected applications and hosts that are configured to offer a service to the organization. Service instances can be internal, like an organization email system or customer-facing, like an organization website. For example, creating financial reports through a web-based application requires a computer, web server, application server, databases, middleware, and network infrastructure. These applications and hosts are all configured to offer the service of financial reporting.

Typically, IT departments create and maintain an inventory that treats devices and applications as standalone, independent objects. Connections between the devices and applications are not included. This is usually referred to as horizontal discovery. This method does not address the biggest challenge for IT departments, which is understanding the connection and dependencies between each object.

Service Mapping maps dependencies, based on a connection between devices and applications. This method is referred to as top-down mapping. The top-down mapping helps you immediately see the impact of a problematic object on the rest of the service instance operation.

![Comparison of horizontal and top-down mapping results](../image/horizontal-top-down-comparison.png "Comparison of horizontal and top-down mapping results")

Service instance maps show infrastructure objects and semantic connections between them. Service Mapping regenerates service instance maps regularly, to keep them updated and relevant. Any faulty objects are shown along with the devices and applications they affect, providing a visual clue of the state of the service instance.

## How does Service Mapping work

Service Mapping can deploy different methods for creating application services. The main method of Service Mapping discovering and mapping devices and applications is using patterns. A pattern is a sequence of operations whose purpose is to detect attributes of devices and applications and their outbound connections. If your organization uses tags for asset management, you can use these tags to map service instances. Service Mapping can also discover devices and applications by following traffic connections between them. This method is referred to as traffic-based mapping. For more information, see [Choose the right method for discovery and mapping application services](choose-mapping-method.md).

## What to know before you begin

You can use Service Mapping only if the Discovery product is activated and set up.

You must define users and configure credentials to allow Service Mapping and Discovery access to applications and devices inside your organization network. For more information, see [Configuring Service Mapping](service-mapping-setup.md).

## Service Mapping on the ServiceNow AI Platform

Service Mapping relies on Discovery and the MID Server to discover devices and applications. Service Mapping uses results of horizontal discovery performed by Discovery. The MID Server facilitates communication between Service Mapping and devices and applications it discovers.

Data collected and organized by Service Mapping is visible in Event Management, Dependency Views, and Application Portfolio Management \(APM\). With Event Management, you can view events to take actions for recovering your organization application services. Dependency Views shows relationships between devices and applications in the context of application services they belong to. When integrated with APM, Service Mapping provides information about components making up a business application and helps APM users to monitor business application performance.

Service Mapping supports domain separation. If your ServiceNow AI Platform uses domain separation, administrators and users can only see and manage application services belonging to their own domain.

To view a list of Service Mapping plugin dependencies, see [Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md).

-   **[Choose the right method for discovery and mapping application services](choose-mapping-method.md)**  
Service Mapping deploys different methods for collecting information about configuration items \(CIs\) and organizing them into application services. The available mapping methods are: pattern-based, tag-based, traffic-based, and discovery based on Predictive Intelligence. Learn about the mapping methods to use the ones that best suit the needs of your organization.
-   **[Discovery of application services on cloud using Service Mapping](cloud-discovery-service-mapping.md)**  
Service Mapping in cloud environments provides critical visibility into application dependencies and connections. By identifying how different application components interact within IaaS and PaaS environments, your organization can gain better insight into its application services and improve overall service management.
-   **[Service Mapping flow](service-mapping-flow.md)**  
Learn about high-level tasks users having different roles perform in Service Mapping.
-   **[Traversal rules in Service Mapping](traversal-rules-service-mapping.md)**  
Traversal rules identify and map relationships between configuration items to create comprehensive application service maps. They connect relevant configuration items based on predefined relationships, promoting accurate service mapping and visualization.

**Parent Topic:**[Service Mapping](../reference/c_ServiceMappingOverview.md)

**Related topics**  


[Service instances \(Application services\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md)

[Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md)

[Event Management](../../event-management/concept/c_EM.md)

[Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/c_BusinesssServiceManagementMaps.md)


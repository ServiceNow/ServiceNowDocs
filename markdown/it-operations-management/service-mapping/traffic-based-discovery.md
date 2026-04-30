---
title: Traffic-based discovery in Service Mapping
description: Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-07-30"
reading_time_minutes: 7
breadcrumb: [Choose the right method for discovery and mapping application services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Traffic-based discovery in Service Mapping

Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping.

## What is traffic-based mapping

Traffic-based mapping can be seen as an enhancement to pattern-based mapping. While pattern-based mapping relies on predefined rules and patterns to identify connections, traffic-based mapping analyzes network traffic to automatically discover connections between CIs in your environment. This approach allows Service Mapping to find those CIs not discovered using patterns alone.

Depending on your configuration, the behavior of traffic-based discovery can vary. If Predictive Intelligence is enabled, Service Mapping automatically adds connections to service instances based on connection rules. These suggestions are generated using traffic-related data from the Configuration Management Database \(CMDB\) and the analysis of application fingerprints, CIs, and processes by Predictive Intelligence.

If discovery based on Predictive Intelligence isn't enabled, Service Mapping automatically adds traffic-based connections using data from the CMDB to the service instances. However, to keep your service instances well-organized, you might need to manually remove connections to irrelevant CIs.

Typically, if the connection suggestions feature is turned off, you use traffic-based discovery at the initial stages of discovering application services. To maintain a clean, organized service map, you can opt to turn off traffic-based discovery after you have completed the discovery and fine-tuning of your application services. For more information, see [Fine-tune application services to implement owner requests](../task/review-implement-business-service-maps.md).

Connections created only through traffic-based discovery aren’t removed. However, if pattern-based discovery runs after traffic-based discovery has run, it might create duplicate connections between CIs. To avoid duplicates, the system removes any connections that were created by traffic-based discovery if they’re also created by pattern-based discovery.

## Traffic-related data from the CMDB

The system uses commands and network flow logs to collect traffic-related data and saves it in the CMDB tables. Service Mapping retrieves this data from the tables to detect CI inbound and outbound connections.

|Table|Source|Used by Service Mapping to|
|-----|------|--------------------------|
|Flow Connector \[sa\_flow\_connection\]|Netflow and VPC logs|Discover dependencies, add connections during top-down discovery.|
|Flow Services IP/Port and Statistics \[sa\_flow\_service\]|Netflow and VPC logs|Discover all services listening on ports. In a base system, Service Mapping does not use data from this table.|
|Flow Server Communication \[sa\_flow\_server\_comm\]|Netflow and VPC logs|Discover services communicating to other services. In a base system, Service Mapping does not use data from this table.|
|TCP Connection \[cmdb\_tcp\]|netstat and lsof commands|Discover connections during top-down discovery.|

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. To enhance traffic-based discovery, you can configure Service Mapping to collect data from Netflow and VPC logs. Service Mapping also accesses the TCP connection data collected by improved Application Dependency Mapping \(ADM\), which Discovery performs as part of horizontal discovery. See [Application Dependency Mapping \(ADM\) for Discovery](../../discovery/reference/r_ApplicationDependencyMapping.md#) to learn more about this process.

## Enabling traffic-based discovery in the system

Traffic-based discovery using commands is available in Service Mapping for use at any level. You can enable it at different levels ranging from the most global to the most specific. For more information, see [Enable traffic-based discovery for an application service](../task/enable-traffic-based-discovery-business-service.md).

-   **Product level**

    By default, traffic-based discovery in Service Mapping is turned off. The **Traffic based discovery** \(**sa.traffic\_based\_discovery.active**\) property controls traffic-based discovery at this level. Enabling traffic-based discovery at the product level facilitates the discovery of all CIs in your environment. However, more specific rules at the service instance, CI type, or specific CI levels can override these settings.

    **Important:** You can’t enable traffic-based discovery at other levels unless it’s enabled at the product level.

    The connection suggestions feature works at the product level. The **sa\_ml.connection\_suggestions.active** property controls this feature. If you enabled traffic-based discovery before the Quebec release and used it to discover at least one application service, the connection suggestions feature is turned off by default.

-   **Service instance level**

    You can enable traffic-based discovery for an individual service instance. In this case, Service Mapping uses traffic-based discovery for all CIs that make up this service instance. However, if traffic-based discovery is turned off for some CI types or specific CIs, those CIs aren’t discovered using this method, even if the service instance is set to use traffic-based discovery.

    For example, you enable traffic-based discovery for a specific service instance that includes a Tomcat server, a MySQL database, and a web application. Service Mapping uses traffic-based discovery to discover the Tomcat server, the MySQL database, and the web application.

-   **CI type level**

    You can create a discovery rule to include or exclude a CI type from traffic-based discovery. This rule takes precedence over the setting that you choose for an individual service instance.

    For example, you enable traffic-based discovery for a specific service instance that includes a Tomcat server, a MySQL database, and a web application. You create a CI type rule that excludes all Tomcat servers from traffic-based discovery. Service Mapping uses traffic-based discovery to discover the MySQL database and the web application since there are no rules to exclude them.

-   **Specific CI level**

    You can create a discovery rule to include or exclude a specific CI type from traffic-based discovery. This rule takes precedence over the setting that you choose for an individual service instance or any rules for CI types.

    For example, you enable traffic-based discovery for a specific service instance that includes a Tomcat server, a MySQL database, and a web application. You create a CI type rule that excludes all Tomcat servers from traffic-based discovery. However, you also create a discovery rule enabling traffic-based discovery for a specific Tomcat server. Service Mapping uses traffic-based discovery to discover the MySQL database, the web application, and that specific Tomcat despite the CI type rule excluding all Tomcat servers.

    See [Enable traffic-based discovery for CI types or specific CIs](../task/t_CreateATrafficBasedDiscoveryRule.md) to learn more about creating rules for CI types or specific CIs.


**Related topics**  


[Pattern-based discovery in Service Mapping](pattern-based-discovery.md)

[Add or remove CIs for multiple application services using connection suggestions](../task/manipulate-connections-suggestions-in-bulk.md)

[Add or remove CIs for single application services using connection suggestions](../task/add-remove-ci-connections-services.md)

[Remove CIs not belonging to application services](../task/remove-cis-not-belonging-business-services.md)

[Data collection and discovery using Netflow](data-collection-netflow-mapping.md)

[Data collection and discovery using VPC Flow Logs](data-collection-vpc-mapping.md)


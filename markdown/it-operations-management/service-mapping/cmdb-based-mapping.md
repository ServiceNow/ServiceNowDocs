---
title: CMDB-based mapping
description: Using data stored in the Configuration Management Database \(CMDB\), you can run top-down discovery and map your organization's application services without having to access a MID Server.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# CMDB-based mapping

Using data stored in the Configuration Management Database \(CMDB\), you can run top-down discovery and map your organization's application services without having to access a MID Server.

Top-down discovery begins with an IP address and retrieves the associated host. It then tries to locate an available MID Server. If a MID Server isn’t available and CMDB-based mapping is active, it is initiated. This feature uses incoming traffic already registered in the CMDB to pinpoint the target process running on an identified IP address and searches for an application linked to it. The application is then mapped as a node on the service map.

If an application isn’t identified, CMDB-based mapping uses Application Dependency Mapping \(ADM\) logic to classify and create an application linked to the target process within the CMDB.

If ADM is unable to classify the application, it creates a simple application in the Application \[cmdb\_ci\_appl\] table in the CMDB. For more information, see [Application Dependency Mapping \(ADM\) for Discovery](../../discovery/reference/r_ApplicationDependencyMapping.md#).

For information on configuring Service Mapping for CMDB-based mapping, see [Configure Service Mapping to work with the Configuration Management Database \(CMDB\)](../task/map-app-services-with-cmdb.md).


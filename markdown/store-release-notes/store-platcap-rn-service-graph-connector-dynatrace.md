---
title: Service Graph Connector for Observability - Dynatrace release notes
description: Version history for the Service Graph Connector for Observability - Dynatrace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-dynatrace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Observability - Dynatrace release notes

Version history for the Service Graph Connector for Observability - Dynatrace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.15.0 - June 2026**
    -   Changed:
        -   Enhanced CMDB data quality with richer host attributes, such as MAC address, serial number, manufacturer, model, CPU, OS version, and virtualization flag, improving reconciliation and reducing duplicates.
        -   Standardized process naming for MSSQL, NGINX, WebSphere, and Apache for better reconciliation with Application CIs discovered from other sources.
        -   Introduced a new extensibility framework for enriching process metadata from Dynatrace. Enriched the data populated for WebSphere CIs with cell and node values.
        -   Fixed duplicate Application CIs on Windows via path normalization.
        -   Added AWS RDS Cloud Database and Service relationships.
        -   Renamed the connector to Dynatrace Classic in the SGC Central Create Connection UI.
-   **Version 1.14.1 - March 2026**
    -   Changed:
        -   Updated the logic for the normalization of process paths, parameters, and command-line argument values for Windows processes to be with consistent with the processing logic for Linux processes.
        -   Established VM-to-server relationships for Azure VMs.
        -   Added unique environment values to the service name to prevent service record flapping.
        -   Added support for classifying Solaris servers.
-   **Version 1.13.1 - September 2025**
    -   Fixed:
        -   Addressed errors caused by payloads larger than 32 MB.
        -   Added missing tags for Kubernetes data.
        -   Bug fixes and other minor improvements.
-   **Version 1.13.0 - August 2025**
    -   New:
        -   Added support for setting up OAuth connection for Grail-enabled tenant from SGC Central for logs and metrics ingestion.
        -   Added support for ingestion of Custom Application from Dynatrace.
        -   Additional mapping for Docker Images with the inclusion of Name, Image ID, and Image Digest information.
        -   Added relationships between Docker Image and Docker Container, and Docker Container and Host.
    -   Changed:
        -   Prior to this release, all service types, except DATABASE\_SERVICE, are mapped to cmdb\_ci\_service\_calculated. DATABASE\_SERVICE is mapped to Database Instance. Beginning with the v1.13 release, all service types are mapped to cmdb\_ci\_service\_calculated.
        -   The install status of the Docker Container is now determined based on the value of the properties.containerStatus.state field in the incoming payload.
        -   Updated the AWS EC2 instance mapping to use the host entityId to ensure accurate relationship creation with the Host CI from the SGO-Dynatrace Hosts data source, thereby avoiding duplicate Host CI insertion.
-   **Version 1.12.0 - May 2025**
    -   New:
        -   Support for setting up and monitoring connections using SGC Central.
        -   New property \(sn\_dynatrace\_integ.saveRESTResponseAsAttachment\) to save the response from Dynatrace as an attachment with a .json extension.
        -   Optimized REST API calls for efficient data retrieval.
        -   Support for discovering new cloud elements:
            -   Azure: Scale sets VM, CosmosDB, RDS, SQL Server, Function App.
            -   AWS: S3 Bucket, DynamoDB, RDS, Lambda Functions.
    -   Fixed: PRB1843990: Issue with importing Kubernetes data and other entities with a larger payload.
-   **Version 1.11.0 - December 2024**
    -   New:
        -   Added a property \(sn\_dynatrace\_integ.createUnmatchedApplicationCIs\) to insert unclassified applications into the cmdb\_ci\_appl table.
        -   Added ability to discover new cloud elements:
            -   Azure: Service Account, Data Center, Virtual Machine, Load Balancer, Storage Account
            -   AWS: Service Account, Data Center, EC2, Load Balancer
        -   Added ability to discover new Kubernetes elements:
            -   Namespace
            -   Node
            -   Pod
            -   Container
            -   Services
-   **Version 1.10.0 - August 2024**
    -   New:
        -   Implemented application classification into the proper configuration management database \(CMDB\) class.
        -   Added discovery capabilities to include Kubernetes clusters, nodes, namespaces, pods, Docker containers, and services.
-   **Version 1.9.0 - March 2024**
    -   New: Adopt new V2 APIs of Dynatrace.
    -   Fixed:
        -   Fixed impact calculation getting executed multiple times for the same Service
        -   Menus intended for admin users in the application navigator will no longer appear for non-admin users
-   **Version 1.8.0 - September 2023**
    -   New: Support for the common connection framework
    -   Fixed:
        -   Added the connectionAliasSysId parameter in the flow designer actions
        -   Fixed the relationship between the process group and calculated services
        -   Mapped the correct source native key \(SNK\) in the class mapping for Configuration Item 2 - To Service
        -   Populated Metric data in a multi-instance setup
        -   The Impact Rule \[em\_impact\_rule\] will not be created if it doesn't exist in the service
-   **Version 1.7.1 - March 2023**

    Fixed: Update the library path.

-   **Version 1.6.7 - August 2022**
    -   New:
        -   Add support for multi-instance
        -   Add property to conditionally bring in running processes
        -   Allow adding events with no matching CI
    -   Fixed:
        -   Invalid groups have been created that start with "-APPLICATION".
        -   Problem Notification setup displays an error.
-   **Version 1.4.0 - May 2022**

    Changed: Move the left navigation items of Dynatrace to the Integration Commons Service Graph Connectors navigation menu.

-   **Version 1.3.0 - November 2021**

    Changed: Removed the dependency on Observability Commons. This allows customers without Event Management to install and use this integration without the event ingestion feature.

-   **Version 1.2.1 - September 2021**
    -   The Service Graph Connector for Observability - Dynatrace imports the following type of data from Dynatrace to ServiceNow CMDB:
        -   Hosts
        -   Processes
        -   Services
        -   Applications
    -   A Service Map is created using the relationship between various applications, application services and infrastructure elements.


---
title: ITOM Visibility and CSDM reference
description: ITOM Visibility consists of two ServiceNow products: Discovery and Service Mapping. These products are responsible for creating Configuration Items \(CIs\) in the CMDB and relating them. The goal of this product view is to help you to understand how ITOM Visibility works with the core CSDM framework.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# ITOM Visibility and CSDM reference

ITOM Visibility consists of two ServiceNow products: Discovery and Service Mapping. These products are responsible for creating Configuration Items \(CIs\) in the CMDB and relating them. The goal of this product view is to help you to understand how ITOM Visibility works with the core CSDM framework.

## Aspects of ITOM Visibility

-   **Discovery**

    Discovery finds computers, servers, printers, a variety of IP-enabled devices, and the applications that run on them. It can then update the CIs in your CMDB with the collected data.

-   **Service Mapping**

    Service Mapping discovers all application services in your organization and builds a comprehensive map of all devices, applications, and configuration profiles that support the associated business services.

    Service Mapping maps dependencies based on the connections between devices and applications. This method, called top-down mapping, helps you immediately see the impact of a problematic object on the rest of the application services.


## Implementing CMDB data

For details on implementing CMDB data to conform with the CSDM framework, see [Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md).

## For more information

[Exploring the CSDM model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-exploring.md).

[Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md).

[Discovery basics](../../discovery/concept/c_GetStartedWithDiscovery.md).

[Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md).

-   **[ITOM Visibility and CMDB tables](../reference/itom-visibility-use-case.md)**  
ITOM Visibility manages and uses CMDB tables. Several ServiceNow products benefit from and add value to ITOM Visibility.
-   **[ITOM Visibility use case](itom-visibility-use-case-example.md)**  
The ITOM Visibility use cases are described in this section.
-   **[ITOM Visibility considerations for CSDM framework](itom-visibility-use-case-trouble.md)**  
Consider these points while implementing the CSDM framework.

**Parent Topic:**[ITOM Visibility reference](../reference/visibility-reference.md)


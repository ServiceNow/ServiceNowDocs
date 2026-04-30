---
title: Problem Management considerations
description: Consider these points while implementing the CSDM framework.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Problem Management product view, Applying CSDM guidelines to your product, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Problem Management considerations

Consider these points while implementing the CSDM framework.

-   Application Service: An application service is a service type that is a logical representation of a deployed application stack.
-   Using application service for a problem: Some of the scenarios where the application service can be used for a problem include:
    -   The problem is for an application issue: In this scenario the application service may be populated in the configuration\_item attribute on the Problem form representing the unique deployment of an application stack. For example, the application service of MyApp 3.0 Prod has been reported as being unavailable.
    -   The problem on an infrastructure CI is impacting devices. In this scenario the application service may be populated on the problem’s Impacted Services related list, task\_cmdb\_ci\_service, to identify the Application Service as one of the impacted services. For example, the Server Acme42 may be impacting my Application Service of MyApp 3.0 Prod and other related services.

**Parent Topic:**[Problem Management product view](pm-use-case-product-view.md)


---
title: Problem Management considerations
description: Consider these points while implementing the CSDM framework.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Applying CSDM guidelines to Problem Management, Configure, Problem Management, IT Service Management]
---

# Problem Management considerations

Consider these points while implementing the CSDM framework.

-   Service instance: A service instance is a service type that is a logical representation of a deployed application stack.
-   Using service instance for a problem: Some of the scenarios where the service instance can be used for a problem include:
    -   The problem is for an application issue: In this scenario the service instance may be populated in the configuration\_item attribute on the Problem form representing the unique deployment of an application stack. For example, the service instance of MyApp 3.0 Prod has been reported as being unavailable.
    -   The problem on an infrastructure CI is impacting devices. In this scenario the service instance might be populated on the problem’s Impacted Services related list, task\_cmdb\_ci\_service, to identify the service instance as one of the impacted services. For example, the Server Acme42 may be impacting **My service instance of MyApp 3.0 Prod** and other related services.

**Parent Topic:**[Applying CSDM guidelines to Problem Management](pm-use-case-product-view.md)


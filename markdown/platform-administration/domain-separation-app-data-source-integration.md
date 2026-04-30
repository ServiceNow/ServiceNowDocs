---
title: Domain separation in third-party application and data source integration
description: This is an overview of domain separation and integration of third-party applications and data sources. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation in third-party application and data source integration

This is an overview of domain separation and integration of third-party applications and data sources. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic-Standard

The Basic-Standard level of domain separation is achieved through data visibility as well the integration design.

**Basic**

-   There is business logic to ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

**Standard**

-   Includes **Basic** level
-   Business logic: Processes can be created or modified per customer by the service provider. The use cases reflect proper use of the application by multiple service provider customers in a single instance.
-   The owner of the instance needs to be able to configure MVP business logic and data parameters per tenant as expected for the specific application.

## Overview

Team should define a few examples with data-driven properties. There should be three different buckets with short description for each one

**Parent Topic:**[Integration with third-party applications and data sources](c_IntegrateWThirdPartyAppsDataSrces.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)


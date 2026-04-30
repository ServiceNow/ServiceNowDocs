---
title: Domain separation and Operational Technology
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Operational Technology. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-02-19"
reading_time_minutes: 1
breadcrumb: [Operational Technology]
---

# Domain separation and Operational Technology

Domain separation is supported for Operational Technology. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Operational Technology domain separation overview

Operational Technology inherits the domain separation features of the dependency applications. As each application can have its own domain separation relationship, there is no one specific support level to associate with Operational Technology. To learn more, see [Domain separation and Workflow Studio](https://www.servicenow.com/docs/access?context=flow-designer-domain-separation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

The following table describes the domain separation support levels and use cases for each Operational Technology application.

|Application|Support level|
|-----------|-------------|
|Operational Technology Manager|Basic|
|Industrial Process Manager|Basic|
|Operational Technology Vulnerability Response|Basic|
|Operational Technology|Basic|
|Operational Technology Change Management|Basic|
|Operational Technology Knowledge Management|Basic|
|Operational Technology Request Management|Basic|

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)


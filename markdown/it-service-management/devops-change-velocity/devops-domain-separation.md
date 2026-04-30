---
title: Domain separation and DevOps Change Velocity
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is unsupported for DevOps Change Velocity. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# Domain separation and DevOps Change Velocity

Domain separation is unsupported for DevOps Change Velocity. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Domain separation in DevOps Change Velocity overview

Use the ServiceNow® DevOps application with your DevOps toolchain to provide data insights, accelerate change, and increase visibility in your DevOps environment using a single system. In DevOps, domain separation targets tenant domain requester use cases in an application. The application has been designed to support requester activities within tenant domains. Logic is in place to route data to tenant domains, based on applicable use cases. The owner of the instance must be able to set up the application to function normally across multiple tenants. The application handles data routing to domains.

All tables in DevOps support data separation only; delegated domain separation is not supported.

To ensure that domain-sensitive information is not available at a global domain, ensure that you create policies at a domain level and not at a global level. While managing Service Providers, create policies at the Service Provider level. If you create policies at a global level instead, when you run the audit, the tag policy "run" findings are created in the Global domain, instead of respective domains.

**Parent Topic:**[DevOps Change Velocity reference](../reference/devops-change-velocity-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)


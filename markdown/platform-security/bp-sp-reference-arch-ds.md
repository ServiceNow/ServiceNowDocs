---
title: Service provider reference architecture
description: Your customers can access service provider \(SP\) services by using a portal that is designed for them to reach their domain-separated instance.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Service provider reference architecture

Your customers can access service provider \(SP\) services by using a portal that is designed for them to reach their domain-separated instance.

## Basic attributes of service provider reference architecture

-   You do not assign fulfillers to a domain. Instead, you share them across domains. This makes it harder to audit how many fulfillers you have per domain.
-   You can share and leverage domain administration. This means that there is no overhead and you can optimize licenses.
-   The number of users on the instance can change when you get a new customer. A new customer can result in tens or even hundreds of thousands of new users on the system. The number of total users is virtually unlimited in one shared environment.

![Reference architecture](../image/bp-sp-reference-architecture-ds.png)

The portal for SP services is dedicated or shared to the SP shared instance. Service providers use ServiceNow shared instances to manage their service delivery.

## Reference hierarchy for domain-separated instances

![Reference hierarchy](../image/bp-ds-hierarchy-3.png)

![Reference hierarchy comparison](../image/bp-dedicated-ds-hybrid-siam.png "SP reference architecture comparison")

-   **[Service provider reference architecture decision trees](bp-ded-instance-decision-tree.md)**  
You can use decision trees and a comparison chart to determine if a new customer should be added to a shared instance or to their own dedicated instance.
-   **[Service provider reference architecture for dedicated instances](bp-sp-reference-arch-dedicated.md)**  
Service provider \(SP\) customers can access SP services by using a portal to a dedicated instance. SPs use these dedicated instances to manage their service delivery.
-   **[Service provider reference architecture for hybrid](bp-sp-reference-arch-hybrid.md)**  
Use the hybrid service provider \(SP\) reference architecture for a customized solution. Your customers require a dedicated instance for a specific service. They can still use the shared SP instance for other services, but it requires integration of each instance.
-   **[Service provider reference architecture for Service Integration Management \(SIAM\)](bp-sp-reference-arch-siam.md)**  
The Service Integration Management Service Integration and Management \(SIAM\) for service provider \(SP\) architecture integrates services for a unified customer experience.

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Alternatives to domain separation](bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)

[Benefits of domain separation](bp-advantages-dom-sep.md)

[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)

[Domain separation levels of support](bp-domain-levels.md)

[Domain separation terms](bp-terms-conditions.md)

[Domain-separate a custom table](bp-ds-custom-table.md)

[Customizing domain properties and themes](../concept/bp-domain-prop-themes.md)

[Managing domain separation for specific uses](../concept/bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](../concept/bp-domain-picker-config-process.md)

[Domain separation performance considerations](../concept/bp-performance-considerations.md)

[Setting up domain hierarchies](../concept/bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](../concept/bp-domain-logs.md)

[Importance of the Default domain](../concept/bp-default-domain.md)

[Contains queries and domain access](../concept/bp-contains-domain-visibility.md)

[Domain paths query method](../concept/bp-domain-query-method.md)

[Slow queries and SQL debugging](../concept/bp-debug-sql.md)

[Before Query business rules](../concept/bp-before-query-business-rules.md)

[Avoiding domain path in scripts](../concept/bp-no-domain-path-in-scripts.md)

[Domain assignments](bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)


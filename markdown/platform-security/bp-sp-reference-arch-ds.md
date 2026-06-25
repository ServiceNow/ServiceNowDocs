---
title: Service provider reference architecture
description: Your customers can access service provider \(SP\) services by using a portal that is designed for them to reach their domain-separated instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-sp-reference-arch-ds.html
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

\[Omitted image "bp-sp-reference-architecture-ds.png"\] Alt text: Reference architecture

The portal for SP services is dedicated or shared to the SP shared instance. Service providers use ServiceNow shared instances to manage their service delivery.

## Reference hierarchy for domain-separated instances

\[Omitted image "bp-ds-hierarchy-3.png"\] Alt text: Reference hierarchy

\[Omitted image "bp-dedicated-ds-hybrid-siam.png"\] Alt text: Reference hierarchy comparison

-   **[Service provider reference architecture decision trees](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-ded-instance-decision-tree.md)**  
You can use decision trees and a comparison chart to determine if a new customer should be added to a shared instance or to their own dedicated instance.
-   **[Service provider reference architecture for dedicated instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-dedicated.md)**  
Service provider \(SP\) customers can access SP services by using a portal to a dedicated instance. SPs use these dedicated instances to manage their service delivery.
-   **[Service provider reference architecture for hybrid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-hybrid.md)**  
Use the hybrid service provider \(SP\) reference architecture for a customized solution. Your customers require a dedicated instance for a specific service. They can still use the shared SP instance for other services, but it requires integration of each instance.
-   **[Service provider reference architecture for Service Integration Management \(SIAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-siam.md)**  
The Service Integration Management Service Integration and Management \(SIAM\) for service provider \(SP\) architecture integrates services for a unified customer experience.

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Domain separation terms]()

[Domain-separate a custom table]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


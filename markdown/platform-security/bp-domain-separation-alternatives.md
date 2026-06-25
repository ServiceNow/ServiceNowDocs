---
title: Alternatives to domain separation
description: You can use a separate instance as an alternative to domain separation for your customers. A separate instance allows you the flexibility to meet the requirements for data separation within the groups and departments in an organization with little to no impact on others.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-separation-alternatives.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Alternatives to domain separation

You can use a separate instance as an alternative to domain separation for your customers. A separate instance allows you the flexibility to meet the requirements for data separation within the groups and departments in an organization with little to no impact on others.

## Separate instances

|Separate instance|Single instance - without domain|
|-----------------|--------------------------------|
|**Pros**|**Pros**|
|Built to suit each customer/organization|May address simple scenarios|
|Minimize impact of customization on others|Cost|
|Release schedule coordination|**Cons**|
|Clean separation|Extensive modifications to baseline code|
|Choose DATACENTER region|Modified base system code skipped during upgrades|
|**Cons**|Must address all secondary and supporting tables as well|
|Cost|Extensive testing required|
|Alignment of instances|No ServiceNow product team to evolve your custom code|
|Testing effort for upgrades| |
|Duplication of effort| |
|Integrations required| |

You can time upgrades and releases separately for each instance. However, if you choose to use separate instances, you need to do a lot of coordination with other people who are administering instances. By configuring an instance with contextual security, form views, reference qualifiers, filters, and robust conditions, you don't have to use domain separation in your company.

With a separate instance, you may address data and process separation but your instance owners must maintain and keep up with the extensive customizations that is required for separate instances.

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

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

[Context and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-context.md)

[Service provider reference architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-ds.md)


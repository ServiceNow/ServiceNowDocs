---
title: Alternatives to domain separation
description: You can use a separate instance as an alternative to domain separation for your customers. A separate instance allows you the flexibility to meet the requirements for data separation within the groups and departments in an organization with little to no impact on others.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
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

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)

[Benefits of domain separation](bp-advantages-dom-sep.md)

[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)

[Domain separation levels of support](bp-domain-levels.md)

[Service provider reference architecture](bp-sp-reference-arch-ds.md)

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

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Service provider reference architecture](bp-sp-reference-arch-ds.md)


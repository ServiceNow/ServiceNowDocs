---
title: Evaluating the need for domain separation
description: You may find that domain separation doesn't always work for your customers' organizations. It's best that you base your decision to go with domain separation by looking at your customers' needs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Evaluating the need for domain separation

You may find that domain separation doesn't always work for your customers' organizations. It's best that you base your decision to go with domain separation by looking at your customers' needs.



## Reasons for domain separation

These factors may help you decide to choose domain separation for your customers' organizations:

-   Your customers have moderate alignment of processes and general platform requirements.
-   Your customers plan to work on tasks as fulfillers rather than as requesters.
-   Your customers have a contractual agreement that requires that data records be isolated, but your instance owner has determined that the requirement may be addressed somewhere else in the configuration.
-   Your company's instance owners have entire entities that operate as physically separate organizations and do not share data, but full reporting is still required. Separate domains would allow data visibility when configured correctly.

## Reasons for no domain separation

These factors can point to reasons why your customers' organizations might not want to set up domain separation:

-   Your customers want to administer their environment, have full ownership of it, and set the roadmap for expansion.
-   Your customers require that the data and process at the physical or database level be completely isolated.

    **Note:**

    Domain-separated instances contain a shared database so this undermines the isolation requirement.

-   Departments in your customers' organization want to isolate records. \(Access controls may suffice.\)
-   Your customers all want their own processes, business rules, and workflows.
-   The corporate culture is one of non-collaboration between your customers' organizations.
-   Your customers interact with the platform as end users only.

![Evaluating reasons for and against choosing domain separation](../image/bp-evaluating-need.png)

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Alternatives to domain separation](bp-domain-separation-alternatives.md)

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


---
title: Context and domain separation
description: The context of a user's session determines the processes, data, and user interface \(UI\) as the user browses through list views, home pages, reports, and knowledge articles. The context is determined by the processes that you create, the business rules that you set, your workflows, and other factors.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Context and domain separation

The context of a user's session determines the processes, data, and user interface \(UI\) as the user browses through list views, home pages, reports, and knowledge articles. The context is determined by the processes that you create, the business rules that you set, your workflows, and other factors.

## User session context

Many factors determine the context of a user session, such as user profiles, groups, company criteria, and so on. In the following diagram, you see that the incidents that a company has created are part of the context.

![User session context](../image/bp-user-session-context.png)

The user in this example has a home domain of Cloud Dimensions.

1.  The branding reflects the settings in the Cloud Dimensions domain and company record.
2.  The application navigator shows the items that are inherited from higher-level domains as well as the modules that are defined in the Cloud Dimensions domain.
3.  The home pages and list data reflect the data that is visible to the user. This data is based on the user’s session context. In this case, the user in the Cloud Dimensions domain can see the data in Cloud Dimensions, child domains, and the global domain.

## User session context starts in the home domain

In the following diagram, you can see the elements of the context.

![User session context home domain](../image/bp-user-session-context-home.png)

The system administrator sets users' home domains on their user records. Typically, a user’s home domain is set to the same domain as their company’s domain. When the user logs in, the domain picker sets automatically to the user’s home domain. Users can return to their home domain at any time by clicking the arrow icon on the domain picker.

The domain picker's list includes domains within the user’s session context. Users may further limit their session context by selecting child domains with the picker.

The context of the user session includes the user's home domain and any child domains. This set of domains in the user’s session context is appended automatically to every query that is sent to the database. That way, the results are limited to just the data in these domains and global data. This process is embedded in the compiled code that is not accessible.

Service accounts that are used for integrations also have user session context. There is user context and records context, each with its own data in its own domain. These contexts affect the integrations. Database queries \(records\) are limited in the same way as interactive users \(users\), meaning that they work as normal but are limited by whatever constraints the developer has configured.

You can learn about additional ways to add domains to a user’s session context in [Service provider reference architecture](../reference/bp-sp-reference-arch-ds.md).

## Record context

As a user drills into individual records, record context is activated. The record context determines the UI elements and processes to apply to the record.

A record’s domain dictates the process, data, and the availability of UI elements within the record.

**Note:**

-   Record context persists even if the user's domain changes.
-   Users can view records concurrently in multiple browser tabs, while maintaining their own record context.

![Record context](../image/bp-record-context.png)

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](bp-what-is-domain-separation.md)

[Domain separation hierarchies](../reference/bp-domain-sep-hierarchies.md)

[Segregating and securing data with domain separation](../reference/bp-segregate-secure.md)

[Alternatives to domain separation](../reference/bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](../reference/bp-evaluation-dom-sep.md)

[Benefits of domain separation](../reference/bp-advantages-dom-sep.md)

[How a database query works with domain separation](bp-db-query-with-ds.md)

[Domain separation levels of support](../reference/bp-domain-levels.md)

[Service provider reference architecture](../reference/bp-sp-reference-arch-ds.md)

[Domain separation terms](../reference/bp-terms-conditions.md)

[Domain-separate a custom table](../reference/bp-ds-custom-table.md)

[Customizing domain properties and themes](bp-domain-prop-themes.md)

[Managing domain separation for specific uses](bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](bp-domain-picker-config-process.md)

[Domain separation performance considerations](bp-performance-considerations.md)

[Setting up domain hierarchies](bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](bp-domain-logs.md)

[Importance of the Default domain](bp-default-domain.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)


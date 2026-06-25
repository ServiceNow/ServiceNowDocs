---
title: Context and domain separation
description: The context of a user's session determines the processes, data, and user interface \(UI\) as the user browses through list views, home pages, reports, and knowledge articles. The context is determined by the processes that you create, the business rules that you set, your workflows, and other factors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-sep-context.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Context and domain separation

The context of a user's session determines the processes, data, and user interface \(UI\) as the user browses through list views, home pages, reports, and knowledge articles. The context is determined by the processes that you create, the business rules that you set, your workflows, and other factors.

## User session context

Many factors determine the context of a user session, such as user profiles, groups, company criteria, and so on. In the following diagram, you see that the incidents that a company has created are part of the context.

\[Omitted image "bp-user-session-context.png"\] Alt text: User session context

The user in this example has a home domain of Cloud Dimensions.

1.  The branding reflects the settings in the Cloud Dimensions domain and company record.
2.  The application navigator shows the items that are inherited from higher-level domains as well as the modules that are defined in the Cloud Dimensions domain.
3.  The home pages and list data reflect the data that is visible to the user. This data is based on the user’s session context. In this case, the user in the Cloud Dimensions domain can see the data in Cloud Dimensions, child domains, and the global domain.

## User session context starts in the home domain

In the following diagram, you can see the elements of the context.

\[Omitted image "bp-user-session-context-home.png"\] Alt text: User session context home domain

The system administrator sets users' home domains on their user records. Typically, a user’s home domain is set to the same domain as their company’s domain. When the user logs in, the domain picker sets automatically to the user’s home domain. Users can return to their home domain at any time by clicking the arrow icon on the domain picker.

The domain picker's list includes domains within the user’s session context. Users may further limit their session context by selecting child domains with the picker.

The context of the user session includes the user's home domain and any child domains. This set of domains in the user’s session context is appended automatically to every query that is sent to the database. That way, the results are limited to just the data in these domains and global data. This process is embedded in the compiled code that is not accessible.

Service accounts that are used for integrations also have user session context. There is user context and records context, each with its own data in its own domain. These contexts affect the integrations. Database queries \(records\) are limited in the same way as interactive users \(users\), meaning that they work as normal but are limited by whatever constraints the developer has configured.

You can learn about additional ways to add domains to a user’s session context in [Service provider reference architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-ds.md).

## Record context

As a user drills into individual records, record context is activated. The record context determines the UI elements and processes to apply to the record.

A record’s domain dictates the process, data, and the availability of UI elements within the record.

**Note:**

-   Record context persists even if the user's domain changes.
-   Users can view records concurrently in multiple browser tabs, while maintaining their own record context.

\[Omitted image "bp-record-context.png"\] Alt text: Record context

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

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


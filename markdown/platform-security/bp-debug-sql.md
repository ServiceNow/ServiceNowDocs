---
title: Slow queries and SQL debugging
description: Debugging SQL and slow queries can help you resolve slowness issues in an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-debug-sql.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Slow queries and SQL debugging

Debugging SQL and slow queries can help you resolve slowness issues in an instance.

When you debug an instance, you can either enable SQL debugging to look for slow queries or you can look for slow queries by checking the Slow Queries \[sys\_query\_pattern\] table by navigating to **System Diagnostics &gt; Stats &gt; Slow Queries**. This table stores all the slow queries in the instance.

When you search the table, look for queries that contain `domain_path` to determine if any slow queries are due to the domain path in your instance.

If you do find slow queries, try to analyze why they are slow.

## Common reasons for slow queries

-   A query has too many OR conditions \(for more information, see [Contains queries and domain access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-contains-domain-visibility.md)\). In the domain hierarchy, place the user or a domain at a hierarchy level where contains or visibility is not needed.
-   The query method is not the domain path query method \(for more information, see [Domain paths query method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-query-method.md)\): If you are not using the domain path query method, contact Customer Service and Support.
-   A query needs a database to be indexed so you can see what is in the database quickly. If you can identify the slow query, run the "explain plan" to see if there are options for indexing available. The "explain plan" is a function of SQL that shows the query and what is going on with it.

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

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


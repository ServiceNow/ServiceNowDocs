---
title: How a database query works with domain separation
description: Using database queries with domain separation in your customers' applications help them protect their data. These queries then speed up the configuration and build processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-db-query-with-ds.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# How a database query works with domain separation

Using database queries with domain separation in your customers' applications help them protect their data. These queries then speed up the configuration and build processes.

## How domain separation protects data

In the following figure, the Incident table \[incident\] has a domain field that is inherited from the incident's task. When you see this domain field, you know that the records in the table can have domain assignments.

When users log in, their home domain appears with the set of domains they may access. This is known as the user’s session context. For more information about session contexts, see [Context and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-context.md).

## Database query with domain separation

\[Omitted image "bp-db-query-with-ds.png"\] Alt text: Database query with domain separation

1.  In a browser, the user from one of the companies, Acme, selects the Open Incidents module to view all incidents where active=true.
2.  The active=true filter is submitted to the application.
3.  The application then sends a query to the database by appending a WHERE clause to active=true. The WHERE clause limits the incident records that are returned to those records that are in the user's domain or the domains that the user may access. Only the records in these domains are returned to the application for processing.
4.  Contextual security is applied, further limiting the data that is returned to the user. The incident records appear in the Open Incidents list.

    **Note:**

    When you apply contextual security, you create limits to the data that are returned to the user. These limits protect other content that you may not want users to see.


To learn more about contextual security, see [Context and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-context.md).

**Note:** This processing logic applies for all queries to the database, including those queries that are triggered using integrations.

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

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


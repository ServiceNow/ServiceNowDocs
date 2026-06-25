---
title: Contains queries and domain access
description: Use a "contains" query only in special cases, such as when users or groups need to see data from a domain that they don't have access to, but you don't want to move those users to a domain. Creating domain "contains" and user or group access for a domain should be an exception, only when absolutely needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-contains-domain-visibility.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Contains queries and domain access

Use a "contains" query only in special cases, such as when users or groups need to see data from a domain that they don't have access to, but you don't want to move those users to a domain. Creating domain "contains" and user or group access for a domain should be an exception, only when absolutely needed.

"Contains" is a domain-to-domain relationship that is many-to-many, and has no effect on the flow of process. If you create a large number of domain "contains" relationships or provide broad access, you will generate queries with too many OR conditions. OR conditions are slow and impact the performance of your instance. Instead of using too many "contains" relationships, set up your domain hierarchy as follows:

\[Omitted image "bp-contains-domain-visibility.png"\] Alt text: Sample query

Before you move users to a domain, make sure that they really should have access to that domain. Weigh the benefits and limitations. The query above is for just one contains relationship. If you have a domain that contains another domain, and that domain is the parent of a number of other domains, you will have many more OR conditions. Be careful when you create a domain map so that you do not impact the performance of your instance.

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

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


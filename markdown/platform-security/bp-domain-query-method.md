---
title: Domain paths query method
description: You can create effective queries with domain paths.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-query-method.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain paths query method

You can create effective queries with domain paths.

Use domain paths instead of domain spooling \(`sys_domain`\) or domain numbering. Queries that use domain paths are much faster than spooling or numbering.

Domain paths is the default query method for instances that have enabled domain separation.

If you want to verify the query method on your instance, look for the following system properties in the admin dashboard:

-   **If domain path is enabled**: In the System Properties table, you see `glide.sys.domain.provider=domain_paths` and `glide.sys.domain.paths.installed=true`.
-   **If domain path is not enabled**: In the System Properties table, you see `glide.sys.domain.provider != domain_paths,glide.sys.domain.paths.installed=false`

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

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


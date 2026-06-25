---
title: Setting up domain hierarchies
description: You can avoid slowdowns and performance impacts in your instance by knowing how domain hierarchies work and by setting them up properly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-hierarchy.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Setting up domain hierarchies

You can avoid slowdowns and performance impacts in your instance by knowing how domain hierarchies work and by setting them up properly.

Based on the domain hierarchy, users have access to the data in their home domain and any child domains. The process flows down to the child domains and the data rises up.

Make changes to the existing domain hierarchy only when needed. When you update the parent of a domain, the system re-establishes the parent domain with all its child domains that change the domain hierarchy. When the domain hierarchy updates, the system triggers a cascade update on all tables that relate to domains for the records that are created on that domain. As a result, a large number of supporting tables have to be updated too.

For the same reasons, even if you must change the domain hierarchy, never do a mass update. Imagine the number of queries that the system has to run to change the domain hierarchy. Always do an update in small batches. Before you start the next batch of updates, make sure that Domain Work Request \(DWR\) records are processed. DWRs are reports that display whether there are errors after you've changed the domain hierarchy.

## Tracking DWR records

In the syslog\_domain table, look for an information entry in the Message column for **DWR execution completed.** to confirm that DWR is completed.

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

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


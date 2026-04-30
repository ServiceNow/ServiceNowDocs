---
title: Setting up domain hierarchies
description: You can avoid slowdowns and performance impacts in your instance by knowing how domain hierarchies work and by setting them up properly.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Setting up domain hierarchies

You can avoid slowdowns and performance impacts in your instance by knowing how domain hierarchies work and by setting them up properly.

Based on the domain hierarchy, users have access to the data in their home domain and any child domains. The process flows down to the child domains and the data rises up.

Make changes to the existing domain hierarchy only when needed. When you update the parent of a domain, the system re-establishes the parent domain with all its child domains that change the domain hierarchy. When the domain hierarchy updates, the system triggers a cascade update on all tables that relate to domains for the records that are created on that domain. As a result, a large number of supporting tables have to be updated too.

For the same reasons, even if you must change the domain hierarchy, never do a mass update. Imagine the number of queries that the system has to run to change the domain hierarchy. Always do an update in small batches. Before you start the next batch of updates, make sure that Domain Work Request \(DWR\) records are processed. DWRs are reports that display whether there are errors after you've changed the domain hierarchy.

## Tracking DWR records

In the syslog\_domain table, look for an information entry in the Message column for **DWR execution completed.** to confirm that DWR is completed.

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](bp-what-is-domain-separation.md)

[Domain separation hierarchies](../reference/bp-domain-sep-hierarchies.md)

[Context and domain separation](bp-domain-sep-context.md)

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

[Checking domain logs for errors and warnings](bp-domain-logs.md)

[Importance of the Default domain](bp-default-domain.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)


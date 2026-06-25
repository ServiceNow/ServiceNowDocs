---
title: Importance of the Default domain
description: Organizing your domains is a crucial part of the domain separation process. If you don't set a default domain, new tasks and user records go to the global domain. Anyone can see the records in the global domain, which means that data can be seen when it is not supposed to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-default-domain.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Importance of the Default domain

Organizing your domains is a crucial part of the domain separation process. If you don't set a default domain, new tasks and user records go to the global domain. Anyone can see the records in the global domain, which means that data can be seen when it is not supposed to.

When you set the default domain, its records are not visible to any user other than an admin.

**Note:** The defaults access can be changed by granting users visibility to the default domain or the parent domain.

You should always set one default domain for the domain records on your instance. The default domain is where the system automatically assigns task and user records that are not already assigned to a domain.

When you create a default domain from the Domain Administration screen, add the name Default in the **Name** field to differentiate it from other domains. Check the **Default** check box for the record.

Maintain regularly the records that you create in the default domain and move them to the correct domains. If records show up often in the default domain, you may need to investigate why. Ideally, you should make sure that all records are created in their appropriate domains \(not global or default domains\).

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

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


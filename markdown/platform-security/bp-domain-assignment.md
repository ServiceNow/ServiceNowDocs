---
title: Domain assignments
description: How you assign a domain impacts the value of the sys\_domain field. The assignments contain designs and business properties that affect how the application functions in each domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-assignment.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain assignments

How you assign a domain impacts the value of the sys\_domain field. The assignments contain designs and business properties that affect how the application functions in each domain.

## Value of the sys\_domain field

The value of the **sys\_domain** field contains the domain that is assigned to the record by any of the following:

-   Company to which the user belongs
-   Business rule that is used when creating the record
-   Module that is used when creating the record
-   Form template that is used when creating the record
-   Domain of the parent record
-   Domain that is assigned to the User record
-   Domain of the user who creates it

Make sure that your domain assignment strategies and designs are well documented and tested so that you are creating records as those strategies and designs are inserted into the correct domain. That way you can see that the properties of each domain should you need to duplicate or modify them.

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

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()


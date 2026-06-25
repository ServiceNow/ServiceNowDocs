---
title: Segregating and securing data with domain separation
description: You can segregate and secure data on the ServiceNow platform in multiple ways, depending on your customer's needs. 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-segregate-secure.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Segregating and securing data with domain separation

You can segregate and secure data on the ServiceNow platform in multiple ways, depending on your customer's needs. 

## Segregating data in multiple ways

The following diagram shows four ways that you can segregate data. You can use separate instances, domain separation, contextual security and business rules, and the reference architecture itself as ways to segregate data.

\[Omitted image "bp-multiple-ways.png"\] Alt text: Four methods of segregating data, business rules, processes, and instances

You can segregate data in these four ways:

1.  Customizing the [reference architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-ds.md) with qualifiers and filters so that departments and groups within a company can focus on their own work. By segregating the data between these departments or groups, a department or group can't see another department or group's records.
2.  Adding contextual security and Before Query business rules as additional layers of security to guard against data breaches. See [Context and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-context.md) and [Before Query business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-before-query-business-rules.md) to learn more about domain separation and business rules.
3.  Adding another level of security in a company by using domain separation. The data from every database query is limited to the data that is visible in a domain before contextual security and business rules are executed.
4.  Using separate instances to segregate the data at the database and application layer.

Separate instances, domain separation, contextual security and business rules, and the reference architecture are ways to segregate data. These four ways relate to each other as indicated by the Comprehensiveness of need arrow in the diagram. How each layer interacts with the other layers depends on how you set up your domain separation configuration.

Not all organizations require domain separation. You might find other alternatives, such as separate instances or a single instance without a domain. To learn more about these alternatives, see [Evaluating the need for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-evaluation-dom-sep.md).

-   **[Cross tenant intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-dom-sep-how-it-works.md)**  
A multi-tenant architecture is where you have a single instance serving multiple tenants. Data, metadata, business logic, and processing context for tenants is automatically handled with access to additional tenant data.

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

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


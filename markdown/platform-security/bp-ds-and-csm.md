---
title: Domain separation and the Customer Service Management \(CSM\) plugin
description: For the best outcome, be aware of how the properties in the CSM plugin work. When the plugin is enabled, you can see the status of your records in your domains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-ds-and-csm.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation and the Customer Service Management \(CSM\) plugin

For the best outcome, be aware of how the properties in the CSM plugin work. When the plugin is enabled, you can see the status of your records in your domains.

Instance owners should contact Customer Service and Support to enable the **csm\_auto\_account\_domain\_generation** property.

**Note:** This base system property is located in the system properties table and is available after CSM plugins are enabled.

-   **What the property does**

    Whenever a new account in the Customer Service application is created, a domain is created and placed under the TOP domain. If the parent field on the account form is populated, and a new record is inserted, it creates that account as a subdomain of the parent.

-   **What happens if this property is not true and the domain is enabled**

    New account records in a domain-separated environment are automatically placed in the default domain.


In the header bar, you can see the status of the records with the plugin enabled.

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

[Domain assignments]()


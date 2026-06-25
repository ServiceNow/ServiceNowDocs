---
title: Configuring domain separation with the domain picker
description: Use the domain picker wisely, and remember the 80/15/5 approach so that you do not customize too much and impact the performance of your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-picker-config-process.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Configuring domain separation with the domain picker

Use the domain picker wisely, and remember the 80/15/5 approach so that you do not customize too much and impact the performance of your instance.

## Verify your domain before making changes

The domain picker gathers all the domains into a list for you to choose from.

If your session times out and even if you don't get logged out, your session falls back to the domain on your user record. You also lose any elevated roles at the same time. In this case, your domain picker could still show the last domain that you selected if the top frame of the list hasn't been reloaded. For this reason, you should reload your list completely if you have been away from the instance for any time.

## Configuring at the TOP domain or the global domain

Domain separation works best when you are providing services to customers that are mostly standard in their configuration and user and group definition. The more that you customize and create "one-off" solutions, the more you create a margin for error. When you create your processes and business logic, any variations should be in properties that work automatically for each customer. While processes can still be adjusted as needed, use great care when you decide when, and to what degree, to create a unique configuration for a single customer.

You need to use an "80-15-5" approach in configuring your domains to avoid too large a margin for customization, and therefore error.

-   Recommended approach for configuration:
    -   **80%** or more **Standard**
    -   **15%** or more **Parametric**
    -   Less than **5%** **Configuration**
-   Determine if a suggested change should be a global or a configurable property.
-   Do not overbuild by adding more and more customization that needs to be managed. Instead, do the following:
    -   Start with the base system features and verify any gaps before you make any changes.
    -   Look for no-code solutions.
    -   Use server-side scripts, build modular APIs, and build in domain-separated properties.
    -   If you must use client scripting, use only ServiceNow APIs. Limit "synchronous" calls \(those that go back and forth from client to server, also called AJAX\).
    -   Write all scripts logically to keep them simple and effective. Enforce peer reviews of code changes and make sure everyone is following the [Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md) in this section.

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


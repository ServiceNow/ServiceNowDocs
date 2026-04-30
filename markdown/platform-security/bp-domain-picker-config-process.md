---
title: Configuring domain separation with the domain picker
description: Use the domain picker wisely, and remember the 80/15/5 approach so that you do not customize too much and impact the performance of your instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
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
    -   Write all scripts logically to keep them simple and effective. Enforce peer reviews of code changes and make sure everyone is following the [Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md) in this section.

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

[Domain separation performance considerations](bp-performance-considerations.md)

[Setting up domain hierarchies](bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](bp-domain-logs.md)

[Importance of the Default domain](bp-default-domain.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Slow queries and SQL debugging](bp-debug-sql.md)

[Before Query business rules](bp-before-query-business-rules.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)


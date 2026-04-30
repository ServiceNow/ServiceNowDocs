---
title: Domain separation performance considerations
description: As you configure domain separation in your application and services, make sure that you consider the number and properties of domains you create. Too many property-heavy domains can impact the performance of your instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation performance considerations

As you configure domain separation in your application and services, make sure that you consider the number and properties of domains you create. Too many property-heavy domains can impact the performance of your instance.

## Limiting property-heavy domains

You can create as many domains as needed, but make sure that you don't create unnecessary domains on the instance. Weighing too many domains on the instance with a lot of properties can impact the performance of your instance.

The number of domains is not what impacts performance but rather what's in them. Too many properties can slow down the [domain picker](bp-domain-picker-config-process.md), which then slows down the overall user experience of your customers. If you are loading the domain picker and already have a large number of domains with a lot of properties, the domain picker has to load all the domains before it gives you control in the session. This process could lead to an outage where you can't access anything on the instance until the domain picker finishes. Before you create new domains, navigate to the domain hierarchy under **Domain Admin** &gt; **Domain Map** and make sure that you actually need to create a new domain or whether an existing [domain hierarchy](bp-domain-hierarchy.md) can work.

## Using Core UI domain picker

The domain reference picker is available in Core UI. With the reference picker, you do not load all the domains at once, but rather the domain is searched as you begin to enter the name of your domain into the domain picker.

Enable the domain reference picker in Core UI by following these steps:

1.  In the application navigator, enter `sys_properties.list`.
2.  Set the **glide.ui.domain\_reference\_picker.enabled** property to true.
3.  Refresh the browser.

**Note:** Do not upload a large number of domains \(over 30\) via integration or import sets without doing some testing first or you might bring down your instance.

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


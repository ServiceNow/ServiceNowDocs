---
title: Domain separation plugin
description: The Domain Support - Domain Extensions Installer plugin activates several domain separation features and properties at once. This plugin is typically referred to as the Domain Separation plugin.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Domain separation plugin

The Domain Support - Domain Extensions Installer plugin activates several domain separation features and properties at once. This plugin is typically referred to as the Domain Separation plugin.

## Recommended practice for activating the Domain Separation plugin

As part of domain separation development, administrators must [request activation](../task/t_ActivateDomainSeparation.md) of this plugin. For best results, activate the Domain Separation plugin at the start of the development process, preferably before any other plugin is enabled.

**Important:** Request to activate the Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) before activating Domain Separation \(plugin com.snc.pa.domain\_support\).

If you enable Domain Separation towards the end of ServiceNow implementation or once an instance has gone live, your application is at risk in both performance and process. On established instances, depending on how things were structured in development, the risk to the platform and its usability could be high. To learn more about domain separation process, see [Exploring domain separation](c_DomainSeparation.md).

For instance, when the Domain Separation plugin is enabled, the **Domain** \(sys\_domain\) column is added to the task table and every existing record is automatically placed in **global**. To use a script to assign all of the records into the correct domains, an established parent/child hierarchy is required. These types of scripted actions risk data corruption or loss, and possible production down time as large amounts of data are moved. Much of the platform code also is placed into **global**, such as business rules, client scripts, form views, and workflows.

If a customer creates code or modifies ServiceNow code, there is risk to platform performance and usability. Instance owners could severely delay their implementation or experience lengthy down-times with this type of approach.

## Features of the Domain Separation plugin

These features are enabled when you activate the plugin:

-   Domain separation is based on the Domain `[sys_domain]` table.
-   Delegated administration lets each domain have separate policy.
-   All records are part of the global domain.
-   The current user's domain determines the domain to use when viewing or operating on a record in a different domain.

**Related topics**  


[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)


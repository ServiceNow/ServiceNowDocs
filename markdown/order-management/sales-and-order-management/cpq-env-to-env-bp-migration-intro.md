---
title: Testing in non-production environments before migration
description: Test configurators in a non-production environment before migrating them to production. The configurators support revenue-critical processes, validate all changes outside production and promote them using controlled environment-to-environment migrations.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Testing in non-production environments before migration

Test configurators in a non-production environment before migrating them to production. The configurators support revenue-critical processes, validate all changes outside production and promote them using controlled environment-to-environment migrations.

CPQ configurators should be tested in non-production environments before they are migrated to a production environment and made available to end users.

CPQ configurators are key to organizations' revenue production processes. Therefore, you must take care to ensure all configurators work as expected before they are introduced to sales users, partners, and customers. All CPQ implementations have at least one non-production environment for this purpose. Some customer IT organizations have development processes that require a larger development stack.

![Workflow](../images/cpq-logik-development-stacks.png)

Because all maintenance and development must be tested in a non-production environment before promotion, this also means that:

-   Migrations must take place only in the production environment. No manual work ever occurs there.
-   Environment-to-environment migration is an essential element of any administration project.

**Related topics**  


[Migrate a blueprint from environment to environment](../task/cpq-migrating-env-to-env.md)

[Migrate a blueprint to an SFDC-integrated destination](../task/cpq-migrating-to-sfdc.md)

[The fullBlueprintMigration parameter](../reference/cpq-fullblueprintmigration-param.md)


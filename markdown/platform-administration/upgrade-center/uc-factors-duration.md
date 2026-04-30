---
title: Factors affecting upgrade duration
description: Various factors affect how long the system takes to perform an upgrade. The Upgrade Monitor on non-production instance can help you understand those factors and estimate how long the upgrade to your production instance takes.
locale: en-US
release: zurich
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Upgrade Monitor module, Explore, Upgrade Center, Upgrade, Administer]
---

# Factors affecting upgrade duration

Various factors affect how long the system takes to perform an upgrade. The Upgrade Monitor on non-production instance can help you understand those factors and estimate how long the upgrade to your production instance takes.

Many factors can affect the duration of the upgrade process:

-   The number of records in the database
-   The number of customizations in the database
-   The number of nodes in the instance
-   The size of tables in the instance that require a schema-change in the instance
-   The number of fix scripts required and the size of the tables those fix scripts manipulate

Upgrading a non-production instance can help you estimate how long the upgrade takes on production, but differences between the instances can significantly affect the duration:

-   When you cloned the production instance to the non-production instance, you may have clone-excluded some tables. This reduces the size of the database and makes the non-production instance upgrade faster than the production instance.
-   The production instance may have more memory and processing power.
-   The production instance may have more nodes than the non-production instance.

After upgrading the first non-production instance, examine the [Upgrade Summary Report](../reference/uc-complete-summary.md) for data to help estimate the impact of these factors.


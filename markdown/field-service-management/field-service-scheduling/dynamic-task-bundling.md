---
title: Dynamic task bundling
description: You can create policies and rules to bundle tasks automatically with Field Service Task Bundling.Policies dictate how many work order tasks should be grouped per bundle, as well as the maximum duration of bundles.Rules specify the parameters for which work order tasks should be bundled.Administrators can enable the Dynamic Bundling before Dynamic Scheduling\(com.snc.dynamic.scheduling.bundle\_before\_scheduling\) property to ensure bundles are generated before dynamic scheduling.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Task Bundling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Dynamic task bundling

You can create policies and rules to bundle tasks automatically with Field Service Task Bundling.

Dynamic task bundling enables administrators to create policies and rules to bundle tasks automatically according to custom criteria.

For information about the policies and rules installed with Field Service Task Bundling, see [Field Service Task Bundling components](../reference/task-bundling-components.md).

## Policies

Policies dictate how many work order tasks should be grouped per bundle, as well as the maximum duration of bundles.

A policy consists of multiples rules. Policies have the following restrictions:

-   Two records minimum per bundle.
-   200 records maximum per bundle.
-   No limit for rules per policy.
-   Policies must have rules to run.
-   Policies must have qualifiers to run.

### Qualifiers

Qualifiers dictate which work order tasks are targeted for bundling. By default, qualifiers are based on assignment groups. If [Field Service Territory Planning](territory-planning-fsm.md) is active, qualifiers are based on territories.

Qualifiers have the following restrictions:

-   Qualifier records can contain only type of qualifier at a time.
-   No duplicate qualifiers enabled per policy.

## Rules

Rules specify the parameters for which work order tasks should be bundled.

A rule can only be assigned to a single policy. Rules only apply if tasks meet the following conditions:

-   Are in the **Draft** state
-   Aren't in a bundle
-   Aren't a bundle itself
-   Aren't a vendor task
-   Don’t have access hours
-   Don’t need a crew
-   Don’t have a fixed window
-   Don’t have subtasks or dependent tasks

## Dynamic scheduling and dynamic bundling

Administrators can enable the **Dynamic Bundling before Dynamic Scheduling**\(**com.snc.dynamic.scheduling.bundle\_before\_scheduling**\) property to ensure bundles are generated before dynamic scheduling.


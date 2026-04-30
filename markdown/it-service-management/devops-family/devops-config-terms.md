---
title: DevOps Config terms
description: These are some of the common DevOps Config terms.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, DevOps Config, IT Service Management]
---

# DevOps Config terms

These are some of the common DevOps Config terms.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

-   **Application**

    The logical composition of an application or application stack, containing the relevant configuration data needed to provision or deploy into a fleet. This can range from a traditional, monolithic structure to a modern structure that can contain multiple micro-services.

-   **Collection**

    A set of components that make up a release composition. Collections are included into deployables, and can be used to test different versions of components.

    This example shows release-1.0 of an application that is currently deployed to the Production environment.

    ![DevOps Config collections](../image/devops-config-collections.png)

    The microservice team that owns the payment service makes a hotfix and decides to add that into a release-1.1 collection that they are now testing in their Test environment.

-   **Component**

    The smallest aggregation unit of configuration data. A microservice that is part of a larger application stack is an example of a component.

-   **Configuration Data Item \(CDI\)**

    A single unit of configuration data \(for example, connection string, heap size, etc.\) that is stored as a key-value pair.

-   **Data Model**

    A hierarchy of related configuration data used to deploy an application or infrastructure.

-   **Deployable**

    A subset of the data model, which encapsulates the set of configuration data that is used to deploy/provision an application or infrastructure for a specific target environment. It generally shares the same nomenclature \(for example, Production, Staging, Test, Development, etc.\).

-   **Snapshot**

    The complete data model of a deployable at the time a configuration change is committed. This includes any included components, collections, and vars, as well as deployable-specific vars and overrides.

-   **Vars**

    Variable configuration data that can be used to roll up configuration values that are used multiple times throughout different sections in the data model.

    Vars created at the component level can be reused anywhere further down, like in a collection and/or deployable. However, vars defined in a particular deployable are intended to be used only in that context \(for example, environment-specific creds, memory settings, etc.\).


**Parent Topic:**[Exploring DevOps Config](../concept/devops-config-getting-started.md)


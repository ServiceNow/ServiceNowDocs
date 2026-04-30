---
title: Sharing components among applications — Component libraries
description: Some applications may share the same basic structure and require nearly identical configuration data. Shared components in CDM enables you to use a component across several applications. For better organization, these shared components are managed in component libraries.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# Sharing components among applications — Component libraries

Some applications may share the same basic structure and require nearly identical configuration data. Shared components in CDM enables you to use a component across several applications. For better organization, these shared components are managed in component libraries.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Component libraries

Component libraries improve consistency and maintainability by ensuring a single source of truth for a component's config data across applications. You can use the unified view in the DevOps Config workspace or [CdmSharedLibraryApi](https://www.servicenow.com/docs/access?context=shared_libraries-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) REST API to create and maintain these libraries.

In this example, an organization sells tea on its website. Both the **Shopping-Cart** and **Browsing-Pane** application services make use of config data for product prices and photo appearance. To ensure that the config data is identical in both DevOps applications, each application uses shared components from the **Tea-Service** component library. The components are managed in the library and the applications each use two of the components from the library.

![Two applications use shared components from a component library](../image/cdm-comp-library-overview.png)

## Working with shared components

-   A user with the sn\_cdm.cdm\_admin role can create and manage a component library and create, add, and delete shared components in the library.
-   While working in an application changeset, you can add, update, or remove a shared component.
-   Applications can use any mix of components: components that are defined in the application \(direct components\) and components from a component library.
-   While working in an application changeset, you cannot modify a shared component in the same way as you can modify a direct component. A collection in an application can, however, override any value in a shared component.
-   For a shared component to be available for use in applications, the component must be in the **Published** state and the library that holds the component must be in the **Available** state.

    In the example, no application can use the **Flavor-Sort-settings** component because it has not been published.



---
title: Blueprints
description: Learn how blueprints define the structure of configuration experiences in CPQ and act as containers for fields, rules, layouts, and configurable products.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [The CPQ Configurator, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Blueprints

Learn how blueprints define the structure of configuration experiences in CPQ and act as containers for fields, rules, layouts, and configurable products.

Blueprints are the foundation of every configuration experience in CPQ. They define the structure, behavior, and visual layout of configurations by linking together all key elements—Fields, Rules, Layouts, and Configurable Products—into a single, manageable container. A blueprint represents the complete configuration logic for one product or experience and ensures consistent behavior across environments.

By using blueprints, administrators can design, deploy, and manage configuration workflows without duplicating content or logic. Each blueprint provides a modular, versioned space to build and refine configuration experiences safely before deploying them to production.

## Blueprint components

A blueprint brings together several key elements that define how a configuration behaves and appears to end users.

-   Fields: Capture data and user input. Blueprints associate only the subset of global fields relevant to that configuration experience.
-   Rules: Define the business logic that governs visibility, validation, product inclusion, and dynamic behaviors. Rules automatically connect to blueprints when their referenced fields are associated.
-   Layouts: Determine how fields and pickers appear in the UI. Each Layout is unique to a single blueprint, though a blueprint can contain multiple Layouts.
-   Configurable Products: Act as the entry point that launches the configuration defined by a blueprint. Multiple products can reference a single blueprint, but each product can only belong to one blueprint.
-   Enrichments: Extend logic beyond the rules engine to handle advanced scripting, external connections, or pricing enrichments.

## Blueprint life cycle

Blueprints are version-controlled entities that progress through a simple life cycle: creation, association, deployment, and migration.

-   Create: Define a new blueprint record and assign a name.
-   Associate: Link fields, rules, layouts, and configurable products to the blueprint.
-   Deploy: Make the blueprint available for end-user configurations in your environment.
-   Export/Import: Move blueprints between development, test, and production environments for versioning and reuse.

## Blueprint administration interface

Each blueprint record includes multiple tabs that provide visibility into its structure and related components:

-   Associated Fields: View all fields and subfields linked to the blueprint, organized by type \(Standard, Sets, product pickers, System\).
-   Related Rules: Review active and inactive rules automatically linked through field references.
-   Layouts: View or modify layouts associated with the blueprint. The most recently saved layout is used by default during runtime.
-   Configurable Products: View all products that launch the configuration experience defined by the blueprint.
-   Deployments: Track the most recent deployments, including date, user, and status.
-   Enrichments: Manage enrichment scripts that run outside the rules engine \(for example, initialization or pricing scripts\).

## Deployment and environments

Deployments make a blueprint visible to end users. All associated changes—fields, rules, layouts, and configurable products—become active upon deployment. Deployment notifications appear in the lower-left corner of the Admin interface, showing status updates such as “In Progress” or “Completed”.

Deployment behavior varies by environment type:

-   Production: Deployed blueprints remain active indefinitely.
-   Test: Automatically undeployed after 30 days of inactivity \(reset upon redeployment\).
-   Demo: Automatically undeployed every weekend for maintenance.

## Migration and version control

Blueprints can be exported and imported across environments to support development life cycles and version control. The exported package includes all related elements such as fields, rules, and layouts, allowing you to migrate configurations without manually recreating components.

When importing, administrators can update Product IDs, rule mappings, and environment-specific references to ensure compatibility in the target org. CPQ maintains unique IDs for each Configurable Product to preserve data integrity across environments.

## General guidelines

-   Create modular blueprints for each major product or configuration flow.
-   Use descriptive names and variable names for clarity and maintainability.
-   Review inactive rules regularly to prevent outdated logic from re-entering deployments.
-   Deploy changes in a controlled environment before promoting to production.
-   Document the enrichment scripts and custom external connections that are used by each blueprint.

**Related topics**  


[Set up blueprints](blueprints_101.md)


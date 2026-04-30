---
title: Migrating a blueprint from test to production
description: You can migrate a blueprint from a test environment to a production environment by using the Matrix Loader or by automating the migration using REST API calls.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Migrating a blueprint from test to production

You can migrate a blueprint from a test environment to a production environment by using the Matrix Loader or by automating the migration using REST API calls.

ServiceNow CPQ Administrators have two ways to migrate a blueprint from test to production migration: by using the Matrix Loader, and by using REST API automation.

-   Matrix Loader migration: From ServiceNow CPQ Admin, an admin can export a blueprint or blueprints to a ZIP file. The admin can then import these artifacts into the production environment. A new configurable product must be created and associated with the blueprint in the production environment. This can be done afterward or by creating the product and editing the blueprint yaml file with the new SFDC product2 id, product code, or partner id before deployment.
-   REST API automation: Robust REST API capabilities let implementers and customers automate test-to-production migration in a CI/CD process.

**Related topics**  


[Testing in non-production environments before migration](cpq-env-to-env-bp-migration-intro.md)


---
title: Migrating a blueprint from test to production
description: You can migrate a blueprint from a test environment to a production environment using the Matrix Loader or REST API automation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/how\_can\_i\_accomplish\_test-to-production\_migration.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Migrating a blueprint from test to production

You can migrate a blueprint from a test environment to a production environment using the Matrix Loader or REST API automation.

CPQ administrators have two ways to migrate a blueprint from test to production: by using the Matrix Loader, and by using REST API automation.

-   Matrix Loader migration: From CPQ admin interface, an admin can export a blueprint or blueprints to a ZIP file. The admin can then import these artifacts into the production environment. Create configurable product and associate it with the blueprint in the production environment. You can do this afterward or create the product and edit the blueprint yaml file with the new SFDC product2 id, product code, or partner id before deployment.
-   REST API automation: Robust REST API capabilities enable implementers and customers to automate test-to-production migration in a CI/CD process.

**Related topics**  


[Testing in non-production environments before migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-env-to-env-bp-migration-intro.md)


---
title: API overview and resources
description: Learn about the APIs that are available in ServiceNow CPQ to manage configurations.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# API overview and resources

Learn about the APIs that are available in ServiceNow CPQ to manage configurations.

ServiceNow CPQ provides APIs for both the end user \(runtime\) for configurations and the administrative side for setup and management.

The runtime APIs support the standard create, read, update, and delete functions for ServiceNow CPQ configurations, along with the ability to retrieve bill of materials \(BOM\) data from ServiceNow CPQ. These APIs can be used to build a headless or custom UI for end users to create ServiceNow CPQ configurations.

Administrative APIs can be used to work with blueprints, fields, sets, product pickers, rules, managed tables, and the Matrix Loader for imports and exports. The admin APIs can be integrated or automated to perform routine tasks like data migration.

## API resources

The following resources can help you get started with ServiceNow CPQ APIs.

To view a Github repository with OpenAPI specifications and Postman collections for ServiceNow CPQ APIs, see:

[API Documentation](https://github.com/logikioopensource/API-Documentation)

For interactive and explorable API documentation with code examples for both runtime and admin APIs, see:

[ServiceNow CPQ API Reference](https://api-docs.logik.io/#introduction)

## Authenticating API calls

Runtime API calls are authenticated using runtime client tokens defined in ServiceNow CPQ Admin. For more information about runtime API calls and runtime client tokens, see:

[Intro to runtime API calls](intro_to_runtime_api_calls.md)

Administrative API calls are authenticated with admin API tokens that are also set up in ServiceNow CPQ Admin. For more information about admin API tokens and permissions, see:

[Intro to admin API keys](cpq-admin-api-keys.md)

**Related topics**  


[Runtime APIs](logik_io_runtime_apis.md)

[Authenticating ServiceNow CPQ API calls](cpq-authenticating-api-calls.md)

[Additional configuration APIs](logik_io_additional_configuration_apis.md)

[Admin APIs: Blueprint import and export](cpq-admin-apis-blueprint-import-and-export.md)

[Admin APIs: Managed tables](admin_apis_managed_tables.md)


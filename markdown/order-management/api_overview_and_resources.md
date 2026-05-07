---
title: API overview and resources
description: Learn about the APIs that are available in CPQ to manage configurations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# API overview and resources

Learn about the APIs that are available in CPQ to manage configurations.

CPQ provides APIs for both the end user \(runtime\) for configurations and the administrative side for setup and management.

The runtime APIs support the standard create, read, update, and delete functions for CPQ configurations, along with the ability to retrieve bill of materials \(BOM\) data from CPQ. These APIs can be used to build a headless or custom UI for end users to create CPQ configurations.

Administrative APIs can be used to work with blueprints, fields, sets, product pickers, rules, managed tables, and the Matrix Loader for imports and exports. The admin APIs can be integrated or automated to perform routine tasks like data migration.

## API resources

The following resources can help you get started with CPQ APIs.

To view a Github repository with OpenAPI specifications and Postman collections for CPQ APIs, see:

[API Documentation](https://github.com/logikioopensource/API-Documentation)

For interactive and explorable API documentation with code examples for both runtime and admin APIs, see:

[CPQ API Reference](https://api-docs.logik.io/#introduction)

## Authenticating API calls

Runtime API calls are authenticated using runtime client tokens defined in CPQ Admin. For more information about runtime API calls and runtime client tokens, see:

[Intro to runtime API calls](intro_to_runtime_api_calls.md)

Administrative API calls are authenticated with admin API tokens that are also set up in CPQ Admin. For more information about admin API tokens and permissions, see:

[Intro to admin API keys](cpq-admin-api-keys.md)

**Related topics**  


[Runtime APIs](logik_io_runtime_apis.md)

[Authenticating CPQ API calls](cpq-authenticating-api-calls.md)

[Additional configuration APIs](logik_io_additional_configuration_apis.md)

[Admin APIs: Blueprint import and export](cpq-admin-apis-blueprint-import-and-export.md)

[Admin APIs: Managed tables](admin_apis_managed_tables.md)


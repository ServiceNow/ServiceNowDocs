---
title: Configuration model
description: Lux makes a component's behavior configurable at three levels: code, admin policy, and individual preference without three separate systems to learn. You add one decorator, @config, to a class field to opt a property into all of it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/configuration-model.html
release: zurich
topic_type: concept
last_updated: "2026-10-03"
reading_time_minutes: 2
keywords: [Configuration model, Three players, Default value, Promotion and upgrade safety, What this chapter covers]
breadcrumb: [Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Configuration model

Lux makes a component's behavior configurable at three levels: code, admin policy, and individual preference without three separate systems to learn. You add one decorator, `@config`, to a class field to opt a property into all of it.

Configuration is stored as metadata override layers rather than as a code fork, so an admin's changes reapply cleanly across upgrades.

## Three players

Every configurable value passes through the same three parties:

-   **Declare: developer**

    Tags which properties are configurable, sets the code-level default, and defines the choices, types, and labels that drive the generated config UI. Nothing is editable until it is declared.

-   **Configure: customer admin**

    Configures shipped pages and widgets directly on the live page, in non-production, then promotes the change through an update set.

-   **Personalize: end user**

    Adjusts their own view within admin-defined bounds.


As the developer you only need to read `this.propertyName` in your component. The framework resolves the value that getter returns.

Configuration is not a replacement for UI Builder, a tool for building widgets or pages, or a standalone no-code builder. This is a pro-code workflow: a developer writes the declaration, and an admin configures what the developer declared.

## Default value

A `@config` property resolves to its developer default, the value assigned in your code.

## Promotion and upgrade safety

`sys_aix_configuration` extends `sys_metadata`, so admin configuration participates in update sets exactly like a business rule or a UI policy; no special export or import path.

**Related topics**  


[Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configurable-properties.md)

[Inline configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/inline-configuration.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/admin-experience.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/admin-experience.md)

[Regions and the wrapper contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/regions-and-the-wrapper-contract.md)

[Theming model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/theming-model.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-schema.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-schema.md)


---
title: Advanced scripting
description: As an app grows in complexity, it may reach the limits of what business rules, script includes, and Flow Designer actions can accomplish through configuration alone. Advanced scripting means writing directly against ServiceNow's server-side JavaScript APIs to handle logic that requires more precision or flexibility than low-code tools provide.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/advanced-scripting.html
release: australia
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 2
keywords: [low-code, app development, advanced scripting]
breadcrumb: [Build your first app, Standard app development, Getting Started guide for developers, Building applications]
---

# Advanced scripting

As an app grows in complexity, it may reach the limits of what business rules, script includes, and Flow Designer actions can accomplish through configuration alone. Advanced scripting means writing directly against ServiceNow's server-side JavaScript APIs to handle logic that requires more precision or flexibility than low-code tools provide.

## When does advanced scripting apply?

The primary API family for this work is the Glide API. Common Glide APIs include:

-   GlideRecord: Query and manipulate table data in script
-   GlideSystem: Access system-level functions like logging and user context
-   GlideDateTime: Handle date and time calculations

Advanced scripting still happens within the same building blocks you have already learned. The difference at the advanced level is the depth of control: you write the full logic yourself rather than configuring pre-built actions or conditions. Common locations for advanced scripts include:

-   Business rules and script includes for server-side logic
-   Flow Designer actions that call script includes to incorporate custom logic into automated workflows

## What is ServiceNow Fluent, and when would I use it?

ServiceNow Fluent is a declarative, TypeScript-based domain-specific language \(DSL\) for defining your application's metadata directly in source code rather than through form and builder interfaces. Instead of configuring a table, business rule, or ACL through the platform UI, you define it in a `.now.ts` file, so your app's structure lives in version-controlled source files alongside the rest of your application.

As a low-code developer getting started in ServiceNow Studio, you will likely configure most metadata through the platform UI. ServiceNow Fluent becomes relevant when you move to more advanced development workflows, particularly if your team uses the ServiceNow IDE or ServiceNow SDK. Key capabilities include:

-   Two-way synchronization, when changes sync between your source code and the platform regardless of which side you edit
-   Dedicated APIs for common metadata types including tables, roles, ACLs, and business rules
-   A general-purpose Record API for metadata types that don't have a dedicated Fluent API

A small number of metadata types can't currently be represented as Fluent code and remain as XML files in the metadata directory. For more information, see [Building applications in source code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications-source-code.md).

**Parent Topic:**[Build your first application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-your-first-app.md)


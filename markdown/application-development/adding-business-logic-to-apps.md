---
title: Adding business logic to apps
description: Business logic lets your app respond automatically to data changes, enforce rules, and perform calculations without requiring user intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/adding-business-logic-to-apps.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
keywords: [low-code, getting started guide]
breadcrumb: [Build your first app, Standard app development, Getting Started guide for developers, Building applications]
---

# Adding business logic to apps

Business logic lets your app respond automatically to data changes, enforce rules, and perform calculations without requiring user intervention.

## Business rules and script includes

In ServiceNow, two of the primary tools for adding server-side business logic are business rules and script includes. Understanding both, and how they work together, helps you build apps that are reliable, maintainable, and consistent.

Business rules are server-side scripts that run automatically when a record in a specific table is inserted, updated, deleted, or queried. Attach a business rule to a table, set conditions that control when it fires, and write the logic that should execute. For example, a business rule could automatically set a priority field based on the value of another field whenever a new record is created. Business rules run at four points in a record's lifecycle:

-   Before: Runs before the record is written to the database, so you can modify field values before they are saved
-   After: Runs after the record is saved, so you can trigger follow-on actions based on the committed data
-   Async: Runs in the background after the record is saved, so it does not slow down the user's experience
-   Display: Runs when a record is loaded for display, before it reaches the user's browser

Script includes are reusable JavaScript libraries that you define once and call from multiple places in your app. Unlike business rules, script includes don't fire automatically. You call them explicitly from a business rule, another script include, or an API. This makes them ideal for logic that needs to run in more than one context. For example, if several business rules have to calculate the same value, you write that calculation once in a script include and call it from each rule, so that any future changes only have to be made in one place.

Business rules and script includes are most effective when used together. Keeping business rules short and focused on triggering conditions, while moving complex logic into script includes, makes code easier to read, test, and maintain. This separation of concerns is a standard for ServiceNow development and becomes especially important as your app grows in complexity.

**Parent Topic:**[Build your first application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-your-first-app.md)


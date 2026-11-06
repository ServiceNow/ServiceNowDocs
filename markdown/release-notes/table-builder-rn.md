---
title: Table Builder release notes
description: The ServiceNow Table Builder application is a centralized way to build tables, forms, and display logic. See the following sections for release notes by version.Table Builder was enhanced in the Brazil patch X release to address issues with the formula editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/table-builder-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Table Builder release notes

The ServiceNow® Table Builder application is a centralized way to build tables, forms, and display logic. See the following sections for release notes by version.

## About Table Builder

-   Build your app’s tables, forms, and display logic from one place, without switching between separate tools.
-   Edit table structure and records together in one view, so you can see how data changes as you build.
-   Bring existing data into your app by importing it from a spreadsheet into a new or existing table.
-   Connect your data by adding reference fields that relate one table to another.
-   Control who can access your data by configuring table permissions as you build.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Install Table Builder by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Browser requirements**

    Internet Explorer isn't supported.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/build-automate-rn-landing.md)

## Brazil patch X

Table Builder was enhanced in the Brazil patch X release to address issues with the formula editor.

### What's new

-   **New role required to add a formula to a column**

    Accessing the formula editor in Table Builder now requires the formula\_read role. Previously, the formula editor stalled in the loading state. This issue is related to PRB2093578.



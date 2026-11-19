---
title: Industrial Centerlines release notes
description: The ServiceNow Industrial Centerlines application helps you identify and maintain critical equipment settings by specifying baseline targets and ranges, and routinely verifying that the settings conform to the defined standard. See the following sections for release notes by version.Manage setting definitions, setting plans, and setting specifications on operational equipment, author centerline standards in the Standards hub, and manage centerline tasks in the Digital Factory Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/icw-centerlines-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-28"
reading_time_minutes: 2
keywords: [centerline, setting definition, setting plan, setting specification, centerline standard]
breadcrumb: [Industrial Connected Workforce release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Industrial Centerlines release notes

The ServiceNow® Industrial Centerlines application helps you identify and maintain critical equipment settings by specifying baseline targets and ranges, and routinely verifying that the settings conform to the defined standard. See the following sections for release notes by version.

## About Industrial Centerlines

-   Standardize equipment base conditions by defining the operator-modifiable settings for each piece of equipment, with value types such as numeric range, numeric target, choice, or text.
-   Establish acceptable values, ranges, and targets for each setting through setting specifications grouped in setting plans.
-   Automate confirmation scheduling with centerline standards that define which settings to verify and when.
-   Reduce quality and reliability losses by having operators confirm settings during centerline tasks, and create deviation tasks when a setting doesn't conform to the standard.

See [Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/icw-centerlining-overview.md) for more information.

## Activation and other requirements

-   **Activation information**

    Industrial Centerlines doesn't have its own SKU. It's included in the ICW Advanced SKU. You can request ICW Advanced from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Industrial Connected Workforce release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/industrial-connected-workforce-rn-landing.md)

## Version 2.0.4

Manage setting definitions, setting plans, and setting specifications on operational equipment, author centerline standards in the Standards hub, and manage centerline tasks in the Digital Factory Workspace.

### What's new

-   **[Setting definitions on operational equipment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/icw-setting-definitions-and-value-types.md)**

    Define each configurable parameter directly on the Settings tab of an equipment record, with type-specific fields for choice and numeric range settings and an optional effective date range. Setting definitions go through an approval workflow before they can be used in centerline tasks. Duplicate one or more definitions to reuse their configuration, and retire published definitions that are no longer valid.

-   **[Setting plans and setting specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/icw-setting-plans-and-specifications.md)**

    Group the standard values for a piece of equipment in a setting plan, and define the target values and limits for each setting definition in a setting specification. The specification form shows only the fields that apply to the setting type, such as limit levels for a numeric range or a choice target for a choice setting. Duplicate a specification to reuse its values.

-   **[Centerline standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/icw-centerline-standards.md)**

    Create a centerline standard from the Standards hub to define the settings that operators check during a centerline audit. Use the condition builder to select the setting definitions for the standard, and set the material scope that's available when operators run the task on mobile. Centerline standards follow the same approval, versioning, and template workflow as Industrial Guided Tasks standards.

-   **[Centerline tasks in the Digital Factory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/centerline-tasks-workspace.md)**

    View, filter, and manage the tasks generated from centerline standards in a dedicated list in the Digital Factory Workspace. Authorized users can edit task data fields and assign a task to themselves using the Assign to me action. Centerline tasks are executed in the Industrial Connected Workforce Mobile Experience.



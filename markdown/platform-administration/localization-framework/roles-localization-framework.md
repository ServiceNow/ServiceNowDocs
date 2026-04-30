---
title: Localization Framework Roles
description: Localization Framework uses different roles to manage different aspects of the application.Manage the following aspects of the Localization Framework application.Request translations for all the configured artifacts into one or more languages.Provide translations for the requested artifact items and approve and publishe the translations.Provides the ability for the users to translate the content without the need of a localization task.Owns the localization projects. Adds all the localization requested items to the projects. Only a Localization manager has the authority to start the project.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework Roles

Localization Framework uses different roles to manage different aspects of the application.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Explore Localization Framework](../concept/exploring-localization-framework.md)

## Localization administrator \[localization\_admin\]

Manage the following aspects of the Localization Framework application.

-   Configures the supported artifacts and custom artifacts for Localization Framework.
-   Configures localization settings for the activated languages.
-   Can request translations into multiple languages for Service Catalog items, Virtual Agent topics, or for any custom artifacts from their respective artifact tables.
-   Can request translations for Service Catalog items, Virtual Agent topics, or for any custom artifact for a particular language from their respective artifact reports in the insights dashboard.
-   Can configure RWS and XTM TMS and can create and configure a custom TMS by inheriting the following roles:
    -   flow\_designer: Can edit the TMS subflows and can create a new TMS configuration record.
    -   connection\_admin: Can access the connections and credentials tables and records.
-   Owns the localization insights dashboard and reports. Can execute the scheduled jobs to display the reports on the dashboard.
-   Views the localization health of the system.
-   localization\_admin role inherits the lcoalization\_requestor, localization\_editor, and localization\_fulfiller role.

### Contains Roles

List of roles contained within the role.

-   localization\_fulfiller
-   localization\_manager
-   localization\_requestor
-   localization\_editor

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Localization requester \[localization\_requestor\]

Request translations for all the configured artifacts into one or more languages.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Localization requester can fulfill translations by inheriting the localization\_fulfiller role.

## Localization fulfiller \[localization\_fulfiller\]

Provide translations for the requested artifact items and approve and publishe the translations.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Fulfillers can translate a localization task in the following ways:

-   Use manual translation if the fulfiller understands both the source and the target language.
-   Use machine translation by using the translator configured in the translation preferences.
-   Exports data to a third-party translator and imports it back after translations.
-   Sends the data via email for translations and receives the translated data back via email.
-   Sends translatable data to a translation management system \(TMS\) for translations.
-   Verifies and approves the translations.
-   Publishes the translations if the language setting workflow has no approval flow.

## Localization editor \[localization\_editor\]

Provides the ability for the users to translate the content without the need of a localization task.

### Contains Roles

The Localization editor role contains the Localization Requestor \[localization\_requestor\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Users assigned to this role can translate content from Virtual Agent Designer NLU Workbench, and Document Templates of HR Service Delivery.

A localization editor can translate the content using machine translation, and also by exporting and importing the content.

## Localization manager \[localization\_manager\]

Owns the localization projects. Adds all the localization requested items to the projects. Only a Localization manager has the authority to start the project.

### Contains Roles

The Localization editor role contains the Localization Fulfiller \[localization\_fulfiller\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

If the Localization Framework Hub and Spoke architecture is set up, the localization\_manager role has access to the following tables on the hub instance:

-   Localization Framework Hub Translation Request \[sn\_lf\_hub\_translation\_request\]
-   Localization Framework Hub Translation Item \[sn\_lf\_hub\_translation\_item\]

For more information, see [Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md)


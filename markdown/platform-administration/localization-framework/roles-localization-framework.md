---
title: Localization Framework Roles
description: Localization Framework uses different roles to manage different aspects of the application. The roles from Localization Framework are also used in Localization Workspace.Manage the following aspects of the Localization Framework application. This role is also used in Localization Workspace.Request translations for all the configured artifacts into one or more languages. This role is used in Localization Framework and Localization Workspace.Provide translations for the requested artifact items and approve and publish the translations. This role is used in Localization Framework and Localization Workspace.Localization editors can translate content without the need for a localization task. This role is used in Localization Framework and Localization Workspace.Owns the localization projects and adds the localization requested items to the projects. Only a Localization manager has the authority to start the project. This role is used by Localization Framework and Localization Workspace.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Localization Framework Roles

Localization Framework uses different roles to manage different aspects of the application. The roles from Localization Framework are also used in Localization Workspace.

For more information about Localization Workspace, see [Localization Workspace](../../localization-workspace/concept/localization-workspace.md). To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Explore Localization Framework](../concept/exploring-localization-framework.md)

## Localization administrator \[localization\_admin\]

Manage the following aspects of the Localization Framework application. This role is also used in Localization Workspace.

-   Configures the supported artifacts and custom artifacts for Localization Framework.
-   Configures localization settings for the activated languages.
-   Can request translations into multiple languages for Service Catalog items, Virtual Agent topics, or for any custom artifacts from their respective artifact tables.
-   Can request translations for Service Catalog items, Virtual Agent topics, or for any custom artifact for a particular language from their respective artifact reports in the insights dashboard.
-   Can configure RWS and XTM TMS and can create and configure a custom TMS by inheriting the following roles:
    -   flow\_designer: Can edit the TMS subflows and can create a new TMS configuration record.
    -   connection\_admin: Can access the connections and credentials tables and records.
-   Owns the localization insights dashboard and reports. Can execute the scheduled jobs to display the reports on the dashboard.
-   Views the localization health of the system.
-   Inherits the localization\_editor, localization\_fulfiller, localization\_manager, and localization\_requestor roles.

### Contains Roles

List of roles contained within the role.

-   localization\_editor
-   localization\_fulfiller
-   localization\_manager
-   localization\_requestor

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

When working in Localization Workspace, the role sn\_cd.content\_admin is required to see Content Publishing artifacts.

## Localization requester \[localization\_requestor\]

Request translations for all the configured artifacts into one or more languages. This role is used in Localization Framework and Localization Workspace.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Localization requester can fulfill translations by inheriting the localization\_fulfiller role.

When working in Localization Workspace, the role sn\_cd.content\_admin is required to see Content Publishing artifacts.

## Localization fulfiller \[localization\_fulfiller\]

Provide translations for the requested artifact items and approve and publish the translations. This role is used in Localization Framework and Localization Workspace.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Fulfillers can translate a localization task in the following ways:

-   Manually translate in the Localization Task web page.
-   Use machine translation by submitting the item to a third-party translator configured in Dynamic Translation.
-   Export source files to a third-party translator and import the returned translations.
-   Send the source files for translation via email and receive the translated files via email.
-   Send translatable items to a translation management system \(TMS\).
-   Verify and approve the translations.
-   Publish the translations if the language workflow has no approval flow.

## Localization editor \[localization\_editor\]

Localization editors can translate content without the need for a localization task. This role is used in Localization Framework and Localization Workspace.

### Contains Roles

The Localization editor role contains the Localization Requester \[localization\_requestor\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Users assigned to this role can translate content from Virtual Agent Designer NLU Workbench, and Document Templates of HR Service Delivery.

A localization editor can translate the content using machine translation, and also by exporting and importing the content.

## Localization manager \[localization\_manager\]

Owns the localization projects and adds the localization requested items to the projects. Only a Localization manager has the authority to start the project. This role is used by Localization Framework and Localization Workspace.

### Contains Roles

The Localization manager role contains the Localization fulfiller \[localization\_fulfiller\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

If the Localization Framework Hub and Spoke architecture is activated, the localization\_manager role has access to the following tables on the hub instance:

-   Localization Framework Hub Translation Request \[sn\_lf\_hub\_translation\_request\]
-   Localization Framework Hub Translation Item \[sn\_lf\_hub\_translation\_item\]

For more information, see [Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md).


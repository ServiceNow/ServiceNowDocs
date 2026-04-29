---
title: Configuration Hub in Localization Workspace
description: Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuration Hub in Localization Workspace

Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.

## Overview of Configuration Hub

Localization Workspace extends other ServiceNow AI Platform applications related to localization. Configuring these dependent applications is a prerequisite to working with Localization Workspace. From version 2.0.2, Configuration Hub gives admins access to tables and properties in these applications from the Localization Workspace interface.

**Note:** Any updates you make in Configuration Hub are saved to tables in the target application.

To open Configuration Hub:

With the localization\_admin or the admin role, navigate to **All** &gt; **Localization Workspace** &gt; **Configuration Hub**. Alternatively, you can select the hub's icon while in the workspace. The navigation pane within Configuration Hub lists applications and their components. Select the name of a component to open its table in a workspace pane.

![Configuration Hub in Localization Workspace, showing the admin's view. Tables and properties in both Localization Framework and Dynamic Translation are available.](../image/lw-configuration-hub1.png)

**Note:** In Configuration Hub, Dynamic Translation is displayed to the admin role only. The localization\_admin role can't view Dynamic Translation.

## Localization Framework

The following components of Localization Framework are available to the localization\_admin or admin role, from Localization Workspace.

-   [Artifact configurations](../../localization-framework/concept/framework-configuration.md) \(the content types in Localization Workspace are built upon artifacts\).
-   [Settings](../../localization-framework/concept/localization-settings.md).
-   [TMS Configurations](../../localization-framework/concept/tms-configuration.md) \(required only if you use a TMS as your translation service provider\).
-   Properties \(visible to the admin role only\).
-   Spoke Configurations \(used for the [hub and spoke architecture](../../localization-framework/concept/localization-framework-hub-spoke-architecture.md)\).
-   Spoke settings \(used for the [hub and spoke architecture](../../localization-framework/concept/localization-framework-hub-spoke-architecture.md)\).
-   [Language Code Mappings](../../dynamic-translation/concept/language-mapper-dt.md) \(may be required if you use a custom third-party translation service\).

## Dynamic Translation

Dynamic Translation is required to use machine translation on your instance. The following components of Dynamic Translation are available to the admin role, from Localization Workspace.

-   [Translator Configurations](../../dynamic-translation/concept/integration-with-other-translation-services.md).
-   [Exclusion Rules](../../dynamic-translation/concept/dyn-translation-exclusion-framework.md).
-   [Create New Rules](../../dynamic-translation/task/dyn-translation-add-exclusion-rule.md).
-   [Test Exclusion Rule](../../dynamic-translation/task/dyn-translation-test-exclusion-rule.md).
-   [Exclusion Provider Pattern](../../dynamic-translation/task/dyn-translation-exclusion-provider.md).
-   [Properties](../../dynamic-translation/reference/dynamic-translation-properties.md).

Guided Setups are also available to the admin role, to outline the initial process of configuring Localization Workspace and its prerequisites. Navigate to **All** &gt; **Localization Workspace** &gt; **Localization Framework Guided Setup** or **Localization Workspace Guided Setup**.

**Parent Topic:**[Configuring Localization Workspace](configuring-localization-workspace.md)


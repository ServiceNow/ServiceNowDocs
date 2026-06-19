---
title: Configuration Hub in Localization Workspace
description: Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/localization-workspace/lw-configuration-hub.html
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2025-12-08"
reading_time_minutes: 3
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Configuration Hub in Localization Workspace

Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.

## Overview of Configuration Hub

Localization Workspace extends other ServiceNow AI Platform applications related to localization. Configuring these dependent applications is a prerequisite to working with Localization Workspace. From version 2.0.2, Configuration Hub gives admins access to tables and properties in these applications from the Localization Workspace interface.

**Note:** Any updates you make in Configuration Hub are saved to tables in the target application.

To open Configuration Hub:

With the localization\_admin or the admin role, navigate to **All** &gt; **Localization Workspace** &gt; **Configuration Hub**. Alternatively, you can select the hub's icon while in the workspace. The navigation pane within Configuration Hub lists applications and their components. Select the name of a component to open its table in a workspace pane.

\[Omitted image "lw-configuration-hub1.png"\] Alt text: Configuration Hub in Localization Workspace, showing the admin's view. Tables and properties in both Localization Framework and Dynamic Translation are available.

**Note:** In Configuration Hub, Dynamic Translation is displayed to the admin role only. The localization\_admin role can't view Dynamic Translation.

## Localization Framework

The following components of Localization Framework are available to the localization\_admin or admin role, from Localization Workspace.

-   [Artifact configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/framework-configuration.md) \(the content types in Localization Workspace are built upon artifacts\).
-   [Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/localization-settings.md).
-   [TMS Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/tms-configuration.md) \(required only if you use a TMS as your translation service provider\).
-   Properties \(visible to the admin role only\).
-   Spoke Configurations \(used for the [hub and spoke architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/localization-framework-hub-spoke-architecture.md)\).
-   Spoke settings \(used for the [hub and spoke architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/localization-framework-hub-spoke-architecture.md)\).
-   [Language Code Mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/language-mapper-dt.md) \(may be required if you use a custom third-party translation service\).

## Dynamic Translation

Dynamic Translation is required to use machine translation on your instance. The following components of Dynamic Translation are available to the admin role, from Localization Workspace.

-   [Translator Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/integration-with-other-translation-services.md).
-   [Exclusion Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-exclusion-framework.md).
-   [Create New Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-add-exclusion-rule.md).
-   [Test Exclusion Rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-test-exclusion-rule.md).
-   [Exclusion Provider Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-exclusion-provider.md).
-   [Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dynamic-translation-properties.md).

Guided Setups are also available to the admin role, to outline the initial process of configuring Localization Workspace and its prerequisites. Navigate to **All** &gt; **Localization Workspace** &gt; **Localization Framework Guided Setup** or **Localization Workspace Guided Setup**.

**Parent Topic:**[Configuring Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/configuring-localization-workspace.md)


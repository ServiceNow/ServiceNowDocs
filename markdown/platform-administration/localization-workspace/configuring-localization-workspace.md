---
title: Configuring Localization Workspace
description: Before using Localization Workspace, configure prerequisites, dependencies, and translation providers.
locale: en-US
release: yokohama
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2025-09-19"
reading_time_minutes: 3
breadcrumb: [Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring Localization Workspace

Before using Localization Workspace, configure prerequisites, dependencies, and translation providers.

## Configuration overview

Localization Workspace builds upon the functionality of other ServiceNow AI Platform applications related to localization. These applications are activated with Localization Workspace if they are not already installed. You must complete the configuration of these applications before configuring Localization Workspace.

1.  [Install Localization Workspace](../task/install-localization-workspace.md).

    You can install the application \(sn\_lw\) if you have the admin role. The application installs related applications and plugins if they are not already installed. Localization Workspace requires a Pro or Pro+ subscription.

2.  Configure prerequisites.

    In the Yokohama release, you must confirm access to the \[sn\_lf\_setting\] table. The admin role is required for this step. The localization\_admin role can't complete this step. See [Confirm access to Settings table](../task/lw-confirm-access-settings-table.md).

3.  Configure dependencies.
    -   [Internationalization \(i18n\) and language plugins](../../localization/concept/exploring-system-localization.md): Install language plugins as part of System Localization. Choose your instance's languages according to your business requirements.
    -   [Localization Framework:](../../localization-framework/concept/exploring-localization-framework.md) Configure Localization Framework as follows.

        Assign roles. See [Localization Framework Roles](../../localization-framework/reference/roles-localization-framework.md#).

        Configure artifacts. See [Artifact configurations](../../localization-framework/concept/framework-configuration.md).

        **Note:** When using Content Publishing artifacts, add the role sn\_cd.content\_admin to your Localization Workspace sys user group. This role is needed to see artifacts related to Content Publishing from Localization Workspace.

        Configure settings, including for the workflows of translation tasks. See [Localization Framework settings](../../localization-framework/concept/localization-settings.md).

        Configure a Translation Management System if your organization uses one. See [Translation Management System configurations](../../localization-framework/concept/tms-configuration.md).

    -   [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md): If you use machine translation to fulfill translation requests, configure Dynamic Translation, including setting up a translator configuration. See [Integration with other translation services](../../dynamic-translation/concept/integration-with-other-translation-services.md).
4.  [Configure a translation provider](../task/lw-configure-translation-provider.md) in Localization Workspace. Translation providers in Localization Workspace are different from translator configurations in Dynamic Translation.

![The Translation Providers list in Localization Workspace.](../image/configuring-localization-workspace1.png)

-   **[Install Localization Workspace](../task/install-localization-workspace.md)**  
You can install the Localization Workspace application \(sn\_lw\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed. Demo data isn't available.
-   **[Confirm access to Settings table](../task/lw-confirm-access-settings-table.md)**  
As part of the configuration for Localization Workspace in Yokohama, confirm access to the Settings table of Localization Framework.
-   **[Configure a translation provider](../task/lw-configure-translation-provider.md)**  
Set up translation providers as part of configuring Localization Workspace. For each target language you can configure multiple translation providers with their pricing.

**Parent Topic:**[ServiceNow AI Platform translation and localization](../../managing-data/concept/translation-and-localization.md)


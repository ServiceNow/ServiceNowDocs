---
title: Configuring Localization Workspace
description: Before using Localization Workspace, configure prerequisites, dependencies, and translation service providers.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring Localization Workspace

Before using Localization Workspace, configure prerequisites, dependencies, and translation service providers.

## Configuration overview

Localization Workspace builds upon the functionality of other ServiceNow AI Platform applications related to localization. These applications are activated with Localization Workspace if they are not already installed. You must complete the configuration of these applications before configuring Localization Workspace.

**Note:** From version 2.0.2, the Localization Workspace interface provides two [Guided Setups](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) to lead admins through the process of configuration, as follows.

-   With the admin role, navigate to **Localization Workspace** &gt; **Localization Framework Guided Setup** for the prerequisite application.
-   Next, navigate to **Localization Workspace** &gt; **Localization Workspace Guided Setup**.

After the initial setup, admins can make adjustments to configurations by using the [Configuration Hub in Localization Workspace](lw-configuration-hub.md).

1.  [Install Localization Workspace](../task/install-localization-workspace.md).

    You can install the application \(sn\_lw\) if you have the admin role. The application installs related applications and plugins if they are not already installed. Check your entitlements to determine whether you have access to Localization Workspace.

2.  Configure prerequisites as needed.

    In the Zurich release, access to the Settings table \[sn\_lf\_setting\] is configured by default. However, in the Yokohama release, you must confirm access to the Settings table \[sn\_lf\_setting\]. The admin role is required for this step. See [Confirm access to Settings table](../task/lw-confirm-access-settings-table.md).

3.  Configure dependencies.
    -   [Internationalization \(i18n\) and language plugins](../../localization/concept/exploring-system-localization.md): Install language plugins as part of System Localization. Choose your instance's languages according to your business requirements.
    -   [Localization Framework:](../../localization-framework/concept/exploring-localization-framework.md) Configure Localization Framework as follows.

        Assign roles. Localization Workspace uses roles from Localization Framework, along with one role specific to Localization Workspace.

        1.  Add Localization Framework roles as needed. See [Localization Framework Roles](../../localization-framework/reference/roles-localization-framework.md#).
        2.  Add the Localization Workspace user role sn\_lw.user. This role is required for all users in Localization Workspace.
        Create at least one group in the Groups \[sys\_user\_group\] table and add roles to the group, then assign your localization users to the appropriate group.

        Configure artifacts. See [Artifact configurations](../../localization-framework/concept/framework-configuration.md).

        **Note:** The role sn\_cd.content\_admin is required to see Content Publishing items from Localization Workspace. If your users need to request translations for Content Publishing material, add sn\_cd.content\_admin to the appropriate group.

        The sn\_cd.content\_admin role is different from the content\_admin role. From version 3.0.0, the sn\_lw.user role contains the content\_admin role.

        Configure settings, including for the workflows of translation tasks. See [Localization Framework settings](../../localization-framework/concept/localization-settings.md). Also on the Localization Framework settings table \(sn\_lf\_settings\), in the **Project Preferences** tab, ensure that check boxes are set as follows.

        -   **Enable projects**: Selected.
        -   **Enable auto creation**: Cleared \(unselected\).
        Configure a Translation Management System if your organization uses one. See [Translation Management System configurations](../../localization-framework/concept/tms-configuration.md).

    -   [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md): If you use machine translation to fulfill translation requests, configure Dynamic Translation, including setting up a translator configuration. See [Integration with other translation services](../../dynamic-translation/concept/integration-with-other-translation-services.md).
4.  Configure custom artifacts, if you plan to use your own artifacts in Localization Workspace. See [Create and configure a custom artifact](../../localization-framework/task/create-configure-custom-artifact.md).

    Set cross-scope access privileges for your artifacts. For more information see [Cross-scope privileges for Localization Workspace](../task/lw-cross-scope-privilege.md).

    Set Restricted Caller Access for Localization Workspace to enable access to artifact resources, if needed. The admin role is required for this step. See [Restricted Caller Access for Localization Workspace](../task/lw-restricted-caller-access.md).

5.  [Configure languages](lw-language-setup.md) in Localization Workspace. Language providers in Localization Workspace are different from translator configurations in Dynamic Translation.

    **Note:** From version 3.0.0, two guided tours are available. One guided tour assists with configuring a language provider, accessible to users with the Localization administrator role \(localization\_admin\). The other guided tour assists with configuring language groups, and is accessible to the Localization administrator role and the Localization requester role \(localization\_requestor\). Find the guided tours by selecting the Help Center icon ![](../../../common/image/Banner_HelpIcon.png) on the Localization Workspace Home screen.

    ![Guided Tours for setting up language providers and groups are accessed from the Help Center icon on the Home screen of Localization Workspace. Availability depends on role.](../image/lw-guidedtours-langs-helpcenter-a.png)


![Language setup in Localization Workspace, opened to display the Language Providers list.](../image/configuring-localization-workspace1.png)

-   **[Install Localization Workspace](../task/install-localization-workspace.md)**  
You can install the Localization Workspace application \(sn\_lw\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed. Demo data isn't available.
-   **[Confirm access to Settings table](../task/lw-confirm-access-settings-table.md)**  
As part of the configuration for Localization Workspace, confirm access to the Settings table of Localization Framework.
-   **[Cross-scope privileges for Localization Workspace](../task/lw-cross-scope-privilege.md)**  
After you create custom translation artifacts, set cross-scope privileges so that your artifacts can be accessed from Localization Workspace.
-   **[Restricted Caller Access for Localization Workspace](../task/lw-restricted-caller-access.md)**  
Give Localization Workspace access to your content by setting Restricted Caller Access privileges. Setting these privileges is required only when target tables or scripts are restricted.
-   **[Configuration Hub in Localization Workspace](lw-configuration-hub.md)**  
Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.
-   **[Language Asset Management](lw-language-asset-management.md)**  
Enhance localization in your instance with Language Asset Management in Localization Workspace. You can upload glossaries to Language Asset Management for editing and storage.
-   **[Language setup in Localization Workspace](lw-language-setup.md)**  
Language setup enables you to flexibly configure target languages and their third-party translation service providers. When your users create translation requests, they can select the languages and providers you have configured.
-   **[Creating email notifications for Localization Workspace](lw-email-notifications.md)**  
As an admin, you can set up email notifications for events in Localization Workspace.

**Parent Topic:**[ServiceNow AI Platform translation and localization](../../managing-data/concept/translation-and-localization.md)


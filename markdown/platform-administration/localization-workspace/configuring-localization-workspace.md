---
title: Configuring Localization Workspace
description: Before using Localization Workspace, configure prerequisites, dependencies, and translation service providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/localization-workspace/configuring-localization-workspace.html
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2025-12-11"
reading_time_minutes: 5
breadcrumb: [Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Configuring Localization Workspace

Before using Localization Workspace, configure prerequisites, dependencies, and translation service providers.

## Configuration overview

Localization Workspace builds upon the functionality of other ServiceNow AI Platform applications related to localization. These applications are activated with Localization Workspace if they are not already installed. You must complete the configuration of these applications before configuring Localization Workspace.

**Note:** From version 2.0.2, the Localization Workspace interface provides two [Guided Setups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/adoption-services/guided-setup.md) to lead admins through the process of configuration, as follows.

-   With the admin role, navigate to **Localization Workspace** &gt; **Localization Framework Guided Setup** for the prerequisite application.
-   Next, navigate to **Localization Workspace** &gt; **Localization Workspace Guided Setup**.

After the initial setup, admins can make adjustments to configurations by using the [Configuration Hub in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-configuration-hub.md).

1.  [Install Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/install-localization-workspace.md).

    You can install the application \(sn\_lw\) if you have the admin role. The application installs related applications and plugins if they are not already installed. Check your entitlements to determine whether you have access to Localization Workspace.

2.  Configure prerequisites as needed.

    In the Zurich release, access to the Settings table \[sn\_lf\_setting\] is configured by default. However, in the Yokohama release, you must confirm access to the Settings table \[sn\_lf\_setting\]. The admin role is required for this step. See [Confirm access to Settings table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-confirm-access-settings-table.md).

3.  Configure dependencies.
    -   [Internationalization \(i18n\) and language plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/exploring-system-localization.md): Install language plugins as part of System Localization. Choose your instance's languages according to your business requirements.
    -   [Localization Framework:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/exploring-localization-framework.md) Configure Localization Framework as follows.

        Assign roles. Localization Workspace uses roles from Localization Framework, along with one role specific to Localization Workspace.

        1.  Add Localization Framework roles as needed. See [Localization Framework Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/roles-localization-framework.md).
        2.  Add the Localization Workspace user role sn\_lw.user. This role is required for all users in Localization Workspace.
        Create at least one group in the Groups \[sys\_user\_group\] table and add roles to the group, then assign your localization users to the appropriate group.

        Configure artifacts. See [Artifact configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/framework-configuration.md).

        **Note:** The role sn\_cd.content\_admin is required to see Content Publishing artifacts from Localization Workspace. If your users need the ability to request translations of Content Publishing artifacts, add sn\_cd.content\_admin to the appropriate group.

        Configure settings, including for the workflows of translation tasks. See [Localization Framework settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/localization-settings.md). Also on the Localization Framework settings table \(sn\_lf\_settings\), in the **Project Preferences** tab, ensure that check boxes are set as follows.

        -   **Enable projects**: Selected.
        -   **Enable auto creation**: Cleared \(unselected\).
        Configure a Translation Management System if your organization uses one. See [Translation Management System configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/tms-configuration.md).

    -   [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dynamic-translation-overview.md): If you use machine translation to fulfill translation requests, configure Dynamic Translation, including setting up a translator configuration. See [Integration with other translation services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/integration-with-other-translation-services.md).
4.  Configure custom artifacts, if you plan to use your own artifacts in Localization Workspace. See [Create and configure a custom artifact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/create-configure-custom-artifact.md).

    Set cross-scope access privileges for your artifacts. For more information see [Cross-scope privileges for Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-cross-scope-privilege.md).

    Set Restricted Caller Access for Localization Workspace to enable access to artifact resources, if needed. The admin role is required for this step. See [Restricted Caller Access for Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-restricted-caller-access.md).

5.  [Configure languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-language-setup.md) in Localization Workspace. Language providers in Localization Workspace are different from translator configurations in Dynamic Translation.

\[Omitted image "configuring-localization-workspace1.png"\] Alt text: Language setup in Localization Workspace, opened to display the Language Providers list.

-   **[Install Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/install-localization-workspace.md)**  
You can install the Localization Workspace application \(sn\_lw\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed. Demo data isn't available.
-   **[Confirm access to Settings table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-confirm-access-settings-table.md)**  
As part of the configuration for Localization Workspace, confirm access to the Settings table of Localization Framework.
-   **[Cross-scope privileges for Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-cross-scope-privilege.md)**  
After you create custom translation artifacts, set cross-scope privileges so that your artifacts can be accessed from Localization Workspace.
-   **[Restricted Caller Access for Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-restricted-caller-access.md)**  
Give Localization Workspace access to your content by setting Restricted Caller Access privileges. Setting these privileges is required only when target tables or scripts are restricted.
-   **[Configuration Hub in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-configuration-hub.md)**  
Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Localization Framework without leaving the Localization Workspace interface.
-   **[Language setup in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-language-setup.md)**  
Language setup enables you to flexibly configure target languages and their third-party translation service providers. When your users create translation requests, they can select the languages and providers you have configured.
-   **[Creating email notifications for Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/lw-email-notifications.md)**  
As an admin, you can set up email notifications for events in Localization Workspace.

**Parent Topic:**[ServiceNow AI Platform translation and localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/translation-and-localization.md)


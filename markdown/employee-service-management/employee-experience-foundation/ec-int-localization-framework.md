---
title: Configure Localization Framework for Content Publishing
description: Configure the translation workflow to enable Content managers to request translation via the Localization Framework. The basic workflow relies on manual translation; you can integrate with a third-party service to receive automatic translation.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure Localization Framework for Content Publishing

Configure the translation workflow to enable Content managers to request translation via the Localization Framework. The basic workflow relies on manual translation; you can integrate with a third-party service to receive automatic translation.

## Before you begin

Role required: Admin

-   [Activate Localization Framework](https://www.servicenow.com/docs/access?context=activate-lf-plugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   \(Optional\) Configure a translation mode, such as machine translations, send to a translation management system, send via email, or export/import: [Translation modes](https://www.servicenow.com/docs/access?context=translation-modes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Create a user group to perform translation:
    -   [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
    -   Assign the `localization_fulfiller` role to the group: [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
    -   Add users to perform translation: [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   Activate the `sn_cd.enable_localization_framework_integration` system property: [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md)

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **Settings**.

2.  Click **New**.

3.  Enter a name for the setting.

4.  Select **All** from the **Artifact** list.

5.  Select the languages into which you want the content translated.

6.  Select the **Workflow Preferences** tab.

7.  Select **Translation -&gt; Publish** from the Workflow list.

8.  From the **Localization fulfiller group** menu, insert the group you created.

9.  Click **Submit**.


## Result

The Content Library displays the **Translate content** button, enabling Content managers to request translation in the languages you have enabled.

To learn more about translation in the Content Library, see [Multilingual support in the Content Library](ec-switch-language.md)


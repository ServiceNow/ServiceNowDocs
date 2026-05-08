---
title: Configure Localization Framework for Content Publishing
description: Configure the translation workflow to enable Content managers to request translation via the Localization Framework. The basic workflow relies on manual translation; you can integrate with a third-party service to receive automatic translation.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup employee communications, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure Localization Framework for Content Publishing

Configure the translation workflow to enable Content managers to request translation via the Localization Framework. The basic workflow relies on manual translation; you can integrate with a third-party service to receive automatic translation.

## Before you begin

Role required: Admin

-   Activate Localization Framework
-   Activate a language
-   \(Optional\) Configure a translation mode, such as machine translations, send to a translation management system, send via email, or export/import: Translation modes.
-   Create a user group to perform translation:
    -   Create a user group
    -   Assign the `localization_fulfiller` role to the group: Assign a role to a group
    -   Add users to perform translation: Add a user to a group
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


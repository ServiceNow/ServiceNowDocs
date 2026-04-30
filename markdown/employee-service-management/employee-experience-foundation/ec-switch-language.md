---
title: Switch language for Content Publishing
description: When creating content from the Content Library, you have the option to select a different language to view in your session similar to changing your language at login.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring translation for Content Publishing after upgrade, Reference, Employee Center, Employee Service Management]
---

# Switch language for Content Publishing

When creating content from the Content Library, you have the option to select a different language to view in your session similar to changing your language at login.

For more information on using a specific language, see [User specific language](https://www.servicenow.com/docs/access?context=r_UserSpecificLanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** You must have additional languages installed before using. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Activate the sn\_cd.enable\_language\_switching system property to use this feature. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md) and [Content Library](ec-streamline-content.md).

When you activate the sn\_cd.enable\_language\_switching system property, created content from your Content Library displays the **Switch language** button. This allows you to switch your system settings language to a different language. The fields on the content form switch to the language you selected and changes the entries in each field if translations are available.

When you switch to a different language, you can also see if there are translations available in that language. For example, **Spanish - translated** indicates translations are available in Spanish for the content you have displayed from the Content Library.

![Switch language](../images/ec-switch-language.png)

When you select a different language and there are translations available for that content, the translations appear as well as all text in the session you are logged in.

**Note:** You can also edit the translated text that appears in your content.

You can preview the translated text before your publish your content via the **Preview on portal** button.

Select the **Switch language** button again after reviewing to switch back to your original language.

**Note:** The Switch language feature is not available in the lists and forms version for Portal, Notification, Mobile, and To-do content found under **Content Categories**.

**Parent Topic:**[Configuring translation for Content Publishing after upgrade](ec-multiple-language-support.md)


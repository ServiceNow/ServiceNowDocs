---
title: CMS translation
description: You can translate CMS sites by activating internationalization plugins and manually translating custom interface strings.Activate an internationalization plugin, which provides a quick way to see translated strings for CMS menus, breadcrumbs, and links. For a full translation, you must translate the instance manually.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Content Management System, Configure UIs and portals, Configure user experiences]
---

# CMS translation

You can translate CMS sites by activating internationalization plugins and manually translating custom interface strings.

Two tables support the translation of a CMS site into other languages.

-   Translated Name / Field \[sys\_translated\]: Stores strings that are shared or commonly used within a site. These include menu section names, menu item names, site breadcrumb names, link names, and footer menu links. Internationalization plugins typically provide translations for these strings. See[System Localization](https://www.servicenow.com/docs/access?context=system-localization-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Translated Text \[sys\_translated\_text\]: Stores unique string translations which you create when you manually translate interface elements. See [Export and edit translation records](https://www.servicenow.com/docs/access?context=t_TranslateTheInterface&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Parent Topic:**[Content Management System](c_ContentManagementSystem.md)

**Related topics**  


[Content Management design](c_ContentManagementPlanning.md)

[Domain separation and the Content Management System](domain-separation-content-management.md)

[Configure Content Management sites](../task/t_CreateASite.md)

[Content Management integration points](c_CMSIntegrationPoints.md)

[Content Management testing](c_ContentManagementTesting.md)

[Global search in Content Management](c_UseGlobalSearchContentManagement.md)

## View a translated CMS site

Activate an internationalization plugin, which provides a quick way to see translated strings for CMS menus, breadcrumbs, and links. For a full translation, you must translate the instance manually.

### Before you begin

Role required: content\_admin or admin

### About this task

This example explains how to view a translated site in Japanese.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the **Go to** filter, select **Name**, enter `I18N`, and then press the Enter key.

3.  Activate both the **I18N - Japanese Translations** and the **I18N: Knowledge Management Internationalization Plugin v2** plugins.

4.  Refresh the browser.

5.  In the **Language** picker in System Settings, select **Japanese**.

6.  Browse the site to see the translated language strings.

7.  Navigate to the ESS Portal at `http://Instance Name.service-now.com/ess/`.

8.  Browse the site to see the translated language strings in the ESS Portal.


**Related topics**  


[Language internationalization support](https://www.servicenow.com/docs/access?context=c_LangInternationalizationSupport&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)


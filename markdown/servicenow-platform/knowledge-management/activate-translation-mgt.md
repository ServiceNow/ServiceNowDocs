---
title: Activate translation management
description: You can activate the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) and I18N:Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugins for translation management if you have the admin role.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure translation management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate translation management

You can activate the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) and I18N:Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugins for translation management if you have the admin role.

## Before you begin

Role required: admin

-   Translation management requires the following plugins. Ensure that these plugins are activated before you install translation management.
    -   **Required ServiceNow plugins**
        -   **Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced\]I18N:Knowledge Management Internationalization Plugin v2 \[com.glideapp.knowledge.i18n2\]**

            The internationalization plugin for the languages you want to make available. The is automatically activated once any of the language plugins are activated.


Translation management also requires enabling the **glide.knowman.translation.enable\_translation\_task** property to add translation task options to the Translation Management submenu under Knowledge menu.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configure translation management](../concept/configure-translation-management.md)


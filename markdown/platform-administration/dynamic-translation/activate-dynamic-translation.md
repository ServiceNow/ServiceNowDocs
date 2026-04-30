---
title: Activate Dynamic Translation
description: Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) to enable all the required APIs.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate Dynamic Translation

Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) to enable all the required APIs.

## Before you begin

You must have the Glide Notification Translation \(com.glide.notification.translation\) plugin installed and enabled.

Role required: admin

## About this task

Dynamic Translation plugin \(com.glide.dynamic\_translation\) activates these related plugins if they are not already active.

<table id="table_ul5_xyw_xjb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flow Designer - Installer\[com.glide.hub\]

</td><td>

Supports the Flow Designer application.

</td></tr><tr><td>

ServiceNow IntegrationHub Runtime\[com.glide.hub.integration.runtime\]

</td><td>

Enables execution of IntegrationHub actions and flows.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - REST\[com.glide.hub.action\_step.rest\]

</td><td>

Action Step - REST

</td></tr><tr><td>

Microsoft Azure Translator Service Spoke\[com.glide.microsoft\_translation\_spoke\]

</td><td>

Provides subflows and actions to dynamically translate the user-entered text, and to detect the language of the text using Microsoft translation services.

</td></tr><tr><td>

ServiceNow Language Detection Service Spoke\[com.glide.language\_detection\_spoke\]

</td><td>

Uses ServiceNow® Language Detection service to provide the ability to detect the language of given text.

</td></tr><tr><td>

Dynamic Translation Spoke\[com.glide.dynamic\_translation.spoke\]

</td><td>

Provides actions that enable the ability to translate text\(s\) from one language to other language\(s\) and to detect the language of given text.

</td></tr><tr><td>

Translation Commons\[com.glide.translation.commons\]

</td><td>

Common utilities for translation features.

</td></tr></tbody>
</table>**Note:** If you activate the Microsoft Azure Translator Service Spoke plugin when the Dynamic Translation plugin \(com.glide.dynamic\_translation\) is inactive, the subflows and actions of the Microsoft Azure Translator Service Spoke plugin are enabled. These subflows can be used in other flows and subflows. However, you cannot call Dynamic Translation APIs.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Dynamic Translation](../concept/configuring-dynamic-translation.md)

**Related topics**  


[List of plugins \(Xanadu\)](../../plugins/reference/list-of-plugins.md#)


---
title: Activate the External Content Integration plugin
description: The External Content Integration feature is activated with the Knowledge Management - External Content Integration plugin \(com.snc.knowledge.external\_integration\).
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with external knowledge sources, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the External Content Integration plugin

The External Content Integration feature is activated with the Knowledge Management - External Content Integration plugin \(com.snc.knowledge.external\_integration\).

## Before you begin

Role required: admin

The Knowledge Management - External Content Integration plugin is not active by default.

The following plugins are automatically activated when the Knowledge Management - External Content Integration plugin is activated:

-   Centralized Connection and Credentials plugin \(com.snc.core.automation.connection\_credential\)
-   Knowledge Management V3 plugin \(com.snc.knowledge3\)
-   [Knowledge Management Advanced Installer plugin](activate-knowledge-advanced-plugin.md) \(com.snc.knowledge\_advanced.installer\)

The **Knowledge** &gt; **Administration** module displays the **External Knowledge Sources** and **External Knowledge Jobs** sub-modules when the Knowledge Management - External Content Integration plugin is activated.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in a future release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers beginning with the Madrid release. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Integration with external knowledge sources](../concept/knowledge-external-content-integration.md)


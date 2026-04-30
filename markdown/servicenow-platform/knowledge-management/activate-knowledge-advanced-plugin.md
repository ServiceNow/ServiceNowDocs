---
title: Activate the Knowledge Management Advanced plugin
description: Activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) to enable advanced features for Knowledge Management.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the Knowledge Management Advanced plugin

Activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) to enable advanced features for Knowledge Management.

## Before you begin

Role required: admin

## About this task

The Knowledge Management Advanced plugin includes feature code and demo data.

The Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\) is used to activate the Knowledge Management Advanced plugin.

Starting with the Xanadu release, the Knowledge Management Advanced plugin is automatically activated for new customers.

**Note:** The Knowledge Management Advanced plugin isn’t automatically activated with the Knowledge Management v3 application.

The Knowledge Management Advanced Installer plugin performs two validation steps prior to activation.

-   Determines whether there are any active Knowledge Management v2 knowledge bases.
-   Determines whether there’s a unique database index on the **Number** field. If a unique constraint has been added to the **Number** field, the plugin activation fails. Resolve this issue by following the instructions in the [Installation of the Knowledge Management Advanced Plugin fails if unique index already exists in article number \[KB0634959\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0634959) article in the Now Support Knowledge Base.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in a future release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers beginning with the Madrid release. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

The Knowledge Management Advanced plugin activates the following features:

-   [Article versioning](../concept/article-versioning.md)
-   [Article subscriptions](../concept/knowledge-article-subscriptions.md)
-   [Article quality index](../concept/knowledge-article-quality-index.md)
-   [Article templates](../concept/knowledge-article-templates.md)
-   [Ownership groups](../concept/enable-ownership-group.md)
-   [In context article creation](../concept/administer-create-article-from-case.md)
-   [Translation management](../concept/translation-management.md)

Demo data is included as part of the Knowledge Management Advanced plugin. If the validation step performed by the Knowledge Management Advanced Installer plugin completes successfully, the Knowledge Management Advanced plugin is activated automatically. However, the demo data isn’t included in this activation. To load the demo data, go to the Knowledge Management Advanced plugin page, select the **Load Demo Data Only** related link, and then select **OK**.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Knowledge Management](../../../configuring-knowledge-management.md)


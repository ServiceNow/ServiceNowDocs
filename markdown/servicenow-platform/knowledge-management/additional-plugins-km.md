---
title: Additional plugins for Knowledge Management
description: After Knowledge Management is activated, you can activate additional plugins that provide access to various additional Knowledge Management features.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Additional plugins for Knowledge Management

After Knowledge Management is activated, you can activate additional plugins that provide access to various additional Knowledge Management features.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

<table id="table_wp2_h15_2v"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Management Core \(com.glideapp.knowledge\)

</td><td>

Installs the core Knowledge Management items used to allow other Knowledge-related plugins to work, such as Knowledge V3, Knowledge Advanced, and Knowledge Service Portal. This plugin is activated by default.

</td></tr><tr><td>

Knowledge Management Advanced Installer \(com.snc.knowledge\_advanced.installer\)

</td><td>

Installs the Knowledge Management Advanced plugin. Activating/upgrading to this plugin validates the knowledge articles and knowledge bases to make sure that the Knowledge Advanced plugin can be successfully installed. If validation fails, check the Plugin Activation logs and follow instructions given to fix any errors. Once you fix all the issues, re-run this plugin.

</td></tr><tr><td>

Knowledge Management Advanced \(com.snc.knowledge\_advanced\)

</td><td>

Adds advanced features to Knowledge Management such as version control and subscriptions. This plugin requires that all knowledge bases are version Knowledge V3. Use the Knowledge Management Advanced Installer plugin to activate this plugin.

</td></tr><tr><td>

Predictive Intelligence for Knowledge Management \(com.snc.knowledge\_ml\)

</td><td id="pi-km-desc">

Provides various Knowledge Management capabilities driven by machine-learning solutions. For example, capabilities such as similar articles and knowledge demand insights. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.**Note:** When you install and activate the Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\), the Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\) is also activated.

</td></tr><tr><td>

Performance Analytics - Content Pack - Knowledge Management \(com.snc.pa.knowledge\_v2\)

</td><td>

Enables the Performance Analytics content pack for the Analytics and Reporting Knowledge Management Solution. Activation of this plugin on production instances might require a separate Performance Analytics license. Contact ServiceNow for details.

</td></tr><tr><td>

Knowledge Management V3 \(com.snc.knowledge3\)

</td><td>

Enables support for Knowledge Management V3. Activate this plugin when you upgrade from Eureka or earlier versions.

</td></tr><tr><td>

I18N: Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\)

</td><td>

Helps create and maintain translations of an article in various languages in a way that is easy to manage translations while authoring as well as viewing articles. Activating internationalization plugins for any of the available languages automatically activates this plugin.

</td></tr><tr><td>

Knowledge Document \(com.snc.knowledge\_document\)

</td><td>

Adds knowledge-based functionalities to the Managed Documents plugin. You can create a knowledge article from a document or update a knowledge document to a newer revision.

</td></tr><tr><td>

Knowledge Management - External Content Integration \(com.snc.knowledge.external\_integration\)

</td><td>

Adds external content search capabilities to the Knowledge Management application. Once configured, this feature creates a copy of the external content on ServiceNow as knowledge articles, and then indexes the articles through Zing Search. You must have appropriate reuse and copy privileges before you configure an external source to be searchable using this feature.

</td></tr><tr><td>

Knowledge Management Wiki Support \(com.glideapp.knowledge2.wiki\)

</td><td>

Enables support to save Knowledge articles in wiki type field instead of html type field.

</td></tr><tr><td>

Knowledge Management KCS Capabilities \(com.snc.knowledge\_kcs\_capabilities\)

</td><td>

Enables the use of KCS roles \(kcs\_contributor, kcs\_publisher, and kcs\_candidate\) and use the metadata fields for the KCS article state \(governance and confidence\).

</td></tr><tr><td>

Knowledge Management - Add-in for Microsoft Word \(com.snc.knowledge.ms\_word\)

</td><td>

Enables authoring content in Microsoft Word and publishing it as a knowledge article using a Word add-in.

</td></tr><tr><td>

Knowledge Blocks \(com.snc.knowledge\_blocks\)

</td><td>

Enables you to create re-usable content blocks that can be included in existing knowledge articles. This feature is capable to display only pieces of an article to specific users.

</td></tr><tr><td>

Knowledge Overview \(com.sn\_knowledge\_overview\)

</td><td>

Enables you to generate reports to provide an overview of knowledge base and article data.

</td></tr></tbody>
</table>**Parent Topic:**[Knowledge Management reference](knowledge-management-reference.md)


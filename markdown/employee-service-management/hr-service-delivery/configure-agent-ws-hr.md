---
title: Setting up HR Service Delivery Agent Workspace
description: Set up HR Service Delivery Agent Workspace so that your agents can engage with your employees, answer questions, create cases, and resolve issues.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Setting up HR Service Delivery Agent Workspace

Set up HR Service Delivery Agent Workspace so that your agents can engage with your employees, answer questions, create cases, and resolve issues.

**Important:**

-   HR Service Delivery Agent Workspace \(Classic\) is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.
-   If you are an existing user of HR Service Delivery Agent Workspace \(Classic\), you can migrate to the Agent Workspace for HR Case Management \(Configurable\) for enhanced features and capabilities. See [Migration Guidelines](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

ServiceNow® HR Service Delivery Agent Workspace uses the Agent Workspace application as a platform.

To set up HR Service Delivery Agent Workspace, you can:

-   Activate the Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin.
-   Activate the Human Resources Scoped App: Workspace \[com.sn\_hr\_agent\_workspace\] plugin.
-   Set up these components of the HR Service Delivery Agent Workspace:
    -   Communication channels and routing.
    -   Additional components and settings that are specific to HR Service Delivery.
    -   Forms in workspace. See Set up forms in Workspace.
    -   Workspace setup. See Set up Workspace.

## Roles installed

By activating the Human Resources Scoped App: Core \[com.sn\_hr\_core\] and Human Resources Scoped App: Workspace \[com.sn\_hr\_agent\_workspace\] plugins, you install the following roles:

<table id="table_vz4_hsk_2rb"><thead><tr><th>

HR role title \[name\]

</th><th>

Description

</th><th>

Contains workspace roles

</th></tr></thead><tbody><tr><td>

HR manager \[sn\_hr\_core.manager\]

</td><td>

Grants access to all HR cases, profiles, and secure information.With this role, you can manage HR Service Delivery Agent Workspace lists and categories.

 This role contains the Workspace List Admin, which is an elevated role. For more information on elevated roles, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

 The Workspace user \[workspace\_user\] role allows you to access HR Service Delivery Agent Workspace and create and access interactions.

</td><td>

Workspace List Admin \[workspace\_list\_admin\] Workspace user \[workspace\_user\]

</td></tr><tr><td>

HR case writer \[sn\_hr\_core.case\_writer\]

</td><td>

Grants access to write all HR cases.With this role, you can access HR Service Delivery Agent Workspace and view, create, and work on existing cases. You can also access all areas of Case and Knowledge Management.

 This role contains the Workspace user role, which allows you to perform interaction agent and interaction queue transfers.

</td><td>

Workspace user \[workspace\_user\] Interaction agent \[interaction\_agent\]

</td></tr><tr><td>

HR agent \[sn\_hr\_core.basic\]

</td><td>

Grants access to basic HR agents to HR Service Delivery Agent Workspace modules.This role contains the Advanced Work Assignment Agent \[awa\_agent\] role, which allows an HR agent to work customer interactions and manages workload across multiple service channels.

</td><td>

-   Advanced Work Assignment Agent \[awa\_agent\]
-   To see all the roles contained within the HR agent \[sn\_hr\_core.basic\] role, see [Components installed with Case and Knowledge Management](../reference/components-installed-with-case-and-knowledge-management.md).

</td></tr><tr><td>

Workspace content manager \[sn\_cd.workspace\_content \_manager\]

</td><td>

Lets you schedule content to workspace.-   The uxframework\_user role allows you to browse and select from the library of UX component records so they can set a component reference field on any accessible table.
-   The sn\_cd.content\_manager role grants access to Content Publishing.
    -   The sn\_esign.config\_manager role can manage the e-signature configurations.
    -   The sn\_cd.content\_approver role can approve content that is scheduled to appear on the Employee Center.

</td><td>

-   UX framework user \[uxframework\_user\]
-   Content Delivery content manager \[sn\_cd.content\_manager\]
    -   E-Signature configuration manager \[sn\_esign.config\_manager\]
    -   Content Delivery approver \[sn\_cd.content\_approver\]

</td></tr><tr><td>

HR Workspace Admin \[sn\_hr\_ws.admin\]

</td><td>

Lets you configure all aspects of HR Service Delivery Agent Workspace.The workspace\_admin role allows you to configure Agent Workspace

 -   The chat\_admin role administers the chat tables.
-   The uxframework\_designer role has write access to UX page element records for designing UIs.
-   The agent\_workspace\_user role allows you to perform interaction agent and interaction queue transfers.
-   The sn\_agent\_recommend.recommendation \_admin role manages agent assist recommendation configurations.
-   The interaction\_admin role allows you to administer the Interaction Management system.
-   The workspace\_list\_admin role allows you to manage workspace lists and categories.
-   The ui\_action\_admin role allows you to manage UI actions.
-   The ui\_builder\_admin role provides permission to use the UI Builder APIs so you can create, update, read, and delete UX pages.
-   The uxframework\_user role allows you to browse and select from the library of UX component records so they can set a component reference field on any accessible table.
-   The sn\_intel\_analyzer.similarity \_analyzer\_admin role allows you to administer the Similarity Analyzer. The Similarity Analyzer defines patterns and trends that can help you resolve a record.
-   The form\_admin role manages forms, form sections, and section elements.
-   The personalize\_form role allows you to personalize forms.
-   The ui\_notification\_admin role allows you to configure notification triggers.

</td><td>

Workspace administrator \[workspace\_admin\]-   Chat admin \[chat\_admin\]
-   UX framework designer \[uxframework\_designer\]
-   Agent workspace user \[agent\_workspace\_user\]
-   Agent recommendation admin \[sn\_agent\_recommend.recommendation \_admin\]
-   Interaction admin \[interaction\_admin\]
-   Workspace list admin \[workspace\_list\_admin\]
-   UI action admin \[ui\_action\_admin\]
-   UI builder admin \[ui\_builder\_admin\]
-   UX framework user \[uxframework\_user\]
-   Similarity Analyzer \[sn\_intel\_analyzer.similarity \_analyzer\_admin\]
-   Form admin \[form\_admin\]
-   Personalize form \[personalize\_form\]
-   UI notification admin \[ui\_notification\_admin\]

</td></tr></tbody>
</table>## Rich text

Rich text allows you to format your comments or work notes to emphasize your message and is readable across many programs and platforms.

You can enable rich text for HR Service Delivery Agent Workspace by using the **glide.ui.journal.use\_html** system property \(**sys\_properties.list**\). By default, this property is set to **false** \(off\).![HR Agent WS - Rich text](../image/agent-ws-hr-rich-text.png)

|Number|Description|
|------|-----------|
|![Toggle compose settings icon](../image/agent-ws-hr-toggle.png)|Toggle compose settings icon that you select to show the rich text editor and stacked view icons.|
|![HR Agent Workspace Case form callout 1](../reference/images/1.png)|Rich text editor slider that you can toggle on to turn on the rich text.|
|![HR Agent Workspace Case form callout 2](../reference/images/2.png)|Stacked view slider that places Comments and Work notes side-by-side or stacked above one another.|

**Warning:** If your company is using other Agent Workspace applications, turning this property to **true** \(on\), might impact your system performance.


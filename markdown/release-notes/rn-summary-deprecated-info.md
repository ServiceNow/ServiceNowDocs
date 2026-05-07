---
title: Deprecation information for all Australia features and products
description: Cumulative release notes summary on deprecation information for Australia features and products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 10
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Deprecation information for all Australia features and products

Cumulative release notes summary on deprecation information for Australia features and products.

For information about deprecated plugins in Australia, refer to Plugin information[Plugin information for all features and productsPlugin information](https://www.servicenow.com/docs/r/release-notes/rn-summary-plugin-info.html)

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   The ability to add hyperscalers from the AICT configuration section is no longer available. You can find any previously created hyperscaler connections in the AI connections section, under Legacy connections.

</td></tr><tr><td>

API

</td><td>

-   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

</td></tr><tr><td>

Adoption Services

</td><td>

Starting with the Australia release, Guided Setup is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Authentication

</td><td>

-   Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:
    -   OAuth API endpoint for external clients
    -   OAuth JWT API endpoint for external clients
    -   OIDC provider to verify ID tokens
-   The \(`glide.login.no_blank_password`\) property is deprecated, since the property is no longer used and changing this property value doesn't effect login behavior.

</td></tr><tr><td>

Clone Admin Console

</td><td>

-   Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.
-   Legacy clones no longer appear in the Clone Admin Console dashboard.

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   The Path Column in the Container Image Package \[sn\_vul\_container\_image\_package\] table for the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations. Path tracking has been moved to the Path Column on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table to support accurate and consistent path and image association.

If you use these integrations you must refer to the Path column available on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table.

-   The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) is deprecated. If you're currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. See more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

</td></tr><tr><td>

Data Management for CSM

</td><td>

-   As part of the CAM Declarative Responsibility Framework enhancements, the following legacy fields have been marked deprecated:
    -   **Restrict access to** field from the Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
    -   **Applicable to** field from the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
-   Starting with the Australia release, the Household plugin \(com.snc.household\) is available as a store plugin and, as such, the family version of the plugin is being prepared for future deprecation. Upon upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Data Separation

</td><td>

-   This application is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Alternatively, you can use Data Filters and access control lists \(ACLs\) to configure data separation for your use cases. For details on how to enable data separation for different use cases using data filters and ACLs, see the [Managing data separation using data filters and ACLs \[KB0558290\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1772519) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Developer Sandboxes

</td><td>

Data generation profiles and templates will no longer available in Developer Sandboxes as of the Brazil release. When you upgrade, the following will happen:

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

**Note:** You can use the Now Assist Data Kit instead of data generation profiles.

</td></tr><tr><td>

Document Intelligence

</td><td>

Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Event Management

</td><td>

-   Alert Clustering Definitions \(ACD\) have been deprecated and fully replaced by Alert Automation in Service Operations Workspace. All existing configurations remain supported with full feature parity.
-   Service Management Dashboard is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Field Service Management

</td><td>

Starting with the Australia release, the **sn\_fsm\_disp\_wrkspc.calendarCollapsedBehavior** property has been removed and its behavior is now controlled by the **sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.calendar\_resources\_page\_size** property, which determines the number of resources loaded on the page.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   The FSO tables `sn_bom_m2m_service_definition_user_criteria` and `sn_bom_m2m_service_definition_customer_condition` are deprecated. If you're on an upgraded instance, you can continue to reference these tables, but they're no longer maintained. Use `sn_csm_case_types_service_user_criteria` and `sn_csm_case_types_service_customer_criteria` instead. For more information, see [FSO Core Banking tables](https://www.servicenow.com/docs/access?context=fso-core-banking-tables&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US).
-   The **Show in Interceptor** field \(`show_in_interceptor`\) on the `sn_bom_service_definition` table is deprecated. Use agent criteria in the `sn_csm_case_types_service_user_criteria` table to control which service definitions appear in the case type selector.

User criteria mappings control the visibility of new service definitions. To hide a service definition, map it to the **No User** user criteria. To make it visible, map it to the **Users with sn\_bom.service\_definition\_read** user criteria. Both user criteria records are predefined in Financial Services Operations Core.

For more information, see [Components installed with case types](https://www.servicenow.com/docs/access?context=service-definitions-components&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Legacy Application Manager

</td><td>

Legacy Application Manager is being deprecated as of Australia patch 1. Bookmarks to Legacy Application Manager redirect to the new Application Manager experience.

</td></tr><tr><td>

Next Experience

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements, defect fixes, and will no longer be supported. Certain system features may continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information activating Next Experience see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Next Experience Components

</td><td>

|UI Element|Description|
|----------|-----------|
|Dashboard overview template|Moved under "Legacy templates" and renamed to "Deprecated - Dashboard overview." This template can still be used, but you should use the new "Dashboard library" template instead, because the Dashboard overview template is marked for eventual deprecation.|

</td></tr><tr><td>

Now Assist

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   Starting with [Australia Patch 1](../quality/australia-patch-1.md) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   The support for manually integrating external agents has been deprecated from [Australia Patch 1](../quality/australia-patch-1.md) release.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

Starting with the [Australia Patch 2](../quality/australia-patch-2.md) release, the [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US) is deprecated, moved to the **Archived** folder and is no longer available for use.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

 

</td></tr><tr><td>

Performance Analytics

</td><td>

-   The **Dashboard Visualization** tab in KPI Composer is no longer supported. Existing data visualization tabs remain but you are not able to create new ones because this feature is connected to Core UI dashboards, which are themselves deprecated.
-   Performance Analytics widgets are deprecated along with Core UI dashboards. Users with the pa\_admin role are still able to create Performance Analytics widgets.
-   The Analytics Hub has been replaced by KPI Details. Attempts to open the Analytics Hub are redirected to KPI Details.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

Business users can no longer create or edit the following Core UI objects:

-   Reports

Create new Core UI reports from sys\_reports.list with the report\_admin role.

-   Interactive filters

Create new Core UI interactive filters from sys\_ui\_hp\_publisher.list with the report\_admin role.

-   Responsive dashboards

Create new responsive dashboards from pa\_dashboards.list with the dashboard\_admin role.

-   PA widgets

Create new Performance Analytics widgets from pa\_widgets.list with the pa\_admin role.


</td></tr><tr><td>

Process Mining

</td><td>

Automation Discovery is deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in the Australia release.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   Starting with Australia release, Scenario Planning for PPM \(com.snc.ppm\_scenario\_planning\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Alternatively, Strategic Planning Workspace \(for SPM pro users\) or Portfolio Planning Workspace \(for SPM standard users\) provides the Scenario Planning capability. For details, see [Scenario planning in Strategic Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US) or [Scenario planning in Portfolio Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-portfolio-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

-   Starting with Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Project Workspace provides the Status Report capability.
-   Starting with Australia release, the PMO dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Execution dashboard provides the PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Portfolio Planning Workspace provides the Investment Portal capability.
-   Starting Australia, Project Workbench is no longer deployed, enhanced, supported or available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Project Workspace

</td><td>

-   Starting with the Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Project Workspace supports status report capability.
-   Starting with Australia release, the Project Management Office \(PMO\) dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Execution dashboard supports PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Portfolio Planning Workspace supports Investment Portal capability.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements or defect fixes, and will no longer be supported. Certain system features might continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information about activating the Next Experience UI, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](../release-notes-summaries.md)


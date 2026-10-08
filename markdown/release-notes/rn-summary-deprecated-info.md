---
title: Deprecation information for all Australia features and products
description: Cumulative release notes summary on deprecation information for Australia features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/rn-summary-deprecated-info.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 11
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Deprecation information for all Australia features and products

Cumulative release notes summary on deprecation information for Australia features and products.

For information about deprecated plugins in Australia, refer to

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Traceloop Warehouse HTTPS connection removed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md)**

The base system Traceloop Warehouse HTTPS connection \(sn\_ai\_security.Traceloop\_API alias\) is removed. If you're upgrading and use Traceloop-based external AI metrics, create a new HTTPS connection under that alias and re-create your credential with connection URL `https://api.traceloop.com`.


-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Adoption Services

</td><td>

Starting with the Australia release, Guided Setup is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **AI Search Profile dashboard**

The **Searchable Documents** and **Documents by Search Source** visualizations have been removed. These visualizations depended on scheduled jobs and legacy dashboard tables which are no longer available.


</td></tr><tr><td>

Clone Admin Console

</td><td>

-   **Static FAQ Content**

Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.

-   **Clone requests via lists and forms \(legacy\)**

Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see [CMDB 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multisource-cmdb.md).

</td></tr><tr><td>

Digital Product Release

</td><td>

-   **[Auto create enhancement from primary epic system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release-properties.md)**

The `sn_dpr_workspace.auto_create_product_enhancement_for_primary_epic` property is removed. Use `sn_dpr_workspace.enhancement_work_item_types` instead.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

</td></tr><tr><td>

Document Intelligence

</td><td>

Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence \(Legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/docintel-nowassist-landing.md).

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **Now LLM Service**

Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


-   **[Enterprise model and asset import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/download-seeded-template-manual-bulk-imports.md)**

Enterprise model and asset import templates that were previously generated from Enterprise Asset Management staging tables have been replaced with seeded import templates.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **Now LLM Service deprecation notice**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Flows, subflows, and actions

</td><td>

The now.assist.creator role is no longer a required role to use generative AI features with Now Assist.

</td></tr><tr><td>

ITSM MCP Server

</td><td>

-   **[Deprecated sn\_itsm\_mcp\_server.requester.escalate tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

The **sn\_itsm\_mcp\_server.requester.escalate** tool is turned off by default. Use **sn\_itsm\_mcp\_server.incident.modify** with the **escalate** and **escalation\_reason** inputs instead.


</td></tr><tr><td>

Impact

</td><td>

On-demand value report and Value potential accelerators have been removed.

</td></tr><tr><td>

Industrial Standards

</td><td>

-   **[Template schedule type for schedule plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/create-events-based-on-schedules.md)**

Removed. You can no longer create a schedule plan from a schedule template, and the Schedule type and Schedule fields are removed from the [Schedule plan form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/scheduled-plan-form.md). Use a custom schedule instead, which can also be shift-based.


</td></tr><tr><td>

Knowledge Center

</td><td>

-   **Now LLM Service deprecation notice**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Legacy Application Manager

</td><td>

Legacy Application Manager is being deprecated as of Australia patch 1. Bookmarks to Legacy Application Manager redirect to the new Application Manager experience.

</td></tr><tr><td>

Next Experience

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements, defect fixes, and will no longer be supported. Certain system features may continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information activating Next Experience see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-adoption-paths.md).

</td></tr><tr><td>

Next Experience Components

</td><td>

|UI Element|Description|
|----------|-----------|
|Dashboard overview template|Moved under "Legacy templates" and renamed to "Deprecated - Dashboard overview." This template can still be used, but you should use the new "Dashboard library" template instead, because the Dashboard overview template is marked for eventual deprecation.|

</td></tr><tr><td>

Operational Technology Discovery

</td><td>

Starting with the Australia release, Operational Technology Discovery is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Playbook

</td><td>

The now.assist.creator role is no longer a required role to generate a playbook or playbook recommendation when using Now Assist.

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Process Mining

</td><td>

You no longer require the now.assist.creator role to access Now Assist features in the Creator Pro Plus package. However, you must enable the relevant Process Mining skill, which serves as the necessary prerequisite. Additionally, you should have appropriate access to the project.

Automation Discovery is deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in the Australia release.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

The pricing engine parallel execution properties, `sn_csm_pricing.enable_pricing_engine_parallel_execution` and `sn_csm_pricing.pricing_engine_parallelism_lines_threshold,`have been removed from Pricing Management to support automatic addition of derived pricing lines and calculation of pricing rollups.

</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

-   **Service Graph Connector Integration for Claroty CTD**

Starting with the Australia release, the Service Graph Connector Integration for Claroty CTD application is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements or defect fixes, and will no longer be supported. Certain system features might continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information about activating the Next Experience UI, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-adoption-paths.md).

</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Otto for Creator

</td><td>

Spoke generation has been removed from ServiceNow Otto for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Otto for Zero Copy Connector

</td><td>

The Ask AI button has been removed from the Model Manager.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Usage Insights

</td><td>

-   **[Usage Insights in Xanadu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/user-exp-analytics-landing.md)**

Usage Insights is no longer supported in the Xanadu release. Upgrade to Yokohama, Zurich, or Australia to continue using Usage Insights.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **Agentic support page**

The **Agentic support** page has been deprecated for ServiceNow Otto for Virtual Agent and ServiceNow Otto panel - Platform. There is no loss of functionality previously provided by the **Agentic support** page. By default, all existing assistants operate in agentic mode. The **Prioritize AI agents during skills discovery** option is available when configuring [additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/additional-chat-features.md).


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **Authentication Program field**

The Authentication Program field is removed from these spoke actions, per Visa IES 26.2. There is no replacement for this field.

    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **Vulnerability Response Integration with Claroty CTD**

Starting with the Australia release, the Vulnerability Response Integration with Claroty CTD application is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

The **Ask AI** button was removed from the Model Manager.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/release-notes-summaries.md)


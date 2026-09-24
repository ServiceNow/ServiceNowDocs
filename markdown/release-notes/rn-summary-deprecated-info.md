---
title: Deprecation information for all Brazil features and products
description: Cumulative release notes summary on deprecation information for Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-deprecated-info.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 20
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Deprecation information for all Brazil features and products

Cumulative release notes summary on deprecation information for Brazil features and products.

For information about deprecated plugins in Brazil, refer to

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Admin Center

</td><td>

-   **[Calculate savings projections for automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-set-up-data-source.md)**

Use a single savings profile formula when configuring custom data sets for automation opportunity discovery. Multiple savings projections are no longer supported.

-   **[Daily recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-set-up-data-source.md)**

The daily recommendation is no longer visible. Only three default configurations are available for custom data sets.


</td></tr><tr><td>

AI Agent Advisor

</td><td>

-   **[Calculate savings projections for automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-set-up-data-source.md)**

Use a single savings profile formula when configuring custom data sets for automation opportunity discovery. Multiple savings projections are no longer supported.

-   **[Daily recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-set-up-data-source.md)**

The daily recommendation is no longer visible. Only three default configurations are available for custom data sets.


</td></tr><tr><td>

AI Control Tower

</td><td>

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Veza API key authentication deprecated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference-system-properties.md)**

The Veza connector now authenticates using OAuth 2.0 instead of an API key. The sn\_ai\_security.veza.api.key system property is deprecated.

-   **[Findings by severity metric removed from Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

The **Findings by severity** metric is removed from the Security Design-time tab, AI security posture subtab.


-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **AI Search Profile dashboard**

The **Searchable Documents** and **Documents by Search Source** visualizations have been removed. These visualizations depended on scheduled jobs and legacy dashboard tables which are no longer available.


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   **HRSD Process Mining Content Pack deprecation**

The HRSD Process Mining Content Pack application \(com.sn\_hr\_process\_optimization\) is deprecated as of the AI Platform Brazil release and will receive no further support. The unified Process Mining Content Pack application replaces it and will auto-install when you upgrade to Brazil or later. The deprecated application will remain active in your instance after upgrade; migrate to the unified Process Mining Content Pack to access new functionality and continued support. No manual migration steps are required—existing configurations transfer automatically.


</td></tr><tr><td>

Collaborative Work Management \(CWM\)

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Common Governance, Risk, and Compliance features

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **Itil role removed from app\_service\_admin**

The sn\_cmdb\_editor and app\_service\_user roles replace the itil role within the app\_service\_admin role. While you can still view Service Instance records and use Unified Map, viewing related items for a CI, such as linked incidents or changes, still requires the itil role.

-   **sn\_getwell\_cis\_processed\_via\_ire database view removal**

sn\_getwell\_cis\_processed view\_ire is deprecated.

-   **CMDB Baseline, Dependency Views, and CMDB Relationship editor**

Starting with the Brazil release, CMDB Baseline is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Unified Map provides the latest experience for this functionality.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **Form changes**
    -   The **Sandbox alias** URL field has been removed from the Allocate Sandbox form. Because sandbox URLs are now randomly generated, you no longer specify a URL at allocation time.
    -   Sandbox templates have been removed from the Allocate Sandbox form.

</td></tr><tr><td>

Discovery

</td><td>

-   **findOrCreateRelationshipType function**

The `findOrCreateRelationshipType` function is deprecated beginning with Zurich Patch 10, Australia Patch 2 Hotfix 2a, Australia Patch 3, and Brazil. Moving forward, it no longer creates CI relationship types. Instead, it finds an existing CI relationship type and returns an error if the type does not exist. Update any custom scripts that call `findOrCreateRelationshipType` to use `findCIRelationshipType` instead.


</td></tr><tr><td>

Discovery store applications

</td><td>

-   **Field mapping for properties.privateEndpointConnections**

The field mapping for properties.privateEndpointConnections is removed from Azure Functions.

-   **WMIC utility**

The connector doesn’t depend on the deprecated WMIC utility when running commands on Windows hosts.


</td></tr><tr><td>

Employee Slate for ITSM

</td><td>

-   ****

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Enterprise model and asset import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/download-seeded-template-manual-bulk-imports.md)**

Enterprise model and asset import templates that were previously generated from Enterprise Asset Management staging tables have been replaced with seeded import templates.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **Now LLM Service deprecation notice**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   **No deprecated or removed features**

There are no deprecated or removed features in this release.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[Classic Dynatrace event integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/dynatrace-advanced-settings-fields.md)**

Replaced by the new Dynatrace Grail connector. Move to the Grail connector to keep receiving Dynatrace alerts.

-   **[Auto-dismissing success banner \(pull connectors\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

Replaced by a persistent activation modal after a passing connection test.


</td></tr><tr><td>

ITSM MCP Server

</td><td>

-   **[Deprecated sn\_itsm\_mcp\_server.requester.escalate tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

The **sn\_itsm\_mcp\_server.requester.escalate** tool is disabled by default. Use **sn\_itsm\_mcp\_server.incident.modify** with the **escalate** and **escalation\_reason** inputs instead.


</td></tr><tr><td>

Identity

</td><td>

-   **[User Registration Request plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UserRegistration.md)**

Starting with the Brazil release, User Registration Request plugin \(com.snc.user\_registration\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.


</td></tr><tr><td>

Impact

</td><td>

-   **Accelerators Retirement**

Jumpstart Your Virtual Agent, Jumpstart Your Natural Language Understanding \(NLU\), Jumpstart Your Multi-Lingual Virtual Agent, Jumpstart Your Issue Auto Resolution, and Jumpstart Your CSDM - Crawl technical Accelerators are no longer available.

-   **Impact Proactive Code Check**

Impact Proactive Code Check/Health Diagnostics UI artifacts, navigation entries, and background jobs are being removed. Ensure your customizations don't depend on Impact Health Diagnostics navigation or diagnostics-specific tables.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   **Legacy Kubernetes discovery API**

The legacy Kubernetes discovery API is deprecated and will be removed in a future release. Use the enhanced discovery capabilities and updated API endpoints introduced in this release.


</td></tr><tr><td>

Operational Technology Discovery

</td><td>

-   **Operational Technology Discovery**

Starting with the Brazil release, Operational Technology Discovery is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Performance Analytics

</td><td>

Starting with the Brazil release, KPI Composer is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Process Mining**

Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.


</td></tr><tr><td>

Pricing Management

</td><td>

-   **Parallel execution properties for the pricing engine**

The sn\_csm\_pricing.enable\_pricing\_engine\_parallel\_execution and sn\_csm\_pricing.pricing\_engine\_parallelism\_lines\_threshold Pricing Engine Parallel Execution properties have been removed. These properties previously controlled parallel execution of pricing plan steps in the pricing engine. The pricing engine now processes pricing requests sequentially. This change helps ensure that rollup calculations and auto-added derived pricing are applied correctly. No replacement properties are available.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Process Mining

</td><td>

-   **Two APIs deprecated**

The following two APIs are deprecated:

    -   promin.api.allow\_no\_role\_mining
    -   promin.api.auto\_share\_project\_with\_creator

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Planning console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/c_TheProjectPlanningConsole.md)**

Starting Brazil release, Planning console is deprecated and is no longer supported. Project managers can [access Project Workspace using Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/access-new-project-workspace.md) to work on project planning.

-   **Process Mining**

Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **Communities**

Communities is no longer deployed, enhanced, or supported. The Communities plugins are set to planned deprecation status, which prevents new customer installations. Existing customers who have Communities installed can continue to use it, but new activations are no longer available. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **Removal of Catalog Roles from request management ACLs**

ACL records on request management tables and fields no longer grant access based on the catalog role or the catalog admin role. ACL records for tables owned by request management, such as Request \[sc\_request\] and Requested Item \[sc\_req\_item\], no longer include catalog-related roles in the list of required roles. Each ACL record retains at least one request management role, so the list is never empty. Users who have only a catalog-related role and no request management role can no longer use these ACL records to access request management tables or features. Another ACL record on the same table might still grant access through a different role. This change affects only the ACL records that the catalog team owns.


</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

-   **Service Graph Connector Integration for Claroty CTD**

Starting with the Brazil release, the Service Graph Connector Integration for Claroty CTD application is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

-   ****
    -   **[ITSM Virtual Agent NLU topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/using-itsm-va.md)**

Starting with the Brazil release, ITSM Virtual Agent pre-built topics is being prepared for future deprecation.

    -   **[ITSM Virtual Agent Lite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-virtual-agent-lite.md)**

ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\) is being prepared for future deprecation.

    -   **[Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   **[Deprecation of Virtual Agent for NLU and keywords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent-landing-page-nlu.md)**

Starting with the Brazil release, Virtual Agent for NLU and Virtual Agent Lite are being prepared for future deprecation. They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **[Deprecation of Virtual Agent channel integrations applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integrate-virtual-agent-nlu.md)**

Starting with the Brazil release, the following Virtual Agent channel integration applications are being prepared for future deprecation:

    -   [Conversational Integration with Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conv-integ-alexa.md)
    -   [Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ivr-voice.md)
    -   [IBM Watson Assistant conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ibm-watson-assistant-config.md)
They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-llm-model-updates.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **Experience switcher**

The Experience switcher has been removed from ServiceNow Studio. ServiceNow IDE capabilities were consolidated under the Explorer tab in ServiceNow Studio. There is no current replacement for the Experience switcher, but each individual application can still be accessed on the ServiceNow AI Platform.

-   **Tools tab**

The Tools tab has been removed from the ServiceNow Studio home page, with no replacement. For links to documentation for each development tool, see [Integrated development tools for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/integrated-development-tools.md).

-   **Create menu**

The Create menu in the top right corner of ServiceNow Studio has been removed. The other Create option in the activity bar is still available and has the same functionality.

-   **Resources**

The Resources section has been removed from the ServiceNow Studio home page. There is no current replacement for the Resources section, but users with Build Agent can prompt in the main chat to access resources.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Process Mining**

Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.


</td></tr><tr><td>

Strategic Spend Tracking for PPM

</td><td>

-   **[Strategic Spend Tracking for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/ppm-strategic-spend-tracking-overview.md)**

Starting with the Brazil release, Strategic Spend Tracking for PPM is being prepared for future deprecation and it will be hidden. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **Vulnerability Response Integration with Claroty CTD**

Starting with the Brazil release, the Vulnerability Response Integration with Claroty CTD application is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)


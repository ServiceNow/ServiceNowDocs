---
title: AI agents, skills, and agentic workflows on by default
description: Starting with the Zurich Patch 4 release, some AI agents, generative AI skills, and agentic workflows are turned on by default in the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.html
release: yokohama
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 9
keywords: [generative AI, Gen AI, default-on]
breadcrumb: [Generative AI skills, Enable AI Experiences]
---

# AI agents, skills, and agentic workflows on by default

Starting with the Zurich Patch 4 release, some AI agents, generative AI skills, and agentic workflows are turned on by default in the ServiceNow AI Platform.

**Important:** Some generative AI skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install an AI product, designated generative AI skills, AI agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The AI plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support ServiceNow Otto functionality. Deactivating these skills can negatively affect some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-native-sku-overview.md).

## AI assets that are on by default

For a list of changes by release, see [Release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/release-notes/new-features-changes.md).

|Product|Type|Asset name|Effective date|
|-------|----|----------|--------------|
||Agentic workflow|Help repair enterprise assets|April 9, 2026|
|[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-landing-page.md)|Skill|Outcome summarization|December 11, 2025|
|[ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)|Skill|[Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-summarize-apo.md)|December 11, 2025|
|[Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-fsc-summarize-po.md)|December 11, 2025|
|ServiceNow Otto for Cloud Cost Management \(CCM\)|Skill|Cloud cost summarizer|September 10, 2026|
||Skill|Acceptance criteria generation|December 11, 2025|
|Doc generation|December 11, 2025|
|Task generation|December 11, 2025|
|[ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-landing-cmdb.md)|Skill|[Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)|December 11, 2025|
|[Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-cmdb-mng-dupe-cis-skill.md)|December 11, 2025|
|[Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-sgc-diagnose.md)|December 11, 2025|
|[Summarize CMDB readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-skill-summ-rdy.md)|July 9, 2026|
|Agentic workflow|[Search CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-awf-search.md)|December 11, 2025|
|Contract Management Pro|Skill|Contracts query enhancer|December 11, 2025|
|Contracts query classifier|April 9, 2026|
|Duration to days converter|December 11, 2025|
|Search contract with contextual input|December 11, 2025|
||Agent|CBS bulk upload agent|April 9, 2026|
|CBS configuration agent|April 9, 2026|
|IA orchestration agent|April 9, 2026|
|Manage groups and roles agent|April 9, 2026|
|Notification agent|April 9, 2026|
|Skill|Next Best Action|April 9, 2026|
|Error Resolution|April 9, 2026|
|Agentic workflow|AI agentic workflow for the CBS setup|April 9, 2026|
||Skill|Spoke generation|December 11, 2025|
|Playbook summarization|June 11, 2026|
|[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)|Skill|Live Agent Assist - Followup Query Enhancer|April 9, 2026|
|Live Agent Assist - Interaction Analyser|July 9, 2026|
|Live Agent Assist - KG Query Generator|July 9, 2026|
|Live Agent Assist - Recommendation Generator|July 9, 2026|
|Agent|Live Agent Assist|July 9, 2026|
|AI voice|April 9, 2026|
|Update case AI voice|June 11, 2026|
||Skill|Case summarization for approvals|April 9, 2026|
|Requested item summarization for approvals|April 9, 2026|
|Request summarization for approvals|April 9, 2026|
|[ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)|Skill|[ADR DOC actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/summarize-docs-genai-skill-ea.md)|December 11, 2025|
|[ADR DOC summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/summarize-docs-genai-skill-ea.md)|December 11, 2025|
|[Business application insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/generate-insights-into-ba.md)|December 11, 2025|
|Create diagram from image|June 11, 2026|
|Diagram change analysis|December 11, 2025|
|Refine text|December 11, 2025|
|Agent|Enterprise Architecture query agent| |
|[Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/esg-landing-page.md)|Skill|[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/extract-data-from-utility-invoices.md)|December 11, 2025|
||Agent|User resolution mapping agent|December 11, 2025|
|Skill|Generate hardware asset insights|April 9, 2026|
|Agentic workflow|Help repair hardware assets|December 11, 2025|
||Skill|Incident summarization|December 11, 2025|
|H&amp;S Action Planner|June 11, 2026|
||Skill|Common control objective creation|December 11, 2025|
|Control objective impact analyzer|December 11, 2025|
|Issue summarization|December 11, 2025|
|Recommendation of similar control objectives|December 11, 2025|
|Regulatory alert summarization|December 11, 2025|
|Regulatory alert impacted citations|December 11, 2025|
|Regulatory alert impacted control objectives|December 11, 2025|
|Regulatory alert impacted controls|December 11, 2025|
|Regulatory alert impacted policies|December 11, 2025|
|Risk assessment summarization|December 11, 2025|
|Risk event summarization|December 11, 2025|
|Agent|Control objective change agent|December 11, 2025|
|Regulatory change task planning agent|December 11, 2025|
|Report an issue|June 11, 2026|
|Risk suggestion AI agent|December 11, 2025|
|Agentic workflow|Get regulatory analysis|December 11, 2025|
|Generate regulatory action plans|December 11, 2025|
|Suggest potential risks|December 11, 2025|
|Optimize issue resolution|June 11, 2026|
|[IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/r_ITOMApplications.md)|Skill|Analyze service health|March 12, 2026|
|Analyze service observability dashboard|March 12, 2026|
|[Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/alert-summarization-now-assist.md)|January 20, 2026|
|[Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/nai-analyze-past-incidents.md)|January 20, 2026|
|Agentic workflow|[Manage alerts autonomously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-autonomous-operator-workflow.md)|January 20, 2026|
|[Analyze alert impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-agentic-aia.md)|June 11, 2026|
|Agent|Azure Monitor MCP Server|August 6, 2026|
|AWS Observability|June 11, 2026|
|SolarWinds Observability|June 11, 2026|
|Datadog APM MCP Server|June 11, 2026|
|Dynatrace MCP Server|June 11, 2026|
|Gemini Cloud Assist A2A Investigation|August 6, 2026|
|Kentik analysis|June 11, 2026|
|New Relic MCP Server|June 11, 2026|
|Prometheus API|June 11, 2026|
|Prometheus Observability|July 9, 2026|
|Splunk MCP Server|June 11, 2026|
|Splunk Observability|August 6, 2026|
|Service level objective \(SLO\) creator|March 12, 2026|
|ThousandEyes Observability|June 11, 2026|
|[ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm.md)|Skill|[Change request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/summarize-change-now-assist.md)|December 11, 2025|
|[Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/generate-chat-summary-interaction-now-assist-itsm.md)|December 11, 2025|
|Generate change risk assessments answers and reasoning|July 9, 2026|
|[Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/summarize-incident-now-assist.md)|December 11, 2025|
|[KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)|April 9, 2026|
|[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/resolve-incident-now-assist.md)|April 9, 2026|
|[Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-chat-recommendation.md)|April 9, 2026|
|Investigate boot time issues|April 9, 2026|
|Investigate Zoom call quality issues|April 9, 2026|
|Agentic workflow|Incident assist|April 9, 2026|
|Legal Service Delivery|Skill|Legal matter summarization|December 11, 2025|
|Legal request summarization|December 11, 2025|
|Conversational intake for Conflict of Interest request|March 12, 2026|
|Agentic workflow|Triage legal requests|December 11, 2025|
||Agent|Plan and execute recall campaign phases and sub-phases|March 12, 2026|
|[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)|Skill|[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)|December 11, 2025|
|Agentic workflow|[Import OT device spreadsheet into OT CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-otm-aiagents-import-ot-device-workflow.md)|December 11, 2025|
||Skill|OT incident summarization|March 12, 2026|
|OT resolution notes generation|March 12, 2026|
|Agentic workflow||March 12, 2026|
||Skill|Common control objective creation|December 11, 2025|
|Control objective impact analyzer|December 11, 2025|
|Recommendation of similar control objectives|December 11, 2025|
|Risk assessment summary|December 11, 2025|
|[Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/bun-public-sector-landing-page.md)|Agent|Investigative Case Management AI agents|March 12, 2026|
||Agentic workflow|Define PO exception mitigation strategy|March 12, 2026|
|Intent to Action|March 12, 2026|
|[ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)|Skill|[Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generating-insights-for-now-assist-for-security.md)|December 11, 2025|
|[Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-pia-report-now-assist-security-incident.md)|December 11, 2025|
|[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-closure-notes-si-now-assist-sec-incident.md)|December 11, 2025|
|[Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/na-sir-quality-assessment.md)|December 11, 2025|
|[Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-recommended-actions-now-assist-for-security.md)|December 11, 2025|
|[Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/summarize-security-incident-now-assist-sec-incident.md)|December 11, 2025|
|Agentic workflow|[Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-soc-efficiency-usecase.md)|March 12, 2026|
|[Close security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-close-incident-usecase.md)|March 12, 2026|
|[Generate SIR shift handover report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/add-incidents-shifthandover-ai-agent.md)|March 12, 2026|
|[Resolve security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
||Skill|Publisher compliance summarization|December 11, 2025|
|Product compliance summarization|December 11, 2025|
|Recommended actions|December 11, 2025|
|SaaS user resolution|December 11, 2025|
|Error log summarization|April 9, 2026|
|Error resolution recommendation|April 9, 2026|
|Contract entitlement data extraction|April 9, 2026|
|Product match reviewer|June 11, 2026|
|Software normalization|June 11, 2026|
|Agentic workflow|Reclamation rule creation|December 11, 2025|
|Removal candidate evaluation|December 11, 2025|
||Skill|EAP doc summarization|December 11, 2025|
|Identify similar records|December 11, 2025|
|Multi feedback summarization|December 11, 2025|
|Planning item doc summarization|December 11, 2025|
|Project doc summarization|December 11, 2025|
|Project insights generation|December 11, 2025|
|Refine records|December 11, 2025|
|Target generation|December 11, 2025|
|Demand summarization|March 12, 2026|
|Agentic workflow|Create stories|December 11, 2025|
|Monitor project tasks|December 11, 2025|
|[ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)|Skill|[Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)|Skill|[Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo-summarize-case.md)|December 11, 2025|
|[Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/summarize-supp-perf.md)|March 12, 2026|
|[Email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/generate-email-response-for-supplier-tasks.md)|March 12, 2026|
|[Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/slo-analyze-sentiments.md)|March 12, 2026|
|ServiceNow Otto for Sales Customer Relationship Management for Telecommunications|Agent|Move order voice AI|March 12, 2026|
|[ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md)|Agentic workflow|Squad resource identifier|March 12, 2026|
|Product release email communication|March 12, 2026|
|Agent|Service Exchange Knowledge Assistant|July 9, 2026|
|[GRC: Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md)|Skill|TPRM issue summarization|December 11, 2025|
|TPRM issue recommendation|March 12, 2026|
|ServiceNow Otto for Threat Intelligence Security Center \(TISC\) \(TISC\)|Skill|TISC case summarization|June 11, 2026|
|TISC report authoring|July 9, 2026|
|[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/vuln-landing-page.md)|Skill|Generate remediation assistance|December 11, 2025|
|[Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-approval-recommendation-skill.md)|December 11, 2025|
|[SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-insights-skill.md)|December 11, 2025|
|[SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-now-assist-api-connector.md)|December 11, 2025|
|[Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/solutions-now-assist-vulnerability-response.md)|December 11, 2025|
|[Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/dedupe-host-vi-now-assist-vulnerability-response.md)|December 11, 2025|
|ServiceNow Otto for Vault|Agentic workflow|Access observer configuration|April 9, 2026|
|Field encryption and auto-generate access policies|September 10, 2026|
|Field encryption with Vault module|April 9, 2026|
|Securing custom apps with Vault agents|April 9, 2026|
|Summarize access observer logs|April 9, 2026|
| | |Classify assets with ServiceNow Vault agents|October 10, 2026|
|ServiceNow Otto for Workplace Service Delivery \(WSD\)|Skill|Workplace case summarization|March 12, 2026|
|Agentic workflow|Workplace Concierge|April 9, 2026|
||Skill|ERP data discovery|December 11, 2025|
|ERP data query|December 11, 2025|
||Skill|[Analytics follow-up generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics hidden insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics query generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/export-db-dv-now-assist-panel.md)|January 20, 2026|
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/na-ai-agents.md)|December 11, 2025|
|[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/conversational-help-skills.md)|December 11, 2025|
|Custom skills|December 11, 2025|
|[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)|April 9, 2026|
|Now Assist Multi-Turn Catalog Ordering|December 11, 2025|
|Now Assist Q&amp;A Genius Results|December 11, 2025|
|Now Assist Topics|December 11, 2025|
|[Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)|February 5, 2026|
|[Smart documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configure-skill-smart-documents.md)|July 9, 2026|
|Subflows and actions|December 11, 2025|
|[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/platform-use-cases.md)|Agentic workflow|Error Analysis and Remediation workflow|June 11, 2026|
|[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/platform-ai-agents-overview.md)|Agent|Error Analysis and Remediation agent|June 11, 2026|


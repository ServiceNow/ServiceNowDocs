---
title: Now Assist skills, agents, and agentic workflows on by default
description: Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.html
release: zurich
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 8
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills, agents, and agentic workflows on by default

Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills, agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The Now Assist plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

## Now Assist AI assets that are on by default

[Release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/release-notes/new-features-changes.md)

|Product|Type|Asset name|Effective date|
|-------|----|----------|--------------|
|[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/impact-landing-page.md)|Skill|Outcome summarization|December 11, 2025|
|[Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-apo.md)|Skill|[Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-summarize-apo.md)|December 11, 2025|
|[Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-for-fsc-common/now-assist-fsc-summarize-po.md)|December 11, 2025|
|[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)|Agent|AI voice|March 12, 2026|
|Update case AI voice|June 11, 2026|
|[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)|Skill|[Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.md)|December 11, 2025|
|[Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.md)|December 11, 2025|
|[Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-sgc-diagnose.md)|December 11, 2025|
|Agentic workflow|[Search CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md)|December 11, 2025|
||Skill|Spoke generation|December 11, 2025|
|Playbook summarization|June 11, 2026|
||Skill|Case summarization for approvals|March 12, 2026|
|Requested item summarization for approvals|March 12, 2026|
|Request summarization for approvals|March 12, 2026|
|[Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-portfolio-management/enterprise-architecture/now-assist-ea.md)|Skill|ADR DOC actions|December 11, 2025|
|ADR DOC summarization|December 11, 2025|
|Business application insights|December 11, 2025|
|Diagram change analysis|December 11, 2025|
|Refine text|December 11, 2025|
|[Now Assist for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/operational-sustainability-management/now-assist-for-esg.md)|Skill||December 11, 2025|
|[Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-for-hardware-asset-management/now-assist-ham.md)|Skill|Generate hardware asset insights|March 12, 2026|
|Agentic workflow|Help repair hardware assets|December 11, 2025|
|Agent|User resolution mapping agent|December 11, 2025|
|[Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)|Skill|Incident summarization|December 11, 2025|
|Agentic workflow||March 12, 2026|
|[Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)|Skill|Case summarization|March 12, 2026|
|Chat reply recommendation|March 12, 2026|
|Chat summarization|March 12, 2026|
|Email reply recommendation|March 12, 2026|
|Resolution notes generation|March 12, 2026|
|Sentiment analysis|March 12, 2026|
|Sidebar discussion summarization|March 12, 2026|
|[Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md)|Skill|Common control objective creation|December 11, 2025|
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
|Agentic workflow|Get regulatory analysis|December 11, 2025|
|Generate regulatory action plans|December 11, 2025|
|Suggest potential risks|December 11, 2025|
|Optimize issue resolution|June 11, 2026|
|Agent|Control objective change agent|December 11, 2025|
|Regulatory change task planning agent|December 11, 2025|
|Report an issue|June 11, 2026|
|Risk suggestion AI agent|December 11, 2025|
|[Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)|Skill|[Analyze service health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/analyze-service-health-in-service-observability.md)|March 12, 2026|
|[Analyze service observability dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/analyze-a-dashboard-in-service-observability.md)|March 12, 2026|
|[Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/alert-summarization-now-assist.md)|January 20, 2026|
|[Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/nai-analyze-past-incidents.md)|January 20, 2026|
|[Service Mapping candidate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)|January 20, 2026|
|[Service Mapping candidates Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)|January 20, 2026|
|Agentic workflow|[Manage alerts autonomously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md)|January 20, 2026|
|[Analyze alert impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-agentic-aia.md)|June 11, 2026|
|Agent|[Service level objective \(SLO\) creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/service-level-objective-management/now-assist-itom-slo-generation.md)|March 12, 2026|
|[Datadog APM MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Dynatrace MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Kentik analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[New Relic MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Prometheus API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Splunk MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)|Skill|[Change request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-change-now-assist.md)|December 11, 2025|
|[Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-chat-recommendation.md)|March 12, 2026|
|[Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/generate-chat-summary-interaction-now-assist-itsm.md)|December 11, 2025|
|[Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-incident-now-assist.md)|December 11, 2025|
|[Investigate boot time issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/investigate-and-resolve-boot-time-issues.md)|March 12, 2026|
|[Investigate Zoom call quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/investigate-and-resolve-zoom-call-issues.md)|March 12, 2026|
|[KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/Now-Assist-generate-article-SOW-itsm.md)|March 12, 2026|
|[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/resolve-incident-now-assist.md)|March 12, 2026|
|[Summarize a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-change-now-assist.md)|January 20, 2026|
|[Summarize a chat conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/generate-chat-summary-interaction-now-assist-itsm.md)|January 20, 2026|
|[Summarize an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-incident-now-assist.md)|January 20, 2026|
|Agentic workflow|[Incident assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-incident-assist-workflow.md)|April 09, 2026|
|[Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)|Skill|Legal matter summarization|December 11, 2025|
|Legal request summarization|December 11, 2025|
|Agentic workflow|Triage legal requests|December 11, 2025|
|[Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-otm-landing.md)|Agentic workflow|[Import OT device spreadsheet into OT CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-otm-aiagents-import-ot-device-workflow.md)|December 11, 2025|
|[Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-otm-landing.md)|Skill|[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)|December 11, 2025|
|[Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)|Skill|[OT incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/summarize-ot-incident-now-assist.md)|March 12, 2026|
|[OT resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/generate-resolution-notes-ot-incident.md)|March 12, 2026|
|Agentic workflow|[Generate OT KB articles agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/agent-ot-knowledge-generator.md)|March 12, 2026|
||Skill|Common control objective creation|December 11, 2025|
|Control objective impact analyzer|December 11, 2025|
|Recommendation of similar control objectives|December 11, 2025|
|Risk assessment summary|December 11, 2025|
|[Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/finance-and-supply-chain/purchase-order-mgmt-landing-page.md)|Agentic workflow|Define PO exception mitigation strategy|March 12, 2026|
|Email Intent to Action|March 12, 2026|
|[Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)|Skill|[Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/generating-insights-for-now-assist-for-security.md)|December 11, 2025|
|[Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/generate-pia-report-now-assist-security-incident.md)|December 11, 2025|
|[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/generate-closure-notes-si-now-assist-sec-incident.md)|December 11, 2025|
|[Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/na-sir-quality-assessment.md)|December 11, 2025|
|[Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/generate-recommended-actions-now-assist-for-security.md)|December 11, 2025|
|[Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/summarize-security-incident-now-assist-sec-incident.md)|December 11, 2025|
|Natural Language Condition Evaluator|March 12, 2026|
|Agentic workflow|[Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-soc-efficiency-usecase.md)|March 12, 2026|
|[Close security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-close-incident-usecase.md)|March 12, 2026|
|[Generate SIR shift handover report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/add-incidents-shifthandover-ai-agent.md)|March 12, 2026|
|[Resolve security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|Agent|[Endpoint Detection and Response AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Exchange online integration handling AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Observable analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Security incident resolution AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Security incident wrap up generator AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Security incident activities handling AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Security incident shift handover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/add-incidents-shifthandover-ai-agent.md)|March 12, 2026|
|[Security incident retrieval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-soc-efficiency-usecase.md)|March 12, 2026|
|[Security metrics analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-soc-efficiency-usecase.md)|March 12, 2026|
|[Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam.md)|Skill|Publisher compliance summarization|December 11, 2025|
|Product compliance summarization|December 11, 2025|
|Recommended actions|December 11, 2025|
|SaaS user resolution|December 11, 2025|
|Error log summarization|April 09, 2026|
|Error resolution recommendation|April 09, 2026|
|Contract entitlement data extraction|April 09, 2026|
|Product match reviewer|June 11, 2026|
|Software normalization|June 11, 2026|
|Agentic workflow|Reclamation rule creation|December 11, 2025|
|Removal candidate evaluation|December 11, 2025|
|[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)|Skill|EAP doc summarization|December 11, 2025|
|Feedback summarization|December 11, 2025|
|Identify similar records|December 11, 2025|
|Multi feedback summarization|December 11, 2025|
|Planning item doc summarization|December 11, 2025|
|Project doc summarization|December 11, 2025|
|Project insights generation|December 11, 2025|
|Refine records|December 11, 2025|
|Target generation|December 11, 2025|
|Agentic workflow|Create stories|December 11, 2025|
|Monitor project tasks|December 11, 2025|
|[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)|Skill|[Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)|Skill|[Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-summarize-case.md)|December 11, 2025|
|[Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/supplier-lifecycle-operations/summarize-supp-perf.md)|March 12, 2026|
|[Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/third-party-risk-management/now-assist-tprm.md)|Skill|TPRM issue summarization|December 11, 2025|
|[Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-vulnerability-response-vr/now-assist-for-vulnerability-response-landing.md)|Skill|Generate remediation assistance|December 11, 2025|
|[Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/sem-approval-recommendation-skill.md)|December 11, 2025|
|[SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/sem-insights-skill.md)|December 11, 2025|
|[SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/using-now-assist-api-connector.md)|December 11, 2025|
|[Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/solutions-now-assist-vulnerability-response.md)|December 11, 2025|
|[Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/dedupe-host-vi-now-assist-vulnerability-response.md)|December 11, 2025|
|[Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-landing.md)|Skill|Workplace case summarization|March 12, 2026|
||Skill|ERP data discovery|December 11, 2025|
|ERP data query|December 11, 2025|
|[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/contract-management-pro/cncore-now-assit-landing.md)|Skill|Contracts query enhancer|December 11, 2025|
|Duration to days converter|December 11, 2025|
|Search contract with contextual input|December 11, 2025|
|Conversational contract search and insights|March 12, 2026|
|[Now Assist in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/now-assist-platform-analytics.md)|Skill|[Analytics follow-up generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/enable-query-generation.md)|December 11, 2025|
|[Analytics hidden insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/enable-query-generation.md)|December 11, 2025|
|[Analytics insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/enable-query-generation.md)|December 11, 2025|
|[Analytics query generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/enable-query-generation.md)|December 11, 2025|
|[Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/platform-analytics/export-db-dv-now-assist-panel.md)|January 20, 2026|
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)|February 5, 2026|
|[AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/na-ai-agents.md)|December 11, 2025|
|[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/conversational-help-skills.md)|December 11, 2025|
|Custom skills|December 11, 2025|
|[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)|March 12, 2026|
|[Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/document-intelligence/exploring-docintel.md)|March 12, 2026|
|Now Assist Multi-Turn Catalog Ordering|December 11, 2025|
|Now Assist Q&amp;A Genius Results|December 11, 2025|
|Now Assist Topics|December 11, 2025|
|[Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)|February 5, 2026|
|Subflows and actions|December 11, 2025|


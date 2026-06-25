---
title: Now Assist skills, agents, and agentic workflows on by default
description: Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.html
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 9
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills, agents, and agentic workflows on by default

Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills, agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Australia Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The Now Assist plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Now Assist AI assets that are on by default

[Release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

|Product|Type|Asset name|Effective date|
|-------|----|----------|--------------|
||Agentic workflow|Help repair enterprise assets|April 9, 2026|
|[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md)|Skill|Outcome summarization|December 11, 2025|
|[Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-apo.md)|Skill|[Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-summarize-apo.md)|December 11, 2025|
|[Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-fsc-summarize-po.md)|December 11, 2025|
||Skill|Acceptance criteria generation|December 11, 2025|
|Doc generation|December 11, 2025|
|Task generation|December 11, 2025|
|[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-landing-cmdb.md)|Skill|[Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)|December 11, 2025|
|[Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-cmdb-mng-dupe-cis-skill.md)|December 11, 2025|
|[Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-sgc-diagnose.md)|December 11, 2025|
|Agentic workflow|[Search CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-search.md)|December 11, 2025|
|[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-now-assit-landing.md)|Skill|Contracts query enhancer|December 11, 2025|
|Contracts query classifier|April 9, 2026|
|Duration to days converter|December 11, 2025|
|Search contract with contextual input|December 11, 2025|
|[Now Assist for Core Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)|Agent|[CBS bulk upload agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
|[CBS configuration agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
|[IA orchestration agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
|[Manage groups and roles agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
|[Notification agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
|Skill|[Next Best Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)|April 9, 2026|
|[Error Resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)|April 9, 2026|
|Agentic workflow|[AI agentic workflow for the CBS setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/using-ai-agent-workflows-na-cbs.md)|April 9, 2026|
||Skill|Spoke generation|December 11, 2025|
|Playbook summarization|June 11, 2026|
|[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-csm.md)|Agent|AI voice|April 9, 2026|
|Update case AI voice|June 11, 2026|
||Skill|Case summarization for approvals|April 9, 2026|
|Requested item summarization for approvals|April 9, 2026|
|Request summarization for approvals|April 9, 2026|
|[Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-ea.md)|Skill|ADR DOC actions|December 11, 2025|
|ADR DOC summarization|December 11, 2025|
|Business application insights|December 11, 2025|
|Create diagram from image|June 11, 2026|
|Diagram change analysis|December 11, 2025|
|Refine text|December 11, 2025|
|Agent|Enterprise Architecture query agent| |
|Operational Sustainability Management \(formerly Environmental, Social, and Governance\)|Skill||December 11, 2025|
|[Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-ham.md)|Agent|User resolution mapping agent|December 11, 2025|
|Skill|Generate hardware asset insights|April 09, 2026|
|Agentic workflow|Help repair hardware assets|December 11, 2025|
|[Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-hs-landing.md)|Skill|Incident summarization|December 11, 2025|
|H&amp;S Action Planner|June 11, 2026|
|[Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-for-irm.md)|Skill|Common control objective creation|December 11, 2025|
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
|[Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom.md)|Skill|[Analyze service health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/analyze-service-health-in-service-observability.md)|March 12, 2026|
|[Analyze service observability dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/analyze-a-dashboard-in-service-observability.md)|March 12, 2026|
|[Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/alert-summarization-now-assist.md)|January 20, 2026|
|[Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/nai-analyze-past-incidents.md)|January 20, 2026|
|Agentic workflow|[Manage alerts autonomously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-autonomous-operator-workflow.md)|January 20, 2026|
|[Analyze alert impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom-agentic-aia.md)|June 11, 2026|
|Agent|[ThousandEyes Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[AWS Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[SolarWinds Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Datadog APM MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Dynatrace MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Kentik analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[New Relic MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Prometheus API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Splunk MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md)|June 11, 2026|
|[Service level objective \(SLO\) creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom-slo-generation.md)|March 12, 2026|
||Skill|Change request summarization|December 11, 2025|
|Chat summarization|December 11, 2025|
|Incident summarization|December 11, 2025|
|KB generation|April 09, 2026|
|Resolution notes generation|April 09, 2026|
|Chat reply recommendation|April 09, 2026|
|Investigate boot time issues|April 09, 2026|
|Investigate Zoom call quality issues|April 09, 2026|
|Agentic workflow|Incident assist|April 09, 2026|
|[Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-lsd-landing.md)|Skill|Legal matter summarization|December 11, 2025|
|Legal request summarization|December 11, 2025|
|Conversational intake for Conflict of Interest request|March 12, 2026|
|Agentic workflow|Triage legal requests|December 11, 2025|
|[Now Assist for Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/now-assist-for-MCO.md)|Skill|[Enhance non conformance description](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-report-an-issue_AI.md)|March 12, 2026|
|Agent|[Plan and execute recall campaign phases and sub-phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-plan-and-execute-recall-campaign-phases-and-subphases.md)|March 12, 2026|
|[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-otm-landing.md)|Skill|[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)|December 11, 2025|
|Agentic workflow|[Import OT device spreadsheet into OT CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-otm-aiagents-import-ot-device-workflow.md)|December 11, 2025|
|[Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)|Skill|[OT incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/summarize-ot-incident-now-assist.md)|March 12, 2026|
|[OT resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-resolution-notes-ot-incident.md)|March 12, 2026|
|Agentic workflow|[Generate OT KB articles agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/agent-ot-knowledge-generator.md)|March 12, 2026|
||Skill|Common control objective creation|December 11, 2025|
|Control objective impact analyzer|December 11, 2025|
|Recommendation of similar control objectives|December 11, 2025|
|Risk assessment summary|December 11, 2025|
|[Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-for-psds.md)|Agent|Investigative Case Management AI agents|March 12, 2026|
|[Now Assist for Purchase Order Management \(POM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-for-purch-order-magmt.md)|Agentic workflow|[Define PO exception mitigation strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/mitigation-strategies-for-po-exceptions.md)|March 12, 2026|
|[Email Intent to Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/convert-emails-to-exceptions.md)|March 12, 2026|
|[Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-security-incident-landing.md)|Skill|[Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generating-insights-for-now-assist-for-security.md)|December 11, 2025|
|[Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-pia-report-now-assist-security-incident.md)|December 11, 2025|
|[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-closure-notes-si-now-assist-sec-incident.md)|December 11, 2025|
|[Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/na-sir-quality-assessment.md)|December 11, 2025|
|[Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-recommended-actions-now-assist-for-security.md)|December 11, 2025|
|[Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/summarize-security-incident-now-assist-sec-incident.md)|December 11, 2025|
|Agentic workflow|[Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-sir-soc-efficiency-usecase.md)|March 12, 2026|
|[Close security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-sir-close-incident-usecase.md)|March 12, 2026|
|[Generate SIR shift handover report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/add-incidents-shifthandover-ai-agent.md)|March 12, 2026|
|[Resolve security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)|March 12, 2026|
|[Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam.md)|Skill|Publisher compliance summarization|December 11, 2025|
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
|[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-spm.md)|Skill|EAP doc summarization|December 11, 2025|
|Feedback summarization|December 11, 2025|
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
|[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo.md)|Skill|[Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)|December 11, 2025|
|[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-slo.md)|Skill|[Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-slo-summarize-case.md)|December 11, 2025|
|[Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/summarize-supp-perf.md)|March 12, 2026|
|[Email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/generate-email-response-for-supplier-tasks.md)|March 12, 2026|
|[Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/slo-analyze-sentiments.md)|March 12, 2026|
|[Now Assist for Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/somt-now-assist.md)|Agent|[Move order voice AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-move-order-somt.md)|March 12, 2026|
|[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-spmc.md)|Agentic workflow|[Squad resource identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-squad-resource-identifier.md)|March 12, 2026|
|[Product release email communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-product-release-email-communication.md)|March 12, 2026|
|[Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-tprm.md)|Skill|TPRM issue summarization|December 11, 2025|
|TPRM issue recommendation|March 12, 2026|
|[Now Assist for Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-tisc-landing.md)|Skill|[TISC case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-tisc-case-summarization.md)|June 11, 2026|
|[Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-landing.md)|Skill|Generate remediation assistance|December 11, 2025|
|[Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-approval-recommendation-skill.md)|December 11, 2025|
|[SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-insights-skill.md)|December 11, 2025|
|[SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/using-now-assist-api-connector.md)|December 11, 2025|
|[Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/solutions-now-assist-vulnerability-response.md)|December 11, 2025|
|[Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/dedupe-host-vi-now-assist-vulnerability-response.md)|December 11, 2025|
|[Now Assist for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-landing.md)|Agentic workflow|[Access observer configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-access-observer-config.md)|April 09, 2026|
|[Field encryption with Vault module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-field-encryption-module.md)|April 09, 2026|
|[Securing custom apps with Vault agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-securing-custom-apps-agents.md)|April 09, 2026|
|[Summarize access observer logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-access-observer-logs.md)|April 09, 2026|
|[Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-wsd-landing.md)|Skill|Workplace case summarization|March 12, 2026|
|Agentic workflow|Workplace Concierge|April 09, 2026|
||Skill|ERP data discovery|December 11, 2025|
|ERP data query|December 11, 2025|
|[Now Assist in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md)|Skill|[Analytics follow-up generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics hidden insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Analytics query generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-query-generation.md)|December 11, 2025|
|[Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-db-dv-now-assist-panel.md)|January 20, 2026|
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md)|December 11, 2025|
|[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)|December 11, 2025|
|Custom skills|December 11, 2025|
|[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)|April 09, 2026|
|[Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/exploring-docintel.md)|April 09, 2026|
|Now Assist Multi-Turn Catalog Ordering|December 11, 2025|
|Now Assist Q&amp;A Genius Results|December 11, 2025|
|Now Assist Topics|December 11, 2025|
|[Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)|February 5, 2026|
|Subflows and actions|December 11, 2025|
|[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md)|Agentic workflow|[Error Analysis and Remediation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/error-framework-daw.md)|June 11, 2026|
|[Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents.md)|Agent|[Error Analysis and Remediation agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/error-framework-daw.md)|June 11, 2026|


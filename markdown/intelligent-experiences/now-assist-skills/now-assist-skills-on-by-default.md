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
reading_time_minutes: 8
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

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/ai-native-sku-overview.md).

## Now Assist AI assets that are on by default

Release notes

|Product|Type|Asset name|Effective date|
|-------|----|----------|--------------|
||Agentic workflow|Help repair enterprise assets|April 9, 2026|
||Skill|Outcome summarization|December 11, 2025|
||Skill|Invoice case summarization|December 11, 2025|
|Purchase order summarization|December 11, 2025|
||Skill|Acceptance criteria generation|December 11, 2025|
|Doc generation|December 11, 2025|
|Task generation|December 11, 2025|
||Skill|Configuration item \(CI\) summarization|December 11, 2025|
|Manage duplicate CIs|December 11, 2025|
|Service Graph Connector diagnosis|December 11, 2025|
|Agentic workflow|Search CMDB|December 11, 2025|
||Skill|Contracts query enhancer|December 11, 2025|
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
|Now Assist for Customer Service Management \(CSM\)|Agent|AI voice|April 9, 2026|
|Update case AI voice|June 11, 2026|
||Skill|Case summarization for approvals|April 9, 2026|
|Requested item summarization for approvals|April 9, 2026|
|Request summarization for approvals|April 9, 2026|
||Skill|ADR DOC actions|December 11, 2025|
|ADR DOC summarization|December 11, 2025|
|Business application insights|December 11, 2025|
|Create diagram from image|June 11, 2026|
|Diagram change analysis|December 11, 2025|
|Refine text|December 11, 2025|
|Agent|Enterprise Architecture query agent| |
|Operational Sustainability Management \(formerly Environmental, Social, and Governance\)|Skill||December 11, 2025|
||Agent|User resolution mapping agent|December 11, 2025|
|Skill|Generate hardware asset insights|April 09, 2026|
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
||Skill|Analyze service health|March 12, 2026|
|Analyze service observability dashboard|March 12, 2026|
|Alert analysis|January 20, 2026|
|Alert investigation|January 20, 2026|
|Agentic workflow|Manage alerts autonomously|January 20, 2026|
|Analyze alert impact|June 11, 2026|
|Agent|ThousandEyes Observability|June 11, 2026|
|AWS Observability|June 11, 2026|
|SolarWinds Observability|June 11, 2026|
|Datadog APM MCP Server|June 11, 2026|
|Dynatrace MCP Server|June 11, 2026|
|Kentik analysis|June 11, 2026|
|New Relic MCP Server|June 11, 2026|
|Prometheus API|June 11, 2026|
|Splunk MCP Server|June 11, 2026|
|Service level objective \(SLO\) creator|March 12, 2026|
||Skill|Change request summarization|December 11, 2025|
|Chat summarization|December 11, 2025|
|Incident summarization|December 11, 2025|
|KB generation|April 09, 2026|
|Resolution notes generation|April 09, 2026|
|Chat reply recommendation|April 09, 2026|
|Investigate boot time issues|April 09, 2026|
|Investigate Zoom call quality issues|April 09, 2026|
|Agentic workflow|Incident assist|April 09, 2026|
||Skill|Legal matter summarization|December 11, 2025|
|Legal request summarization|December 11, 2025|
|Conversational intake for Conflict of Interest request|March 12, 2026|
|Agentic workflow|Triage legal requests|December 11, 2025|
||Skill|Enhance non conformance description|March 12, 2026|
|Agent|Plan and execute recall campaign phases and sub-phases|March 12, 2026|
||Skill|Search for a related record|December 11, 2025|
|Agentic workflow|Import OT device spreadsheet into OT CMDB|December 11, 2025|
||Skill|OT incident summarization|March 12, 2026|
|OT resolution notes generation|March 12, 2026|
|Agentic workflow||March 12, 2026|
||Skill|Common control objective creation|December 11, 2025|
|Control objective impact analyzer|December 11, 2025|
|Recommendation of similar control objectives|December 11, 2025|
|Risk assessment summary|December 11, 2025|
||Agent|Investigative Case Management AI agents|March 12, 2026|
||Agentic workflow|Define PO exception mitigation strategy|March 12, 2026|
|Email Intent to Action|March 12, 2026|
||Skill|Correlation insights generation|December 11, 2025|
|Post-incident analysis|December 11, 2025|
|Resolution notes generation|December 11, 2025|
|Security incident quality assessment|December 11, 2025|
|Security incident recommended actions|December 11, 2025|
|Security incident summarization|December 11, 2025|
|Agentic workflow|Analyze security operations metrics|March 12, 2026|
|Close security incident|March 12, 2026|
|Generate SIR shift handover report|March 12, 2026|
|Resolve security incident|March 12, 2026|
||Skill|Publisher compliance summarization|December 11, 2025|
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
||Skill|EAP doc summarization|December 11, 2025|
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
||Skill|Negotiation summarization|December 11, 2025|
|Procurement case summarization|December 11, 2025|
|Purchase requisition summarization|December 11, 2025|
|Sourcing event summarization|December 11, 2025|
|Sourcing request summarization|December 11, 2025|
||Skill|Supplier case summarization|December 11, 2025|
|Supplier performance summarization|March 12, 2026|
|Email response|March 12, 2026|
|Sentiment analysis|March 12, 2026|
|Now Assist for Sales CRM for Telecommunications|Agent|Move order voice AI|March 12, 2026|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|Agentic workflow|Squad resource identifier|March 12, 2026|
|Product release email communication|March 12, 2026|
||Skill|TPRM issue summarization|December 11, 2025|
|TPRM issue recommendation|March 12, 2026|
||Skill|TISC case summarization|June 11, 2026|
||Skill|Generate remediation assistance|December 11, 2025|
|Now Assist recommendation|December 11, 2025|
|SEM insights|December 11, 2025|
|SPC setup connector|December 11, 2025|
|Suggest vulnerability solutions|December 11, 2025|
|Vulnerable item deduplication|December 11, 2025|
|Now Assist for Vault|Agentic workflow|Access observer configuration|April 09, 2026|
|Field encryption with Vault module|April 09, 2026|
|Securing custom apps with Vault agents|April 09, 2026|
|Summarize access observer logs|April 09, 2026|
|Now Assist for Workplace Service Delivery \(WSD\)|Skill|Workplace case summarization|March 12, 2026|
|Agentic workflow|Workplace Concierge|April 09, 2026|
||Skill|ERP data discovery|December 11, 2025|
|ERP data query|December 11, 2025|
||Skill|Analytics follow-up generation|December 11, 2025|
|Analytics hidden insights generation|December 11, 2025|
|Analytics insights generation|December 11, 2025|
|Analytics query generation|December 11, 2025|
|Dashboard and visualization export|January 20, 2026|
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/na-ai-agents.md)|December 11, 2025|
|[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)|December 11, 2025|
|Custom skills|December 11, 2025|
|[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)|April 09, 2026|
|[Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/exploring-docintel.md)|April 09, 2026|
|Now Assist Multi-Turn Catalog Ordering|December 11, 2025|
|Now Assist Q&amp;A Genius Results|December 11, 2025|
|Now Assist Topics|December 11, 2025|
|[Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)|February 5, 2026|
|Subflows and actions|December 11, 2025|
|[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-use-cases.md)|Agentic workflow|Error Analysis and Remediation workflow|June 11, 2026|
|[Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-ai-agents.md)|Agent|Error Analysis and Remediation agent|June 11, 2026|


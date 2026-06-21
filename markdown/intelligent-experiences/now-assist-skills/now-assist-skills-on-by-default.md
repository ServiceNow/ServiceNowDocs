---
title: Now Assist skills, agents, and agentic workflows on by default
description: Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.html
release: yokohama
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 7
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills, agents, and agentic workflows on by default

Starting with the Zurich Patch 4 release, some Now Assist skills, agents, and agentic workflows are turned on by default.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills, agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Yokohama Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The Now Assist plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

|Product|Type|Asset name|Effective date|Release notes|
|-------|----|----------|--------------|-------------|
||Skill|Outcome summarization|January 20, 2026||
||Skill|Invoice case summarization|January 20, 2026||
||Skill|Purchase order summarization|January 20, 2026||
||Skill|Doc generation|January 20, 2026||
||Skill|Task generation|January 20, 2026||
||Skill|Configuration item \(CI\) summarization|January 20, 2026| |
||Skill|Manage duplicate CIs|January 20, 2026| |
||Skill|Service Graph Connector diagnosis|January 20, 2026| |
||Agentic workflow|Search CMDB|January 20, 2026| |
||Skill|Spoke generation|January 20, 2026||
||Skill|ADR DOC actions|January 20, 2026||
||Skill|ADR DOC summarization|January 20, 2026||
||Skill|Business application insights|January 20, 2026||
||Skill||January 20, 2026| |
||Agent|User resolution mapping agent|January 20, 2026||
||Agentic workflow|Help repair hardware assets|January 20, 2026||
||Skill|Incident summarization|January 20, 2026| |
||Skill|Common control objective creation|January 20, 2026| |
||Agent|Control objective change agent|January 20, 2026| |
||Agentic workflow|Get regulatory analysis|January 20, 2026| |
||Agentic workflow|Generate regulatory action plans|January 20, 2026| |
||Skill|Issue summarization|January 20, 2026| |
||Skill|Recommendation of similar control objectives|January 20, 2026| |
||Skill|Regulatory alert summarization|January 20, 2026| |
||Skill|Regulatory alert impacted citations|January 20, 2026| |
||Skill|Regulatory alert impacted control objectives|January 20, 2026| |
||Skill|Regulatory alert impacted controls|January 20, 2026| |
||Skill|Regulatory alert impacted policies|January 20, 2026| |
||Agent|Regulatory change task planning agent|January 20, 2026| |
||Skill|Risk assessment summarization|January 20, 2026| |
||Skill|Risk event summarization|January 20, 2026| |
||Agent|Risk suggestion AI agent|January 20, 2026| |
||Agentic workflow|Suggest potential risks|January 20, 2026| |
||Skill|Change request summarization|January 20, 2026||
||Skill|Alert analysis|January 20, 2026||
||Skill|Alert investigation|January 20, 2026||
||Skill|Service Mapping Candidate|January 20, 2026||
||Skill|Service Mapping Candidates Impact|January 20, 2026||
||Agentic workflow|Manage alerts autonomously|January 20, 2026||
||Skill|Chat summarization|January 20, 2026||
||Skill|Incident summarization|January 20, 2026||
||Skill|Investigate boot time issues|May 5, 2026||
||Skill|Investigate Zoom call quality issues|May 5, 2026||
||Skill|Summarize a change request|January 20, 2026||
||Skill|Summarize a chat conversation|January 20, 2026||
||Skill|Summarize an incident|January 20, 2026||
||Skill|Legal matter summarization|January 20, 2026||
||Skill|Legal request summarization|January 20, 2026||
||Agentic workflow|Triage legal requests|January 20, 2026||
||Agentic workflow|Import OT device spreadsheet into OT CMDB|January 20, 2026||
||Skill|Search for a related record|January 20, 2026||
||Skill|Common control objective creation|January 20, 2026||
||Skill|Control objective impact analyzer|January 20, 2026||
||Skill|Recommendation of similar control objectives|January 20, 2026||
||Skill|Risk assessment summary|January 20, 2026||
||Skill|Correlation insights generation|January 20, 2026||
||Skill|Post-incident analysis|January 20, 2026||
||Skill|Resolution notes generation|January 20, 2026||
||Skill|Security incident quality assessment|January 20, 2026||
||Skill|Security incident recommended actions|January 20, 2026||
||Skill|Security incident summarization|January 20, 2026||
||Skill|Contract entitlement data extraction|May 05, 2026||
||Skill|Publisher compliance summarization|January 20, 2026||
||Skill|Product compliance summarization|January 20, 2026||
||Skill|Recommended actions|January 20, 2026||
||Skill|Error log summarization|April 09, 2026||
||Skill|Error resolution recommendation|April 09, 2026||
||Agentic workflow|Reclamation rule creation|January 20, 2026||
||Agentic workflow|Removal candidate evaluation|January 20, 2026||
||Skill|SaaS user resolution|January 20, 2026||
||Skill|EAP doc summarization|January 20, 2026||
||Skill|Feedback summarization|January 20, 2026||
||Skill|Identify similar records|January 20, 2026||
||Agentic workflow|Monitor project tasks|January 20, 2026||
||Skill|Multi feedback summarization|January 20, 2026||
||Skill|Planning item doc summarization|January 20, 2026||
||Skill|Project doc summarization|January 20, 2026||
||Skill|Project insights generation|January 20, 2026||
||Skill|Refine records|January 20, 2026||
||Skill|Target generation|January 20, 2026||
||Skill|Negotiation summarization|January 20, 2026||
||Skill|Procurement case summarization|January 20, 2026||
||Skill|Purchase requisition summarization|January 20, 2026||
||Skill|Sourcing event summarization|January 20, 2026||
||Skill|Sourcing request summarization|January 20, 2026||
||Skill|Supplier case summarization|January 20, 2026||
||Skill|TPRM issue summarization|January 20, 2026| |
||Skill|Generate remediation assistance|January 20, 2026||
||Skill|Now Assist recommendation|January 20, 2026||
||Skill|SEM insights|January 20, 2026||
||Skill|SPC setup connector|January 20, 2026||
||Skill|Suggest vulnerability solutions|January 20, 2026||
||Skill|Vulnerable item deduplication|January 20, 2026||
||Skill|Contracts query enhancer|January 20, 2026||
||Skill|Duration to days converter|January 20, 2026||
||Skill|Search contract with contextual input|January 20, 2026||
||Skill|Analytics follow-up generation|January 20, 2026||
||Skill|Analytics hidden insights generation|January 20, 2026||
||Skill|Analytics insights generation|January 20, 2026||
||Skill|Analytics query generation|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/enable-ai-experiences/na-ai-agents.md)|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/conversational-help-skills.md)|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|Custom skills|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)|May 05, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|[Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/document-intelligence/exploring-docintel.md)|May 05, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|Now Assist Multi-Turn Catalog Ordering|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|Now Assist Q&amp;A Genius Results|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|Now Assist Topics|January 20, 2026||
|[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)|Skill|Subflows and actions|January 20, 2026||


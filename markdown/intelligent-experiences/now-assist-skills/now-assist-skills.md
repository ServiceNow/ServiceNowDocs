---
title: Now Assist skills
description: Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skills/now-assist-skills.html
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 10
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Now Assist skills overview

Now Assist skills are discrete, reusable generative AI capabilities that perform a specific type of work within a workflow. A skill focuses on a single, well‑defined task, such as summarizing content, generating text, analyzing records, or providing recommendations, and returns an output that can be reviewed, used, or acted on by a user or workflow.

Skills are the foundational AI building blocks used across Now Assist experiences, workflows, and products. They enable AI‑powered assistance without requiring custom model development.

## What a skill does

Skills are designed to:

-   Perform one focused action

    A skill handles a specific task, such as summarizing a record, generating a response, or analyzing data, rather than completing an end to end workflow.

-   Operate within an existing workflow or product context

    Skills are used in the context of where users work, such as records, tasks, forms, or panels, and act on the data available in that context.

-   Use generative AI safely and securely

    Skills run on the ServiceNow AI Platform and respect data boundaries, access controls, and domain separation.

-   Return usable output

    The output of a skill can be reviewed by the user, edited if needed, or used to support downstream actions in a workflow.


## How users interact with skills

Depending on the product and configuration, users can interact with skills in different ways:

-   Triggering a skill from a contextual UI, such as a panel or record.
-   Using a skill as part of a workflow driven experience.
-   Receiving output generated automatically by a workflow or agentic process.

In all cases, skills are designed to assist, not replace, user decision making by reducing manual effort.

**Note:** Some skills are turned on by default, depending on the product and release. Other skills require explicit enablement or configuration in the Now Assist admin experience. Deactivating certain skills may impact dependent features or workflows.

## Available skills by workflow

<table id="table_yz3_mqd_dbc"><thead><tr><th class="filter">

Workflow

</th><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

Technology

</td><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   Acceptance criteria generation
-   Docs summarization
-   Doc generation
-   Task generation

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-landing-cmdb.md)

</td><td>

-   [Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)
-   [Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-cmdb-mng-dupe-cis-skill.md)
-   [Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-sgc-diagnose.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Core Business Suite \(CBS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)

</td><td>

-   [Next Best Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)
-   [Error Resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/now-assist-cbs.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-ea.md)

</td><td>

-   ADR DOC summarization and actions
-   Business application insights
-   Create diagram from image
-   Diagram change analysis
-   Refine text
-   Register a business application
-   Register a digital integration

</td></tr><tr><td>

Technology

</td><td>

Operational Sustainability Management \(formerly Environmental, Social, and Governance\)

</td><td>



</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-ham.md)

</td><td>

-   Generate hardware asset insights

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-for-irm.md)

</td><td>

-   Common control objective creation
-   Control objective impact analyzer
-   
-   Issue summarization
-   Recommendations for regulatory alert impacted areas
-   Recommendation of similar control objectives
-   Regulatory alert summarization
-   Regulatory alert impacted citations
-   Regulatory alert impacted control objectives
-   Regulatory alert impacted controls
-   Regulatory alert impacted policies
-   Risk assessment summarization
-   Risk event summarization
-   Risk event summarization in the classic UI


</td></tr><tr><td>

Technology

</td><td>

[Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom.md)

</td><td>

-   [Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/alert-summarization-now-assist.md)
-   [Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/nai-analyze-past-incidents.md)
-   [Analyze service health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/analyze-service-health-in-service-observability.md)
-   [Analyze service observability dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/analyze-a-dashboard-in-service-observability.md)
-   [LEAP installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap.md)
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Catalog task summarization
-   Change request risk explanation
-   Change request summarization
-   Chat reply recommendation
-   Chat summarization
-   Email recommendation
-   Incident assist
-   Incident sentiment analysis
-   Incident summarization
-   Investigate boot time issues
-   Investigate Zoom call quality issues
-   KB generation
-   Release notes generation
-   Request activity response generation
-   Request summarization
-   Requested item activity response generation
-   Requested item summarization
-   Resolution notes generation
-   Sidebar discussion summarization
-   Suggested steps generation

</td></tr><tr><td>

Technology

</td><td>

[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-otm-landing.md)

</td><td>

[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)

</td><td>

-   [OT incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/summarize-ot-incident-now-assist.md)
-   [OT resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-resolution-notes-ot-incident.md)

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Control objective impact analyzer
-   Common control objective creation
-   Recommendation of similar control objectives
-   Risk assessment summary

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-security-incident-landing.md)

</td><td>

-   [Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generating-insights-for-now-assist-for-security.md)
-   [Generate content for shift handover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/add-incidents-shifthandover-ai-agent.md)
-   [Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-pia-report-now-assist-security-incident.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-closure-notes-si-now-assist-sec-incident.md)
-   [Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/na-sir-quality-assessment.md)
-   [Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/generate-recommended-actions-now-assist-for-security.md)
-   [Security incident resolution plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/config-resolution-plan-skill.md)
-   [Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/summarize-security-incident-now-assist-sec-incident.md)
-   [Security operations metrics analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-sir-soc-efficiency-usecase.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam.md)

</td><td>

-   Contract entitlement data extraction
-   Error log summarization
-   Error resolution recommendation
-   Publisher compliance summarization
-   Product compliance summarization
-   Product match reviewer
-   Recommended actions
-   Software normalization
-   SaaS user resolution

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-spm.md)

</td><td>

-   Create a demand
-   EAP doc summarization
-   Identify similar records
-   Demand summarization
-   Goal insights
-   Multi feedback summarization
-   Planning item doc summarization
-   Project doc summarization
-   Project insights generation
-   Refine records
-   Story generation
-   Target generation
-   Write planning item

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-tprm.md)

</td><td>

-   TPRM issue summarization
-   TPRM issue management recommendation

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-tisc-landing.md)

</td><td>

[TISC case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-tisc-case-summarization.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-landing.md)

</td><td>

-   [Approval recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-approval-recommendation-skill.md)
-   [Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-approval-recommendation-skill.md)
-   [SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-insights-skill.md)
-   [SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/using-now-assist-api-connector.md)
-   [Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/solutions-now-assist-vulnerability-response.md)
-   [Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/dedupe-host-vi-now-assist-vulnerability-response.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-csm.md)

</td><td>

-   Activity response generation
-   Automated quality assurance
-   Case summarization
-   Chat recommendation
-   Chat summarization
-   Customer summarization
-   Email recommendation
-   KB generation
-   Resolution notes generation
-   Sentiment analysis case
-   Sentiment analysis dashboard
-   Sentiment analysis for email interactions
-   Sidebar summarization
-   Special handling notes summarization
-   Suggested steps generation
-   Trending topics dashboard

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-fsm.md)

</td><td>

-   KB generation
-   Sidebar summarization
-   Work order task summarization

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)

</td><td>

-   Case summarization
-   Disputes intake via Virtual Agent
-   Customer profile summarization
-   Customer interaction context summary
-   Insurance customer profile summarization
-   Insurance interaction context summary

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/now-assist-for-MCO.md)

</td><td>

[Enhance non conformance description](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-report-an-issue_AI.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-management.md)

</td><td>

[Order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-summarize-order.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-for-psds.md)

</td><td>

-   Government case summarization
-   Chat summarization

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-for-sales-and-order-management-som.md)

</td><td>

[Opportunity summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-spmc.md)

</td><td>

-   [Account onboarding case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-onboard-case.md)
-   [Customer play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-success-play.md)
-   [Customer service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-knowledge-graph.md)
-   [Engagement summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-engagement.md)
-   [Internal play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-plays.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-generate-knowledge-article.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-generate-resolution.md)
-   [Risk signal and issues summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-risk-signals-issues.md)
-   [Service problem case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-case.md)
-   [Success initiative summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-success-init.md)
-   [Test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-test.md)
-   [Touchpoint summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-summarize-touchpoint.md)
-   [Transform mapping assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-tmt-generate-transform-maps.md)

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Requested item summarization for approvals
-   Request summarization for approvals
-   Case summarization for approvals

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-hs-landing.md)

</td><td>

-   Incident summarization
-   H&amp;S Action Planner

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-hrsd.md)

</td><td>

-   Case summarization
-   Chat reply recommendation
-   Chat summarization
-   Email recommendation
-   KB generation
-   Employee information summarization
-   Resolution notes generation
-   Sentiment analysis for HR case
-   Sentiment analysis for HR task
-   Sidebar discussion summarization

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-lsd-landing.md)

</td><td>

-   Conversational intake for Conflict of Interest request
-   Get category of the legal request
-   Legal matter summarization
-   Legal request summarization
-   Triage legal request AI Search
-   Triage legal request capability

</td></tr><tr><td>

Employee

</td><td>

[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-now-assit-landing.md)

</td><td>

-   Contract analysis
-   Contract metadata extraction
-   Contract obligation extraction
-   Contracts query classifier
-   Conversational contract search and insights

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-wsd-landing.md)

</td><td>

-   Reserve Space Virtual Agent topic
-   Workplace Case Summarization

</td></tr><tr><td>

Creator

</td><td>



</td><td>

-   App generation
-   
-   [Catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-catalog-item-using-now-assist.md)
-   App summary generation
-   
-   Code Assist autocomplete
-   Code Assist edit
-   Code assist summarization
-   Code Assist generation
-   Event handler generation
-   
-   
-   
-   
-   
-   Mobile card generation
-   Playbook generation
-   Playbook generation with images
-   Playbook recommendations
-   Playbook summarization
-   [Process inefficiency highlights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/generate-highlights.md)
-   
-   Spoke generation
-   Test generation
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/run-worknotes-analysis.md)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-article-optimization.md)
-   [Complete record generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)
-   [Document summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/generate-document-summary-now-assist.md)
-   [Dynamic Guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dynamic-guidance.md)
-   [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)
-   [GAF skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-gaf.md)
-   [Knowledge content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-platform-knowledge.md)
-   [Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/docintel-exploring-now-assist.md)
-   [Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-global-navigation.md)
-   [New column data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/potential-knowledge-gaps.md)
-   [Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)
-   [ServiceNow Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)
-   [TextToResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md)

</td><td>

[Dashboard summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/use-now-assist-cm.md)

</td></tr><tr><td>

Data and Analytics

</td><td>

[Now Assist skills for Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md)

</td><td>

[AI Data Explorer skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/activate-now-ass-explorer.md)-   [Analytics exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/launch-now-assist-explorer.md)
-   [Exploration summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/summarize-exploration.md)
-   [Refine text in exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/write-text-exploration.md)

[Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-query-generation.md)-   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

Skills installed by default with Platform:

-   [Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-db-dv-now-assist-panel.md)
-   [Data visualization generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/use-dv-generation.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-apo.md)

</td><td>

-   [Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-summarize-apo.md)
-   [Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-fsc-summarize-po.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-slo.md)

</td><td>

-   [Email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/generate-email-response-for-supplier-tasks.md)
-   [Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/slo-analyze-sentiments.md)
-   [Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-slo-summarize-case.md)
-   [Supplier summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/cust-na-fsc-supplier-skill.md)
-   [Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/summarize-supp-perf.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo.md)

</td><td>

-   [Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)

</td></tr><tr><td>

App Engine

</td><td>



</td><td>

Custom app record summarization

</td></tr><tr><td>

Impact

</td><td>

[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md)The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/jumpstart-now-assist-creator.md)
-   [Jumpstart Your Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/jumpstart-your-now-assist-document-intelligence.md)
-   [Jumpstart Your Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/jumpstart-now-assist-virtual-agent.md)
-   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/jumpstart-now-assist-skill-kit.md)

</td></tr><tr><td>

Vault

</td><td>

[Now Assist for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-landing.md)

</td><td>

-   [Check role access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/check-role-access-now-assist-vault.md)
-   [Generate custom data pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/generate-custom-data-pattern-now-assist-vault.md)
-   [Schedule Data Discovery job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/schedule-data-discovery-job-now-assist-vault.md)

</td></tr><tr><td>

Other

</td><td>



</td><td>

-   ERP data discovery
-   ERP data query

</td></tr></tbody>
</table>
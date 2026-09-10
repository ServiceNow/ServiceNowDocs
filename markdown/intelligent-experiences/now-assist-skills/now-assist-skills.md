---
title: Now Assist skills
description: Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills.html
release: yokohama
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 6
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/next-experience-pickers.md).\)

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

<table id="table_yz3_mqd_dbc"><thead><tr><th class="filter">

Workflow

</th><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

Technology

</td><td>



</td><td>

-   Docs summarization
-   Doc generation
-   Task generation

</td></tr><tr><td>

Technology

</td><td>

[ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-landing-cmdb.md)

</td><td>

-   [Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)
-   [Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-cmdb-mng-dupe-cis-skill.md)
-   [Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-sgc-diagnose.md)

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   ADR DOC summarization and actions
-   Business application insights
-   Register a business application
-   Register a digital integration

</td></tr><tr><td>

Technology

</td><td>

[ServiceNow Otto for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)

</td><td>

[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/extract-data-from-utility-invoices.md)

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Common control objective creation
-   Control objective rationalization and deduplication
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

-   Control objective impact analyzer

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Alert analysis
-   Alert investigation
-   LEAP installer
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>



</td><td>

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
-   Resolution notes generation
-   Sidebar discussion summarization
-   Suggested steps generation

</td></tr><tr><td>

Technology

</td><td>

[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)

</td><td>

[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Common control objective creation
-   Recommendation of similar control objectives
-   Risk assessment summary

</td></tr><tr><td>

Technology

</td><td>

[ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)

</td><td>

-   [Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generating-insights-for-now-assist-for-security.md)
-   [Generate content for shift handover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/add-incidents-shifthandover-ai-agent.md)
-   [Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-pia-report-now-assist-security-incident.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-closure-notes-si-now-assist-sec-incident.md)
-   [Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/na-sir-quality-assessment.md)
-   [Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/generate-recommended-actions-now-assist-for-security.md)
-   [Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/summarize-security-incident-now-assist-sec-incident.md)
-   [Security operations metrics analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-soc-efficiency-usecase.md)

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Error log summarization
-   Error resolution recommendation
-   Publisher compliance summarization
-   Product compliance summarization
-   Recommended actions
-   SaaS user resolution
-   Contract entitlement data extraction

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Create a demand
-   EAP doc summarization
-   Identify similar records
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



</td><td>

TPRM issue summarization

</td></tr><tr><td>

Technology

</td><td>

[ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-landing.md)

</td><td>

-   [Approval recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-approval-recommendation-skill.md)
-   [Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-approval-recommendation-skill.md)
-   [SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-insights-skill.md)
-   [SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-now-assist-api-connector.md)
-   [Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/solutions-now-assist-vulnerability-response.md)
-   [Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/dedupe-host-vi-now-assist-vulnerability-response.md)

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Activity response generation
-   Case summarization
-   Chat recommendation
-   Chat summarization
-   Email recommendation
-   KB generation
-   Resolution notes generation
-   Sentiment analysis case
-   Sentiment analysis dashboard
-   Sidebar summarization
-   Suggested steps generation
-   Trending topics dashboard

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   KB generation
-   Sidebar summarization
-   Work order task summarization

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Case summarization
-   Disputes intake via Virtual Agent

</td></tr><tr><td>

Customer

</td><td>

[ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-management.md)

</td><td>

[Order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-mgmt-summarize-order.md)

</td></tr><tr><td>

Customer

</td><td>

[ServiceNow Otto for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-for-psds.md)

</td><td>

-   [Government case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-psds-summarize-case.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-psds-summarize-chat.md)

</td></tr><tr><td>

Customer

</td><td>

[ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md)

</td><td>

-   [Account onboarding case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-onboard-case.md)
-   [Customer play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-success-play.md)
-   [Customer service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-knowledge-graph.md)
-   [Engagement summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-engagement.md)
-   [Internal play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-plays.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-knowledge-article.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-resolution.md)
-   [Risk signal and issues summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-risk-signals-issues.md)
-   [Service problem case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-case.md)
-   [Success initiative summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-success-init.md)
-   [Test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-test.md)
-   [Touchpoint summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-touchpoint.md)
-   [Transform mapping assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-transform-maps.md)

</td></tr><tr><td>

Employee

</td><td>



</td><td>

Incident summarization

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Case summarization
-   Chat reply recommendation
-   Chat summarization
-   Email recommendation
-   ER case summarization
-   ER interview summarization
-   KB generation
-   Employee information summarization
-   Resolution notes generation
-   Sentiment analysis for HR case
-   Sentiment analysis for HR task
-   Sidebar discussion summarization

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Get category of the legal request
-   Legal matter summarization
-   Legal request summarization
-   Triage legal request AI Search
-   Triage legal request capability

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Contract analysis
-   Contract metadata extraction
-   Contract obligation extraction

</td></tr><tr><td>

Employee

</td><td>



</td><td>

Reserve Space Virtual Agent topic

</td></tr><tr><td>

Creator

</td><td>



</td><td>

-   App generation
-   [Catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/create-catalog-item-using-now-assist.md)
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
-   
-   Spoke generation
-   Test generation
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/run-worknotes-analysis.md)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-article-optimization.md)
-   [Complete record generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/conversational-help-skills.md)
-   [Document summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/generate-document-summary-now-assist.md)
-   [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)
-   [GAF skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/configure-gaf.md)
-   [Identify duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/Now-Assist-identify-and-review-duplicate-articles.md)
-   [Knowledge content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-platform-knowledge.md)
-   [Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-global-navigation.md)
-   [New column data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/potential-knowledge-gaps.md)
-   [ServiceNow Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)
-   [TextToResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)

</td></tr><tr><td>

Data and Analytics

</td><td>

[Now Assist skills for Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/now-assist-in-platform-analytics.md)

</td><td>

[AI Data Explorer skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/activate-now-ass-explorer.md)-   [Analytics exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/launch-now-assist-explorer.md)
-   [Exploration summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/summarize-exploration.md)
-   [Refine text in exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/write-text-exploration.md)

[Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md)-   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

Skills installed by default with Platform:

-   [Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/export-db-dv-now-assist-panel.md)
-   [Data visualization generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/use-dv-generation.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)

</td><td>

-   [Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-summarize-apo.md)
-   [Invoice inquiry solution generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/use-invoice-inquiry-solution-generator-skill.md)
-   [Purchase order line mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/use-purchase-order-line-mapping.md)
-   [Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-fsc-summarize-po.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)

</td><td>

-   [Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo-summarize-case.md)
-   [Supplier summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/cust-na-fsc-supplier-skill.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)

</td><td>

-   [Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)

</td></tr><tr><td>

Impact

</td><td>

[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-landing-page.md)The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-creator.md)
-   [Jumpstart Your Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-virtual-agent.md)
-   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-skill-kit.md)

</td></tr></tbody>
</table>
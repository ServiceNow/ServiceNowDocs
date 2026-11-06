---
title: Generative AI skills
description: ServiceNow AI Platform products contain generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills.html
release: yokohama
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 8
keywords: [Skills, Generative AI, Gen AI]
breadcrumb: [Generative AI skills, Enable AI Experiences]
---

# Generative AI skills

ServiceNow AI Platform products contain generative AI skills that are tailored to meet the needs of users in different workflows.

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/next-experience-pickers.md).\)

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support ServiceNow Otto functionality. Deactivating these skills can negatively affect some features.

## IT and digital operations

<table id="table_technology-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

ServiceNow Otto for Collaborative Work Management \(CWM\)

</td><td>

-   Acceptance criteria generation
-   CWM subtask generation
-   CWM contextual task generation
-   Docs summarization
-   Doc generation
-   Task generation

</td></tr><tr><td>

ServiceNow Otto for Cloud Cost Management \(CCM\)

</td><td>

Cloud cost summarizer

</td></tr><tr><td>

[ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)

</td><td>

-   [ADR DOC summarization and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/summarize-docs-genai-skill-ea.md)
-   [Business application insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/generate-insights-into-ba.md)
-   Review AI-generated business process map diagram
-   Diagram change analysis
-   Refine text
-   [Register a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/register-business-application-using-conversational-experience.md)
-   [Register a digital integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/register-digital-integration-using-conv-exp.md)

</td></tr><tr><td>



</td><td>

-   Generate hardware asset insights

</td></tr><tr><td>

[IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/r_ITOMApplications.md)

</td><td>

[ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-visibility-landing-page.md)

-   [Service mapping candidate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/activate-sm-candidate-skill.md)
-   [Service mapping candidates impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/activate-sm-candidates-impact-skill.md)

 [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-health-landing-page.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-health-landing-page.md)

-   [Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/alert-summarization-now-assist.md)
-   [Alert group analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/alert-group-analysis-el.md)
-   [Alert group description generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/alert-group-descr-generate-el.md)
-   [Past incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/nai-past-incidents.md)
-   [AI-generated incident creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/create-incident-now-assist-el.md)
-   Analyze service observability dashboard
-   Analyze service health
-   Error analysis

</td></tr><tr><td>

[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/r_ITServiceManagement.md)

</td><td>

-   [Change request risk explanation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/change-risk-exp-now-assist.md)
-   [Change request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/summarize-change-now-assist.md)
-   [Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-chat-recommendation.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/generate-chat-summary-interaction-now-assist-itsm.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-email-recommendation.md)
-   Generate change risk assessments answers and reasoning
-   [Incident activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-activities-response-generation.md)
-   [Incident assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-incident-assist.md)
-   [Incident sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/sentiment-analysis-now-assist-itsm.md)
-   [Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/summarize-incident-now-assist.md)
-   Investigate boot time issues
-   Investigate Zoom call quality issues
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)
-   [Major incident management email content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-mim-email-recommendation.md)
-   [Release notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-dpr-generate-release-notes.md)
-   Request activity response generation
-   Requested item activity response generation
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/resolve-incident-now-assist.md)
-   [Sidebar discussion summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-sidebar-discussion.md)
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/resolution-steps-generation-now-assist-itsm.md)

</td></tr><tr><td>

[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)

</td><td>

[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)

</td></tr><tr><td>



</td><td>

-   OT incident summarization
-   OT resolution notes generation

</td></tr><tr><td>



</td><td>

-   Extract entitlements from contract
-   Error log summarization
-   Error resolution recommendation
-   Publisher compliance summarization
-   Product compliance summarization
-   Recommended actions
-   SaaS user resolution
-   Contract entitlement data extraction
-   Product match reviewer
-   Software normalization
-   Spend transaction software classification
-   Spend transaction software normalization

</td></tr><tr><td>



</td><td>

-   Acceptance criteria generation
-   Create a demand
-   EAP doc summarization
-   Epic status assessment
-   Goal insights
-   Identify similar records
-   Multi feedback summarization
-   Planning item doc summarization
-   Portfolio insights
-   Project doc summarization
-   Project insights generation
-   Project plan generation
-   Refine records
-   Risk generation
-   Story generation
-   Target generation
-   Write planning item

</td></tr></tbody>
</table>## Security and Risk

<table id="table_vault-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

[ServiceNow Otto for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)

</td><td>

[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/extract-data-from-utility-invoices.md)

</td></tr><tr><td>



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

Risk event summarization in the classic UI


</td></tr><tr><td>



</td><td>

-   Control objective impact analyzer
-   Common control objective creation
-   Recommendation of similar control objectives
-   Risk assessment summary
-   GRC case summarization

</td></tr><tr><td>

GRC: Compliance Case Management

</td><td>

GRC case summarization

</td></tr><tr><td>

[GRC: Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md)

</td><td>

TPRM issue summarization

</td></tr><tr><td>

ServiceNow Otto for Smart Assessment Engine \(SAE\)

</td><td>

Draft response generation

</td></tr><tr><td>

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

[Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/tisc-landing-page.md)

</td><td>

TISC case summarization

</td></tr><tr><td>

[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/vuln-landing-page.md)

</td><td>

-   [Approval recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-approval-recommendation-skill.md)
-   [Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-approval-recommendation-skill.md)
-   [SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sem-insights-skill.md)
-   [SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-now-assist-api-connector.md)
-   [Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/solutions-now-assist-vulnerability-response.md)
-   [Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/dedupe-host-vi-now-assist-vulnerability-response.md)

</td></tr></tbody>
</table>## Customer experiences \(CRM\)

<table id="table_customer-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)

</td><td>

-   [Activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/generate-a-recommendation-to-respond-to-an-activity.md)
-   Automated quality assurance
-   [Call summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/summarize-a-call-by-using-now-assist-for-customer-service-management-csm.md)
-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm-summarize-case.md)
-   [Chat recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/generate-chat-reply-recommendations.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm-summarize-chat.md)
-   Create case based on service definition recommendations
-   Customer summarization
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/generate-email-reply-recommendations.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/Now-Assist-generate-article-csm-workspace.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm-generate-resolution.md)
-   [Sentiment analysis case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/analyze-sentiments-in-now-assist-for-csm.md)
-   [Sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/use-sentiment-analysis-dashboard.md)
-   Sentiment analysis for email interactions
-   [Sidebar summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/summarize-sidebar-conversations.md)
-   Special handling notes summarization
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)
-   [Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/view-trending-topics-dashboard.md)

</td></tr><tr><td>

Field Service Management

</td><td>

-   KB generation
-   Sidebar summarization
-   Work order task summarization

</td></tr><tr><td>

[Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/fso-overview.md)

</td><td>

-   Case summarization
-   [Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/submit-dispute-case-disputes-intake-via-virtual-agent.md)
-   Customer profile summarization
-   Customer interaction context summary

</td></tr><tr><td>

Sales Customer Relationship Management \(Sales CRM\)

</td><td>

[Order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-mgmt-summarize-order.md)

</td></tr><tr><td>

[Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/bun-public-sector-landing-page.md)

</td><td>

-   [Government case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-psds-summarize-case.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-psds-summarize-chat.md)
-   Document screening
-   Investigative case narrative refinement
-   Investigative case summarization

</td></tr><tr><td>

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md)

</td><td>

-   Account onboarding case summarization
-   Analyze metric trend
-   Customer play summary
-   Engagement summary
-   Internal play summary
-   Renewal insight engine
-   Risk signal and issues summary
-   Success initiative summary
-   Touchpoint summary

</td></tr><tr><td>

[Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/proactive-service-exp-workflows/assurance-workflows.md)

</td><td>

-   Event-context candidate recommender
-   Executive insight generator

</td></tr><tr><td>

[Telecommunications, Media, and Technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/telecom-media-tech-landing.md)

</td><td>

-   Comprehensive summary of linked records
-   [Customer service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-knowledge-graph.md)
-   Deadlock letter draft generation
-   Generate Telecom Customer 360 insights
-   Remote hands request summarization
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-resolution.md)
-   Resolution notes generation for ADR
-   [Service problem case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-case.md)
-   [Test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-test.md)
-   


</td></tr><tr><td>

[Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-exchange/tmt-service-bridge-both-landing-page.md)

</td><td>

Transform mapping assist

</td></tr></tbody>
</table>## Employee experiences

<table id="table_employee-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>



</td><td>

-   Requested item summarization for approvals
-   Request summarization for approvals
-   Case summarization for approvals

</td></tr><tr><td>



</td><td>

Incident summarization

</td></tr><tr><td>



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

Legal Service Delivery

</td><td>

-   Get category of the legal request
-   Legal matter summarization
-   Legal request summarization
-   Triage legal request AI Search
-   Triage legal request capability

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   [Contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/cncore-NA-review-land.md)
-   [Contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/cncore-metadata-extract-land.md)
-   Contract obligation extraction
-   Contracts query classifier
-   Conversational contract search and insights

</td></tr><tr><td>



</td><td>

-   Reserve Space Virtual Agent topic
-   Workplace case summarization

</td></tr><tr><td>

[ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)

</td><td>

-   [Email response for invoice case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/generate-email-invoice-case-apo.md)
-   [Email response for invoice task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/generate-email-invoice-task-apo.md)
-   [Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-summarize-apo.md)
-   [Invoice inquiry solution generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/use-invoice-inquiry-solution-generator-skill.md)
-   Knowledge article generation for invoice case
-   [Purchase order line mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/use-purchase-order-line-mapping.md)
-   [Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-fsc-summarize-po.md)
-   [Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/analyze-sentiments-in-invoice-case.md)

</td></tr><tr><td>

[ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)

</td><td>

-   [Email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/generate-email-response-for-supplier-tasks.md)
-   [Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/slo-analyze-sentiments.md)
-   [Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo-summarize-case.md)
-   [Supplier summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/cust-na-fsc-supplier-skill.md)
-   [Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/summarize-supp-perf.md)

</td></tr><tr><td>

[ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)

</td><td>

-   [Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)
-   [Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-summarize-record.md)

</td></tr></tbody>
</table>## AI Platform

<table id="table_platform-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

[Now Assist skills in the Platform workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)

</td><td>

-   [Article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-article-optimization.md)
-   [Catalog item form slot-fill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/catalog-item-form-slot-fill.md)
-   [Complete record generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/conversational-help-skills.md)
-   [Document summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/generate-document-summary-now-assist.md)
-   Dynamic Guidance
-   [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)
-   [GAF skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/configure-gaf.md)
-   [Identify duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/Now-Assist-identify-and-review-duplicate-articles.md)
-   [Knowledge content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-platform-knowledge.md)
-   [Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-global-navigation.md)
-   [New column data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/potential-knowledge-gaps.md)
-   [Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)
-   [ServiceNow Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)
-   [Smart documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configure-skill-smart-documents.md)
-   [Standard ticket page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-in-standard-ticket-page.md)
-   [TextToResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)
-   Voice Assist for Docs

</td></tr><tr><td>

[ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-landing-cmdb.md)

</td><td>

-   Analyze the CMDB search request
-   CI form contextual help
-   [Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)
-   [Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-cmdb-mng-dupe-cis-skill.md)
-   [Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-sgc-diagnose.md)
-   [Summarize CMDB readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-skill-summ-rdy.md)

</td></tr><tr><td>



</td><td>

-   Check role access
-   Generate custom data pattern
-   Schedule Data Discovery job

</td></tr><tr><td>



</td><td>

-   ERP data discovery
-   ERP data query

</td></tr><tr><td>

Now Assist skills for Analytics

</td><td>

AI Data Explorer skills -   Analytics exploration
-   [Exploration summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/summarize-exploration.md)
-   [Refine text in exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/write-text-exploration.md)

 [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/enable-query-generation.md) -   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

 Skills installed by default with Platform:

 -   [Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/export-db-dv-now-assist-panel.md)
-   [Data visualization generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/use-dv-generation.md)

</td></tr><tr><td>

[Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/localization-workspace.md)

</td><td>

Generate Glossary

</td></tr></tbody>
</table>## App development

<table id="table_app-engine-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>



</td><td>

Custom app record summarization

</td></tr><tr><td>

Creator

</td><td>

-   
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
-   
-   Mobile card generation
-   Playbook generation
-   Playbook generation from KB
-   Playbook generation with images
-   Playbook recommendations
-   Playbook summarization
-   Process inefficiency highlights
-   
-   Spoke generation
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/run-worknotes-analysis.md)

</td></tr></tbody>
</table>## Impact

<table id="table_impact-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-landing-page.md) The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-creator.md)
-   
-   [Jumpstart Your Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-virtual-agent.md)
-   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/jumpstart-now-assist-skill-kit.md)

</td></tr></tbody>
</table>
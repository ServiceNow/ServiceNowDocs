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
reading_time_minutes: 7
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/next-experience-pickers.md).\)

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

[Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/now-assist-for-cwm-landing.md)

</td><td>

-   [Docs summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/summarize-doc-now-assist-cwm.md)
-   [Doc generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/generate-summarize-and-refine-content-of-docs-with-now-assist.md)
-   [Task generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/generate-tasks-cwm-docs-now-assist.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)

</td><td>

-   [Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.md)
-   [Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.md)
-   [Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-sgc-diagnose.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/now-assist-ea.md)

</td><td>

-   [ADR DOC summarization and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/summarize-docs-genai-skill-ea.md)
-   [Business application insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/generate-insights-into-ba.md)
-   [Register a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/register-business-application-using-conversational-experience.md)
-   [Register a digital integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/register-digital-integration-using-conv-exp.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/operational-sustainability-management/now-assist-for-esg.md)

</td><td>

[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/operational-sustainability-management/extract-data-from-utility-invoices.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md)

</td><td>

-   [Common control objective creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/take-actions-on-the-recommendations-for-similar-control-objectives.md)
-   [Control objective rationalization and deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/ai-generated-recommendations-for-similar-control-objective.md)
-   [Use Recommendation of similar control objectives skill to generate suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md)
-   [Issue summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/summarize-an-issue.md)
-   [Recommendations for regulatory alert impacted areas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Recommendation of similar control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md)
-   [Regulatory alert summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Risk assessment summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/generate-risk-assessment-summary-genai.md)
-   [Risk event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/generate-risk-event-summary-in-the-risk-workspace.md)
-   [Risk event summarization in the classic UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/generate-a-risk-event-summary.md)

-   [Control objective impact analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/identify-control-objectives-impacted-by-citation-updates.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)

</td><td>

-   [Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-for-it-operations-management/alert-summarization-now-assist.md)
-   [Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-for-it-operations-management/nai-analyze-past-incidents.md)
-   [LEAP installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap.md)
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)

</td><td>

-   [Change request risk explanation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/change-risk-exp-now-assist.md)
-   [Change request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-change-now-assist.md)
-   [Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-chat-recommendation.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/generate-chat-summary-interaction-now-assist-itsm.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-email-recommendation.md)
-   [Incident assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-incident-assist.md)
-   [Incident sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/sentiment-analysis-now-assist-itsm.md)
-   [Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-incident-now-assist.md)
-   Investigate boot time issues
-   Investigate Zoom call quality issues
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/Now-Assist-generate-article-SOW-itsm.md)
-   [Release notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-dpr-generate-release-notes.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/resolve-incident-now-assist.md)
-   [Sidebar discussion summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-sidebar-discussion.md)
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/resolution-steps-generation-now-assist-itsm.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)

</td><td>

[Search for a related record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/now-assist-for-privacy-management.md)

</td><td>

-   [Common control objective creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/privacy-take-actions-on-the-recommendations-for-similar-control-objectives.md)
-   [Recommendation of similar control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/privacy-generate-recommendation-for-a-new-control-objective.md)
-   [Risk assessment summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/privacy-generate-risk-assessment-summary.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)

</td><td>

-   [Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/generating-insights-for-now-assist-for-security.md)
-   [Generate content for shift handover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/add-incidents-shifthandover-ai-agent.md)
-   [Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/generate-pia-report-now-assist-security-incident.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/generate-closure-notes-si-now-assist-sec-incident.md)
-   [Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/na-sir-quality-assessment.md)
-   [Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/generate-recommended-actions-now-assist-for-security.md)
-   [Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/summarize-security-incident-now-assist-sec-incident.md)
-   [Security operations metrics analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-soc-efficiency-usecase.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam.md)

</td><td>

-   [Error log summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/troubleshooting-saas-now-assist-sam.md)
-   [Error resolution recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/troubleshooting-saas-now-assist-sam.md)
-   [Publisher compliance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/summarize-publisher-compliance-now-assist-sam.md)
-   [Product compliance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/summarize-product-compliance-now-assist-sam.md)
-   [Recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/recommended-actions-now-assist-sam.md)
-   [SaaS user resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/automate-userresolution-saas-now-assist-sam.md)
-   [Contract entitlement data extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-for-software-asset-management-sam/extract-entitlements-from-contracts-now-assist-sam.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)

</td><td>

-   [Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/demand-creation-using-now-assist.md)
-   [EAP doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/enterprise-agile-planning/summarize-and-refine-docs-content-in-eap.md)
-   [Identify similar records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/identify-similar-demand-records.md)
-   [Multi feedback summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/feedback-summary-sentiment-topics.md)
-   [Planning item doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/summarize-documents-genai-skill-spw.md)
-   [Project doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/summarize-doc-content-genai-skill-pw.md)
-   [Project insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/email-project-summary-skill-pw.md)
-   [Refine records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/refine-text-with-write-planning-item-skill.md)
-   [Story generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-stories-from-epics-now-assist-eap.md)
-   [Target generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-targets-for-goal.md)
-   [Write planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/refine-text-with-write-planning-item-skill.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/now-assist-tprm.md)

</td><td>

[TPRM issue summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/create-a-summary-of-issue.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/now-assist-for-vulnerability-response-landing.md)

</td><td>

-   [Approval recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-approval-recommendation-skill.md)
-   [Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-approval-recommendation-skill.md)
-   [SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-insights-skill.md)
-   [SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/using-now-assist-api-connector.md)
-   [Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/solutions-now-assist-vulnerability-response.md)
-   [Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-vr/dedupe-host-vi-now-assist-vulnerability-response.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)

</td><td>

-   [Activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/generate-a-recommendation-to-respond-to-an-activity.md)
-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-case.md)
-   [Chat recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-chat.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/generate-email-reply-recommendations.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/Now-Assist-generate-article-csm-workspace.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-generate-resolution.md)
-   [Sentiment analysis case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.md)
-   [Sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/use-sentiment-analysis-dashboard.md)
-   [Sidebar summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/summarize-sidebar-conversations.md)
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)
-   [Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/view-trending-topics-dashboard.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)

</td><td>

-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-for-field-service-management-fsm/na-fsm-generate-kb-article.md)
-   [Sidebar summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-for-field-service-management-fsm/na-fsm-summarize-sidebar-platform.md)
-   [Work order task summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-for-field-service-management-fsm/generate-wot-summ-fsm.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)

</td><td>

-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-case-using-now-assist-fso.md)
-   [Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/submit-dispute-case-disputes-intake-via-virtual-agent.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-management.md)

</td><td>

[Order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-mgmt-summarize-order.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/public-sector-digital-services/now-assist-for-psds.md)

</td><td>

-   [Government case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/public-sector-digital-services/now-assist-psds-summarize-case.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/public-sector-digital-services/now-assist-psds-summarize-chat.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)

</td><td>

-   [Account onboarding case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-onboard-case.md)
-   [Customer play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-success-play.md)
-   [Customer service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-knowledge-graph.md)
-   [Engagement summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-engagement.md)
-   [Internal play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-plays.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-knowledge-article.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-resolution.md)
-   [Risk signal and issues summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-risk-signals-issues.md)
-   [Service problem case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-case.md)
-   [Success initiative summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-success-init.md)
-   [Test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-test.md)
-   [Touchpoint summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-touchpoint.md)
-   [Transform mapping assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-transform-maps.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)

</td><td>

[Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-summarize-safety-incident.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)

</td><td>

-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-summarize-case.md)
-   [Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/chat-recommendations-nahr.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-chat.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/email-recommendation-nahr.md)
-   ER case summarization
-   ER interview summarization
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/gen-kb-now-assisthr.md)
-   [Employee information summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/employee-summary-lh.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-res-note.md)
-   [Sentiment analysis for HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/analyze-sentiments-now-assist.md)
-   [Sentiment analysis for HR task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/tcase-now-assist-hr.md)
-   [Sidebar discussion summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-hrsd/sidebar-discussion-nahr.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)

</td><td>

-   [Get category of the legal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)
-   [Legal matter summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-summarize-case.md)
-   [Legal request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-summarize-case.md)
-   [Triage legal request AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)
-   [Triage legal request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-now-assit-landing.md)

</td><td>

-   [Contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-NA-review-land.md)
-   [Contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-metadata-extract-land.md)
-   [Contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-na-reminder-agentic-wf.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-landing.md)

</td><td>

[Reserve Space Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-for-wsd/wsd-reserve-a-space-now-assist-va.md)

</td></tr><tr><td>

Creator

</td><td>

[Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator/now-assist-for-creator-landing.md)

</td><td>

-   [App generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/sns-app-gen-using-landing.md)
-   [Catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/service-catalog/create-catalog-item-using-now-assist.md)
-   [App summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/summarize-an-app-in-servicenow-studio.md)
-   [Client script summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/building-applications/client-script-summarization-generation.md)
-   [Code Assist autocomplete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/generate-code-with-autocomplete.md)
-   Code Assist edit
-   [Code assist summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/explain-and-summarize-code-with-quick-actions.md)
-   [Code Assist generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/generate-code.md)
-   [Event handler generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/ui-builder/configure-an-event-handler-with-now-assist.md)
-   [Experience generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/building-applications/generate-ui.md)
-   [Flow generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator/flow-generation-landing.md)
-   [Flow generation with images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator/flow-generation-with-images-landing.md)
-   [Flow recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator/flow-recommendations-landing.md)
-   [Flow summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator/flow-summarization-landing.md)
-   Mobile card generation
-   [Playbook generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md)
-   [Playbook generation with images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md)
-   [Playbook recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/playbook-recommendations.md)
-   [Robotic Process Automation \(RPA\) bot generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/rpa-hub/rpa-bot-generation.md)
-   [Spoke generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/create-spk-now-spk-gen.md)
-   [Test generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/test-generation/tg-implement.md)
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/process-mining/run-worknotes-analysis.md)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-article-optimization.md)
-   [Complete record generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/conversational-help-skills.md)
-   [Document summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/ai-platform-capabilities/generate-document-summary-now-assist.md)
-   [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)
-   [GAF skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/configure-gaf.md)
-   [Identify duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-identify-and-review-duplicate-articles.md)
-   [Knowledge content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-platform-knowledge.md)
-   [Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/now-assist-global-navigation.md)
-   [New column data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skills/potential-knowledge-gaps.md)
-   [ServiceNow Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)
-   [TextToResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)

</td></tr><tr><td>

Data and Analytics

</td><td>

[Now Assist skills for Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/now-assist-in-platform-analytics.md)

</td><td>

[AI Data Explorer skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/activate-now-ass-explorer.md)-   [Analytics exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/launch-now-assist-explorer.md)
-   [Exploration summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/summarize-exploration.md)
-   [Refine text in exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/write-text-exploration.md)

[Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/enable-query-generation.md)-   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

Skills installed by default with Platform:

-   [Dashboard and visualization export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/export-db-dv-now-assist-panel.md)
-   [Data visualization generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/use-dv-generation.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-apo.md)

</td><td>

-   [Invoice case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-summarize-apo.md)
-   [Invoice inquiry solution generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/use-invoice-inquiry-solution-generator-skill.md)
-   [Purchase order line mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/use-purchase-order-line-mapping.md)
-   [Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-for-fsc-common/now-assist-fsc-summarize-po.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)

</td><td>

-   [Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-summarize-case.md)
-   [Supplier summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-for-fsc-common/cust-na-fsc-supplier-skill.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)

</td><td>

-   [Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)

</td></tr><tr><td>

Impact

</td><td>

[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-landing-page.md)The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-creator.md)
-   [Jumpstart Your Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-virtual-agent.md)
-   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-skill-kit.md)

</td></tr></tbody>
</table>
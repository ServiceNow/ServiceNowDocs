---
title: Now Assist skills
description: Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 10
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](../../now-assist-admin/concept/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](../../ai-implementation/concept/ai-native-sku-overview.md).

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

[Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/now-assist-for-cwm-landing.md)

</td><td>

-   [Acceptance criteria generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/generate-acceptance-criteria-for-stories-in-cwm.md)
-   [Docs summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/summarize-doc-now-assist-cwm.md)
-   [Doc generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/generate-summarize-and-refine-content-of-docs-with-now-assist.md)
-   [Task generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/generate-tasks-cwm-docs-now-assist.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)

</td><td>

-   [Configuration item \(CI\) summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.md)
-   [Manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.md)
-   [Service Graph Connector diagnosis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-sgc-diagnose.md)

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

-   [ADR DOC summarization and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/summarize-docs-genai-skill-ea.md)
-   [Business application insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md)
-   [Diagram change analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/compare-modeling-diagrams.md)
-   [Refine text](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/elaborate-or-shorten-content-form-fields.md)
-   [Register a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/register-business-application-using-conversational-experience.md)
-   [Register a digital integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/register-digital-integration-using-conv-exp.md)

</td></tr><tr><td>

Technology

</td><td>

[Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md)

</td><td>

[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/extract-data-from-utility-invoices.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-hardware-asset-management/now-assist-ham.md)

</td><td>

-   [Generate hardware asset insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-hardware-asset-management/generate-asset-analysis-now-assist-ham.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md)

</td><td>

-   [Common control objective creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/take-actions-on-the-recommendations-for-similar-control-objectives.md)
-   [Control objective impact analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/identify-control-objectives-impacted-by-citation-updates.md)
-   [Generate recommendation for similar control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md)
-   [Issue summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/summarize-an-issue.md)
-   [Recommendations for regulatory alert impacted areas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Recommendation of similar control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md)
-   [Regulatory alert summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Regulatory alert impacted policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md)
-   [Risk assessment summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-risk-assessment-summary-genai.md)
-   [Risk event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-risk-event-summary-in-the-risk-workspace.md)
-   [Risk event summarization in the classic UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-a-risk-event-summary.md)


</td></tr><tr><td>

Technology

</td><td>

[Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)

</td><td>

-   [Alert analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/alert-summarization-now-assist.md)
-   [Alert investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/nai-analyze-past-incidents.md)
-   [Analyze service health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/analyze-service-health-in-service-observability.md)
-   [Analyze service observability dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/analyze-a-dashboard-in-service-observability.md)
-   [LEAP installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap.md)
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)

</td><td>

-   [Catalog task summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-request-summarization-skill.md)
-   [Change request risk explanation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/change-risk-exp-now-assist.md)
-   [Change request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-change-now-assist.md)
-   [Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-chat-recommendation.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/generate-chat-summary-interaction-now-assist-itsm.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-email-recommendation.md)
-   [Incident assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-incident-assist.md)
-   [Incident sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/sentiment-analysis-now-assist-itsm.md)
-   [Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/summarize-incident-now-assist.md)
-   [Investigate boot time issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/investigate-and-resolve-boot-time-issues.md)
-   [Investigate Zoom call quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/investigate-and-resolve-zoom-call-issues.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/Now-Assist-generate-article-SOW-itsm.md)
-   [Release notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-dpr-generate-release-notes.md)
-   [Request activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-request-summarization-skill.md)
-   [Request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-request-summarization-skill.md)
-   [Requested item activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-request-summarization-skill.md)
-   [Requested item summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-request-summarization-skill.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/resolve-incident-now-assist.md)
-   [Sidebar discussion summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-sidebar-discussion.md)
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/resolution-steps-generation-now-assist-itsm.md)

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

[Now Assist for Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/now-assist-for-privacy-management.md)

</td><td>

-   [Control objective impact analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/identify-control-objectives-impacted-by-citation-updates.md)
-   [Common control objective creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/privacy-take-actions-on-the-recommendations-for-similar-control-objectives.md)
-   [Recommendation of similar control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/privacy-generate-recommendation-for-a-new-control-objective.md)
-   [Risk assessment summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/privacy-generate-risk-assessment-summary.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)

</td><td>

-   [Correlation insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/generating-insights-for-now-assist-for-security.md)
-   [Generate content for shift handover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/add-incidents-shifthandover-ai-agent.md)
-   [Post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/generate-pia-report-now-assist-security-incident.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/generate-closure-notes-si-now-assist-sec-incident.md)
-   [Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/na-sir-quality-assessment.md)
-   [Security incident recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/generate-recommended-actions-now-assist-for-security.md)
-   [Security incident resolution plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/config-resolution-plan-skill.md)
-   [Security incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/summarize-security-incident-now-assist-sec-incident.md)
-   [Security operations metrics analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-soc-efficiency-usecase.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam.md)

</td><td>

-   [Error log summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/troubleshooting-saas-now-assist-sam.md)
-   [Error resolution recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/troubleshooting-saas-now-assist-sam.md)
-   [Publisher compliance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/summarize-publisher-compliance-now-assist-sam.md)
-   [Product compliance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/summarize-product-compliance-now-assist-sam.md)
-   [Recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/recommended-actions-now-assist-sam.md)
-   [SaaS user resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/automate-userresolution-saas-now-assist-sam.md)
-   [Contract entitlement data extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/extract-entitlements-from-contracts-now-assist-sam.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)

</td><td>

-   [Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/demand-creation-using-now-assist.md)
-   [EAP doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/summarize-and-refine-docs-content-in-eap.md)
-   [Identify similar records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/identify-similar-demand-records.md)
-   [Demand summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/demand-summarization-skill.md)
-   [Goal insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-insights-for-goal.md)
-   [Multi feedback summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/feedback-summary-sentiment-topics.md)
-   [Planning item doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/summarize-documents-genai-skill-spw.md)
-   [Project doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/summarize-doc-content-genai-skill-pw.md)
-   [Project insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/email-project-summary-skill-pw.md)
-   [Refine records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/refine-text-with-write-planning-item-skill.md)
-   [Story generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/generate-stories-from-epics-now-assist-eap.md)
-   [Target generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-targets-for-goal.md)
-   [Write planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/refine-text-with-write-planning-item-skill.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/now-assist-tprm.md)

</td><td>

-   [TPRM issue summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-a-summary-of-issue.md)
-   [TPRM issue management recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-recommendation-tprm-issue.md)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/now-assist-for-vulnerability-response-landing.md)

</td><td>

-   [Approval recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-approval-recommendation-skill.md)
-   [Now Assist recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-approval-recommendation-skill.md)
-   [SEM insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/sem-insights-skill.md)
-   [SPC setup connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/using-now-assist-api-connector.md)
-   [Suggest vulnerability solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/solutions-now-assist-vulnerability-response.md)
-   [Vulnerable item deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/dedupe-host-vi-now-assist-vulnerability-response.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)

</td><td>

-   [Activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/generate-a-recommendation-to-respond-to-an-activity.md)
-   [Automated quality assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/quality-assurance-management.md)
-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-case.md)
-   [Chat recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-chat.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/generate-email-reply-recommendations.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/Now-Assist-generate-article-csm-workspace.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-generate-resolution.md)
-   [Sentiment analysis case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.md)
-   [Sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/use-sentiment-analysis-dashboard.md)
-   [Sidebar summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/summarize-sidebar-conversations.md)
-   [Suggested steps generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)
-   [Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/view-trending-topics-dashboard.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)

</td><td>

-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/na-fsm-generate-kb-article.md)
-   [Sidebar summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/na-fsm-summarize-sidebar-platform.md)
-   [Work order task summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/generate-wot-summ-fsm.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)

</td><td>

-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-case-using-now-assist-fso.md)
-   [Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/submit-dispute-case-disputes-intake-via-virtual-agent.md)
-   [Customer profile summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-customer-profile-fso.md)
-   [Customer interaction context summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-customer-context-fso.md)

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

-   [Government case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-psds-summarize-case.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-psds-summarize-chat.md)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)

</td><td>

-   [Account onboarding case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-onboard-case.md)
-   [Customer play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-success-play.md)
-   [Customer service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-knowledge-graph.md)
-   [Engagement summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-engagement.md)
-   [Internal play summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-plays.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-knowledge-article.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-resolution.md)
-   [Risk signal and issues summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-risk-signals-issues.md)
-   [Service problem case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-case.md)
-   [Success initiative summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-success-init.md)
-   [Test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-test.md)
-   [Touchpoint summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-touchpoint.md)
-   [Transform mapping assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-transform-maps.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/now-assisit-employee-exp.md)

</td><td>

-   [Requested item summarization for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/explore-now-assist-for-emp-exp.md)
-   [Request summarization for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/explore-now-assist-for-emp-exp.md)
-   [Case summarization for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/explore-now-assist-for-emp-exp.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)

</td><td>

[Incident summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-summarize-safety-incident.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)

</td><td>

-   [Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-summarize-case.md)
-   [Chat reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/chat-recommendations-nahr.md)
-   [Chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-chat.md)
-   [Email recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/email-recommendation-nahr.md)
-   [KB generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/gen-kb-now-assisthr.md)
-   [Employee information summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/employee-summary-lh.md)
-   [Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-res-note.md)
-   [Sentiment analysis for HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/analyze-sentiments-now-assist.md)
-   [Sentiment analysis for HR task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/tcase-now-assist-hr.md)
-   [Sidebar discussion summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/sidebar-discussion-nahr.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)

</td><td>

-   [Conversational intake for Conflict of Interest request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/lsd-config-converse-intake.md)
-   [Get category of the legal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)
-   [Legal matter summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-summarize-case.md)
-   [Legal request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-summarize-case.md)
-   [Triage legal request AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)
-   [Triage legal request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/trans-legal-request-agent.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-now-assit-landing.md)

</td><td>

-   [Contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-NA-review-land.md)
-   [Contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-metadata-extract-land.md)
-   [Contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-reminder-agentic-wf.md)
-   [Contracts query classifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-converse-skill.md)
-   [Conversational contract search and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-converse-skill.md)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-landing.md)

</td><td>

-   [Reserve Space Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/wsd-reserve-a-space-now-assist-va.md)
-   [Workplace Case Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/summarize-workplace-case.md)

</td></tr><tr><td>

Creator

</td><td>

[Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md)

</td><td>

-   [App generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-using-landing.md)
-   [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent.md)
-   [Catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/create-catalog-item-using-now-assist.md)
-   [App summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/summarize-an-app-in-servicenow-studio.md)
-   [Summarize a client script using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/client-script-summarization-generation.md)
-   [Code Assist autocomplete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/generate-code-with-autocomplete.md)
-   [Code Assist edit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/edit-code-now-assist.md)
-   [Code assist summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/explain-and-summarize-code-with-quick-actions.md)
-   [Code Assist generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/generate-scripts-from-text.md)
-   [Event handler generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/configure-an-event-handler-with-now-assist.md)
-   [Create an AI-generated experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-ui.md)
-   [Flow generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/flow-generation-landing.md)
-   [Flow generation with images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/flow-generation-with-images-landing.md)
-   [Flow recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/flow-recommendations-landing.md)
-   [Flow summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/flow-summarization-landing.md)
-   Mobile card generation
-   [Playbook generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-a-playbook-outline.md)
-   [Playbook generation with images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-a-playbook-outline.md)
-   [Playbook recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-playbook-recommendations.md)
-   [Process inefficiency highlights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/generate-highlights.md)
-   [Robotic Process Automation \(RPA\) bot generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md)
-   [Spoke generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-spk-now-spk-gen.md)
-   [Test generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/test-generation/tg-implement.md)
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/run-worknotes-analysis.md)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](../../now-assist-platform/concept/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](now-assist-article-optimization.md)
-   [Complete record generation](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Conversational Help](conversational-help-skills.md)
-   [Document summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/generate-document-summary-now-assist.md)
-   [Dynamic Guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/dynamic-guidance.md)
-   [Extract information from documents](now-assist-extract-information-from-documents.md)
-   [GAF skills](../../now-assist-ai-agents/task/configure-gaf.md)
-   [Knowledge content recommendation](now-assist-platform-knowledge.md)
-   [Multimodal chat](../../document-intelligence/concept/docintel-exploring-now-assist.md)
-   [Navigation](now-assist-global-navigation.md)
-   [New column data generation](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](potential-knowledge-gaps.md)
-   [Requester approval checklist](service-portal-approval-checklist-skill.md)
-   [ServiceNow Lens](../../../product/servicenow-lens/concept/servicenow-lens-landing-page.md)
-   [TextToResult](../../knowledge-graph/concept/knowledge-graph-landing.md)

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



</td><td>

-   Invoice case summarization
-   [Purchase order summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-for-fsc-common/now-assist-fsc-summarize-po.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)

</td><td>

-   [Email response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/generate-email-response-for-supplier-tasks.md)
-   [Sentiment analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slo-analyze-sentiments.md)
-   [Supplier case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-summarize-case.md)
-   [Supplier summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-for-fsc-common/cust-na-fsc-supplier-skill.md)
-   [Supplier performance summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/summarize-supp-perf.md)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)

</td><td>

-   [Negotiation summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Procurement case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Purchase requisition summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Sourcing event summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)
-   [Sourcing request summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-summarize-record.md)

</td></tr><tr><td>

App Engine

</td><td>

[Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)

</td><td>

[Custom app record summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/custom-app-record-summarization-na-for-app-engine.md)

</td></tr><tr><td>

Impact

</td><td>

[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md)The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-creator.md)
-   [Jumpstart Your Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/accelerator-and-initiative-list/jumpstart-your-now-assist-document-intelligence.md)
-   [Jumpstart Your Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-virtual-agent.md)
-   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-skill-kit.md)

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

[Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)

</td><td>

-   [ERP data discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-erp-data-discovery-skill.md)
-   [ERP data query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-erp-data-query.md)

</td></tr></tbody>
</table>
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

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](../../now-assist-admin/concept/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

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

[Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=australia&pubname=australia-it-business-management&ft:locale=en-US)

</td><td>

-   [Acceptance criteria generation](https://www.servicenow.com/docs/access?context=generate-acceptance-criteria-for-stories-in-cwm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Docs summarization](https://www.servicenow.com/docs/access?context=summarize-doc-now-assist-cwm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Doc generation](https://www.servicenow.com/docs/access?context=generate-summarize-and-refine-content-of-docs-with-now-assist&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Task generation](https://www.servicenow.com/docs/access?context=generate-tasks-cwm-docs-now-assist&version=australia&pubname=australia-it-business-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td><td>

-   [Configuration item \(CI\) summarization](https://www.servicenow.com/docs/access?context=na-cmdb-agent-ci-summarizer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Manage duplicate CIs](https://www.servicenow.com/docs/access?context=now-assist-cmdb-mng-dupe-cis-skill&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Service Graph Connector diagnosis](https://www.servicenow.com/docs/access?context=now-assist-sgc-diagnose&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Core Business Suite \(CBS\)](https://www.servicenow.com/docs/access?context=now-assist-cbs&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)

</td><td>

-   [Next Best Action](https://www.servicenow.com/docs/access?context=now-assist-cbs&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)
-   [Error Resolution](https://www.servicenow.com/docs/access?context=now-assist-cbs&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)

</td><td>

-   [ADR DOC summarization and actions](https://www.servicenow.com/docs/access?context=summarize-docs-genai-skill-ea&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
-   [Business application insights](https://www.servicenow.com/docs/access?context=generate-insights-into-ba&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
-   [Diagram change analysis](https://www.servicenow.com/docs/access?context=compare-modeling-diagrams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
-   [Refine text](https://www.servicenow.com/docs/access?context=elaborate-or-shorten-content-form-fields&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
-   [Register a business application](https://www.servicenow.com/docs/access?context=register-business-application-using-conversational-experience&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
-   [Register a digital integration](https://www.servicenow.com/docs/access?context=register-digital-integration-using-conv-exp&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)

</td><td>

[Extract data from utility invoices](https://www.servicenow.com/docs/access?context=extract-data-from-utility-invoices&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)

</td><td>

-   [Generate hardware asset insights](https://www.servicenow.com/docs/access?context=generate-asset-analysis-now-assist-ham&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

</td><td>

-   [Common control objective creation](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Control objective impact analyzer](https://www.servicenow.com/docs/access?context=identify-control-objectives-impacted-by-citation-updates&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Generate recommendation for similar control objective](https://www.servicenow.com/docs/access?context=generate-recommendation-for-a-new-control-objective&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Issue summarization](https://www.servicenow.com/docs/access?context=summarize-an-issue&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Recommendations for regulatory alert impacted areas](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Recommendation of similar control objectives](https://www.servicenow.com/docs/access?context=generate-recommendation-for-a-new-control-objective&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Regulatory alert summarization](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Regulatory alert impacted citations](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Regulatory alert impacted control objectives](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Regulatory alert impacted controls](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Regulatory alert impacted policies](https://www.servicenow.com/docs/access?context=create-recommendation-reg-alert&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Risk assessment summarization](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Risk event summarization](https://www.servicenow.com/docs/access?context=generate-risk-event-summary-in-the-risk-workspace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Risk event summarization in the classic UI](https://www.servicenow.com/docs/access?context=generate-a-risk-event-summary&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)


</td></tr><tr><td>

Technology

</td><td>

[Now Assist for ITOM](https://www.servicenow.com/docs/access?context=now-assist-itom&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

</td><td>

-   [Alert analysis](https://www.servicenow.com/docs/access?context=alert-summarization-now-assist&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Alert investigation](https://www.servicenow.com/docs/access?context=nai-analyze-past-incidents&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Analyze service health](https://www.servicenow.com/docs/access?context=analyze-service-health-in-service-observability&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Analyze service observability dashboard](https://www.servicenow.com/docs/access?context=analyze-a-dashboard-in-service-observability&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [LEAP installer](https://www.servicenow.com/docs/access?context=aiops-leap&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

</td><td>

-   [Catalog task summarization](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Change request risk explanation](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Change request summarization](https://www.servicenow.com/docs/access?context=summarize-change-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Chat reply recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-chat-recommendation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Chat summarization](https://www.servicenow.com/docs/access?context=generate-chat-summary-interaction-now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Email recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Incident assist](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Incident sentiment analysis](https://www.servicenow.com/docs/access?context=sentiment-analysis-now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Incident summarization](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Investigate boot time issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Investigate Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [KB generation](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Release notes generation](https://www.servicenow.com/docs/access?context=now-assist-itsm-dpr-generate-release-notes&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Request activity response generation](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Request summarization](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Requested item activity response generation](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Requested item summarization](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Resolution notes generation](https://www.servicenow.com/docs/access?context=resolve-incident-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Sidebar discussion summarization](https://www.servicenow.com/docs/access?context=now-assist-itsm-sidebar-discussion&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
-   [Suggested steps generation](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Operational Technology \(OT\) Manager Foundation](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=australia&pubname=australia-operational-technology&ft:locale=en-US)

</td><td>

[Search for a related record](https://www.servicenow.com/docs/access?context=search-related-records-ot-cmdb-tables-now-assist-otm&version=australia&pubname=australia-operational-technology&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&version=australia&pubname=australia-operational-technology&ft:locale=en-US)

</td><td>

-   [OT incident summarization](https://www.servicenow.com/docs/access?context=summarize-ot-incident-now-assist&version=australia&pubname=australia-operational-technology&ft:locale=en-US)
-   [OT resolution notes generation](https://www.servicenow.com/docs/access?context=generate-resolution-notes-ot-incident&version=australia&pubname=australia-operational-technology&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Privacy Management](https://www.servicenow.com/docs/access?context=now-assist-for-privacy-management&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

</td><td>

-   [Control objective impact analyzer](https://www.servicenow.com/docs/access?context=identify-control-objectives-impacted-by-citation-updates&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Common control objective creation](https://www.servicenow.com/docs/access?context=privacy-take-actions-on-the-recommendations-for-similar-control-objectives&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Recommendation of similar control objectives](https://www.servicenow.com/docs/access?context=privacy-generate-recommendation-for-a-new-control-objective&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Risk assessment summary](https://www.servicenow.com/docs/access?context=privacy-generate-risk-assessment-summary&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=australia&pubname=australia-security-management&ft:locale=en-US)

</td><td>

-   [Correlation insights generation](https://www.servicenow.com/docs/access?context=generating-insights-for-now-assist-for-security&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Generate content for shift handover](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Post-incident analysis](https://www.servicenow.com/docs/access?context=generate-pia-report-now-assist-security-incident&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Resolution notes generation](https://www.servicenow.com/docs/access?context=generate-closure-notes-si-now-assist-sec-incident&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Security incident quality assessment](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Security incident recommended actions](https://www.servicenow.com/docs/access?context=generate-recommended-actions-now-assist-for-security&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Security incident resolution plan](https://www.servicenow.com/docs/access?context=config-resolution-plan-skill&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Security incident summarization](https://www.servicenow.com/docs/access?context=summarize-security-incident-now-assist-sec-incident&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Security operations metrics analysis](https://www.servicenow.com/docs/access?context=now-assist-sir-soc-efficiency-usecase&version=australia&pubname=australia-security-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)

</td><td>

-   [Error log summarization](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Error resolution recommendation](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Publisher compliance summarization](https://www.servicenow.com/docs/access?context=summarize-publisher-compliance-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Product compliance summarization](https://www.servicenow.com/docs/access?context=summarize-product-compliance-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Recommended actions](https://www.servicenow.com/docs/access?context=recommended-actions-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [SaaS user resolution](https://www.servicenow.com/docs/access?context=automate-userresolution-saas-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
-   [Contract entitlement data extraction](https://www.servicenow.com/docs/access?context=extract-entitlements-from-contracts-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)

</td><td>

-   [Create a demand](https://www.servicenow.com/docs/access?context=demand-creation-using-now-assist&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [EAP doc summarization](https://www.servicenow.com/docs/access?context=summarize-and-refine-docs-content-in-eap&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Identify similar records](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Demand summarization](https://www.servicenow.com/docs/access?context=demand-summarization-skill&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Goal insights](https://www.servicenow.com/docs/access?context=generate-insights-for-goal&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Multi feedback summarization](https://www.servicenow.com/docs/access?context=feedback-summary-sentiment-topics&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Planning item doc summarization](https://www.servicenow.com/docs/access?context=summarize-documents-genai-skill-spw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Project doc summarization](https://www.servicenow.com/docs/access?context=summarize-doc-content-genai-skill-pw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Project insights generation](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Refine records](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Story generation](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Target generation](https://www.servicenow.com/docs/access?context=generate-targets-for-goal&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Write planning item](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=australia&pubname=australia-it-business-management&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

</td><td>

-   [TPRM issue summarization](https://www.servicenow.com/docs/access?context=create-a-summary-of-issue&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [TPRM issue management recommendation](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

</td></tr><tr><td>

Technology

</td><td>

[Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=australia&pubname=australia-security-management&ft:locale=en-US)

</td><td>

-   [Approval recommendation](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Now Assist recommendation](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [SEM insights](https://www.servicenow.com/docs/access?context=sem-insights-skill&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [SPC setup connector](https://www.servicenow.com/docs/access?context=using-now-assist-api-connector&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Suggest vulnerability solutions](https://www.servicenow.com/docs/access?context=solutions-now-assist-vulnerability-response&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Vulnerable item deduplication](https://www.servicenow.com/docs/access?context=dedupe-host-vi-now-assist-vulnerability-response&version=australia&pubname=australia-security-management&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td><td>

-   [Activity response generation](https://www.servicenow.com/docs/access?context=generate-a-recommendation-to-respond-to-an-activity&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Automated quality assurance](https://www.servicenow.com/docs/access?context=quality-assurance-management&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Case summarization](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-case&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Chat recommendation](https://www.servicenow.com/docs/access?context=generate-chat-reply-recommendations&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-chat&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Email recommendation](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [KB generation](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-csm-generate-resolution&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Sentiment analysis case](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Sentiment analysis dashboard](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Sidebar summarization](https://www.servicenow.com/docs/access?context=summarize-sidebar-conversations&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Suggested steps generation](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Trending topics dashboard](https://www.servicenow.com/docs/access?context=view-trending-topics-dashboard&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

</td><td>

-   [KB generation](https://www.servicenow.com/docs/access?context=na-fsm-generate-kb-article&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
-   [Sidebar summarization](https://www.servicenow.com/docs/access?context=na-fsm-summarize-sidebar-platform&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
-   [Work order task summarization](https://www.servicenow.com/docs/access?context=generate-wot-summ-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)

</td><td>

-   [Case summarization](https://www.servicenow.com/docs/access?context=summarize-case-using-now-assist-fso&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)
-   [Disputes intake via Virtual Agent](https://www.servicenow.com/docs/access?context=submit-dispute-case-disputes-intake-via-virtual-agent&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)
-   [Customer profile summarization](https://www.servicenow.com/docs/access?context=summarize-customer-profile-fso&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)
-   [Customer interaction context summary](https://www.servicenow.com/docs/access?context=summarize-customer-context-fso&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=now-assist-for-MCO&version=australia&pubname=australia-manufacturing&ft:locale=en-US)

</td><td>

[Enhance non conformance description](https://www.servicenow.com/docs/access?context=mco-report-an-issue_AI&version=australia&pubname=australia-manufacturing&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=australia&pubname=australia-order-management&ft:locale=en-US)

</td><td>

[Order summarization](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=australia&pubname=australia-order-management&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=australia&pubname=australia-government-industry&ft:locale=en-US)

</td><td>

-   [Government case summarization](https://www.servicenow.com/docs/access?context=now-assist-psds-summarize-case&version=australia&pubname=australia-government-industry&ft:locale=en-US)
-   [Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-psds-summarize-chat&version=australia&pubname=australia-government-industry&ft:locale=en-US)

</td></tr><tr><td>

Customer

</td><td>

[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)

</td><td>

-   [Account onboarding case summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-onboard-case&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Customer play summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-success-play&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Customer service summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-knowledge-graph&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Engagement summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-engagement&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Internal play summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-plays&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [KB generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-knowledge-article&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-resolution&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Risk signal and issues summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-risk-signals-issues&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Service problem case summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-case&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Success initiative summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-success-init&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Test summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-test&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Touchpoint summary](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-touchpoint&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
-   [Transform mapping assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-transform-maps&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

-   [Requested item summarization for approvals](https://www.servicenow.com/docs/access?context=explore-now-assist-for-emp-exp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Request summarization for approvals](https://www.servicenow.com/docs/access?context=explore-now-assist-for-emp-exp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Case summarization for approvals](https://www.servicenow.com/docs/access?context=explore-now-assist-for-emp-exp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

[Incident summarization](https://www.servicenow.com/docs/access?context=now-assist-hs-summarize-safety-incident&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

-   [Case summarization](https://www.servicenow.com/docs/access?context=now-assist-hrsd-summarize-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Chat reply recommendation](https://www.servicenow.com/docs/access?context=chat-recommendations-nahr&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-hrsd-chat&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Email recommendation](https://www.servicenow.com/docs/access?context=email-recommendation-nahr&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [KB generation](https://www.servicenow.com/docs/access?context=gen-kb-now-assisthr&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Employee information summarization](https://www.servicenow.com/docs/access?context=employee-summary-lh&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-hrsd-res-note&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Sentiment analysis for HR case](https://www.servicenow.com/docs/access?context=analyze-sentiments-now-assist&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Sentiment analysis for HR task](https://www.servicenow.com/docs/access?context=tcase-now-assist-hr&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Sidebar discussion summarization](https://www.servicenow.com/docs/access?context=sidebar-discussion-nahr&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

-   [Conversational intake for Conflict of Interest request](https://www.servicenow.com/docs/access?context=lsd-config-converse-intake&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Get category of the legal request](https://www.servicenow.com/docs/access?context=trans-legal-request-agent&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Legal matter summarization](https://www.servicenow.com/docs/access?context=now-assist-lsd-summarize-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Legal request summarization](https://www.servicenow.com/docs/access?context=now-assist-lsd-summarize-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Triage legal request AI Search](https://www.servicenow.com/docs/access?context=trans-legal-request-agent&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Triage legal request capability](https://www.servicenow.com/docs/access?context=trans-legal-request-agent&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

-   [Contract analysis](https://www.servicenow.com/docs/access?context=cncore-NA-review-land&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Contract metadata extraction](https://www.servicenow.com/docs/access?context=cncore-metadata-extract-land&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Contract obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Contracts query classifier](https://www.servicenow.com/docs/access?context=cncore-conf-converse-skill&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Conversational contract search and insights](https://www.servicenow.com/docs/access?context=cncore-conf-converse-skill&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Employee

</td><td>

[Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td><td>

-   [Reserve Space Virtual Agent topic](https://www.servicenow.com/docs/access?context=wsd-reserve-a-space-now-assist-va&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
-   [Workplace Case Summarization](https://www.servicenow.com/docs/access?context=summarize-workplace-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

</td></tr><tr><td>

Creator

</td><td>

[Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

-   [App generation](https://www.servicenow.com/docs/access?context=sns-app-gen-using-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Build Agent](https://www.servicenow.com/docs/access?context=build-agent&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Catalog item generation](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [App summary generation](https://www.servicenow.com/docs/access?context=summarize-an-app-in-servicenow-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Summarize a client script using Now Assist](https://www.servicenow.com/docs/access?context=client-script-summarization-generation&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Code Assist autocomplete](https://www.servicenow.com/docs/access?context=generate-code-with-autocomplete&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [Code Assist edit](https://www.servicenow.com/docs/access?context=edit-code-now-assist&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [Code assist summarization](https://www.servicenow.com/docs/access?context=explain-and-summarize-code-with-quick-actions&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [Code Assist generation](https://www.servicenow.com/docs/access?context=generate-scripts-from-text&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [Event handler generation](https://www.servicenow.com/docs/access?context=configure-an-event-handler-with-now-assist&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Create an AI-generated experience](https://www.servicenow.com/docs/access?context=generate-ui&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Flow generation](https://www.servicenow.com/docs/access?context=flow-generation-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Flow generation with images](https://www.servicenow.com/docs/access?context=flow-generation-with-images-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Flow recommendations](https://www.servicenow.com/docs/access?context=flow-recommendations-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Flow summarization](https://www.servicenow.com/docs/access?context=flow-summarization-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   Mobile card generation
-   [Playbook generation](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Playbook generation with images](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Playbook recommendations](https://www.servicenow.com/docs/access?context=generate-playbook-recommendations&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Process inefficiency highlights](https://www.servicenow.com/docs/access?context=generate-highlights&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   [Robotic Process Automation \(RPA\) bot generation](https://www.servicenow.com/docs/access?context=rpa-bot-generation&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Spoke generation](https://www.servicenow.com/docs/access?context=create-spk-now-spk-gen&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Test generation](https://www.servicenow.com/docs/access?context=tg-implement&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Work notes analysis](https://www.servicenow.com/docs/access?context=run-worknotes-analysis&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](../../now-assist-platform/concept/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](now-assist-article-optimization.md)
-   [Complete record generation](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Conversational Help](conversational-help-skills.md)
-   [Document summarization](https://www.servicenow.com/docs/access?context=generate-document-summary-now-assist&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Dynamic Guidance](https://www.servicenow.com/docs/access?context=dynamic-guidance&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)
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

[Now Assist skills for Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

</td><td>

[AI Data Explorer skills](https://www.servicenow.com/docs/access?context=activate-now-ass-explorer&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)-   [Analytics exploration](https://www.servicenow.com/docs/access?context=launch-now-assist-explorer&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   [Exploration summarization](https://www.servicenow.com/docs/access?context=summarize-exploration&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   [Refine text in exploration](https://www.servicenow.com/docs/access?context=write-text-exploration&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

[Query Generation skills](https://www.servicenow.com/docs/access?context=enable-query-generation&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)-   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

Skills installed by default with Platform:

-   [Dashboard and visualization export](https://www.servicenow.com/docs/access?context=export-db-dv-now-assist-panel&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   [Data visualization generation](https://www.servicenow.com/docs/access?context=use-dv-generation&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td><td>

-   [Invoice case summarization](https://www.servicenow.com/docs/access?context=now-assist-summarize-apo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Purchase order summarization](https://www.servicenow.com/docs/access?context=now-assist-fsc-summarize-po&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td><td>

-   [Email response](https://www.servicenow.com/docs/access?context=generate-email-response-for-supplier-tasks&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Sentiment analysis](https://www.servicenow.com/docs/access?context=slo-analyze-sentiments&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Supplier case summarization](https://www.servicenow.com/docs/access?context=now-assist-slo-summarize-case&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Supplier summarization](https://www.servicenow.com/docs/access?context=cust-na-fsc-supplier-skill&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Supplier performance summarization](https://www.servicenow.com/docs/access?context=summarize-supp-perf&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td><td>

-   [Negotiation summarization](https://www.servicenow.com/docs/access?context=now-assist-spo-summarize-record&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Procurement case summarization](https://www.servicenow.com/docs/access?context=now-assist-spo-summarize-record&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Purchase requisition summarization](https://www.servicenow.com/docs/access?context=now-assist-spo-summarize-record&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Sourcing event summarization](https://www.servicenow.com/docs/access?context=now-assist-spo-summarize-record&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Sourcing request summarization](https://www.servicenow.com/docs/access?context=now-assist-spo-summarize-record&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

App Engine

</td><td>

[Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

[Custom app record summarization](https://www.servicenow.com/docs/access?context=custom-app-record-summarization-na-for-app-engine&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td></tr><tr><td>

Impact

</td><td>

[Impact](https://www.servicenow.com/docs/access?context=impact-landing-page&version=australia&pubname=australia-impact&ft:locale=en-US)The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   [Jumpstart Your Now Assist for Creator](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-creator&version=australia&pubname=australia-impact&ft:locale=en-US)
-   [Jumpstart Your Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=jumpstart-your-now-assist-document-intelligence&version=australia&pubname=australia-impact&ft:locale=en-US)
-   [Jumpstart Your Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-virtual-agent&version=australia&pubname=australia-impact&ft:locale=en-US)
-   [Jumpstart Your Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=jumpstart-now-assist-skill-kit&version=australia&pubname=australia-impact&ft:locale=en-US)

</td></tr><tr><td>

Vault

</td><td>

[Now Assist for Vault](https://www.servicenow.com/docs/access?context=now-assist-vault-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td><td>

-   [Check role access](https://www.servicenow.com/docs/access?context=check-role-access-now-assist-vault&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Generate custom data pattern](https://www.servicenow.com/docs/access?context=generate-custom-data-pattern-now-assist-vault&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Schedule Data Discovery job](https://www.servicenow.com/docs/access?context=schedule-data-discovery-job-now-assist-vault&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Other

</td><td>

[Now Assist for Zero Copy Connector](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

</td><td>

-   [ERP data discovery](https://www.servicenow.com/docs/access?context=now-assist-erp-data-discovery-skill&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [ERP data query](https://www.servicenow.com/docs/access?context=now-assist-erp-data-query&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

</td></tr></tbody>
</table>
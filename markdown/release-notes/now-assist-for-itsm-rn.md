---
title: ServiceNow Otto for IT Service Management \(ITSM\) release notes
description: The ServiceNow Otto for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. ServiceNow Otto for IT Service Management \(ITSM\) was enhanced and updated in the Brazil release.Updates and enhancements to ServiceNow Otto for IT Service Management \(ITSM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/now-assist-for-itsm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for IT Service Management \(ITSM\) release notes

The ServiceNow Otto for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. ServiceNow Otto for IT Service Management \(ITSM\) was enhanced and updated in the Brazil release.

## About ServiceNow Otto for IT Service Management \(ITSM\)

-   Accelerate incident resolution by using agentic AI workflows that autonomously triage, categorize, investigate, and resolve ITSM incidents, reducing manual effort for service desk agents.
-   Boost agent productivity with generative AI skills that summarize incidents, chat interactions, and change requests, and automatically generate resolution notes and knowledge articles.
-   Extend AI-driven automation across Change Management, Incident Management, and Digital End-User Experience with purpose-built AI agents and agentic workflows.

See [ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-itsm.md) for more information.

## Activation and other requirements

**Important:** ServiceNow Otto for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Brazil Early Availability

Updates and enhancements to ServiceNow Otto for IT Service Management \(ITSM\).

### What's new

-   **[Create change request AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-create-change-ai-agent-auto.md)**

    This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.

-   **[Change CI suggestion AI agent \(latest\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-ci-suggestion-ai-agent-auto.md)**

    This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change request without requiring multiple user interactions.

-   **[Change request plans AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-request-plans-ai-agent-auto.md)**

    This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.

-   **[Change template suggestion AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-template-suggestion-ai-agent-auto.md)**

    This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.


### What's changed

-   **[Generate change risk assessment answers by using ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/generate-change-risk-assessment-answers-now-assist.md)**

    The skill now also reads all dynamic schema store type fields on the change request form. These fields are retrieved automatically, so they don't require an **AI Risk Data Sources** record or an entry in the change request fields property. The skill uses the retrieved values when it suggests answers.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-itsm-aiagents-assess-quality-change-request-workflow.md)**

    The new autonomous mode is introduced, where the AI agent automatically records the quality rating and the explanation as a work note on the change request. The agent also creates a record in the AI Change Quality Scores table. This record stores the change request, the explanation, the per-field score, the rating, and the numerical score. The agent does not update any fields on the change request.


### What's deprecated or removed

-   ****
    -   **[ITSM Virtual Agent NLU topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/using-itsm-va.md)**

        Starting with the Brazil release, ITSM Virtual Agent pre-built topics is being prepared for future deprecation.

    -   **[ITSM Virtual Agent Lite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-virtual-agent-lite.md)**

        ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\) is being prepared for future deprecation.

    -   **[Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

        Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.



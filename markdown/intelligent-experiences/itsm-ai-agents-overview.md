---
title: IT Service Management AI agents
description: The following AI agents are available for IT Service Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-ai-agents-overview.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 6
breadcrumb: [IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# IT Service Management AI agents

The following AI agents are available for IT Service Management.

-   **[Additional incident context AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-additional-incident-context-agent-ai-agent.md)**  
This AI agent retrieves information beyond the incident itself and presents the output in a readable format. This agent is strictly read-only; it can only retrieve and present information. It cannot update, modify, or perform any write operations on any records \(such as adding comments, changing fields, reassigning, resolving, or closing incidents\).
-   **[Agent client collector \(ACC\) diagnostic AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-acc-agent-client-collector-acc-diagnostic-agent-ai-agent.md)**  
This agent assists users in resolving ACC errors by providing suggestions based on the error codes found in the ACC Error Reports. It aims to help users resolve errors efficiently and effectively.
-   **[Categorize ITSM incident AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-categorize-itsm-incident-ai-agent.md)**  
This AI agent assigns the appropriate category and subcategory to an incident.
-   **[Change backout plan AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-backout-plan-ai-agent.md)**  
This AI agent creates a backout plan for a provided change request.
-   **[Change CI suggestion AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-ci-suggestion-ai-agent.md)**  
This AI agent recommends a list of relevant configuration items \(CIs\) that can be added as Affected CIs to the current change request.
-   **[Change conflict assessor AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-conflict-assessor-ai-agent.md)**  
This AI agent can assess conflicts for changes. This includes checking mandatory fields and trigger conflict detection, and updating worknotes.
-   **[Change implementation plan AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-implementation-plan-ai-agent.md)**  
This AI agent generates a step-by-step implementation plan for a given change request. It reviews details of the current request, searches similar historical change requests, and collaborates with the user to create, revise, and finalize an actionable implementation plan. Only the final approved version is updated in the change request.
-   **[Change justification proposal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-justification-proposal-ai-agent.md)**  
This AI agent identifies the justification for a provided change request.
-   **[Change outage assistant AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-outage-assistant-ai-agent.md)**  
This AI agent creates outage records for the change request based on the impacted CIs.
-   **[Change quality assessor AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-quality-assessor-ai-agent.md)**  
This AI agent provides suggestions to improve inputs for a change form.
-   **[Change request plans AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-request-plans-ai-agent.md)**  
This AI agent helps change owners and approvers by drafting high-quality, context-aware change request content.
-   **[Change risk and impact analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-risk-and-impact-analysis-ai-agent.md)**  
This AI agent evaluates the risks and potential impacts associated with a provided change request.
-   **[Change test plan AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-change-test-plan-ai-agent.md)**  
This AI agent identifies the test plan for a provided change request.
-   **[Classify service and CI AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-classify-service-and-ci-ai-agent.md)**  
This AI agent assigns the appropriate service and offering to an incident. It can also assign the appropriate configuration item.
-   **[Create incident AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-create-incident-ai-agent.md)**  
This AI agent manages the end-to-end process of formally logging IT support requests, specifically for user requests like "create an incident," "raise an incident," "open a new incident," "open an IT ticket," or "raise an IT support ticket."
-   **[Create incident AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-create-incident-with-voice-ai-voice-agent.md)**  
This AI agent creates new incidents when the user explicitly mentions they want to create a new incident or report a new issue.
-   **[DEX diagnosis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-dex-dex-diagnosis-ai-agent.md)**  
This AI agent specializes in structured root cause diagnosis of device and application performance issues through a step-by-step process. This agent aggregates device health metrics, event logs and historical incident data, then systematically evaluates each source to isolate relevant evidence.
-   **[DEX remediation trigger AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-dex-dex-remediation-trigger-ai-agent.md)**  
This AI agent receives a resolution plan, checks for remedial actions, and executes the supported ones on end-user devices \(Windows OS and MacOS endpoints\) to resolve common device and application issues. Remedial actions are concrete, executable fix steps such as restarting services, clearing cache, or cleaning up temporary files.
-   **[DEX resolution plan AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-dex-dex-resolution-plan-ai-agent.md)**  
This AI agent generates a resolution plan for the given issue based strictly on the root cause provided. The agent ensures all suggested steps are evidence-based, actionable, and aligned with the diagnosed root cause. No resolution is proposed outside these defined sources.
-   **[Find catalog item AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-find-catalog-item-ai-agent.md)**  
This AI agent identifies relevant catalog items for a given incident and adds all detected catalog item links to the incident's additional comments.
-   **[Finish change plan AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-finish-change-plan-ai-agent.md)**  
This AI agent flushes the cache and informs the user that execution finished successfully.
-   **[Incident category configuration AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-category-configuration-ai-agent.md)**  
This AI agent orchestrates the complete lifecycle of incident category and subcategory configuration for the Choices \[sys\_choice\] table. It supports three interaction modes: guided conversation, file upload \(CSV/XLSX\), and industry-based recommendations.
-   **[Incident context AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-context-ai-agent.md)**  
This AI agent helps users answer questions related to a given incident using information from the incident record and its related records. This agent is strictly read-only — it can only retrieve and present information.
-   **[Incident knowledge article AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-knowledge-article-ai-agent.md)**  
This AI agent can resolve incidents by finding existing similar knowledge articles and attaching them to the incident. It can also create a knowledge article for the incident.
-   **[Incident known error article AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-known-error-article-ai-agent.md)**  
This AI agent can find similar known error articles for an incident and attach them to the incident. It can also resolve the incident.
-   **[Incident resolution details AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-resolution-details-ai-agent.md)**  
This AI agent suggests resolution notes for an incident.
-   **[Incident routing configuration AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-incident-routing-configuration-agent-ai-agent.md)**  
This AI agent creates, modifies, and deactivates assignment rules for incident routing.
-   **[ITSM incident resolution investigation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-itsm-incident-resolution-investigation-ai-agent.md)**  
This AI agent retrieves incident details and can add attached knowledge articles and additional comments.
-   **[ITSM incident resolution plan investigation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-itsm-incident-resolution-plan-investigation-ai-agent.md)**  
This AI agent gets incident details, reviews similar incidents and knowledge articles, and then generates an incident resolution plan.
-   **[Link incident to problem AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-link-incident-to-problem-ai-agent.md)**  
This AI agent links an incident to a problem that was created in the last six months.
-   **[Link major incident AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-link-major-incident-ai-agent.md)**  
This AI agent gathers information from an incident and checks for similar currently active major incidents.
-   **[Link major incident or problem AI Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-link-major-incident-or-problem-ai-agent.md)**  
This AI agent automatically identifies and links the most relevant major incident or problem with an incident.
-   **[Manage ticket AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-manage-ticket-ai-voice-agent.md)**  
This AI voice agent assists users with managing their active incidents and requested items.
-   **[Password reset AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-password-reset-with-voice-ai-voice-agent.md)**  
This AI voice agent helps users reset their password during phone-based interactions.
-   **[Post incident review AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-post-incident-review-ai-agent.md)**  
This AI agent generates a post-incident review report for the user to review and revise after a major incident report.
-   **[Request catalog item AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-request-catalog-item-with-voice-ai-voice-agent.md)**  
This AI voice agent assists users in finding and delivering catalog items. If the item is not categorized as software, then the catalog link is sent through email or SMS. If the item is software, this agent will help create the request.
-   **[Schedule change request AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-schedule-change-request-ai-agent.md)**  
This AI agent schedules a change request.
-   **[Standard change template proposal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-standard-change-template-proposal-ai-agent.md)**  
Provided with a change request, this AI agent searches for similar changes and returns a list of similar changes to use for a proposal record.
-   **[Standard change template recommender AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-standard-change-template-recommender-ai-agent.md)**  
This AI agent helps users create and submit change requests. Invoke it whenever the user asks to log, create, submit, initiate, or help with a change record of any type \(standard, routine, scheduled, maintenance, infrastructure, software, database, security, or any changes specific to IT service management\).
-   **[Submit account unlock catalog AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-submit-account-unlock-catalog-with-voice-ai-voice-agent.md)**  
This AI voice agent helps users unlock accounts by invoking a tool call to submit an account-unlock catalog request.
-   **[Troubleshoot Outlook issue AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-troubleshoot-outlook-issue-with-voice-ai-voice-agent.md)**  
This AI voice agent troubleshoots Microsoft Outlook issues. It also sends a troubleshooting article link to the user by email when requested.

**Parent Topic:**[Available AI agents on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-landing-page.md)


---
title: Now Assist for ITSM release notes
description: Version history for the Now Assist for ITSM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-now-assist.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Now Assist for ITSM release notes

Version history for the Now Assist for ITSM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 15.0.1 - June 2026**
    -   New:
        -   The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
        -   Knowledge feedback tasks are now deduplicated — the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
        -   The Change Quality Agent now persists quality scores per change record — including timestamps and contributing factors — available for dashboards, audits, and risk-detection workflows.
        -   A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
        -   The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
        -   A new manager dashboard aggregates incidents into issue-based clusters with health metrics and drill-down views, giving incident managers a consolidated view of emerging problem areas.
        -   IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
        -   The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
        -   A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.
    -   Changed:
        -   The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
        -   Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
        -   The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
        -   The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.
    -   Fixed:
        -   Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
        -   Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.
    -   Removed: Suggested Steps has been deprecated and removed. Customers should transition to AI-driven recommendations in Now Assist for ITSM.
-   **Version 13.1.1 - May 2026 \(Zurich, Australia\)**

    New: Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.

-   **Version 14.0.4 - May 2026**
    -   New:
        -   Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.
        -   Use the ITSM MCP server to query and retrieve any information within the context of an incident.
    -   Removed: Incident assist skill has been deprecated, moved to the Archive section, and is no longer available for use.
-   **Version 13.0.10 - April 2026**
    -   Changed:
        -   Change Request Risk Explanation - Skill configuration moved to NASK
        -   Change Request Summarization - Skill configuration moved to NASK
        -   Digital Product Release:The Generate Release Notes skill, which generates AI-powered release notes for product and service releases, is active by default.
-   **Version 12.2.7 - March 2026 \(Zurich\)**
    -   New:
        -   Added new 3p model support for existing and new skills, models: gemini-3-flash, gpt-5-mini, claude-4-5-haiku
        -   New ITSM Interactive conversational dashboard for VA and Interactions.
        -   Activity response generation skills for Requests and Requested items in both Core UI and SOW.
        -   Diagnose and resolve Zoom call issues with the new Zoom AI capability, which provides device-level root cause analysis and suggested resolutions.
        -   Monitor device boot time and use Now Assist to quickly diagnose startup delays and get actionable resolutions to resolve boot performance issues.
        -   Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.
    -   Changed: For new users, some skills are active by default.
-   **Version 12.1.1 - January 2026 \(Zurich\)**

    New: IT Service Management AI agent collection \(5.1.2\).

-   **Version 11.3.2 - January 2026 \(Yokohama\)**
    -   New:
        -   Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit
        -   Expanding attachment summarization capabilities to include additional document formats and language
        -   Generating resolution notes using the Now Assist context menu
        -   Generating an activity response using the Now Assist context menu
        -   Masking roles for controlled access to agentic workflows, AI agents, and skills
        -   Empowering service desk agents to diagnose and resolve incidents on DEX monitored devices
    -   Changed - For new users, some skills are active by default. For information, see Now Assist for IT Service Management \(ITSM\) release notes \(Yokohama\).
-   **Version 12.0.6 - December 2025**
    -   See the Now Assist for IT Service Management \(ITSM\) release notes for more information.
    -   New:
        -   Empowering service desk agents to quickly diagnose and resolve issues on Digital End-User Experience \(DEX\) monitored devices using the DEX issue diagnosis and resolution agentic AI workflow that provides root cause analysis, actionable resolution plans, and automated documentation.
        -   Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit
        -   Expanding attachment summarization capabilities to include additional document formats and language
        -   Creating a knowledge article in any incident state
        -   Edit a knowledge article when one article is attached to an incident
        -   Generating resolution notes using the Now Assist context menu
        -   Generating an activity response using the Now Assist context menu
        -   Selecting the desired knowledge base and template for creating knowledge articles using the new knowledge article interceptor page
        -   Masking roles for controlled access to agentic workflows, AI agents, and skills
        -   Empowering service desk agents to quickly diagnose and resolve issues on Digital End-User Experience \(DEX\) monitored devices using the DEX issue diagnosis and resolution agentic AI workflow that provides root cause analysis, actionable resolution plans, and automated documentation.
    -   Changed: For new users, some skills are active by default. For information, see Now Assist for IT Service Management \(ITSM\) release notes.
-   **Version 11.2.0 - October 2025 \(Yokohama, Zurich\)**
    -   Fixed:
        -   Defects
        -   Improved run time for Classify service offering agent
-   **Version 8.2.0 - October 2025 \(Xanadu\)**
    -   Fixed:
        -   Refactor all ITSM Agentic Workflows for platform security
        -   Fix script for Custom roles for agents/workflows
        -   Improved run time for Classify service offering agent
-   **Version 11.1.4 - September 2025**
    -   New:
        -   Use the Assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, identify affected CIs, and view the list of impacted services.
        -   Use the Schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
        -   Use the Explain SLA agentic workflow to understand the breakdown of task assignment and ownership for the SLA relevant to a specific incident, problem, case, or change request. Gain insight into the potential causes of a breach or delays.
        -   Use the Assess quality of a Change Request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
        -   Use the Wrap-up and resolve incident agentic workflow to resolve incidents, create, or attach Knowledge Base \(KB\) articles, update duplicate incident information, and attach Known Error \(KE\) articles to the incident record.
-   **Version 10.0.0 - August 2025**

    New: 3rd Party \(3P\) model support for AI Agents. Supports Gemini, Claude, Azure and Now LLM models.

-   **Version 9.0.3 - June 2025 \(Yokohama\)**

    Fixed: Change risk cosmetic and NowLLM issues.

-   **Version 8.1.0 - June 2025 \(Xanadu\)**
    -   New in the Xanadu Patch 9 release:
        -   Available AI agents use cases Agentic workflow Description Generate post incident reviews
        -   Generate a post incident report of a major incident and inform the fulfiller.
        -   Generate change request plans and schedule Given the change request number, come up with a detailed implementation plan, test plan, backout plan, risk and impact analysis, and justification. and schedule the change.
        -   Triage and categorize ITSM incidents This agentic workflow enables fulfillers to identify the category, subcategory and configuration items for an incident automatically, and link associated major incidents or known problems.
        -   Notify users with Twilio
        -   Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.
        -   Investigate and resolve ITSM incidents
        -   This agentic workflow enables fulfillers to investigate and resolve ITSM incidents. The workflow will check for related catalog items, knowledge articles, and similar resolved incidents to generate resolution steps for the incident. Manage Microsoft 365 group members
        -   Add or remove users and emails from an Microsoft 365 distribution list \(DL\) or email list to ensure the right individuals receive important communications and updates.
-   **Version 9.0.1 - May 2025**
    -   New:
        -   Identify the category, subcategory, and configuration item for a given incident automatically using a team of AI agents in the Triage and categorize ITSM incidents agentic workflow.
        -   Get recommendations to resolve incidents by using a team of AI agents for catalog, knowledge, and past incidents in the Investigate and resolve ITSM incidents agentic workflow.
        -   Manage Microsoft 365 group members using AI agents in the Manage Microsoft 365 group members agentic workflow.
        -   Generate the Risk and impact analysis and the Justification fields using the AI agents in the Generate change request plans agentic workflow.
    -   Changed in this release:
        -   The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.
        -   The following AI agents have been added to the workflow:
            -   Link major incident AI agent
            -   Link incident to problem AI agent
        -   The Incident categorize AI agent has been renamed to Categorize incident AI agent.
        -   The term use case is replaced with the term agentic workflow. For example, the Notify users with Twilio use case is now referred to as the Notify users with Twilio agentic workflow.
        -   The naming of the AI agents has changed. For example, Twilio SMS texter has been renamed to Twilio SMS texter AI agent.
    -   Using Now Assist for ITSM skills:
        -   New:
            -   Suggested steps generation skill to suggest next steps for resolution by analyzing clusters of similar closed and resolved incidents.
            -   Attachment summarization to include contextually relevant data from transcribed JPEG and PNG attachments on all incident summaries.
            -   Sentiment analysis to analyze sentiment of the requester with respect to an incident and understand the sentiment reasoning, trend and score to take informed decision.​
-   **Version 8.0.0 - March 2025**
    -   New in the Yokohama Patch 1 release:
        -   Using ITSM AI Agent Collection
            -   Use ITSM AI Agent Collection to boost productivity, and autonomously resolve business tasks.
        -   Available AI agents use cases
            -   Post-incident reporting
                -   Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.
            -   Change request planning
                -   Enhance IT productivity and help decrease the time to schedule change and manage change risk using AI agents. These AI agents can look up similar changes, generate implementation, back out, and test plans to manage change effectively.
            -   Incident categorizing
                -   Autonomously recommend incident categorization using AI agents. The AI agent assigns a category, subcategory, and a configuration item \(CI\) to incidents based on the incident description. The assigned CI is also based on callers associated with that item.
            -   Twilio texting
                -   Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.
-   **Version 6.1.3 - March 2025**
    -   New in the Xanadu Patch 7 release:
        -   Using ITSM AI Agent Collection
            -   Use ITSM AI Agent Collection to boost productivity, and autonomously resolve business tasks.
        -   Available AI agents use cases
            -   Post-incident reporting
                -   Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.
        -   Change request planning
            -   Enhance IT productivity and help decrease the time to schedule change and manage change risk using AI agents. These AI agents can look up similar changes, generate implementation, back out, and test plans to manage change effectively.
        -   Incident categorizing
            -   Autonomously recommend incident categorization using AI agents. The AI agent assigns a category, subcategory, and a configuration item \(CI\) to incidents based on the incident description. The assigned CI is also based on callers associated with that item.
        -   Twilio texting
            -   Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.
-   **Version 7.0.2 - February 2025**
    -   New:
        -   Email reply recommendations - Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations.
        -   Incident deflection with Now Assist - Reduce the number of incidents to be resolved by deflecting issues with self-service in a ServiceNow portal
        -   Changed
            -   Customize change risk skill - Efficiently explain the risk of a change request by adding custom input fields to the following input tables:
                -   Change request
                -   Past similar change request
                -   Incident caused by change
            -   Refine the explanation to a change risk by shortening or lengthening a response .
            -   Use risk assessment values as an input to explain the risk of a change request.
        -   Improvements to Service Disruptions and Escalate IT Ticket VA topics to provide latest status via LLM generated response
    -   Changed:
        -   Incident and change request summarizations - Updated user interface to be more intuitive. The new interface is available in Service Operations Workspace and in the Core UI.
        -   Knowledge Generation - Display knowledge article templates that can be used to create articles by using a system property. In earlier releases, the templates were displayed by default.
-   **Version 6.0.5 - November 2024**
    -   New:
        -   Change request
            -   Risk rating explanation for a change request
            -   Summarization improvements to include additional details, such as affected CIs and impacted services
        -   Incident
            -   Ask questions about an incident by using the Now Assist panel
            -   On-demand incident resolution notes using Now Assist context menu
            -   Summarization improvements to include additional details, such as SLAs, affected CIs and impacted services, and child incidents
        -   Proactive actionable ITSM Virtual Agent notifications
    -   Changed: Resolution notes generation skill improvements to show root cause and resolution steps taken \(for upgrade customers\)
-   **Version 5.0.8 - November 2024**

    Changed: Remove Min Word count applicability check for record summary Remove Min Word count for Change Summarization.

-   **Version 5.0.4 - August 2024**
    -   New: Knowledge creation from a group of similar incidents Now Assist Virtual Agent integrated with Slack AI Search integrated with Recommended Actions in Service Operations Workspace Change request summarization Task Intelligence for similar incidents in Service Operations Workspace Live agent chat reply recommendations Sidebar chat summarization
    -   Fixed: few translation messages Honored domain separation for Resolution skill
-   **Version 4.0.4 - July 2024**
    -   Fixed:
        -   For instances using domain separation, fixed issue in child domains where the incident created from chat interaction was not populating the short description and description fields.
        -   Resolved the issue where resolution notes skill was not honoring visibility conditions for domain separation.
-   **Version 4.0.3 - June 2024**
    -   Fixed:
        -   Unable to edit/customize Now Assist resolve action in UI16
        -   Creating a New Incident to Resolve fails to create an Incident
        -   Conditional check to use ProblemModalUIHelpers
-   **Version 3.1.5 - June 2024**
    -   Fixed:
        -   Unable to edit/customize Now Assist resolve action in UI16
        -   Creating a New Incident to Resolve fails to create an Incident
        -   Work note field value not saved when incident has minimum word count
        -   Conditional check to use ProblemModalUIHelpers
-   **Version 4.0.1 - May 2024**
    -   New:
        -   Knowledge generation based on resolved incident
        -   LLM-based Virtual Agent topic templates
            -   Service Disruptions
            -   Escalate IT Ticket
            -   Check IT Ticket Status
            -   Open IT Ticket
            -   Reset Password
            -   Change Password
            -   Unlock Account
        -   Chat Summarization
            -   Added support for configuration of input portals for chat summarization
            -   Enabled live agent to live agent summarization
            -   Added chat summarization trigger when using create incident quick action
        -   Incident Summarization configuration - Allow ability to include below additional inputs for summarization
            -   Service Level Agreement
            -   Affected CIs and Impacted Services
            -   Child Incidents
        -   Prompt Management - Provide out-of-the-box prompt headers that can be included when adding additional fields for incident summarization
        -   Skills visibility and access configurations based on condition builder and user roles
    -   Changed:
        -   Priority field added as a default input for incident summarization
        -   Incident summarization can now be triggered on closed state
        -   Exclude previously generated summaries in worknotes/comments during new summarization
-   **Version 3.1.2 - February 2024**
    -   New: Role attribution support to tag worknotes or comments by persona \(agent, user, or system\)
    -   Fixed:
        -   Issues with inconsistent AI icon display on fields generated by Now Assist
        -   Issue of AI-generated short description and description fields not being saved for saved incidents created from chat interactions
-   **Version 3.0.3 - November 2023**
    -   New:
        -   Incident summarization trigger when an incident is saved during reassignments
        -   Chat summarization on incident creation
        -   Knowledge base generation from an incident \(Innovation Lab\)
    -   Fixed:
        -   Resolved minor script errors
        -   Minor adjustments to error messages to be consistent
-   **Version 2.0.2 - September 2023**

    Supercharge your ITSM workflows with Generative AI capabilities for Incident Management.

    -   New
        -   Chat summarization for an interaction
        -   Incident summarization
        -   Resolution notes generation for an incident
        -   Now Assist panel for incident and interaction
    Note: To use Now assist for ITSM capabilities on Service Operations Workspace, upgrade to or download the Service Operations Workspace 3.1.0 version.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


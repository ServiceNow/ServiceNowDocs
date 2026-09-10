---
title: July 16 2026 Now Assist Suite release notes
description: Now Assist Suite version and compatibility information for the July 16 2026 release on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/na-suite-rn-2026-07-16.html
release: store
topic_type: reference
last_updated: "2026-07-16"
reading_time_minutes: 124
breadcrumb: [Now Assist Suite - July 2026 release notes, Now Assist Suite release notes]
---

# July 16 2026 Now Assist Suite release notes

Now Assist Suite version and compatibility information for the July 16 2026 release on the ServiceNow Store.

Note: Now Assist Suite versions are cumulative. For app version updates that have been carried forward from previous releases, refer to the release notes page for the application's "Last updated" date or the ServiceNow Store app listing. See [Now Assist suite versions in the Application Manager](https://www.servicenow.com/docs/r/platform-administration/application-manager/now-assist-suites-app-mgr.html) for more details.

## Suite version 28.11.20260716 - Zurich Patch 11

<table id="table_d5w_ybb_bkc"><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

3.4.8

</td><td>

Includes a fix to 400 bad request error for the canvas APIs.

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.7.4

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.3.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI agents for SLO

</td><td>

2.0.3

</td><td>

New

Added a Reliability Domain Agent that analyzes historical, post-incident data to identify service level objective \(SLO\) and synthetic monitoring gaps across configuration items \(CIs\) and services, then generates reliability tasks to address them.

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.3.1

</td><td>

-   New

None

-   Changed

Workplace Utilization QnA Agent can now be used by users with the sn\_wsd\_spcmgmt.space\_planner role

-   Fixed

The AI Agent was not always able to block the location after submitting an emergency maintenance request

-   Removed

None


</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed

 -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed

Deprecated searching and scraping functionality.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.5.0

</td><td>

Fixed - Streamline ACLs

</td></tr><tr><td>

Common AI Framework

</td><td>

1.0.1

</td><td>

New:

 AI Framework that autonomously discovers schema, samples, and aggregates live ServiceNow tables, and presents a sourced answer without modifying any data.

</td></tr><tr><td>

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Conversation Insights

</td><td>

3.1.0

</td><td>

New: Conversation Insights now supports customers with data sovereignty requirements. The application can be re-enabled for customers using local SKUs, allowing deployment with local conversation insights services.-   Changed: None
-   Fixed: The assignment of the sn\_aci.insights\_read\_write role to the conv-insights-svc-account user has been corrected to ensure proper handling of inheritance flag information.
-   Removed: None

</td></tr><tr><td>

Conversational Studio

</td><td>

10.0.5

</td><td>

Fixed

Errors encountered when migrating over 200 topics from NLU to LLM have been resolved. The migration process now supports chunked processing, resumability, and improved UI feedback. Migration data is decoupled from previous dependencies, batch creation, resume, and cancel actions are now supported.

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

29.2.2

</td><td>

Changed Maintenance release.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

2.0.1

</td><td>

New

 -   Agent renamed to "Vision AI Agent"
-   Requests now routed via the MultiModal Service \(MMS\) to enable more consistent and scalable multimodal processing \(up to 500MB video files\)
-   Improved response quality for Video Workflow use cases
-   Supported video formats: MP4, MOV, WEBM, AVI, MKV, and WMV

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.3.2

</td><td>

Fixed:

 Updated the version for ServiceNow Docs Connector to fix dependency failures

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

3.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

-   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to ensure certification and release standards.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

FSM Scheduling AI Agent Collection

</td><td>

1.0.7

</td><td>

Initial release

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed

AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.4.0

</td><td>

-   New: n/a
-   Changed

Security related enhancements on existing AI Voice agents

-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

List AI Experience

</td><td>

3.0.0

</td><td>

AI Filter Assist allows users to define conditions using natural language in an intuitive, dialog-driven interface. This feature helps reduce the cognitive load of building conditions using the traditional condition builder by allowing users to type or speak a prompt that will then create the query needed to filter, sort, or group data.

 This release we fixed two defects in AI Filter Assister where an ACL had a typo in it's script and "Add to existing filters" mode was selectable even though it should be disabled.

</td></tr><tr><td>

Manage Order Operations

</td><td>

2.0.3

</td><td>

New Changed

 -   Order exception support for quantity and shipping location: Customers can request quantity and shipping location updates, along with expedite requests via chat and voice channels.
-   Voice assistant intake for order exceptions: Customers can submit expedite, quantity, and shipping location requests via voice. Requests are captured and converted into order cases for resolution in CSM/FSM Configurable Workspace.
-   Unified extension point for feasibility checks: A single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) validates delivery, quantity, and shipping feasibility, replacing the earlier expedite-only ATP check.
-   Auto-populated account and contact on interactions: Account and Contact fields are populated during chat handoff, giving agents immediate customer context and improving summarization accuracy.
-   AI-generated summaries for agent handoff: Agents receive a concise AI-generated summary instead of full chat history, improving context and productivity.

</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

1.0.2

</td><td>

New:

Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and reason about goals, portfolio plans, and projects. The following tools are available in this release: Tool Description get\_goals Retrieves goals and objectives. generate\_goal\_insights Generates AI-powered insights for goals and targets. get\_portfolio\_plans Retrieves portfolio plans. generate\_portfolio\_insights Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies. get\_projects Retrieves projects. generate\_project\_insights Detects project risks, analyzes status trajectory, and provides recommendations. identify\_project\_risks Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts. get\_ai\_status\_report Generates a RAG \(Red, Amber, Green\) status report across resources, cost, schedule, and scope.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.2.0

</td><td>

Changed

Minor API changes for another app support internally

</td></tr><tr><td>

Now Assist AI Helper - Galileo Inside

</td><td>

2.1.2

</td><td>

This plugin was updated to be compatible with the October version of Now Assist.

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

31.0.5

</td><td>

-   New

-   Changed

    -   Browser tabs that open during goal execution in adaptive desktop actions remain open after the goal completes. Use the keep\_tab\_open system property to turn this behavior on or off. The property is turned on by default.
    -   Adaptive desktop actions is enhanced to improve execution efficiency.
-   Fixed

-   Removed


</td></tr><tr><td>

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

8.0.0

</td><td>

New:

 -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
-   Enhanced workflow to enable requesters to accept/reject the case resolution.

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

29.2.3

</td><td>

Changed Updated versions of dependent apps.

</td></tr><tr><td>

Now Assist for code generation

</td><td>

28.5.23

</td><td>

Now Assist for code generation features now inherit skill-level ACLs configured in Now Assist Admin, ensuring restricted features are only available to authorized users.

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

4.3.0

</td><td>

\* Changed

 - Engagement tool for DEX agents to obtain employee approval before auto-triggering device actions. This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

4.3.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Error Framework

</td><td>

1.0.3

</td><td>

Initial Release

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

10.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

-   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify features.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

7.0.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

Now Assist for Health and Safety

</td><td>

1.4.1

</td><td>

New: Contextual Action Planner sidebar in the Health and Safety Workspace: Create actions manually or from AI suggestions, and review them in context across incidents, observations, investigations, cases, audits, work permits, risk assessments, meetings, etc.

</td></tr><tr><td>

Now Assist for Impact

</td><td>

4.0.5

</td><td>

Code Fix Agent: Enhanced Error Logging

 When the Code Fix Agent runs into a problem, you will now see a plain-language explanation of what went wrong and what to do next - right on the remediation record. Select the links navigate directly to the relevant error record, so there's no need to hunt through system logs.

</td></tr><tr><td>

Now Assist for Legal Service Delivery

</td><td>

1.8.1

</td><td>

-   New

-   Changed Support for upgraded versions of third party LLMs has been provided.

-   Fixed Legal request and matter summarization now delivers improved accuracy across all supported models

-   Removed


</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

2.2.2

</td><td>

Multilingual Enhancements

 ICM Case Narrative Ai Agent Support

</td></tr><tr><td>

Now Assist for Purchase Order Management \(POM\)

</td><td>

1.2.0

</td><td>

New:

 The automatic conversion of supplier emails into PO exceptions workflow now supports:

 -   Additional languages, enabling better recognition of non-English supplier communications
-   ERP purchase order IDs, allowing precise matching with purchase order data from enterprise resource planning systems

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

10.0.0

</td><td>

New:

 -   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
-   The Savings Opportunity Discovery agentic workflow analyzes contracts, spend data, sourcing pipeline data, and supplier performance on a recurring schedule to automatically identify a prioritized list of savings opportunities. Category managers can review each opportunity in the Now Assist Panel and create a pipeline project or dismiss the opportunity directly from the panel.

</td></tr><tr><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

8.0.0

</td><td>

New:

 -   Ability to link emails to the created cases and the supplier records
-   Ability to create assessment templates and error handling while cancelling created assessments

</td></tr><tr><td>

Now Assist for Telecommunications

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

6.0.7

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.13

</td><td>

-   New

None

-   Changed

None

-   Fixed

None

-   Removed

None


</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

3.0.3

</td><td>

- Added an agentic workflow for servicenow table record navigation

 - Support for Visual and Doc Qna

</td></tr><tr><td>

OT Manager Foundation

</td><td>

3.3.3

</td><td>

New Certified for Australia Patch 3

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.3.1

</td><td>

Multilingual Enhancements

 ICM Case Refinement Agent

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New:

 -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
-   Users can upload images or diagrams which contain a process flow/flow diagram. The Template AI agent reads these documents and analyzes the template and template items required.
-   The Template ai agent creates a draft template along with template items based on the document and provides draft template details which are verified by the user.

</td></tr><tr><td>

Telecommunications Media and Technology AI agent collection

</td><td>

6.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Universal Request AI agent collection

</td><td>

1.0.9

</td><td>

Fixed minor system defects

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|AI Agent Advisor|1.2.2|2026-07-09|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.10.0|2026-07-09|
|AI Agents for Customer Success Management|2.7.4|2026-06-16|
|AI Agents for Discovery|3.2.1|2026-07-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.1|2026-06-16|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|AI Agents for ITAM|4.4.0|2026-07-09|
|AI agents for Observability|6.1.4|2026-07-09|
|AI Agents for Service Exchange Provider|1.1.4|2026-07-09|
|AI agents for SLO|2.0.3|2026-06-16|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Workplace Service Delivery|3.3.1|2026-06-16|
|AI Control Tower for Now Assist|5.0.2|2026-07-09|
|AI Dashboard Insights|1.2.3|2026-07-09|
|AI Data Explorer|5.1.6|2026-07-09|
|AI Desktop Actions|5.0.1|2026-07-09|
|AI Enhanced Recommended Actions|1.0.3|2026-07-09|
|AI Experience Framework Skills|1.2.0|2026-07-09|
|AI Help Framework|1.0.6|2026-07-09|
|AI Search RAG|6.1.0|2026-06-16|
|AI Specialists for Security Incident Response|1.0.5|2026-07-09|
|AI Websearch|4.1.0|2026-06-16|
|AIOps Agentic Workforce|2.1.0|2026-07-09|
|Alert Assist|3.10.0|2026-07-09|
|Amazon Bedrock Spoke|1.5.0|2026-06-16|
|Analytics Generation|4.1.15|2026-07-09|
|App Generation|28.3.12|2026-07-09|
|App Summary|28.2.6|2025-12-11|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Build Agent Premium|1.4.1|2026-07-09|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Chat Recommendation|1.8.3|2026-07-09|
|Chat Summarization for Virtual Agent|1.11.4|2026-07-09|
|CMDB MCP Server|1.0.1|2026-07-09|
|Common AI Framework|1.0.1|2026-06-16|
|Complaint Case AI Agents collection|1.4.3|2026-07-09|
|Conversation Evaluator|3.0.4|2026-06-16|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Conversational Help|2.0.3|2026-03-12|
|Conversational subflows and actions|29.2.2|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.2.2|2026-06-16|
|Customer Service Management AI agent collection|6.1.0|2026-07-09|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Dynamic Guidance|28.3.2|2026-06-16|
|Employee Slate for Now Assist|1.1.5|2026-07-09|
|External content connectors - Now assist agent|1.1.2|2026-07-09|
|Field Service Management AI agent collection|3.0.1|2026-06-16|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|Generative AI Controller|14.1.2|2026-07-09|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|7.1.1|2026-07-09|
|HR Service Delivery AI agent collection|7.1.1|2026-07-09|
|HR Talent AI Agent Collection|5.0.4|2026-07-09|
|HR Voice AI Agents|2.3.6|2026-06-16|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|3.2.2|2026-07-09|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management AI agent collection|10.0.1|2026-07-09|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|ITOM AI Agents For Service Mapping|1.4.0|2026-07-09|
|Knowledge Center|31.11.3|2026-07-09|
|Knowledge Graph|8.1.0|2026-07-09|
|LEAP|4.1.0|2026-07-09|
|List AI Experience|3.0.0|2026-06-16|
|Manage Invoice Operations|1.1.2|2026-07-09|
|Manage Order Operations|2.0.3|2026-06-16|
|Manufacturing Commercial Operations AI agents collection|2.3.0|2026-07-09|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Metadata Search|1.0.12|2026-07-09|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.2|2026-07-09|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.6.0|2026-07-09|
|Model Context Protocol Client|2.2.0|2026-06-16|
|Model Context Protocol Server|1.6.1|2026-07-09|
|Notifications Email Agents|2.2.0|2026-07-09|
|Now Assist Admin Console|10.1.5|2026-07-09|
|Now Assist Agents for requestor|3.6.1|2026-07-09|
|Now Assist AI Agents|8.1.7|2026-07-09|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|31.0.5|2026-06-16|
|Now Assist Analytics|5.1.2|2026-07-09|
|Now Assist Center|5.0.5|2026-07-09|
|Now Assist context menu|3.7.1|2026-07-09|
|Now Assist Data Kit|8.1.6|2026-07-09|
|Now Assist for Accounts Payable Operations \(APO\)|8.0.0|2026-06-16|
|Now Assist for App Engine|29.2.3|2026-06-16|
|Now Assist for Automation Center|1.2.4|2026-07-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for code generation|28.5.23|2026-06-16|
|Now Assist for Collaborative Work Management \(CWM\)|6.1.2|2026-07-09|
|Now Assist for Complaint Case \(CSM\)|2.1.6|2026-07-09|
|Now Assist for Configuration Management Database \(CMDB\)|4.0.0|2026-07-09|
|Now Assist for Contract Analysis|1.0.11|2026-07-09|
|Now Assist for CPQ|1.0.5|2026-07-09|
|Now Assist for Creator|28.9.4|2026-07-09|
|Now Assist for Customer Service Management \(CSM\)|13.1.1|2026-07-09|
|Now Assist for Digital End-user Experience \(DEX\)|4.3.0|2026-06-16|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.3.2|2026-06-16|
|Now Assist for Enterprise Architecture \(EA\)|7.4.0|2026-07-09|
|Now Assist for Error Framework|1.0.3|2026-06-16|
|Now Assist for Field Service Management \(FSM\)|10.0.1|2026-06-16|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|7.0.0|2026-06-16|
|Now Assist for Hardware Asset Management|4.4.0|2026-07-09|
|Now Assist for Health and Safety|1.4.1|2026-06-16|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.3.2|2026-07-09|
|Now Assist for Impact|4.0.5|2026-06-16|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.8.0|2026-07-09|
|Now Assist for IT Service Management \(ITSM\)|16.0.3|2026-07-09|
|Now Assist for Legal Service Delivery|1.8.1|2026-06-16|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.3.0|2026-07-09|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.2.2|2026-07-09|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|12.1.1|2026-07-09|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.8|2026-05-05|
|Now Assist for Prompt Assistance|5.1.4|2026-07-09|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.2.2|2026-06-16|
|Now Assist for Purchase Order Management \(POM\)|1.2.0|2026-06-16|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Sales and Order Management for Telecommunications|4.1.2|2026-07-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.5|2026-07-09|
|Now Assist for Security Incident Response \(SIR\)|6.3.4|2026-07-09|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.1.4|2026-07-09|
|Now Assist for Setup|3.1.4|2026-07-09|
|Now Assist for Setup Core|2.1.5|2026-07-09|
|Now Assist for Software Asset Management \(SAM\)|9.0.0|2026-07-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|10.0.0|2026-06-16|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.7.1|2026-07-09|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|8.0.0|2026-06-16|
|Now Assist for Talent|1.8.3|2026-07-09|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.7|2026-06-16|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|5.1.1|2026-07-09|
|Now Assist for Vulnerability Response|5.1.0|2026-07-09|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.13|2026-06-16|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in AI Search|17.1.4|2026-07-09|
|Now Assist in Catalog Builder|7.3.0|2026-07-09|
|Now Assist in Catalog item forms|1.4.2|2026-07-09|
|Now Assist in Contract Management|2.3.2|2026-07-09|
|Now Assist in Conversational Catalog Request|7.1.1|2026-07-09|
|Now Assist in Document Intelligence|6.2.0|2026-07-09|
|Now Assist in Document Management|3.0.1|2026-07-09|
|Now Assist in Knowledge Management|30.11.3|2026-07-09|
|Now Assist in Standard Ticket Page|1.3.0|2026-07-09|
|Now Assist in Virtual Agent|20.0.8|2026-07-09|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|3.0.3|2026-06-16|
|Now Assist Service Quality|2.0.2|2026-07-09|
|Now Assist Skill Discovery and Execution|10.2.3|2026-07-09|
|Now Assist Skill Kit|9.1.1|2026-07-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Opportunity Management AI Features|1.0.9|2026-07-09|
|OT Manager Foundation|3.3.3|2026-06-16|
|Platform AI Agents and Skills|13.1.9|2026-07-09|
|prompt-management|2.0.6|2026-07-09|
|Public Sector Digital Services AI Agent Collection|1.3.1|2026-06-16|
|Query Generation|6.1.1|2026-07-09|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|Recommended Actions for Security Operations|2.2.4|2026-07-09|
|RSM AI agent collection|1.3.0|2026-03-12|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.18|2026-07-09|
|ServiceNow AI Lens|7.0.2|2026-07-09|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.1.0|2026-05-05|
|UI Generation|28.2.14|2026-01-23|
|Universal Request AI agent collection|1.0.9|2026-06-16|
|Voice input for Now Assist|1.5.0|2026-07-09|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|
|Zero Touch Service Desk|2.3.5|2026-07-09|

## Suite version 29.3.20260716 - Australia Patch 3

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

3.3.2

</td><td>

New

 -   Added a new "Waiting for requester" activity state to support workflows requiring user follow-up or additional input.
-   Added telemetry instrumentation for the in-product agentic experience to enable activity usage and engagement tracking.
-   Introduced support for configurable visibility of the "Restart/Cancel Activity" option in the overflow menu to avoid conflicts with playbook activities.
-   Completed foundational integration exploration between Suggested Actions AI Agent capabilities and the in-product experience.

 Changed

 -   Updated headers across CSP, modal, and inline experiences from "AI Workflows" to "AI Activity" for improved terminology consistency.
-   Renamed "Input required" to "Input needed" for clearer user messaging.
-   Updated activity action text from "Cancel" to "Stop Activity."
-   Refined follow-up action labels and completed several small UI and copy improvements to enhance overall usability and consistency.

 Fixed

 -   Resolved workflow handling for requester wait-state scenarios to ensure activities properly reflect and manage pending user responses.
-   Addressed overflow menu conflicts between activity controls and playbook activity options.

 Removed: Removed outdated terminology and legacy labels associated with prior AI workflow naming and activity actions.

</td></tr><tr><td>

Agentic Contact Center for Banking

</td><td>

1.3.0

</td><td>

Changed: Updated dependency from AI Foundation to FSO Now Assist

</td></tr><tr><td>

Agentic Contact Center for Insurance

</td><td>

1.1.0

</td><td>

New application

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.9.0

</td><td>

New - -   AIOps AI Specialist \(limited availavilblity\) - The AIOps AI Specialist AI is ServiceNow's purpose-built AI agent for IT Operations, designed to autonomously monitor, correlate, triage, and resolve infrastructure and application events at enterprise scale.
-   Onboarding of the AIOps AI Specialist, including setting up the scope for the AI Agent, testing it and confgiure its task
-   Remediation agent that works alongside the AIOps AI Specialist
-   Proactive grouping recommendation using AI

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.7.4

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

AI Agents for Discovery

</td><td>

3.0.0

</td><td>

New:

 AI Agent that investigates the missing attribute brought in through Pattern based discovery, finding affected CIs and links errors to standard error codes.

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.3.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI Agents for Health and Safety

</td><td>

1.3.3

</td><td>

Fixed: Missing xml field that were causing data quality tests to fail

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

4.3.0

</td><td>

In this version, the following enhancements have been made:

 -   Security and access control management have been enhanced with simplified installation and automatic configuration handling.
-   Stockroom locations no longer appear for software requests.
-   The Orchestrator now displays human-readable output in work notes.
-   Document extraction now works seamlessly with improved field configuration.

</td></tr><tr><td>

AI agents for Observability

</td><td>

6.0.5

</td><td>

New: Added Splunk, AWS CloudWatch, ThousandEyes, SolarWinds, and Prometheus as supported investigation backends for the Analyze alert impact agentic workflow, expanding the alert insights available.Changed

-   Updated the Analyze alert impact agentic workflow to route all alert investigation through a single SRE Investigate AI Agent, delivering consistent behavior across all supported backends and simplifying the path for adding new vendor agents.
-   Migrated New Relic and Datadog integrations to Model Context Protocol \(MCP\) agents, standardizing on vendor-maintained tool surfaces so the investigation workflows stay current as vendors ship updates.

Deprecated: Deprecated the Dynatrace Analysis AI Agent, superseded by the Dynatrace MCP Server Agent.

</td></tr><tr><td>

AI agents for SLO

</td><td>

2.0.3

</td><td>

New: Added a Reliability Domain Agent that analyzes historical, post-incident data to identify service level objective \(SLO\) and synthetic monitoring gaps across configuration items \(CIs\) and services, then generates reliability tasks to address them.

</td></tr><tr><td>

AI agents for Synthetic Monitoring

</td><td>

1.2.2

</td><td>

Initial Release

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.3.1

</td><td>

-   New: None

-   Changed: Workplace Utilization QnA Agent can now be used by users with the sn\_wsd\_spcmgmt.space\_planner role

-   Fixed: The AI Agent was not always able to block the location after submitting an emergency maintenance request

-   Removed: None


</td></tr><tr><td>

AI Control Tower for Enterprise AI Foundation

</td><td>

1.1.1

</td><td>

-   New

    -   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   View the entity, risk, and control for each assessment directly in task and work queue lists, without opening individual records.
    -   Access authority documents, agency mappings, and citations for additional AI regulatory frameworks in the AI Risk and Compliance content pack.
-   Changed: Added automated impact assessment flow whenever an AI Dataset is created.

-   Fixed

    -   Localization and Performance issues are fixed.
    -   Fixed issue w.r.t to retired controls. Retired controls are excluded from the control based widgets.
    -   Fixed issue related to synchronization of AI asset life cycle tasks between AI Risk and Compliance and AICT workspace.
    -   Fixed functional domain issue w.r.t indicators feature on AI asset record page.

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

4.0.0

</td><td>

This is a "marker app" with no new functionality added; its purpose is to automatically trigger installation of other apps.

</td></tr><tr><td>

AI Data Explorer

</td><td>

5.0.8

</td><td>

-   Improved keyboard navigation in explorations:
    -   Navigate explorations fully via keyboard, including text and action buttons.
    -   Move up/down buttons have been added under the drag-and-drop icon.
-   The data visualization sparkle icon is no longer shown for data sources in a non-supported secure scope.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

4.0.1

</td><td>

-   New

    -   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
    -   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
    -   Switch to AI-assisted recording by selecting the new Record with AI \(recommended\) check box that replaces the previous capture modes in the Create desktop action modal.
    -   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
    -   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
    -   Control data visibility and security by using the Shared and Mark As Sensitive fields on the Desktop action parameter form.
    -   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.
-   Changed

-   Fixed

-   Removed


</td></tr><tr><td>

AI for document designer

</td><td>

22.3.4

</td><td>

New

 -   AI for Document Designer - A new AI-powered application that integrates with the Microsoft Word add-in, enabling users to generate and manage report content directly within Word documents using Now Assist.
-   AI-powered Word content generation - A custom AI skill that generates Microsoft Word report content through natural language prompts, allowing users to create document sections conversationally.
-   Content insertion into Word documents - Support for inserting AI-generated content \(HTML and OOXML formats\) directly into Word documents via sn-office-addin handlers.
-   Multi-conversation document editing - Ability to edit and refine document content across multiple conversations with the AI assistant, enabling iterative content development.
-   Data model, ACLs, and roles - Purpose-built data model with access controls and role definitions to secure AI-generated document content and manage user permissions.

 Changed: AI agent accuracy and prompt enhancements - Improved agent accuracy and refined prompts based on Architecture Review Board \(ARB\) feedback for higher quality content generation.

 Fixed: AI agent icons updated in add-in - Corrected the icons displayed for the AI agent within the Microsoft Word add-in.

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed

 -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

AIOps Agentic Workforce

</td><td>

2.0.1

</td><td>

New

AIOps AI Specialist \(L1 AI Worker\)

AI-powered first responder that autonomously triages alerts, reduces noise, enriches context, and provides remediation recommendations across the alert lifecycle. -   Context-rich alert investigation - Enhanced alert analysis using CMDB topology, incident history, and operational signals to provide deeper insights and faster decision-making.
-   Knowledge-driven investigation - Integrated knowledge sources, including KB articles into the investigation workflow to improve accuracy and deflect incidents
-   Remediation suggestions from existing subflows - AI-generated remediation recommendations leveraging existing alert rules and subflows to accelerate resolution and ensure consistency.
-   SRE AI Specialist integration - Integrates seamlessly with the SRE AI Specialist for deeper investigation, including observability data analysis and root cause hypotheses

 Dedicated AIOps Manager Homepage

New homepage for AIOps Managers and Event Management Admins to onboard, configure, and manage AI Specialists from a centralized command center.

</td></tr><tr><td>

Alert Assist

</td><td>

3.9.3

</td><td>

New: Proactive Grouping Recommendations - AI-generated grouping recommendations help AIOps administrators identify alert correlation opportunities with greater speed and accuracy.

 Changed: Updated supported LLM versions to GPT-4o Mini and Claude Haiku 4.5, bringing the latest model improvements to the platform.

 Fixed: The Autonomous Operator was not automatically updating the description of HLA alerts. This has been corrected.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.5.0

</td><td>

Fixed - Streamline ACLs

</td></tr><tr><td>

Analytics Generation

</td><td>

4.1.10

</td><td>

-   Fixed ability to add to an exploration a list type data visualization.
-   Fixed the ability to edit a data visualization in Visualization Designer.

</td></tr><tr><td>

APO - Foundation

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies.

</td></tr><tr><td>

APO - Prime

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies.

</td></tr><tr><td>

App Engine - Prime

</td><td>

29.1.5

</td><td>

Changed: Updated versions of dependent apps.

</td></tr><tr><td>

App Life Cycle AI Agents

</td><td>

29.3.1

</td><td>

Changed: Maintenance release.

</td></tr><tr><td>

App Summary

</td><td>

29.3.1

</td><td>

Changed: Maintenance release. No customer facing updates.

</td></tr><tr><td>

Build Agent Premium

</td><td>

1.3.1

</td><td>

-   New

    -   Upload files to Build Agent to provide context: images \(PNG, JPEG, GIF, WEBP\), documents \(PDF, DOC, DOCX, XLS, XLSX\), and text/code files \(TS, JS, PY, JSON, MD, HTML, YAML, and more\)
    -   View update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab.
    -   Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.
    -   Validate user interface output during app creation with the UI validation tool in Build Agent, now available in ServiceNow Studio.
    -   Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.
-   Changed: New MCP integrations in ServiceNow Studio: Added support for many new connectors including Atlassian Rovo, DocuSign, Figma, GitHub, Linear, Miro, Prisma Postgres, and Zoom \(Chat, Docs, Revenue Accelerator, Whiteboard\)


</td></tr><tr><td>

Business Continuity Management Advanced

</td><td>

1.1.3

</td><td>

1. AI Agents and skills

 2. Business Continuity management features for impact analysis, business continuity plans, crisis management, and crisis map.

</td></tr><tr><td>

Business Continuity Management Foundation

</td><td>

1.1.3

</td><td>

1. AI Agents and skills

 2. Business Continuity management features for impact analysis, business continuity plans, and crisis management.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.8.2

</td><td>

Restrict context based on requestor's data

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.11.3

</td><td>

-   Support execution of Agent Chat, Sidebar Chat and Call Summarization to execute through Mosaic
-   Restrict Agent Chat Summarization Card only to the agent invoking it
-   Provide support to add default tables in Sidebar Chat Summarization configuration
-   Uptake Cobalt Raven ACLs Brazil Directive on the table sys\_generative\_ai\_predictions\_log

</td></tr><tr><td>

Collaborative Work Management - Advanced

</td><td>

2.0.3

</td><td>

New:

 -   Team Member Role for SPM Project Workspace - Enables team members to access CWM and manage project tasks. Users can perform CRUD operations on project tasks, demand, and idea tables, and have calendar access. Role assignments and permissions are managed to enhance collaboration within the workspace.
-   AI-powered import of Tasks and Stories into CWM Boards from spreadsheets, documents, and images using Now Assist.
-   Inline comments in Docs to collaborate on specific text in a document through threaded discussions. Mention colleagues with @ to notify them directly, and receive email notifications when a comment is added, a reply is posted, or you are @-mentioned in a Doc.

</td></tr><tr><td>

Common AI Framework

</td><td>

1.0.1

</td><td>

New:

 AI Framework that autonomously discovers schema, samples, and aggregates live ServiceNow tables, and presents a sourced answer without modifying any data.

</td></tr><tr><td>

Complaint Case AI Agents collection

</td><td>

1.4.1

</td><td>

Enhancements and defects fixed:

 1.  AI modified field indicator. AI Sparkle on Fields: AI-generated field indicators are now displayed consistently across both the platform UI and Workspace.
2.  Complaint Case Intake Agent
    -   Added the hyperlink to the complaint case number.
    -   Prompt enhancements on location and products
    -   Related Parties for Consumers.
3.  Complaint Case Research Agent
    -   Deleted default tasks after the creation of agent tasks.
    -   Prompt enhancement on multi messages into one.
    -   Search profile separation

</td></tr><tr><td>

Contract Management Pro - Prime

</td><td>

1.0.9

</td><td>

-   New

-   Changed

    -   Identify missing clauses in contract revisions with improved accuracy.
    -   Support for upgraded versions of third party LLMs has been provided.
-   Fixed

    -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
    -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.
-   Removed


</td></tr><tr><td>

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Conversation Insights

</td><td>

3.1.0

</td><td>

New: Conversation Insights now supports customers with data sovereignty requirements. The application can be re-enabled for customers using local SKUs, allowing deployment with local conversation insights services.-   Changed: None
-   Fixed: The assignment of the sn\_aci.insights\_read\_write role to the conv-insights-svc-account user has been corrected to ensure proper handling of inheritance flag information.
-   Removed: None

</td></tr><tr><td>

Conversational Studio

</td><td>

9.0.3

</td><td>

-   New

    -   General access for Premium Chat on Portals, Employee Slate, MS Teams, and Mobile
    -   Voice Input for Premium Chat
    -   Voice Assistant support on the 3rd party mobile app.
    -   New metrics supported for the conversation auto evaluation feature
-   Changed

    -   Now Assist Panel Platform \(default\) assistant would be turned on by default for new customers
    -   UX improvement on the Assistant edit flow
    -   Inactive assistants can be tested in the Testing panel
    -   Assets can be assigned to inactive assistants.
    -   Setup topics without Gen AI skill will have visible and discoverable false, toggle will be disabled. For Setup topics that have Gen AI skills, admin can still toggle these flags.
-   Fixed

    -   Number of Promoted Assets is no longer restricted from the Assistant edit flow
    -   Accessibility color contrast

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

29.2.2

</td><td>

Changed: Maintenance release.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

6.0.3

</td><td>

Changed:

 -   Added voice-driven case status retrieval and updates, enabling customers to check open case statuses and submit updates through guided voice interactions across Genesys, NICE, Five9, 3CLogic, and Amazon Connect, reducing live agent dependency.
-   Enhanced Provide Customer 360 Insights with Enterprise Graph and AI Agent deep research for richer, more contextual query results.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

2.0.1

</td><td>

New

 -   Agent renamed to "Vision AI Agent"
-   Requests now routed via the MultiModal Service \(MMS\) to enable more consistent and scalable multimodal processing \(up to 500MB video files\)
-   Improved response quality for Video Workflow use cases
-   Supported video formats: MP4, MOV, WEBM, AVI, MKV, and WMV

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.3.2

</td><td>

Fixed:

 Updated the version for ServiceNow Docs Connector to fix dependency failures

</td></tr><tr><td>

Enhanced Features for IRM Enterprise

</td><td>

22.3.4

</td><td>

\[Changed\]

This application replaces the Now Assist for IRM application to access the AI-powered features.

</td></tr><tr><td>

Enhanced Features for IRM Professional

</td><td>

22.3.3

</td><td>

\[Changed\]

This application replaces the Now Assist for IRM application to access the AI-powered features.

</td></tr><tr><td>

Enterprise Architecture - Advanced

</td><td>

1.0.1

</td><td>

New: Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.

</td></tr><tr><td>

Enterprise Architecture - Prime

</td><td>

1.0.1

</td><td>

New

 -   Generate a business process map \(BPM\) diagram in the Enterprise Modeling and Visualization by uploading an image of an existing process diagram.
-   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.

</td></tr><tr><td>

External content connectors - Now assist agent

</td><td>

1.1.1

</td><td>

-   New: Improvements to the AI Agent to support NextWave compatible experience.

-   Fixed

    -   Agent prompt quality improvements.
    -   Hallucination issues to improve AI Agent performance.
-   Removed: Implicit dependency on the Webcrawler external content connector. The Webcrawler connector now needs to be installed explicitly as a soft dependency.


</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

3.0.1

</td><td>

New

 -   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

 Changed Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to ensure certification and release standards.

 -   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

 Fixed None

 Removed None

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

4.1.0

</td><td>

New: -   Added Insurance CSR support AI agent for Interaction page
-   Added Insurance CSR customer insights AI agent for Customer 360 Page
-   Added Insurance Data Lookup tool
-   Added Conversation Transcript Reader tool

</td></tr><tr><td>

Flow Execution Analysis

</td><td>

29.2.8

</td><td>

New-   Summarize flow execution details when flow reporting is off.
-   Identify potential causes of flow errors.
-   Resolve flow errors with suggested fixes.

</td></tr><tr><td>

FSC Common - Foundation

</td><td>

1.2.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

FSC Common - Prime

</td><td>

1.2.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

FSM - Advanced

</td><td>

2.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify features. -   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed None

Removed None

</td></tr><tr><td>

FSM - Foundation

</td><td>

2.0.1

</td><td>

New

 -   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content \(links, code, special characters\).
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins/analysts can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

 Changed

 -   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify that features meet release standards.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

 Fixed : None

 Removed : None

</td></tr><tr><td>

FSM Scheduling AI Agent Collection

</td><td>

1.0.7

</td><td>

Initial release

</td></tr><tr><td>

Generative AI Controller

</td><td>

14.0.1

</td><td>

-   New: Guardian prompt injection detection is being enabled as always-on and in blocking mode by default for Skills. Added granular admin controls to enable Guardian's prompt injection detection independently for skills, agents, or both
-   Changed: Increased Gen AI execution log \(sys\_generative\_ai\_log\) retention to six months.

</td></tr><tr><td>

GRC Common GenAI

</td><td>

22.3.4

</td><td>

This release includes improvements to GRC Common Generative AI in issue resolution, issue action planning, agent skill configuration, subscription management, and translations.

 New Fetch-Issue-Details Tool: A new tool enables the issue resolution AI agent to fetch issue details by issue number or identifier, complementing the existing tool and enhancing response accuracy. No upgrade action is required, but customers with customizations should review the new mappings.

 Refined Action Plan and Remediation Agents: Improvements to the issue action plan and remediation tasks AI agents and their supporting tools ensure more reliable and consistent generation of action plans and remediation suggestions across multiple AI model providers, with better usage tracking. Customers with custom post-processors should re-validate changes.

 Updated Issue Summarization Skill: The Now Assist issue summarization skill includes new configuration records offering descriptions and guides for configuration and prompt customization, enhancing the administrator and end-user experience without requiring upgrade actions.

 Generative-AI Asset Subscriptions and Translations: Eight new asset subscriptions have been added for tracking and governance of GRC AI capabilities, and translations across supported languages have been refreshed to improve the experience for non-English users. Customers should verify subscription states post-upgrade.

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

22.3.1

</td><td>

This release includes the following changes:

 -   Added default deny ACLs on Control Objective skills, the Risk Identification Agent, and the Risk Assessment Summarization skill.
-   Excluded audit entry control objectives from skills.
-   Enabled audit entry support for related records.
-   Excluded audit entry risks from the Risk Identification Agent.
-   Enabled third-party model support for the Risk Identification Agent and the Risk Assessment Summarization skill.

</td></tr><tr><td>

Group-Action Framework

</td><td>

7.0.1

</td><td>

New: Backend support for HR Knowledge Gaps. This capability will be taken up by the Knowledge Center team in a future release. No customer-facing updates in this release.

 Changed: Nothing changed in this release.

 Fixed: Various minor defects fixed.

 Removed: Nothing removed in this release.

</td></tr><tr><td>

Hardware Asset Management - Advanced

</td><td>

1.0.1

</td><td>

In this version, all generated summaries and user-facing content now display in the user's preferred language.

</td></tr><tr><td>

HR Service Delivery AI agent collection

</td><td>

7.0.2

</td><td>

Resolved defects affecting content and agent tool functionality

</td></tr><tr><td>

HR Talent AI Agent Collection

</td><td>

5.0.2

</td><td>

New Added new skills for Interview health tracker.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

HRSD - Advanced

</td><td>

2.0.2

</td><td>

Changed App and plugin dependencies have been updated.

</td></tr><tr><td>

HRSD - Foundation

</td><td>

2.0.2

</td><td>

Changed App and plugin dependencies have been updated.

</td></tr><tr><td>

HRSD - Prime

</td><td>

2.0.2

</td><td>

Changed App and plugin dependencies have been updated.

</td></tr><tr><td>

Industrial Control Tower Advanced

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Foundation

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Prime

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

Integrated Risk Management Advanced

</td><td>

22.3.3

</td><td>

The IRM Advanced plugin has updated its dependencies by replacing the Now Assist IRM plugin with the IRM Professional plugin, while maintaining dependencies on AI Platform Advanced and IRM Foundation. This change means that installing the Advanced tier now includes all Professional tier features, but generative AI capabilities are no longer included transitively and remain accessible through the Foundation dependency. Customers upgrading to this release will have the IRM Professional plugin added automatically and should verify the status of the IRM Generative AI plugin, deactivating it if preferred.

</td></tr><tr><td>

Integrated Risk Management Foundation

</td><td>

22.3.2

</td><td>

The IRM Foundation plugin has been updated to include a new dependency on the IRM Generative AI plugin, in addition to the existing dependencies on AI Platform Foundation and IRM Standard. This change ensures that installing or upgrading IRM Foundation automatically includes generative AI capabilities for all IRM tiers built on Foundation, including higher tiers such as Standard, Professional, Advanced, and Enterprise. Upon upgrading, the IRM Generative AI plugin is installed automatically, but customers may deactivate it if they do not wish to use its capabilities. Additionally, customers should verify that AI-related entitlements, such as generative AI subscriptions, are properly assigned to users who will use these features.

</td></tr><tr><td>

Integrated Risk Management Prime

</td><td>

22.3.3

</td><td>

The IRM Prime plugin now depends on IRM Enterprise, in addition to AI Platform Foundation and IRM Advanced, for installation or activation. This change ensures that AI features in Prime rely on data managed by IRM Enterprise entitlements, improving functionality by automatically resolving and including IRM Enterprise if not already installed. Customers upgrading to version 22.3.0 must have IRM Enterprise licensed and available to complete the upgrade; no data migrations or configuration changes are needed, and existing integrations remain unaffected.

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

22.3.1

</td><td>

New Implemented meta data changes to enable AI native support for all skills and agents in the Regulatory Change Management application.

 Changed Improved agent instructions and supporting tools for the Regulatory Alert Analysis and Recommendations agent to ensure more reliable and consistent responses.

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

22.3.2

</td><td>

Fixed Risk Event Summary now generates correctly when a task is associated with a Risk Event.

</td></tr><tr><td>

IT Service Management

</td><td>

3.0.2

</td><td>

New:

Employee experience

Front door employee experience \(Employee Slate\): a conversation-first portal with a unified Activity Hub displaying open incidents and requested items, fulfillment progress, a Needs Attention area, and a simplified Request experience. Fulfiller experience

Catalog tasks on the landing page: IT agents can track catalog tasks alongside incidents and requests on the fulfiller homepage.Admin experience

-   Expand to Service Operations: a guided upgrade path adds Major Incident, Problem, On call, and Walk up Management, with one-click install and direct navigation to admin setup.
-   Employee Slate IT Service Management onboarding: the configuration console includes the Employee Slate setup task as part of IT Service Management onboarding.
-   CMDB onboarding: the configuration console includes configuration item setup task as part of IT Service Management onboarding.

Changed:

Fulfiller experience

-   Embedded Now Assist enhancements: the incident record card now surfaces contextual actions at resolution: draft or attach a knowledge article, propose a major incident, create change or problem records, and share resolution steps with the requester. Actions appear only when relevant to the incident context.
-   Incident form layout: updates to the Incident details layout, including the position of Attachments and Configuration Items on the form.

Admin experience

-   AI agent improvements: improvements to the AI agents that help configure routing rules, categories, and subcategories.
-   Configuration console setup tasks: updated header and footer for a consistent experience and clearer understanding of each task.

</td></tr><tr><td>

IT Service Management Advanced

</td><td>

3.0.1

</td><td>

New:

Fulfiller actions from an incident: Fulfillers can create a change request, propose a major incident, and create a problem record for an incident.Changed:

-   Enhanced embedded Now Assist chat module card with contextual resolution actions: draft or attach a knowledge article, propose a major incident, create a change or problem, and send next steps to the requester.
-   AI-assisted incident triage, resolution guidance, and summaries surfaced natively on the record.

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.4.0

</td><td>

-   New: n/a
-   Changed

Security related enhancements on existing AI Voice agents

-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

ITOM - Advanced

</td><td>

1.0.10

</td><td>

New in ITOM - Advanced

 -   Added AI agents to automate monitoring and remediation for Discovery, MID Servers, Certificate Management, Service Mapping, and LEAP.
-   Added AI Agent Topology Mapping to provide governance and visibility to your AI estate.
-   Added ITOM URL Discovery to surface shadow SaaS and unmanaged applications directly in the CMDB.
-   Added ITOM Configuration Console to simplify onboarding for Discovery and Event Management with guided, best-practice setup.
-   Added AIOps Learning Enhanced Automation Playbooks to turn historical incidents into dynamic, reusable resolution intelligence.

</td></tr><tr><td>

ITOM - Prime

</td><td>

1.0.6

</td><td>

See the Now Assist for Platform and AIOps Experience release notes.

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.3.2

</td><td>

New

 -   Service Mapping supports the Model Context Protocol \(MCP\), providing a conversational interface for live application service data. Service Mapping admins can connect Claude Desktop to a ServiceNow instance and query service topology, server-to-service relationships, related CIs, and unmapped configuration items.
-   Service Mapping Workspace widgets1. Business app linked to App services - Indicating the count of business applications that were linked to application services by the Business App Mapping AI Agent.2. Maps created by Now Assist - Indicating the count of the service maps created by Service Mapping AI Agent.

 Changed

 -   The AI specialists for Service Mapping are renamed as AI Agents for Service Mapping.
-   View the service map created by Service Mapping AI Agent through the AI Activity list.

</td></tr><tr><td>

Knowledge Center

</td><td>

31.10.8

</td><td>

The Knowledge Center centralized hub for Knowledge Admin and Manager:

 1. Is an entry point for KM Management personas to manage all capabilities and configurations 2. Guides users on the next-best actions to take by displaying actionable key insights 3. Is a suite of KM Tools for suggesting content creation, updates, duplicates, and article retire

</td></tr><tr><td>

Knowledge Graph

</td><td>

8.0.0

</td><td>

Changes:

 - Added changes for better Typo handling for Table Labels.

 - Added internal usage tracking enhancements.

</td></tr><tr><td>

LEAP

</td><td>

4.0.0

</td><td>

-   New

    -   Discover and execute Ansible playbooks from LEAP automation opportunities to promote faster incident resolution
    -   Track missed automation opportunities in LEAP to identify gaps in automation coverage
    -   Auto-generate resolution steps for all critical and high severity automation opportunities post initial run
    -   Improved resolution step relevance as irrelevant steps filtered out by group problem description
    -   LEAP available with Now Assist for ITSM
-   Changed

    -   Product renamed from AIOps LEAP to LEAP \(Learning-Enhanced Automation Platform\)
    -   AI-enhanced and structured knowledge base articles published to the Knowledge Center
-   Fixed

    -   Automation Opportunities page load time reduced from 3+ seconds
    -   Value Dashboard page load time reduced from 4+ seconds
    -   Resolved stale resolution steps reappearing in record metric table after SOW Flow updates
    -   Fixed sharp-edged AI Gradient button for Regenerate in AO Details to match default theme
    -   Fixed UI issues on resolution steps filter in LEAP Settings page
    -   Fixed missing help content on LEAP Installer Skill Activation page
    -   Reverted unintended default UI filter that auto-generated resolution steps
    -   Fixed Maintenance ACL Roles being overridable by Admins in LEAP Automation Playbooks

</td></tr><tr><td>

Legal Service Delivery - Prime

</td><td>

1.0.9

</td><td>

-   New

-   Changed Support for upgraded versions of third party LLMs has been provided.

-   Fixed Legal request and matter summarization now delivers improved accuracy across all supported models

-   Removed


</td></tr><tr><td>

List AI Experience

</td><td>

3.0.0

</td><td>

AI Filter Assist allows users to define conditions using natural language in an intuitive, dialog-driven interface. This feature helps reduce the cognitive load of building conditions using the traditional condition builder by allowing users to type or speak a prompt that will then create the query needed to filter, sort, or group data.

 This release we fixed two defects in AI Filter Assister where an ACL had a typo in it's script and "Add to existing filters" mode was selectable even though it should be disabled.

</td></tr><tr><td>

Manage Invoice Operations

</td><td>

1.1.0

</td><td>

-   New Delivery note upload for quantity disputes: Customers can upload delivery notes during case creation, enabling the invoice dispute intake assistant AI agent to validate and resolve quantity disputes without human intervention.

-   Changed Order line quantity validation for disputes: The invoice dispute support assistant AI agent uses order line data when sold product records are unavailable such as new orders, non-serialized products, or services. It auto-approves valid disputes and escalates only when data is unclear.


</td></tr><tr><td>

Manage Order Operations

</td><td>

2.0.3

</td><td>

New: Automated email notifications for order cases: Send emails when the AI agent opens an order case from a Business Portal chat and when the case is resolved. Closure emails include resolution and quote details, if generated. Voice-created cases don't trigger emails.Scripted extension point for quote thresholds: A scripted extension point to integrate the manage order operations AI agent with your inventory, ERP, and quote systems for quote threshold evaluation. The AI agent generates a quote when a quantity-change request exceeds the configured price threshold. -   Changed

-   Order exception support for quantity and shipping location: Customers can request quantity and shipping location updates, along with expedite requests via chat and voice channels.
-   Voice assistant intake for order exceptions: Customers can submit expedite, quantity, and shipping location requests via voice. Requests are captured and converted into order cases for resolution in CSM/FSM Configurable Workspace.
-   Unified extension point for feasibility checks: A single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) validates delivery, quantity, and shipping feasibility, replacing the earlier expedite-only ATP check.
-   Auto-populated account and contact on interactions: Account and Contact fields are populated during chat handoff, giving agents immediate customer context and improving summarization accuracy.
-   AI-generated summaries for agent handoff: Agents receive a concise AI-generated summary instead of full chat history, improving context and productivity.

</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

1.0.2

</td><td>

New:

Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and reason about goals, portfolio plans, and projects. The following tools are available in this release: Tool Description get\_goals Retrieves goals and objectives. generate\_goal\_insights Generates AI-powered insights for goals and targets. get\_portfolio\_plans Retrieves portfolio plans. generate\_portfolio\_insights Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies. get\_projects Retrieves projects. generate\_project\_insights Detects project risks, analyzes status trajectory, and provides recommendations. identify\_project\_risks Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts. get\_ai\_status\_report Generates a RAG \(Red, Amber, Green\) status report across resources, cost, schedule, and scope.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.12.0

</td><td>

Removed : api-version query parameter from Create Response OEM action

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.5.0

</td><td>

New

Enabled the mobile card generation capability to be executed Off-Glide to improve scalability and performance.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.2.0

</td><td>

Changed

Minor API changes for another app support internally

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

1.5.1

</td><td>

Performance improvements implemented, and third-party IDPs now allowed to be used.

</td></tr><tr><td>

Notifications Email Agents

</td><td>

2.1.1

</td><td>

New:

 -   Multi-intent identification support
-   Missing inputs extraction
-   email branding/template support for email generation

</td></tr><tr><td>

Now Assist Agents for requestor

</td><td>

3.5.0

</td><td>

Approval checklist generator skill accepts additional context parameter that is used to resolve checklist's unknown items.

</td></tr><tr><td>

Now Assist AI Helper - Galileo Inside

</td><td>

2.1.2

</td><td>

This plugin was updated to be compatible with the October version of Now Assist.

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

31.0.5

</td><td>

-   New

-   Changed

    -   Browser tabs that open during goal execution in adaptive desktop actions remain open after the goal completes. Use the keep\_tab\_open system property to turn this behavior on or off. The property is turned on by default.
    -   Adaptive desktop actions is enhanced to improve execution efficiency.
-   Fixed

-   Removed


</td></tr><tr><td>

Now Assist Analytics

</td><td>

5.0.3

</td><td>

-   New

    -   Analytics dashboards pertaining to AI agents, AI assistants, and skills are consolidated inside Now Assist Center &gt; Monitor.
    -   Executions dashboard in Now Assist Center: Deep dive into individual executions of assistants and agents to improve performance.
    -   Business value dashboard in Now Assist Center: Analyze the impact of AI assets on time and cost savings and set formula for calculating value per AI asset \(skills, AI agents, agentic workflows\)
-   Changed

-   Fixed

-   Removed


</td></tr><tr><td>

Now Assist Center

</td><td>

4.0.2

</td><td>

-   AI asset inventory. A new Asset Inventory page provides a single, consolidated view of every AI asset deployed across the instance including AI agents, agentic workflows, skills, subflows, actions, data assets, virtual assistants, topics, catalog items, and knowledge graphs. Each asset type surfaces active/inactive status, and the list supports column personalization so administrators can tailor the view to their needs. Assets from AI Agent Studio, Data Kit, and the platform catalog are unified in a single browsable surface.
-   AI readiness assessment. Administrators can now validate their instance's readiness for AI adoption directly within Now Assist Center. The new AI Readiness page supports on-demand and scheduled assessment execution across both Now Assist and Agentic AI assessment types. Results are surfaced in a dedicated Assessment Details page with historical tracking, enabling teams to identify configuration gaps, measure readiness over time, and accelerate the path to their first production AI solution.
-   AI Agent Advisor enhancements. The AI Agent Advisor experience has been refined based on feedback from the May release. Updates include an improved automation opportunities list page with better filtering and layout, redesigned Agent Advisor cards, a refreshed home page CTA experience that surfaces opportunities at a glance, a new Agent Advisor settings page, and stack metrics page improvements. These changes reduce friction in the discovery-to-deployment journey and improve the quality of agent recommendations surfaced to administrators.
-   Expanded OOTB skill configuration. The conversational administration experience now surfaces additional out-of-the-box skill configuration paths, including skill availability configuration and display experience settings extending the reach of guided, in-product setup to more of the Now Assist skill catalog.

</td></tr><tr><td>

Now Assist context menu

</td><td>

3.6.4

</td><td>

- Defects fixes and off glide LLM execution migration

</td></tr><tr><td>

Now Assist Data Kit

</td><td>

8.0.4

</td><td>

- Increased sample data input limit for SDG requests - Users \(Data Kit Admin\) can now select up to 50 seed records from a data collection or table when submitting a Synthetic Data Generation request, up from the previous default of 3. The maximum sample size is also configurable by NADK Admins via sys\_property.

 - Plausibility Metrics for Synthetic Data - Introduced plausibility scoring as a new data quality insight layer within the Generated Data view \(Data Kit &gt; Home &gt; Synthetic Data tab &gt; Open Generated Data &gt; Data Insight &gt; Plausibility\). Validates that generated field values are realistic, internally consistent, and free of garbage data.

 - OOB data sets

</td></tr><tr><td>

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

8.0.0

</td><td>

New:

 -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
-   Enhanced workflow to enable requesters to accept/reject the case resolution.

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed AI skill execution is now performed off glide

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

29.2.3

</td><td>

Changed Updated versions of dependent apps.

</td></tr><tr><td>

Now Assist for code generation

</td><td>

28.5.23

</td><td>

Now Assist for code generation features now inherit skill-level ACLs configured in Now Assist Admin, ensuring restricted features are only available to authorized users.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

6.0.1

</td><td>

New: AI-powered import of Tasks and Stories into CWM Boards from spreadsheets, documents, and images using Now Assist.

</td></tr><tr><td>

Now Assist for Complaint Case \(CSM\)

</td><td>

2.1.5

</td><td>

Changed: No new features, enhancements or fixes. Since there are updates to the AI agents, the version of this application must also be updated.

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

3.8.0

</td><td>

Fixed Security fixes

</td></tr><tr><td>

Now Assist for Contract Analysis

</td><td>

1.0.9

</td><td>

Existing feature: with latest third party model versions

</td></tr><tr><td>

Now Assist for Creator

</td><td>

29.2.5

</td><td>

New

 -   Build Agent
    -   Upload files to Build Agent to provide context: images \(PNG, JPEG, GIF, WEBP\), documents \(PDF, DOC, DOCX, XLS, XLSX\), and text/code files \(TS, JS, PY, JSON, MD, HTML, YAML, and more\)
    -   View update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab
    -   Connect Build Agent\_to external MCP servers in\_ServiceNow Studio. Previously, MCP server connectivity was only available in the\_ServiceNow IDE.
    -   Validate user interface output during app creation with the UI validation tool in\_Build Agent, now available in\_ServiceNow Studio.
    -   Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.
-   Catalog Item Generation Migrated Now Assist for Catalog Generation skill group \(Create Catalog Item and Refine Skill\) to Mosaic \(off-Glide GenAI Controller\) by enabling offglide routing via OneExtend
-   Flow Execution Analysis Net new app in Now Assist for Creator
-   Playbook Generation Playbooks now automatically generate a concise, AI-powered summary of a Playbook's purpose, structure, and logic, helping new process owners quickly understand existing workflows without manual documentation.
-   Widget Generation and Widget Updation Australia support
-   Changed

Build Agent New MCP integrations in ServiceNow Studio: Added support for 12 connectors including Atlassian Rovo, DocuSign, Figma, GitHub, Linear, Miro, Prisma Postgres, and Zoom \(Chat, Docs, Revenue Accelerator, Whiteboard\)


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

14.0.5

</td><td>

Fixed:

 The system ran out of memory because the trending topics feature \(for assigning cases to groups in Customer Service\) is trying to handle too much data at once.

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

4.3.0

</td><td>

\* Changed

 - Engagement tool for DEX agents to obtain employee approval before auto-triggering device actions. This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

4.3.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

7.3.1

</td><td>

New

 -   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.
-   Generate a business process map \(BPM\) diagram in the Enterprise Modeling and Visualization by uploading an image of an existing process diagram.

</td></tr><tr><td>

Now Assist for Error Framework

</td><td>

1.0.3

</td><td>

Initial Release

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

10.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify features. -   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

3.2.0

</td><td>

New: -   Added Insurance Customer Profile Summarization skill for Customer 360
-   Added Insurance interaction context summary skill

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

7.0.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

Now Assist for Hardware Asset Management

</td><td>

4.3.0

</td><td>

This release delivers UI modernization and quality improvements. The Now Assist for HAM interface has been upgraded to the latest UI framework, with improved parsing and rendering of Asset Summary responses. Accessibility improvements have also been applied.

 Improvements:

 1.  Currency fields extracted from purchase order attachments now display correctly.
2.  A missing field configuration in the purchase order attachment flow has been added.
3.  A component reliability issue in the record review workflow has been fixed.

</td></tr><tr><td>

Now Assist for Health and Safety

</td><td>

1.4.1

</td><td>

New: Contextual Action Planner sidebar in the Health and Safety Workspace: Create actions manually or from AI suggestions, and review them in context across incidents, observations, investigations, cases, audits, work permits, risk assessments, meetings, etc.

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

13.2.3

</td><td>

Consistent model support and on prem support

 Security guardrails and Defect fixes related to content and metrics

 Gen AI Trace logs improvement

</td></tr><tr><td>

Now Assist for Impact

</td><td>

4.0.5

</td><td>

Code Fix Agent: Enhanced Error Logging

 When the Code Fix Agent runs into a problem, you will now see a plain-language explanation of what went wrong and what to do next - right on the remediation record. Select the links navigate directly to the relevant error record, so there's no need to hunt through system logs.

</td></tr><tr><td>

Now Assist for IRM

</td><td>

22.3.3

</td><td>

The Now Assist for IRM application has been reclassified as an installed-as-dependency plugin, making it a platform-managed dependency that is hidden from the main user interface and no longer appears as a standalone application tile in the ServiceNow App Store. Despite this change, AI-driven IRM functionality remains unchanged and continues to operate as before. Users should now access AI features through the IRM Native SKU applications; the AI dependency loads transparently, and no customer action is required to maintain existing functionality.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

2.6.16

</td><td>

New:

 -   AIOps AI Specialist - Autonomous Alert Management \(Limited Availability\) The AIOps AI Specialist is ServiceNow's purpose-built AI agent for IT Operations. It autonomously monitors, triages, and resolves infrastructure and application alerts, executing the full NOC workflow without requiring human intervention on every event. In this release, the AI Specialist can:
    -   Automatically pick up alerts based on configurable scope and filter rules
    -   Run alert analysis, investigation, and impact assessment autonomously
    -   Collaborate with the SRE Agent for deep-level investigation using A2A integration with observability tools and hyperscalers
    -   Hand off to a remediation agent to execute subflow-based fixes
    -   Close alerts determined to be insignificant noise
    -   Be triggered manually by assigning an alert directly to the AI Worker user
-   Onboarding Experience for the AIOps AI Specialist - A guided setup flow helps NOC team managers configure and activate the AI Specialist quickly and consistently.
-   Remediation Agent - A new remediation agent works alongside the AIOps AI Specialist to automatically identify and execute the appropriate remediation subflow for an alert.
-   Proactive Grouping Recommendations - Alert Assist now proactively analyzes incoming alerts and recommends grouping candidates before a NOC operator opens a case. The engine uses intelligent field selection to identify the most relevant alert attributes, supports all LLM types, and handles high-cardinality and verbose alert data gracefully. Recommendations are refreshed every 5 minutes via a scheduled job.
-   AI Resolution Attribution - When the AIOps AI Specialist closes an alert, the system records it as "Closed by AI," capturing which alerts were fully handled autonomously. This enables NOC teams to measure automation rate and track AI-driven closure trends over time.
-   Text to Configuration Agent - Available out of the box, the Text to Configuration Agent allows operators to configure AIOps settings using natural language - no form-filling required.

 Changed:

 -   The AI Worker alert management rule now supports coexistence with autonomous mode.
-   The auto-close path for insignificant noise alerts has been updated for more reliable handling.
-   Autonomous Styled Output now generates a remediation anchor to support downstream remediation workflows.
-   LLM Model Upgrades - Alert Assist skills have been updated to use gpt-4o-mini \(previously gpt-small\) and Claude Haiku 4.5 \(previously claude-small\), improving output quality and aligning with current model availability.

 Fixed:

 -   The AI Investigation Report displayed an infinite loading spinner on timeout.
-   The Regenerate action in the AI Insights card was non-deterministic. The Express List also showed incorrect insight data when the first analysis run failed.
-   The Autonomous Operator was not updating descriptions on individual HLA alerts.
-   Alert Assist was logging unnecessary errors when no related changes passed the relevance threshold.
-   Alert Assist was logging null pointer exceptions during skill availability checks.

</td></tr><tr><td>

Now Assist for Legal Service Delivery

</td><td>

1.8.1

</td><td>

-   New

-   Changed Support for upgraded versions of third party LLMs has been provided.

-   Fixed Legal request and matter summarization now delivers improved accuracy across all supported models

-   Removed


</td></tr><tr><td>

Now Assist for Operational Sustainability

</td><td>

22.3.2

</td><td>

Changed

 - This release includes security enhancements that strengthen access controls across the application.

 Fixed

 - ESG business domain scope and knowledge graph tags for disclosure report - Corrected the ESG business domain scope and updated knowledge graph tags for the ESG disclosure report to ensure accurate AI-assisted content generation.

</td></tr><tr><td>

Now Assist for Order Management

</td><td>

2.2.1

</td><td>

- Automate the end-to-end creation, validation, and resolution of order exception cases on the Business Portal for Expedite, Additional Quantity, and Ship to Different Location requests.- Capture customer inputs in the Virtual Agent, extract intent and values inline, validate them against inventory, availability, location, and unit-of-measure rules, and confirm with the customer before acting.- Run a pricing threshold check and, when required, generate a quote for customer approval before resolving the case and updating case lines to Resolved.- Hand off seamlessly to a live agent at any failure or rejection point, with full conversation context, case number, and a clickable case link in NAVA preserved.

</td></tr><tr><td>

Now Assist for Platform

</td><td>

12.0.0

</td><td>

Updated App/Plugin dependencies

</td></tr><tr><td>

Now Assist for Platform Advanced

</td><td>

2.0.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

Now Assist for Platform Foundation

</td><td>

2.0.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

Now Assist for Platform Prime

</td><td>

2.0.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

22.3.1

</td><td>

-   New

    -   Implemented meta data changes to enable AI native support to all the skills and agents on regulatory change management product.
    -   All the plugin dependency and role changes to enable AI Native capabilities are implemented as part of this application.
-   Changed

The Now Assist issue summarization skill includes new configuration records offering descriptions and guides for configuration and prompt customization, enhancing the administrator and end-user experience without requiring upgrade actions.


</td></tr><tr><td>

Now Assist for Prompt Assistance

</td><td>

5.0.4

</td><td>

New: -   Customers will be able to view latency numbers in evaluation run reports \(Agentic Evaluation\). Two latency scores will be available:
    -   Total session time: Measures the complete end-to-end task duration, including AI processing, tool usage, and user input delays.
    -   Agent processing time: Captures the time the AI agent spends working on the task, not counting user delays or waiting.
-   Agent Instruction Optimization - added support for the latest third-party \(3P\) models, Hierarchical Agents, and Voice Agents.
-   'Suggested Fixes' in Agentic Evaluation - added support for Hierarchical Agents.
-   Added Skill Group capability to update LLM providers across all Agentic Judges simultaneously through Now Assist Admin.

 Changed

-   Modified Overall Task Completeness evaluation for improved evaluation accuracy.
-   Agent Instruction Optimization - Enhanced gatekeeping mechanisms for AIO Log Analyzer, Agent Instruction Generator, Tool Description Generator

NOTE: These features and additions will be usable within Now Assist Skill Kit &gt; Agentic Evaluation

</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

2.2.2

</td><td>

Multilingual Enhancements

 ICM Case Narrative Ai Agent Support

</td></tr><tr><td>

Now Assist for Purchase Order Management \(POM\)

</td><td>

1.2.0

</td><td>

New:

 The automatic conversion of supplier emails into PO exceptions workflow now supports:

 -   Additional languages, enabling better recognition of non-English supplier communications
-   ERP purchase order IDs, allowing precise matching with purchase order data from enterprise resource planning systems

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

1.1.3

</td><td>

New dependant plugin - Opportunity Management AI Features added.

</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

6.1.2

</td><td>

Fixed

 -   Submitting feedback on AI-generated recommended actions fails for non-admin users \(e.g., analysts\).
-   Correlation Insights - No output for certain CIs.
-   Generate Insights action visible even when Now Assist for Security Incident Response was not installed.

 Changed

 -   Summarization skill enhancement to honor chronological order of events and to give more weightage to recent activity.
-   AI Gradient styling for Correlation Insights and Summarization.

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Smart Assessment Engine

</td><td>

22.3.5

</td><td>

New:

 -   AI-powered response generation
-   Smart Assessment Admin can activate/deactivate this capability at the template category level.
-   Sources considered for response generation using AI
    -   Previous Assessment Analysis: Automatically generates response suggestions by analyzing similar completed assessments either in classic or previous Smart Assessments
    -   Document Intelligence Integration: Extracts relevant information from uploaded documents to suggest assessment responses
-   Custom extension point to control the grounded sources
-   Localization updates

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

8.0.1

</td><td>

New feature:

Entitlement creation error handling - This feature uses AI to suggest resolutions when users upload the standard Excel import template for entitlement creation.

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

10.0.0

</td><td>

New:

 -   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
-   The Savings Opportunity Discovery agentic workflow analyzes contracts, spend data, sourcing pipeline data, and supplier performance on a recurring schedule to automatically identify a prioritized list of savings opportunities. Category managers can review each opportunity in the Now Assist Panel and create a pipeline project or dismiss the opportunity directly from the panel.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.6.1

</td><td>

Non Glide Cobalt Raven ACLs added.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

9.6.0

</td><td>

-   New:
    -   Introduced Project QandA conversational capability to ask questions about your project in natural language and get instant, AI-generated answers directly from the project workspace, without having to manually analyze project data.
    -   Use Portfolio insights to analyze planning items in a portfolio plan for execution delays, delayed starts, planned versus approved date misalignments, and projects at risk. View AI-generated root causes and recommended actions to mitigate identified risks and issues.
-   Changed:
    -   Project insights now includes scope creep as an additional topic and considers work notes at the task level as additional context, providing richer and more actionable project visibility.
    -   Updated formatting for in-app insight widgets to improve readability and presentation within the project workspace.
    -   Project Risk Detection now includes clickable links in AI Rationale for quick navigation to referenced project records. Refined Mitigation plan formatting for a better reading experience.

</td></tr><tr><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

8.0.0

</td><td>

New:

 -   Ability to link emails to the created cases and the supplier records
-   Ability to create assessment templates and error handling while cancelling created assessments

</td></tr><tr><td>

Now Assist for Talent

</td><td>

1.8.2

</td><td>

- Migrated Generate Talking Points and Text to Growth Plan skills to the Mosaic AI framework.- Added Interview Scheduling enhancements.- GenAI evaluation framework: created GenAI MATs and auto-eval runs for Job Requisition Creation and Interview Scheduling agentic flows.

</td></tr><tr><td>

Now Assist for Telecommunications

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

6.0.7

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

Now Assist for Third-Party Risk Management

</td><td>

22.3.2

</td><td>

New

Added skill categorization metadata for improved organization.Changed

Enhanced application visibility by setting private flag to restrict access.Fixed

Resolved duplicate issue recommendations when multiple issues generated for a single question \(PRB2015422\).

</td></tr><tr><td>

Now Assist for Vault

</td><td>

2.1.1

</td><td>

-   Use Now Assist to Vault to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.
-   Surface sensitive data access by users automatically by leveraging Now Assist to configure, audit, and summarize your Access Observer logs.

</td></tr><tr><td>

Now Assist for Voice

</td><td>

5.0.3

</td><td>

New

-   Admins can configure pronunciation dictionaries for voice assistants. Define custom pronunciations for domain-specific and company-specific terms using phonetic spelling or phoneme format. Entries are scoped per language and deployment and applied during voice interactions.
-   AI voice assistants now support SIP call handling. Configure SIP transfer targets and methods, and expose SIP call data for integration with CCaaS providers.
-   Voice deployments support multiple secondary languages with dynamic selection prompts. APIs return translated prompts, welcome messages, and tool execution text for all configured secondary languages. Language selection prompts are generated dynamically based on available languages and trigger phrases.
-   Russian, Danish, and Turkish voice options are now available. Each language includes male and female voice options for different conversational contexts.
-   New deployment attributes are available for advanced voice configuration. Configure noise suppression levels, orchestration and gateway modes, and selectively disable authentication flows for specific deployments.
-   Filler message delay is now configurable per deployment. The default is 15 seconds. Set the wait time before filler words are spoken during processing-intensive operations to control conversational pacing.
-   Voice assistants now support PSTN request processing. The system selects the appropriate request processor based on the active communication channel, enabling PSTN alongside existing providers.

Changed

-   Voice analytics dashboard now organises performance metrics across four tabs - Overview, Performance, Insights, and Assist consumption - with new metrics for resolution rate, authentication performance, tool execution, conversation sentiment signals, and AI agent assist consumption.
-   execute\_tool and execute\_tool\_guest API responses now include execution plan and task identifiers. Use these identifiers to track and troubleshoot tool executions.
-   Voice language configurations can now be deleted across application scopes. Only voice admins have permission to delete configurations from other scopes.
-   Execution latency metrics are now captured for agent evaluation. The system records execution time data for voice agent plans to support performance analysis.

Fixed

Corrected language selection prompts for secondary languages to align with voice-based language selection behavior.Removed

None

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data - across all types of findings within USEM.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.13

</td><td>

-   New

None

-   Changed

None

-   Fixed

None

-   Removed

None


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

17.0.7

</td><td>

Changed

Suggestion readers are now mapped automatically when Premium Chat is enabled for global search, a workspace, or a service portal, so suggested content surfaces without additional setup.Fixed

-   Resolved an issue that prevented hybrid search from being enabled for some search application configurations.
-   Suggested Utterances now carry over correctly when a portal is upgraded to Premium.

</td></tr><tr><td>

Now Assist in Catalog Builder

</td><td>

7.2.0

</td><td>

Made minor enhancements.

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

2.2.1

</td><td>

-   New

-   Changed

    -   Identify missing clauses in contract revisions with improved accuracy.
    -   Support for upgraded versions of third party LLMs has been provided.
-   Fixed

    -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
    -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.
-   Removed


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

6.1.2

</td><td>

Changed

 -   Updated default model configuration per ServiceNow platform guidance
-   Removed UI bounding box visualization feature to resolve node restart issues caused by memory contention during candidate mapping

 Fixed

 -   Removed the legacy "enable\_multimodal" key in the configuration
-   Extracted field values returning "empty" instead of "missing in document" when no value is found in the source document

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.1.0

</td><td>

No new features are added as part of this release.

</td></tr><tr><td>

Now Assist in Knowledge Management

</td><td>

30.10.3

</td><td>

Knowledge generation capabilities through Now Assist panel and in-product

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.1.0

</td><td>

Use the Standard Ticket Summary Fields related list to configure summary fields on the standard ticket page such that the page displays the Summarize button, enabling requesters to view Now Assist-generated overviews of recent ticket activity and details.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

19.0.10

</td><td>

New

 -   Premium Chat available for portal, mobile, and Microsoft Teams. Options reflect configurations and AI Search status. Enable/disable per channel. Not for guest users; Virtual Agent notifications are not yet supported.
-   Voice input toggle at the assistant level for premium chat. End users activate it in preferences.
-   Unlimited asset promotion. Assets appear as pills in standard/enhanced chat, suggested topics in premium chat.
-   Configure greeting and fallbacks for premium chat using OOB scripts, static text, or topics. Legacy configs pre-filled on upgrade.
-   Mobile chat embed supports theming, analytics, and record context via URL parameters.
-   Toggle contextual suggestions in Now Assist panel for autosuggest and homepage.
-   Inactivity timeout max now 300 seconds.
-   Banner alerts when premium chat setup in progress.
-   'All assets' view in assistant edit flow with empty state handling.
-   Only active assets can be promoted; inactive assets are hidden from tables.

 Changed

 -   Display experience config updated for portals/mobile-reflects customer type, configuration and AI Search status. CSM portals restrict certain experiences.
-   Premium chat logic revised for mobile/portal. Custom apps option removed.
-   Tooltips updated for conversational catalog Items-clarify parity gaps and form interactions.

 Fixed

 -   Catalog auto-start with sources PRB2013012
-   Skill selection recording PRB2006757
-   Zero-result timeouts PRB2017263
-   Voice setup mobile-only PRB1987951
-   Enhanced chat end response PRB1994560
-   Premium chat upgrade greeting/fallback PRB2028521
-   CSM portal external user PRB2023644
-   Duplicate Now Assist panel channels PRB2026739
-   Asset tab refresh and add card PRB2029087
-   Asset ordering and unsupported types PRB2028691
-   Review tab details PRB2028587
-   Chat menu items PRB2014288
-   Provider unlinking PRB2026631
-   Missing sources PRB2009215
-   Voice tags PRB2019586
-   Empty secondary language save PRB2024758
-   Config attribute removal on channel save PRB2025395
-   Genesys/3CLogic URLs PRB2023611
-   Localization strings PRB2025243
-   Amazon Connect PSTN block PRB2021363
-   Genesys API Key switching PRB2021070
-   Test button UI PRB2017785
-   Tag addition PRB2016968
-   AI Agent modal button PRB2017769
-   Orphaned deployment configs PRB2011804
-   External sources URL PRB2008332
-   Learn more URL PRB2018834
-   Search profile rename PRB2006849
-   cloud\_document\_enabled default PRB2018953
-   Zero genius results handling PRB2010786
-   Branding menu items PRB2018544
-   Channel save PRB2023061
-   BT1 pipeline PRB2022683
-   Databroker URI PRB2016144
-   Branding menu items PRB2016228
-   upgradeAISApp check PRB2016713
-   Designer UI PRB1988383
-   Zero query attribute PRB2029160

 Removed

 -   'sn\_nowassist\_va.enable\_nap\_aix\_experience' property
-   Custom PSTN
-   Premium chat for custom apps mobile
-   Inactive asset promotion

</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

3.0.3

</td><td>

- Added an agentic workflow for servicenow table record navigation

 - Support for Visual and Doc Qna

</td></tr><tr><td>

Now Assist Service Quality

</td><td>

1.1.1

</td><td>

New:

Auto QA Breakdown DashboardChanged:

-   UX improvements
-   Functional improvements in Admin UI

Fixed:

UI Fixes related to data visualization

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

10.1.1

</td><td>

Fixed

 -   Fixed an issue where the system got stuck in a loop during sensitive detection in topic execution.
-   Restored missing code required for conversational testing.
-   Fixed an issue where entity scoring ignored the label for reference choice fields.
-   Corrected a mismatch where DateTime values were not displayed in the selected format.
-   Fixed a looping issue where the Virtual Agent kept asking the same question despite receiving a user response.
-   Improved the slot-filling prompt to better handle relative date inputs \(e.g., tomorrow, next week\).

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

9.0.4

</td><td>

Ability to evaluate agentic voice assistant and the agents within it.

 -   Evaluate standalone voice agents and voice assistants independently.
-   Select out-of-the-box evaluation metrics.
-   Use multiple forms of data input for evaluation, including file upload, synthetic generation, and manual entry.
-   View evaluation results at both aggregate and individual scenario levels.

 Ability to view the following latency numbers in evaluation run reports -

 -   Total session time: Measures the complete end-to-end task duration, including AI processing, tool usage, and user input delays.
-   Agent processing time: Captures the time the AI agent spends working on the task, not counting user delays or waiting.

</td></tr><tr><td>

Operational Sustainability Management Advanced

</td><td>

22.3.1

</td><td>

Changed

 - Updated metadata for OSM AI Advanced - Application metadata has been updated to reflect current AI capabilities and configurations.

</td></tr><tr><td>

Opportunity Management AI Features

</td><td>

1.0.3

</td><td>

New

 -   Manage CRM records conversationally - create, view, and update opportunities, contacts, leads, tasks, and accounts using natural language via a conversational interface. Use your MCP client to connect to the Sales CRM MCP server.
-   Get AI-generated summaries of opportunity activity, bringing together emails, tasks, meetings, and product details without manual review.

</td></tr><tr><td>

OT Manager Foundation

</td><td>

3.3.3

</td><td>

New Certified for Australia Patch 3

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

13.0.8

</td><td>

New:

 -   Agentic workflow to pro-actively identify escalations. The workflow evaluates various parameters like time remaining for SLA, urgency, priority, impact etc. to provides an escalation label \(Critical, High, Medium\) and reason for escalation.
-   Skill to predict the next action including attaching relevant KBs, inking cases to Problem tickets, and updating form fields based on record context.
-   Quick Wins skill that leverages an LLM to analyze task details-including descriptions, short descriptions, journal fields, relevant KBs, and past resolution notes-to determine if a task qualifies as a quick win
-   Skill editing capabilities in NASK, providing a consistent editing experience across NAA and NASK
-   Citations feature for summarization is now ready for uptake

 Changed:

 -   Ability to filter on additional fields from record table \(Asst group, Service, CI\) for Analyze Task Trends
-   Update Resolution notes activity filtering to include ai activity \(include\_ai\_updates\) config
-   Updates to Citations to include related records
-   Filter on additional params from record table for IWIS
-   Summary of the generated work plan
-   Auto classification of records GAF and config for Analyze task trends

</td></tr><tr><td>

POM - Foundation

</td><td>

1.1.2

</td><td>

Purchase Order Management - Foundation is the foundation-tier AI subscription for purchase order exception management on the ServiceNow AI Platform. Extending Now Assist for Purchase Order Management, this offering unlocks Platform Foundation features for enterprises that require the most advanced AI capabilities across their purchase order exception workflows. Purchase Order Management - Foundation adds access to Now Assist Platform Foundation, enabling organizations to take advantage of the latest platform-level AI innovations as they become available.

</td></tr><tr><td>

POM - Prime

</td><td>

1.1.1

</td><td>

New: Enhancement to the automatic conversion of supplier emails into PO Exception cases, now supporting additional languages and ERP purchase order IDs for improved PO identification.

</td></tr><tr><td>

Privacy Management Advanced

</td><td>

22.3.1

</td><td>

-   New

    -   Implemented meta data changes to enable AI native support to all the skills and agents on privacy management product.
    -   All the plugin dependency and role changes to enable AI Native capabilities are implemented as part of this application.
-   Changed The Now Assist issue summarization skill includes new configuration records offering descriptions and guides for configuration and prompt customization, enhancing the administrator and end-user experience without requiring upgrade actions.


</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.3.1

</td><td>

Multilingual Enhancements

 ICM Case Refinement Agent

</td></tr><tr><td>

Query Generation

</td><td>

6.0.0

</td><td>

New

 Support Extended Fields

 Mosaic initiative

</td></tr><tr><td>

Query Orchestrator

</td><td>

1.1.0

</td><td>

New: -   Added new KG Query Decomposer Skill
-   Added Execute compound query on KG and KB Subflow

</td></tr><tr><td>

Recommendation template

</td><td>

22.3.1

</td><td>

Changed

Query range ACL's -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
-   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
-   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.

</td></tr><tr><td>

Recommended Actions for Security Operations

</td><td>

2.2.1

</td><td>

Changed Updated the Query range ACL.

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Prime

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Prime

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Security Incident Response - Advanced

</td><td>

1.0.7

</td><td>

Changed Updated the dependency version.

</td></tr><tr><td>

Security Incident Response - Foundation

</td><td>

1.0.7

</td><td>

Changed Updated the dependency version.

</td></tr><tr><td>

Security Incident Response - Prime

</td><td>

1.0.7

</td><td>

Changed Updated the dependency version.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

6.0.1

</td><td>

-   New Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables: auto-map Excel column headers to ServiceNow table fields, auto-map Excel choice column values to ServiceNow choice field values, and auto-map Excel reference column values to ServiceNow reference field values.

-   Changed ServiceNow AI Lens now uses visual gradient indicators to distinguish AI-filled form fields from manually entered data.

-   Fixed

-   Removed


</td></tr><tr><td>

SLO - Foundation

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

SLO - Prime

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

Software Asset Management AI Advanced

</td><td>

2.0.1

</td><td>

New feature: Entitlement creation error handling - This feature uses AI to suggest resolutions when users upload the standard Excel import template for entitlement creation.

</td></tr><tr><td>

Software Asset Management AI Prime

</td><td>

2.0.1

</td><td>

New feature: Entitlement creation error handling - This feature uses AI to suggest resolutions when users upload the standard Excel import template for entitlement creation.

</td></tr><tr><td>

SPO - Foundation

</td><td>

1.2.0

</td><td>

Changed: Updated application and plugin dependencies to ensure correct installation sequencing and compatibility.

</td></tr><tr><td>

SPO - Prime

</td><td>

1.2.0

</td><td>

Changed: Updated application and plugin dependencies to ensure correct installation sequencing and compatibility.

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New:

 -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
-   Users can upload images or diagrams which contain a process flow/flow diagram. The Template AI agent reads these documents and analyzes the template and template items required.
-   The Template ai agent creates a draft template along with template items based on the document and provides draft template details which are verified by the user.

</td></tr><tr><td>

Technology Advanced

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Technology Foundation

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Technology Prime

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications Advanced

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Foundation

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Media and Technology AI agent collection

</td><td>

6.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Prime

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications, Media and Technology - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications, Media and Technology - Foundation

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications, Media and Technology - Prime

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Third-party Risk Management Advanced

</td><td>

22.3.2

</td><td>

New Added skill categorization metadata for improved organization.

 Fixed Resolved duplicate issue recommendations when multiple issues generated for a single question \(PRB2015422\).

</td></tr><tr><td>

Third-party Risk Management Professional Plus

</td><td>

22.3.2

</td><td>

New Added skill categorization metadata for improved organization.

 Fixed Resolved duplicate issue recommendations when multiple issues generated for a single question \(PRB2015422\).

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data - across all types of findings within USEM.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Foundation

</td><td>

2.0.0

</td><td>

No new features with this release. Updated the application to support bundling with other USEM applications.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Prime

</td><td>

2.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data - across all types of findings within USEM.

</td></tr><tr><td>

Universal Request AI agent collection

</td><td>

1.0.9

</td><td>

Fixed minor system defects

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.4.0

</td><td>

Resolved an installation issue that prevented Voice Input from activating correctly on some instances.

</td></tr><tr><td>

WSD - Advanced

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

WSD - Foundation

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

WSD - Prime

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.3.2|2026-06-16|
|Agentic Contact Center for Banking|1.3.0|2026-06-16|
|Agentic Contact Center for Insurance|1.1.0|2026-06-16|
|AI Agent Advisor|1.2.2|2026-07-09|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.9.0|2026-06-16|
|AI Agents for Customer Success Management|2.7.4|2026-06-16|
|AI Agents for Discovery|3.0.0|2026-06-16|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.1|2026-06-16|
|AI Agents for Health and Safety|1.3.3|2026-06-16|
|AI Agents for ITAM|4.3.0|2026-06-16|
|AI agents for Observability|6.0.5|2026-06-16|
|AI Agents for Service Exchange Provider|1.1.4|2026-07-09|
|AI agents for SLO|2.0.3|2026-06-16|
|AI agents for Synthetic Monitoring|1.2.2|2026-06-16|
|AI Agents for Workplace Service Delivery|3.3.1|2026-06-16|
|AI Control Tower for Enterprise AI Foundation|1.1.1|2026-06-16|
|AI Control Tower for Now Assist|4.0.0|2026-06-16|
|AI Dashboard Insights|1.2.3|2026-07-09|
|AI Data Explorer|5.0.8|2026-06-16|
|AI Desktop Actions|4.0.1|2026-06-16|
|AI Enhanced Recommended Actions|1.0.2|2026-05-05|
|AI Experience Framework Skills|1.2.0|2026-07-09|
|AI for document designer|22.3.4|2026-06-16|
|AI Search RAG|6.1.0|2026-06-16|
|AI Websearch|4.1.0|2026-06-16|
|AIOps Agentic Workforce|2.0.1|2026-06-16|
|Alert Assist|3.9.3|2026-06-16|
|Amazon Bedrock Spoke|1.5.0|2026-06-16|
|Analytics Generation|4.1.10|2026-06-16|
|APO - Foundation|1.2.0|2026-06-16|
|APO - Prime|1.2.0|2026-06-16|
|App Engine - Prime|29.1.5|2026-06-16|
|App Generation|28.3.11|2025-12-11|
|App Life Cycle AI Agents|29.3.1|2026-06-16|
|App Summary|29.3.1|2026-06-16|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Build Agent Premium|1.3.1|2026-06-16|
|Business Continuity Management Advanced|1.1.3|2026-06-16|
|Business Continuity Management Foundation|1.1.3|2026-06-16|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Chat Recommendation|1.8.2|2026-06-16|
|Chat Summarization for Virtual Agent|1.11.3|2026-06-16|
|Collaborative Work Management - Advanced|2.0.3|2026-06-16|
|Common AI Framework|1.0.1|2026-06-16|
|Complaint Case AI Agents collection|1.4.1|2026-06-16|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Contract Management Pro - Prime|1.0.9|2026-06-16|
|Conversation Evaluator|3.0.4|2026-06-16|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|9.0.3|2026-06-16|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Core Business Suite|3.2.7|2026-07-09|
|Core Business Suite Advanced|3.0.7|2026-07-09|
|Core Business Suite Advanced for Finance|3.0.7|2026-07-09|
|Core Business Suite Advanced for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Advanced for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Advanced for Legal|3.0.7|2026-07-09|
|Core Business Suite Advanced for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Advanced for Workplace Services|3.0.7|2026-07-09|
|Core Business Suite AI Agent|3.2.7|2026-07-09|
|Core Business Suite for Finance|3.2.7|2026-07-09|
|Core Business Suite for Health and Safety|3.2.7|2026-07-09|
|Core Business Suite for Human Resources|3.2.7|2026-07-09|
|Core Business Suite for Legal|3.2.7|2026-07-09|
|Core Business Suite For Source To Pay|3.2.7|2026-07-09|
|Core Business Suite For Workplace Service Delivery|3.2.7|2026-07-09|
|Core Business Suite Foundation|3.0.7|2026-07-09|
|Core Business Suite Foundation for Finance|3.0.7|2026-07-09|
|Core Business Suite Foundation for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Foundation for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Foundation for Legal|3.0.7|2026-07-09|
|Core Business Suite Foundation for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Foundation for Workplace Services|3.0.7|2026-07-09|
|Core Business Suite Prime|3.0.7|2026-07-09|
|Core Business Suite Prime for Finance|3.0.7|2026-07-09|
|Core Business Suite Prime for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Prime for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Prime for Legal|3.0.7|2026-07-09|
|Core Business Suite Prime for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Prime for Workplace Services|3.0.7|2026-07-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|1.2.0|2026-07-09|
|CPQ for Manufacturing Foundation|1.2.0|2026-07-09|
|CSM - Advanced|1.0.0|2026-04-09|
|CSM - Foundation|1.0.0|2026-04-09|
|CSM - Prime|1.0.0|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.2.2|2026-06-16|
|Customer Service Management AI agent collection|6.0.3|2026-06-16|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DCNAM - Advanced|2.0.2|2026-07-09|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Dynamic Guidance|28.3.2|2026-06-16|
|Employee Slate for Now Assist|1.2.0|2026-07-09|
|Enhanced Features for IRM Enterprise|22.3.4|2026-06-16|
|Enhanced Features for IRM Professional|22.3.3|2026-06-16|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|External content connectors - Now assist agent|1.1.1|2026-06-16|
|Field Service Management AI agent collection|3.0.1|2026-06-16|
|Financial Services Operations AI agent collection|4.1.0|2026-06-16|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Form data collector|2.0.1|2026-04-09|
|FSC Common - Foundation|1.2.0|2026-06-16|
|FSC Common - Prime|1.2.0|2026-06-16|
|FSM - Advanced|2.0.1|2026-06-16|
|FSM - Foundation|2.0.1|2026-06-16|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Generative AI Controller|14.0.1|2026-06-16|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.3.4|2026-06-16|
|GRC Shared GenAI|22.3.1|2026-06-16|
|Group-Action Framework|7.0.1|2026-06-16|
|Hardware Asset Management - Advanced|1.0.1|2026-06-16|
|HCLS - Advanced|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|Health and Safety - Advanced|1.0.4|2026-05-05|
|Health and Safety - Foundation|1.0.4|2026-05-05|
|Health and Safety - Prime|1.0.4|2026-05-05|
|HR Service Delivery AI agent collection|7.0.2|2026-06-16|
|HR Talent AI Agent Collection|5.0.2|2026-06-16|
|HR Voice AI Agents|2.3.6|2026-06-16|
|HRSD - Advanced|2.0.2|2026-06-16|
|HRSD - Foundation|2.0.2|2026-06-16|
|HRSD - Prime|2.0.2|2026-06-16|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Industrial Control Tower Advanced|1.0.0|2026-06-16|
|Industrial Control Tower Foundation|1.0.0|2026-06-16|
|Industrial Control Tower Prime|1.0.0|2026-06-16|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Prime|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Insights Clustering Utils|3.2.2|2026-07-09|
|Integrated Risk Management Advanced|22.3.3|2026-06-16|
|Integrated Risk Management Foundation|22.3.2|2026-06-16|
|Integrated Risk Management Prime|22.3.3|2026-06-16|
|IRM Compliance GenAI|22.3.1|2026-06-16|
|IRM Risk GenAI|22.3.2|2026-06-16|
|IT Service Management|3.0.2|2026-06-16|
|IT Service Management Advanced|3.0.1|2026-06-16|
|IT Service Management AI agent collection|9.1.1|2026-07-09|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|ITOM - Advanced|1.0.10|2026-06-16|
|ITOM - Prime|1.0.6|2026-06-16|
|ITOM AI Agents For Service Mapping|1.3.2|2026-06-16|
|ITSM - Advanced|2.1.2|2026-07-09|
|ITSM - Foundation|2.1.2|2026-07-09|
|ITSM - Prime|2.1.2|2026-07-09|
|Knowledge Center|31.10.8|2026-06-16|
|Knowledge Graph|8.0.0|2026-06-16|
|LEAP|4.0.0|2026-06-16|
|Legal Service Delivery - Prime|1.0.9|2026-06-16|
|List AI Experience|3.0.0|2026-06-16|
|Manage Invoice Operations|1.1.0|2026-06-16|
|Manage Order Operations|2.0.3|2026-06-16|
|Manufacturing Commercial Operations Advanced|1.2.0|2026-07-09|
|Manufacturing Commercial Operations AI agents collection|2.3.0|2026-07-09|
|Manufacturing Commercial Operations Foundation|1.2.0|2026-07-09|
|Manufacturing Commercial Operations Prime|1.2.0|2026-07-09|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Metadata Search|1.0.11|2026-05-05|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.0|2026-06-16|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.5.0|2026-06-16|
|Model Context Protocol Client|2.2.0|2026-06-16|
|Model Context Protocol Server|1.5.1|2026-06-16|
|Notifications Email Agents|2.1.1|2026-06-16|
|Now Assist Admin Console|10.0.12|2026-07-02|
|Now Assist Agents for requestor|3.5.0|2026-06-16|
|Now Assist AI Agents|8.0.12|2026-07-04|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|31.0.5|2026-06-16|
|Now Assist Analytics|5.0.3|2026-06-16|
|Now Assist Center|4.0.2|2026-06-16|
|Now Assist context menu|3.6.4|2026-06-16|
|Now Assist Data Kit|8.0.4|2026-06-16|
|Now Assist for Accounts Payable Operations \(APO\)|8.0.0|2026-06-16|
|Now Assist for Advanced Work Assignment \(AWA\)|1.0.3|2026-06-16|
|Now Assist for App Engine|29.2.3|2026-06-16|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for code generation|28.5.23|2026-06-16|
|Now Assist for Collaborative Work Management \(CWM\)|6.0.1|2026-06-16|
|Now Assist for Complaint Case \(CSM\)|2.1.5|2026-06-16|
|Now Assist for Configuration Management Database \(CMDB\)|3.8.0|2026-06-16|
|Now Assist for Contract Analysis|1.0.9|2026-06-16|
|Now Assist For Core Business Suite|3.2.7|2026-07-09|
|Now Assist for CPQ|1.0.5|2026-07-09|
|Now Assist for Creator|29.2.5|2026-06-16|
|Now Assist for CSM Major Issue Management|1.1.0|2026-07-09|
|Now Assist for Digital End-user Experience \(DEX\)|4.3.0|2026-06-16|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.3.2|2026-06-16|
|Now Assist for Enterprise Architecture \(EA\)|7.3.1|2026-06-16|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for Error Framework|1.0.3|2026-06-16|
|Now Assist for Field Service Management \(FSM\)|10.0.1|2026-06-16|
|Now Assist for Financial Services Operations \(FSO\)|3.2.0|2026-06-16|
|Now Assist for FSC Common|7.0.0|2026-06-16|
|Now Assist for Hardware Asset Management|4.3.0|2026-06-16|
|Now Assist for Health and Safety|1.4.1|2026-06-16|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.2.3|2026-06-16|
|Now Assist for ICW|1.0.0|2026-05-05|
|Now Assist for Impact|4.0.5|2026-06-16|
|Now Assist for IRM|22.3.3|2026-06-16|
|Now Assist for IT Operations Management \(ITOM\)|2.6.16|2026-06-16|
|Now Assist for IT Service Management \(ITSM\)|15.1.2|2026-07-09|
|Now Assist for Legal Service Delivery|1.8.1|2026-06-16|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.3.0|2026-07-09|
|Now Assist for Operational Sustainability|22.3.2|2026-06-16|
|Now Assist for Order Management|2.2.1|2026-06-16|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|12.0.0|2026-06-16|
|Now Assist for Platform Advanced|2.0.0|2026-06-16|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Platform Foundation|2.0.0|2026-06-16|
|Now Assist for Platform Prime|2.0.0|2026-06-16|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.3.1|2026-06-16|
|Now Assist for Process Mining|3.0.12|2026-05-05|
|Now Assist for Prompt Assistance|5.0.4|2026-06-16|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.2.2|2026-06-16|
|Now Assist for Purchase Order Management \(POM\)|1.2.0|2026-06-16|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for Sales and Order Management for Telecommunications|4.1.2|2026-07-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.3|2026-06-16|
|Now Assist for Security Incident Response \(SIR\)|6.1.2|2026-06-16|
|Now Assist for Security Incident Response integrations|1.2.1|2026-06-16|
|Now Assist for Service Exchange|1.1.4|2026-07-09|
|Now Assist for Setup|3.1.4|2026-07-09|
|Now Assist for Setup Core|2.1.5|2026-07-09|
|Now Assist for Smart Assessment Engine|22.3.5|2026-06-16|
|Now Assist for Software Asset Management \(SAM\)|8.0.1|2026-06-16|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|10.0.0|2026-06-16|
|Now Assist for Spoke Generation|1.6.1|2026-06-16|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.6.0|2026-06-16|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|8.0.0|2026-06-16|
|Now Assist for Talent|1.8.2|2026-06-16|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.7|2026-06-16|
|Now Assist for Third-Party Risk Management|22.3.2|2026-06-16|
|Now Assist for Threat Intelligence Security Center|2.2.0|2026-07-09|
|Now Assist for Vault|2.1.1|2026-06-16|
|Now Assist for Voice|5.0.3|2026-06-16|
|Now Assist for Vulnerability Response|5.0.0|2026-06-16|
|Now Assist for WDF|2.1.4|2026-07-09|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.13|2026-06-16|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in AI Search|17.0.7|2026-06-16|
|Now Assist in Catalog Builder|7.2.0|2026-06-16|
|Now Assist in Catalog item forms|1.3.2|2026-05-05|
|Now Assist in Contract Management|2.2.1|2026-06-16|
|Now Assist in Conversational Catalog Request|7.0.2|2026-05-05|
|Now Assist in Document Intelligence|6.1.2|2026-06-16|
|Now Assist in Document Management|2.1.0|2026-06-16|
|Now Assist in Knowledge Management|30.10.3|2026-06-16|
|Now Assist in Standard Ticket Page|1.1.0|2026-06-16|
|Now Assist in Virtual Agent|19.0.10|2026-06-16|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|3.0.3|2026-06-16|
|Now Assist Service Quality|1.1.1|2026-06-16|
|Now Assist Skill Discovery and Execution|10.1.1|2026-06-16|
|Now Assist Skill Kit|9.0.4|2026-06-16|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|22.3.1|2026-06-16|
|Opportunity Management AI Features|1.0.3|2026-06-16|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Platform AI Agents and Skills|13.0.8|2026-06-16|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.1.1|2026-06-16|
|Privacy Management Advanced|22.3.1|2026-06-16|
|prompt-management|1.0.11|2026-03-12|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|1.3.1|2026-06-16|
|Query Generation|6.0.0|2026-06-16|
|Query Orchestrator|1.1.0|2026-06-16|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.3.1|2026-06-16|
|Recommended Actions for Security Operations|2.2.1|2026-06-16|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|Sales and Order Management for Technology Provider - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Technology Provider - Prime|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications - Advanced|2.1.2|2026-07-09|
|Sales and Order Management for Telecommunications - Prime|2.1.2|2026-07-09|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.4|2026-06-16|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.11|2026-05-05|
|Security Incident Response - Advanced|1.0.7|2026-06-16|
|Security Incident Response - Foundation|1.0.7|2026-06-16|
|Security Incident Response - Prime|1.0.7|2026-06-16|
|Service Exchange - Advanced|1.1.4|2026-07-09|
|Service Exchange - Foundation|1.1.4|2026-07-09|
|Service Exchange - Prime|1.1.4|2026-07-09|
|ServiceNow AI Lens|6.0.1|2026-06-16|
|SLO - Foundation|1.2.0|2026-06-16|
|SLO - Prime|1.2.0|2026-06-16|
|Software Asset Management AI Advanced|2.0.1|2026-06-16|
|Software Asset Management AI Prime|2.0.1|2026-06-16|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SOM for Manufacturing Advanced|1.2.0|2026-07-09|
|SOM for Manufacturing Prime|1.2.0|2026-07-09|
|SPO - Foundation|1.2.0|2026-06-16|
|SPO - Prime|1.2.0|2026-06-16|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Technology Advanced|1.0.4|2026-06-16|
|Technology Foundation|1.0.4|2026-06-16|
|Technology Prime|1.0.4|2026-06-16|
|Telecommunications Advanced|2.0.1|2026-06-16|
|Telecommunications Foundation|2.0.1|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecommunications Prime|2.0.1|2026-06-16|
|Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Telecommunications, Media and Technology - Foundation|1.0.4|2026-06-16|
|Telecommunications, Media and Technology - Prime|1.0.3|2026-06-16|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Management Advanced|22.3.2|2026-06-16|
|Third-party Risk Management Professional Plus|22.3.2|2026-06-16|
|Threat Intelligence Security Center - Advanced|3.0.1|2026-07-09|
|TNI - Advanced|2.0.2|2026-07-09|
|TNI and DCNAM AI Content Collection|2.0.1|2026-07-09|
|TSOM - Advanced|2.0.2|2026-07-09|
|TSOM - Prime|2.0.1|2026-07-09|
|UI Generation|29.2.5|2026-05-05|
|Unified Security Exposure Management \(USEM\) - Advanced|2.0.0|2026-06-16|
|Unified Security Exposure Management \(USEM\) - Foundation|2.0.0|2026-06-16|
|Unified Security Exposure Management \(USEM\) - Prime|2.0.0|2026-06-16|
|Universal Request AI agent collection|1.0.9|2026-06-16|
|Voice input for Now Assist|1.4.0|2026-06-16|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|Zero Copy Connector Hub|3.0.1|2026-03-12|
|Zero Touch Service Desk|2.3.5|2026-07-09|

## Suite version 29.4.20260716 - Australia Patch 4

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

3.4.8

</td><td>

Includes a fix to 400 bad request error for the canvas APIs.

</td></tr><tr><td>

Agentic Contact Center for Banking

</td><td>

1.3.0

</td><td>

Changed: Updated dependency from AI Foundation to FSO Now Assist

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.7.4

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.3.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI agents for SLO

</td><td>

2.0.3

</td><td>

New Added a Reliability Domain Agent that analyzes historical, post-incident data to identify service level objective \(SLO\) and synthetic monitoring gaps across configuration items \(CIs\) and services, then generates reliability tasks to address them.

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.3.1

</td><td>

-   New None

-   Changed Workplace Utilization QnA Agent can now be used by users with the sn\_wsd\_spcmgmt.space\_planner role

-   Fixed The AI Agent was not always able to block the location after submitting an emergency maintenance request

-   Removed None


</td></tr><tr><td>

AI for document designer

</td><td>

22.3.4

</td><td>

New

 -   AI for Document Designer - A new AI-powered application that integrates with the Microsoft Word add-in, enabling users to generate and manage report content directly within Word documents using Now Assist.
-   AI-powered Word content generation - A custom AI skill that generates Microsoft Word report content through natural language prompts, allowing users to create document sections conversationally.
-   Content insertion into Word documents - Support for inserting AI-generated content \(HTML and OOXML formats\) directly into Word documents via sn-office-addin handlers.
-   Multi-conversation document editing - Ability to edit and refine document content across multiple conversations with the AI assistant, enabling iterative content development.
-   Data model, ACLs, and roles - Purpose-built data model with access controls and role definitions to secure AI-generated document content and manage user permissions.

 Changed AI agent accuracy and prompt enhancements - Improved agent accuracy and refined prompts based on Architecture Review Board \(ARB\) feedback for higher quality content generation.

 Fixed AI agent icons updated in add-in - Corrected the icons displayed for the AI agent within the Microsoft Word add-in.

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed

 -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed Deprecated searching and scraping functionality.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.5.0

</td><td>

Fixed - Streamline ACLs

</td></tr><tr><td>

APO - Foundation

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies.

</td></tr><tr><td>

APO - Prime

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies.

</td></tr><tr><td>

App Engine - Prime

</td><td>

29.1.5

</td><td>

Changed Updated versions of dependent apps.

</td></tr><tr><td>

App Life Cycle AI Agents

</td><td>

29.3.1

</td><td>

Changed Maintenance release.

</td></tr><tr><td>

Business Continuity Management Advanced

</td><td>

1.1.3

</td><td>

1. AI Agents and skills

 2. Business Continuity management features for impact analysis, business continuity plans, crisis management, and crisis map.

</td></tr><tr><td>

Business Continuity Management Foundation

</td><td>

1.1.3

</td><td>

1. AI Agents and skills

 2. Business Continuity management features for impact analysis, business continuity plans, and crisis management.

</td></tr><tr><td>

Common AI Framework

</td><td>

1.0.1

</td><td>

New:

 AI Framework that autonomously discovers schema, samples, and aggregates live ServiceNow tables, and presents a sourced answer without modifying any data.

</td></tr><tr><td>

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Conversation Insights

</td><td>

3.1.0

</td><td>

-   New: Conversation Insights now supports customers with data sovereignty requirements. The application can be re-enabled for customers using local SKUs, allowing deployment with local conversation insights services.
-   Changed: None
-   Fixed: The assignment of the sn\_aci.insights\_read\_write role to the conv-insights-svc-account user has been corrected to ensure proper handling of inheritance flag information.
-   Removed: None

</td></tr><tr><td>

Conversational Studio

</td><td>

10.0.5

</td><td>

Fixed Errors encountered when migrating over 200 topics from NLU to LLM have been resolved. The migration process now supports chunked processing, resumability, and improved UI feedback. Migration data is decoupled from previous dependencies, batch creation, resume, and cancel actions are now supported.

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

29.2.2

</td><td>

Changed Maintenance release.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

2.0.1

</td><td>

New

 -   Agent renamed to "Vision AI Agent"
-   Requests now routed via the MultiModal Service \(MMS\) to enable more consistent and scalable multimodal processing \(up to 500MB video files\)
-   Improved response quality for Video Workflow use cases
-   Supported video formats: MP4, MOV, WEBM, AVI, MKV, and WMV

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.3.2

</td><td>

Fixed:

 Updated the version for ServiceNow Docs Connector to fix dependency failures

</td></tr><tr><td>

Enterprise Architecture - Advanced

</td><td>

1.0.1

</td><td>

New Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.

</td></tr><tr><td>

Enterprise Architecture - Prime

</td><td>

1.0.1

</td><td>

New

 -   Generate a business process map \(BPM\) diagram in the Enterprise Modeling and Visualization by uploading an image of an existing process diagram.
-   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

3.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to ensure certification and release standards. -   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

Flow Execution Analysis

</td><td>

29.2.8

</td><td>

New

 -   Summarize flow execution details when flow reporting is off.
-   Identify potential causes of flow errors.
-   Resolve flow errors with suggested fixes.

</td></tr><tr><td>

FSC Common - Foundation

</td><td>

1.2.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

FSC Common - Prime

</td><td>

1.2.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

FSM - Advanced

</td><td>

2.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

-   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify features.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

FSM - Foundation

</td><td>

2.0.1

</td><td>

New

 -   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content \(links, code, special characters\).
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins/analysts can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

 Changed

 -   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify that features meet release standards.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

 Fixed : None

 Removed : None

</td></tr><tr><td>

FSM Scheduling AI Agent Collection

</td><td>

1.0.7

</td><td>

Initial release

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

Industrial Control Tower Advanced

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Foundation

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Prime

</td><td>

1.0.0

</td><td>

New Update to include AI native and risk calculator

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.4.0

</td><td>

-   New: n/a
-   Changed Security related enhancements on existing AI Voice agents

-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

Legal Service Delivery - Prime

</td><td>

1.0.9

</td><td>

-   New

-   Changed Support for upgraded versions of third party LLMs has been provided.

-   Fixed Legal request and matter summarization now delivers improved accuracy across all supported models

-   Removed


</td></tr><tr><td>

List AI Experience

</td><td>

3.0.0

</td><td>

AI Filter Assist allows users to define conditions using natural language in an intuitive, dialog-driven interface. This feature helps reduce the cognitive load of building conditions using the traditional condition builder by allowing users to type or speak a prompt that will then create the query needed to filter, sort, or group data.

 This release we fixed two defects in AI Filter Assister where an ACL had a typo in it's script and "Add to existing filters" mode was selectable even though it should be disabled.

</td></tr><tr><td>

Manage Order Operations

</td><td>

2.0.3

</td><td>

New: Automated email notifications for order cases: Send emails when the AI agent opens an order case from a Business Portal chat and when the case is resolved. Closure emails include resolution and quote details, if generated. Voice-created cases don't trigger emails.Scripted extension point for quote thresholds: A scripted extension point to integrate the manage order operations AI agent with your inventory, ERP, and quote systems for quote threshold evaluation. The AI agent generates a quote when a quantity-change request exceeds the configured price threshold. Changed

 -   Order exception support for quantity and shipping location: Customers can request quantity and shipping location updates, along with expedite requests via chat and voice channels.
-   Voice assistant intake for order exceptions: Customers can submit expedite, quantity, and shipping location requests via voice. Requests are captured and converted into order cases for resolution in CSM/FSM Configurable Workspace.
-   Unified extension point for feasibility checks: A single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) validates delivery, quantity, and shipping feasibility, replacing the earlier expedite-only ATP check.
-   Auto-populated account and contact on interactions: Account and Contact fields are populated during chat handoff, giving agents immediate customer context and improving summarization accuracy.
-   AI-generated summaries for agent handoff: Agents receive a concise AI-generated summary instead of full chat history, improving context and productivity.

</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

1.0.2

</td><td>

New:

Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and reason about goals, portfolio plans, and projects. The following tools are available in this release: Tool Description get\_goals Retrieves goals and objectives. generate\_goal\_insights Generates AI-powered insights for goals and targets. get\_portfolio\_plans Retrieves portfolio plans. generate\_portfolio\_insights Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies. get\_projects Retrieves projects. generate\_project\_insights Detects project risks, analyzes status trajectory, and provides recommendations. identify\_project\_risks Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts. get\_ai\_status\_report Generates a RAG \(Red, Amber, Green\) status report across resources, cost, schedule, and scope.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.2.0

</td><td>

Changed

Minor API changes for another app support internally

</td></tr><tr><td>

Now Assist AI Helper - Galileo Inside

</td><td>

2.1.2

</td><td>

This plugin was updated to be compatible with the October version of Now Assist.

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

31.0.5

</td><td>

-   New

-   Changed

    -   Browser tabs that open during goal execution in adaptive desktop actions remain open after the goal completes. Use the keep\_tab\_open system property to turn this behavior on or off. The property is turned on by default.
    -   Adaptive desktop actions is enhanced to improve execution efficiency.
-   Fixed

-   Removed


</td></tr><tr><td>

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

8.0.0

</td><td>

New:

 -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
-   Enhanced workflow to enable requesters to accept/reject the case resolution.

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed AI skill execution is now performed off glide

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

29.2.3

</td><td>

Changed Updated versions of dependent apps.

</td></tr><tr><td>

Now Assist for code generation

</td><td>

28.5.23

</td><td>

Now Assist for code generation features now inherit skill-level ACLs configured in Now Assist Admin, ensuring restricted features are only available to authorized users.

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

4.3.0

</td><td>

\* Changed

 - Engagement tool for DEX agents to obtain employee approval before auto-triggering device actions. This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

4.3.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Error Framework

</td><td>

1.0.3

</td><td>

Initial Release

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

10.0.1

</td><td>

New

-   AI-powered mobile form auto-fill for field technicians. Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
-   Consistent AI visual indicators across applications. AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
-   Parts Debrief automation in NAP and NAVA. Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
-   Expanded AI summarization and knowledge workflows. Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
-   Create work order agent with enhanced persona coverage. System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
-   FSM AI Mandate features available on mobile and workspace. FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
-   Telemetry for AI feature usage. Admins can track AI lens feature usage for FSM use cases.
-   Skill refinement for FSM digital agents. FSM agents enhanced for improved automation and workflow handling.

Changed

-   Broadened test and validation coverage for FSM AI use cases. Testing expanded across mobile/agent/NextWave experiences to certify features.
-   Enhanced automation for AI SKU and agent studio test cases. Remaining automation scenarios completed with monitoring on latest NAP version.
-   Improved parts debrief workflow handling. Better management of edge cases like unrecognized assets and invalid task states.
-   Refined questionnaire answer validation in summarization workflows. Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
-   Performance testing for Q1 deliveries. Testing conducted to ensure system stability and responsiveness.

Fixed

NoneRemoved

None

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

7.0.0

</td><td>

Minor defect fixes

</td></tr><tr><td>

Now Assist for Health and Safety

</td><td>

1.4.1

</td><td>

New: Contextual Action Planner sidebar in the Health and Safety Workspace: Create actions manually or from AI suggestions, and review them in context across incidents, observations, investigations, cases, audits, work permits, risk assessments, meetings, etc.

</td></tr><tr><td>

Now Assist for Impact

</td><td>

4.0.5

</td><td>

Code Fix Agent: Enhanced Error Logging

 When the Code Fix Agent runs into a problem, you will now see a plain-language explanation of what went wrong and what to do next - right on the remediation record. Select the links navigate directly to the relevant error record, so there's no need to hunt through system logs.

</td></tr><tr><td>

Now Assist for Legal Service Delivery

</td><td>

1.8.1

</td><td>

-   New

-   Changed Support for upgraded versions of third party LLMs has been provided.

-   Fixed Legal request and matter summarization now delivers improved accuracy across all supported models

-   Removed


</td></tr><tr><td>

Now Assist for Operational Sustainability

</td><td>

22.3.2

</td><td>

Changed

 - This release includes security enhancements that strengthen access controls across the application.

 Fixed

 - ESG business domain scope and knowledge graph tags for disclosure report - Corrected the ESG business domain scope and updated knowledge graph tags for the ESG disclosure report to ensure accurate AI-assisted content generation.

</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

2.2.2

</td><td>

Multilingual Enhancements

 ICM Case Narrative Ai Agent Support

</td></tr><tr><td>

Now Assist for Purchase Order Management \(POM\)

</td><td>

1.2.0

</td><td>

New:

 The automatic conversion of supplier emails into PO exceptions workflow now supports:

 -   Additional languages, enabling better recognition of non-English supplier communications
-   ERP purchase order IDs, allowing precise matching with purchase order data from enterprise resource planning systems

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed

Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

10.0.0

</td><td>

New:

 -   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
-   The Savings Opportunity Discovery agentic workflow analyzes contracts, spend data, sourcing pipeline data, and supplier performance on a recurring schedule to automatically identify a prioritized list of savings opportunities. Category managers can review each opportunity in the Now Assist Panel and create a pipeline project or dismiss the opportunity directly from the panel.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.6.1

</td><td>

Non Glide Cobalt Raven ACLs added.

</td></tr><tr><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

8.0.0

</td><td>

New:

 -   Ability to link emails to the created cases and the supplier records
-   Ability to create assessment templates and error handling while cancelling created assessments

</td></tr><tr><td>

Now Assist for Telecommunications

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

6.0.7

</td><td>

Mosaic migration done for couple of Skills

 Product Release Content Generator

 Renewal Insight Engine

</td></tr><tr><td>

Now Assist for Vault

</td><td>

2.1.1

</td><td>

-   Use Now Assist to Vault to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.
-   Surface sensitive data access by users automatically by leveraging Now Assist to configure, audit, and summarize your Access Observer logs.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.13

</td><td>

-   New None

-   Changed None

-   Fixed None

-   Removed None


</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

3.0.3

</td><td>

- Added an agentic workflow for servicenow table record navigation

 - Support for Visual and Doc Qna

</td></tr><tr><td>

Operational Sustainability Management Advanced

</td><td>

22.3.1

</td><td>

Changed

 - Updated metadata for OSM AI Advanced - Application metadata has been updated to reflect current AI capabilities and configurations.

</td></tr><tr><td>

OT Manager Foundation

</td><td>

3.3.3

</td><td>

New Certified for Australia Patch 3

</td></tr><tr><td>

POM - Foundation

</td><td>

1.1.2

</td><td>

Purchase Order Management - Foundation is the foundation-tier AI subscription for purchase order exception management on the ServiceNow AI Platform. Extending Now Assist for Purchase Order Management, this offering unlocks Platform Foundation features for enterprises that require the most advanced AI capabilities across their purchase order exception workflows. Purchase Order Management - Foundation adds access to Now Assist Platform Foundation, enabling organizations to take advantage of the latest platform-level AI innovations as they become available.

</td></tr><tr><td>

POM - Prime

</td><td>

1.1.1

</td><td>

New:

Enhancement to the automatic conversion of supplier emails into PO Exception cases, now supporting additional languages and ERP purchase order IDs for improved PO identification.

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.3.1

</td><td>

Multilingual Enhancements

 ICM Case Refinement Agent

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Prime

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Prime

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Security Incident Response - Advanced

</td><td>

1.0.7

</td><td>

Changed

Updated the dependency version.

</td></tr><tr><td>

Security Incident Response - Foundation

</td><td>

1.0.7

</td><td>

Changed

Updated the dependency version.

</td></tr><tr><td>

Security Incident Response - Prime

</td><td>

1.0.7

</td><td>

Changed

Updated the dependency version.

</td></tr><tr><td>

SLO - Foundation

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

SLO - Prime

</td><td>

1.2.0

</td><td>

Updated app/plugin dependencies

</td></tr><tr><td>

SPO - Foundation

</td><td>

1.2.0

</td><td>

Changed: Updated application and plugin dependencies to ensure correct installation sequencing and compatibility.

</td></tr><tr><td>

SPO - Prime

</td><td>

1.2.0

</td><td>

Changed: Updated application and plugin dependencies to ensure correct installation sequencing and compatibility.

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New:

 -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
-   Users can upload images or diagrams which contain a process flow/flow diagram. The Template AI agent reads these documents and analyzes the template and template items required.
-   The Template ai agent creates a draft template along with template items based on the document and provides draft template details which are verified by the user.

</td></tr><tr><td>

Technology Advanced

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Technology Foundation

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Technology Prime

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications Advanced

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Foundation

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Media and Technology AI agent collection

</td><td>

6.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications Prime

</td><td>

2.0.1

</td><td>

New support of 3p models and security fixes

 Small models:Claude Haiku 4.5GPT\_5 miniLarge Models:Claude Sonnet 4.6GPT\_5.4

</td></tr><tr><td>

Telecommunications, Media and Technology - Advanced

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications, Media and Technology - Foundation

</td><td>

1.0.4

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Telecommunications, Media and Technology - Prime

</td><td>

1.0.3

</td><td>

We do not have any changes in this app. Releasing this version as part of bundle

</td></tr><tr><td>

Universal Request AI agent collection

</td><td>

1.0.9

</td><td>

Fixed minor system defects

</td></tr><tr><td>

WSD - Advanced

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

WSD - Foundation

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

WSD - Prime

</td><td>

1.0.2

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|Agentic Contact Center for Banking|1.3.0|2026-06-16|
|Agentic Contact Center for Insurance|1.2.2|2026-07-09|
|AI Agent Advisor|1.2.2|2026-07-09|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.10.0|2026-07-09|
|AI Agents for Customer Success Management|2.7.4|2026-06-16|
|AI Agents for Discovery|3.2.1|2026-07-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.1|2026-06-16|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|AI Agents for ITAM|4.4.0|2026-07-09|
|AI agents for Observability|6.1.4|2026-07-09|
|AI Agents for Service Exchange Provider|1.1.4|2026-07-09|
|AI agents for SLO|2.0.3|2026-06-16|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Workplace Service Delivery|3.3.1|2026-06-16|
|AI Control Tower for Enterprise AI Foundation|1.2.1|2026-07-09|
|AI Control Tower for Now Assist|5.0.2|2026-07-09|
|AI Dashboard Insights|1.2.3|2026-07-09|
|AI Data Explorer|5.1.6|2026-07-09|
|AI Desktop Actions|5.0.1|2026-07-09|
|AI Enhanced Recommended Actions|1.0.3|2026-07-09|
|AI Experience Framework Skills|1.2.0|2026-07-09|
|AI for document designer|22.3.4|2026-06-16|
|AI Help Framework|1.0.6|2026-07-09|
|AI Search RAG|6.1.0|2026-06-16|
|AI Specialists for Security Incident Response|1.0.5|2026-07-09|
|AI Websearch|4.1.0|2026-06-16|
|AIOps Agentic Workforce|2.1.0|2026-07-09|
|Alert Assist|3.10.0|2026-07-09|
|Amazon Bedrock Spoke|1.5.0|2026-06-16|
|Analytics Generation|4.1.15|2026-07-09|
|APO - Foundation|1.2.0|2026-06-16|
|APO - Prime|1.2.0|2026-06-16|
|App Engine - Prime|29.1.5|2026-06-16|
|App Generation|28.3.12|2026-07-09|
|App Life Cycle AI Agents|29.3.1|2026-06-16|
|App Summary|29.4.0|2026-07-09|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Build Agent Premium|1.4.1|2026-07-09|
|Business Continuity Management Advanced|1.1.3|2026-06-16|
|Business Continuity Management Foundation|1.1.3|2026-06-16|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Chat Recommendation|1.8.3|2026-07-09|
|Chat Summarization for Virtual Agent|1.11.4|2026-07-09|
|CMDB MCP Server|1.0.1|2026-07-09|
|Collaborative Work Management - Advanced|2.0.5|2026-07-09|
|Common AI Framework|1.0.1|2026-06-16|
|Complaint Case AI Agents collection|1.4.3|2026-07-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Contract Management Pro - Prime|1.0.11|2026-07-09|
|Conversation Evaluator|3.0.4|2026-06-16|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Conversational Help|2.0.3|2026-03-12|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Core Business Suite|3.2.7|2026-07-09|
|Core Business Suite Advanced|3.0.7|2026-07-09|
|Core Business Suite Advanced for Finance|3.0.7|2026-07-09|
|Core Business Suite Advanced for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Advanced for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Advanced for Legal|3.0.7|2026-07-09|
|Core Business Suite Advanced for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Advanced for Workplace Services|3.0.7|2026-07-09|
|Core Business Suite AI Agent|3.2.7|2026-07-09|
|Core Business Suite for Finance|3.2.7|2026-07-09|
|Core Business Suite for Health and Safety|3.2.7|2026-07-09|
|Core Business Suite for Human Resources|3.2.7|2026-07-09|
|Core Business Suite for Legal|3.2.7|2026-07-09|
|Core Business Suite For Source To Pay|3.2.7|2026-07-09|
|Core Business Suite For Workplace Service Delivery|3.2.7|2026-07-09|
|Core Business Suite Foundation|3.0.7|2026-07-09|
|Core Business Suite Foundation for Finance|3.0.7|2026-07-09|
|Core Business Suite Foundation for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Foundation for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Foundation for Legal|3.0.7|2026-07-09|
|Core Business Suite Foundation for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Foundation for Workplace Services|3.0.7|2026-07-09|
|Core Business Suite Prime|3.0.7|2026-07-09|
|Core Business Suite Prime for Finance|3.0.7|2026-07-09|
|Core Business Suite Prime for Health and Safety|3.0.7|2026-07-09|
|Core Business Suite Prime for Human Resources|3.0.7|2026-07-09|
|Core Business Suite Prime for Legal|3.0.7|2026-07-09|
|Core Business Suite Prime for Source to Pay|3.0.7|2026-07-09|
|Core Business Suite Prime for Workplace Services|3.0.7|2026-07-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|1.2.0|2026-07-09|
|CPQ for Manufacturing Foundation|1.2.0|2026-07-09|
|CSM - Advanced|2.0.1|2026-07-09|
|CSM - Foundation|2.0.1|2026-07-09|
|CSM - Prime|2.0.1|2026-07-09|
|CSM MCP Server|1.0.4|2026-07-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.2.2|2026-06-16|
|Customer Service Management AI agent collection|6.1.0|2026-07-09|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DCNAM - Advanced|2.0.2|2026-07-09|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Dynamic Guidance|28.3.2|2026-06-16|
|Employee Slate for Now Assist|1.2.0|2026-07-09|
|Enhanced Features for IRM Enterprise|22.4.1|2026-07-09|
|Enhanced Features for IRM Professional|22.4.1|2026-07-09|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|External content connectors - Now assist agent|1.1.2|2026-07-09|
|Field Service Management AI agent collection|3.0.1|2026-06-16|
|Financial Services Operations AI agent collection|4.2.1|2026-07-09|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Form data collector|2.2.1|2026-07-09|
|FSC Common - Foundation|1.2.0|2026-06-16|
|FSC Common - Prime|1.2.0|2026-06-16|
|FSM - Advanced|2.0.1|2026-06-16|
|FSM - Foundation|2.0.1|2026-06-16|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Generative AI Controller|14.1.2|2026-07-09|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.4.0|2026-07-09|
|GRC Shared GenAI|22.4.0|2026-07-09|
|Group-Action Framework|7.1.1|2026-07-09|
|Hardware Asset Management - Advanced|1.0.2|2026-07-09|
|HCLS - Advanced|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|Health and Safety - Advanced|1.0.6|2026-07-09|
|Health and Safety - Foundation|1.0.6|2026-07-09|
|Health and Safety - Prime|1.0.6|2026-07-09|
|HR Service Delivery AI agent collection|7.1.1|2026-07-09|
|HR Talent AI Agent Collection|5.0.4|2026-07-09|
|HR Voice AI Agents|2.3.6|2026-06-16|
|HRSD - Advanced|2.1.0|2026-07-09|
|HRSD - Foundation|2.1.0|2026-07-09|
|HRSD - Prime|2.1.0|2026-07-09|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Industrial Control Tower Advanced|1.0.0|2026-06-16|
|Industrial Control Tower Foundation|1.0.0|2026-06-16|
|Industrial Control Tower Prime|1.0.0|2026-06-16|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Prime|1.0.3|2026-07-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Insights Clustering Utils|3.2.2|2026-07-09|
|Integrated Risk Management Advanced|22.4.0|2026-07-09|
|Integrated Risk Management Foundation|22.4.0|2026-07-09|
|Integrated Risk Management Prime|22.4.0|2026-07-09|
|IRM Compliance GenAI|22.4.0|2026-07-09|
|IRM Risk GenAI|22.4.0|2026-07-09|
|IT Service Management|3.1.1|2026-07-09|
|IT Service Management Advanced|3.1.1|2026-07-09|
|IT Service Management AI agent collection|10.0.1|2026-07-09|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|ITOM - Advanced|1.1.0|2026-07-09|
|ITOM - Prime|1.1.0|2026-07-09|
|ITOM AI Agents For Service Mapping|1.4.0|2026-07-09|
|ITSM - Advanced|2.2.2|2026-07-09|
|ITSM - Foundation|2.2.3|2026-07-09|
|ITSM - Prime|2.2.2|2026-07-09|
|Knowledge Center|31.11.3|2026-07-09|
|Knowledge Graph|8.1.0|2026-07-09|
|LEAP|4.1.0|2026-07-09|
|Legal Service Delivery - Prime|1.0.9|2026-06-16|
|List AI Experience|3.0.0|2026-06-16|
|Manage Invoice Operations|1.1.2|2026-07-09|
|Manage Order Operations|2.0.3|2026-06-16|
|Manufacturing Commercial Operations Advanced|1.2.0|2026-07-09|
|Manufacturing Commercial Operations AI agents collection|2.3.0|2026-07-09|
|Manufacturing Commercial Operations Foundation|1.2.0|2026-07-09|
|Manufacturing Commercial Operations Prime|1.2.0|2026-07-09|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Metadata Search|1.0.12|2026-07-09|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.2|2026-07-09|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.6.0|2026-07-09|
|Model Context Protocol Client|2.2.0|2026-06-16|
|Model Context Protocol Server|1.6.1|2026-07-09|
|Notifications Email Agents|2.2.0|2026-07-09|
|Now Assist Admin Console|10.1.5|2026-07-09|
|Now Assist Agents for requestor|3.6.1|2026-07-09|
|Now Assist AI Agents|8.1.7|2026-07-09|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|31.0.5|2026-06-16|
|Now Assist Analytics|5.1.2|2026-07-09|
|Now Assist Center|5.0.5|2026-07-09|
|Now Assist context menu|3.7.1|2026-07-09|
|Now Assist Data Kit|8.1.6|2026-07-09|
|Now Assist for Accounts Payable Operations \(APO\)|8.0.0|2026-06-16|
|Now Assist for Advanced Work Assignment \(AWA\)|1.0.3|2026-06-16|
|Now Assist for AIRC|22.4.0|2026-07-09|
|Now Assist for App Engine|29.2.3|2026-06-16|
|Now Assist for Automation Center|1.2.4|2026-07-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for code generation|28.5.23|2026-06-16|
|Now Assist for Collaborative Work Management \(CWM\)|6.1.2|2026-07-09|
|Now Assist for Complaint Case \(CSM\)|2.1.6|2026-07-09|
|Now Assist for Configuration Management Database \(CMDB\)|4.0.0|2026-07-09|
|Now Assist for Contract Analysis|1.0.11|2026-07-09|
|Now Assist For Core Business Suite|3.2.7|2026-07-09|
|Now Assist for CPQ|1.0.5|2026-07-09|
|Now Assist for Creator|29.4.1|2026-07-09|
|Now Assist for CSM Major Issue Management|1.1.0|2026-07-09|
|Now Assist for Customer Service Management \(CSM\)|14.1.1|2026-07-09|
|Now Assist for Digital End-user Experience \(DEX\)|4.3.0|2026-06-16|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.3.2|2026-06-16|
|Now Assist for Enterprise Architecture \(EA\)|7.4.1|2026-07-09|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for Error Framework|1.0.3|2026-06-16|
|Now Assist for Field Service Management \(FSM\)|10.0.1|2026-06-16|
|Now Assist for Financial Services Operations \(FSO\)|3.3.1|2026-07-09|
|Now Assist for FSC Common|7.0.0|2026-06-16|
|Now Assist for Hardware Asset Management|4.4.0|2026-07-09|
|Now Assist for Health and Safety|1.4.1|2026-06-16|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.3.2|2026-07-09|
|Now Assist for ICW|1.0.0|2026-05-05|
|Now Assist for Impact|4.0.5|2026-06-16|
|Now Assist for IRM|22.4.0|2026-07-09|
|Now Assist for IT Operations Management \(ITOM\)|2.8.0|2026-07-09|
|Now Assist for IT Service Management \(ITSM\)|16.0.3|2026-07-09|
|Now Assist for Legal Service Delivery|1.8.1|2026-06-16|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.3.0|2026-07-09|
|Now Assist for Operational Sustainability|22.3.2|2026-06-16|
|Now Assist for Order Management|2.2.2|2026-07-09|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|12.1.1|2026-07-09|
|Now Assist for Platform Advanced|2.1.0|2026-07-09|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Platform Foundation|2.1.0|2026-07-09|
|Now Assist for Platform Prime|2.1.0|2026-07-09|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.4.0|2026-07-09|
|Now Assist for Process Mining|3.1.2|2026-07-09|
|Now Assist for Prompt Assistance|5.1.4|2026-07-09|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.2.2|2026-06-16|
|Now Assist for Purchase Order Management \(POM\)|1.2.0|2026-06-16|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for Sales and Order Management for Telecommunications|4.1.2|2026-07-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.5|2026-07-09|
|Now Assist for Security Incident Response \(SIR\)|6.3.4|2026-07-09|
|Now Assist for Security Incident Response integrations|1.2.1|2026-06-16|
|Now Assist for Service Exchange|1.1.4|2026-07-09|
|Now Assist for Setup|3.1.4|2026-07-09|
|Now Assist for Setup Core|2.1.5|2026-07-09|
|Now Assist for Smart Assessment Engine|22.4.1|2026-07-09|
|Now Assist for Software Asset Management \(SAM\)|9.0.0|2026-07-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|10.0.0|2026-06-16|
|Now Assist for Spoke Generation|1.6.1|2026-06-16|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.7.1|2026-07-09|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|8.0.0|2026-06-16|
|Now Assist for Talent|1.8.3|2026-07-09|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.7|2026-06-16|
|Now Assist for Third-Party Risk Management|22.3.4|2026-07-09|
|Now Assist for Threat Intelligence Security Center|2.2.0|2026-07-09|
|Now Assist for Vault|2.1.1|2026-06-16|
|Now Assist for Voice|5.1.1|2026-07-09|
|Now Assist for Vulnerability Response|5.1.0|2026-07-09|
|Now Assist for WDF|2.1.4|2026-07-09|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.13|2026-06-16|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in AI Search|17.1.4|2026-07-09|
|Now Assist in Catalog Builder|7.3.0|2026-07-09|
|Now Assist in Catalog item forms|1.4.2|2026-07-09|
|Now Assist in Contract Management|2.3.2|2026-07-09|
|Now Assist in Conversational Catalog Request|7.1.1|2026-07-09|
|Now Assist in Document Intelligence|6.2.0|2026-07-09|
|Now Assist in Document Management|3.0.1|2026-07-09|
|Now Assist in Knowledge Management|30.11.3|2026-07-09|
|Now Assist in Standard Ticket Page|1.3.0|2026-07-09|
|Now Assist in Virtual Agent|20.0.8|2026-07-09|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|3.0.3|2026-06-16|
|Now Assist Service Quality|2.0.2|2026-07-09|
|Now Assist Skill Discovery and Execution|10.2.3|2026-07-09|
|Now Assist Skill Kit|9.1.1|2026-07-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|22.3.1|2026-06-16|
|Opportunity Management AI Features|1.0.9|2026-07-09|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Platform AI Agents and Skills|13.1.9|2026-07-09|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.1.1|2026-06-16|
|Privacy Management Advanced|22.4.0|2026-07-09|
|prompt-management|2.0.6|2026-07-09|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|1.3.1|2026-06-16|
|Query Generation|6.1.1|2026-07-09|
|Query Orchestrator|1.2.1|2026-07-09|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.4.0|2026-07-09|
|Recommended Actions for Security Operations|2.2.4|2026-07-09|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|Sales and Order Management for Technology Provider - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Technology Provider - Prime|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications - Advanced|2.1.2|2026-07-09|
|Sales and Order Management for Telecommunications - Prime|2.1.2|2026-07-09|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.4|2026-06-16|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.18|2026-07-09|
|Security Incident Response - Advanced|1.0.7|2026-06-16|
|Security Incident Response - Foundation|1.0.7|2026-06-16|
|Security Incident Response - Prime|1.0.7|2026-06-16|
|Service Exchange - Advanced|1.1.4|2026-07-09|
|Service Exchange - Foundation|1.1.4|2026-07-09|
|Service Exchange - Prime|1.1.4|2026-07-09|
|ServiceNow AI Lens|7.0.2|2026-07-09|
|SLO - Foundation|1.2.0|2026-06-16|
|SLO - Prime|1.2.0|2026-06-16|
|Software Asset Management AI Advanced|2.1.0|2026-07-09|
|Software Asset Management AI Prime|2.1.1|2026-07-09|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SOM for Manufacturing Advanced|1.2.0|2026-07-09|
|SOM for Manufacturing Prime|1.2.0|2026-07-09|
|SPO - Foundation|1.2.0|2026-06-16|
|SPO - Prime|1.2.0|2026-06-16|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Technology Advanced|1.0.4|2026-06-16|
|Technology Foundation|1.0.4|2026-06-16|
|Technology Prime|1.0.4|2026-06-16|
|Telecommunications Advanced|2.0.1|2026-06-16|
|Telecommunications Foundation|2.0.1|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecommunications Prime|2.0.1|2026-06-16|
|Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Telecommunications, Media and Technology - Foundation|1.0.4|2026-06-16|
|Telecommunications, Media and Technology - Prime|1.0.3|2026-06-16|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Management Advanced|22.3.4|2026-07-09|
|Third-party Risk Management Professional Plus|22.3.4|2026-07-09|
|Threat Intelligence Security Center - Advanced|3.0.1|2026-07-09|
|TNI - Advanced|2.0.2|2026-07-09|
|TNI and DCNAM AI Content Collection|2.0.1|2026-07-09|
|TSOM - Advanced|2.0.2|2026-07-09|
|TSOM - Prime|2.0.1|2026-07-09|
|UI Generation|29.2.5|2026-05-05|
|Unified Security Exposure Management \(USEM\) - Advanced|2.1.0|2026-07-09|
|Unified Security Exposure Management \(USEM\) - Foundation|2.1.0|2026-07-09|
|Unified Security Exposure Management \(USEM\) - Prime|2.1.0|2026-07-09|
|Universal Request AI agent collection|1.0.9|2026-06-16|
|Voice input for Now Assist|1.5.0|2026-07-09|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|Zero Copy Connector Hub|3.0.1|2026-03-12|
|Zero Touch Service Desk|2.3.5|2026-07-09|


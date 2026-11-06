---
title: October 01 2026 Now Assist Suite release notes
description: Now Assist Suite version and compatibility information for the October 01 2026 release on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/na-suite-rn-2026-10-01.html
release: store
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 33
breadcrumb: [Now Assist Suite - October 2026 release notes, Now Assist Suite release notes]
---

# October 01 2026 Now Assist Suite release notes

Now Assist Suite version and compatibility information for the October 01 2026 release on the ServiceNow Store.

Note: Now Assist Suite versions are cumulative. For app version updates that have been carried forward from previous releases, refer to the release notes page for the application's "Last updated" date or the ServiceNow Store app listing. See [Now Assist suite versions in the Application Manager](https://www.servicenow.com/docs/r/platform-administration/application-manager/now-assist-suites-app-mgr.html) for more details.

## Suite version 29.6.20261001 - Australia Patch 6

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Admin Center

</td><td>

6.0.9

</td><td>

Fixed : Updating the Self healing agent scheduled job to on-demand.

</td></tr><tr><td>

OpenAI Generative AI Spoke

</td><td>

3.4.0

</td><td>

Changed - Actions - Add Response Format input for all the actions

</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

22.0.18

</td><td>

New -   Admins can configure tool access permissions for Model Context Protocol \(MCP\) server integrations. When adding or editing an MCP server configuration, admins can select tools and set their access status as Allowed, Disallowed, or Require Approval. The interface supports bulk permission changes, search, authentication flows, and error handling for tool loading.
-   Admins can add Web applications as a communication channel under WebRTC. The WebRTC section supports adding new web applications, including an Engagement Messenger section with configuration links and read-only fields for Voice Service ID, Orchestrator Host URL, and WebSocket URL.
-   Admins can make retry attempts editable directly on the Caller Verification screen. The retry attempt value is now adjustable within the UI, improving workflow efficiency.
-   Caller verification supports a discard changes pop-up when refreshing configuration. Users are prompted to confirm before discarding unsaved changes during configuration refresh.
-   Caller verification includes a refresh configuration option. Admins can refresh configuration directly from the Assistant Designer page.
-   Caller verification now displays updated error messages for configuration issues. The UI provides clearer guidance for missing identification methods and factors.
-   Voice assistant handles form validation errors in Caller Verification. Mandatory fields not filled trigger a red card error, improving clarity.
-   Admins can select language input using DTMF or voice options. The Language and Voice page includes a new section for input selection, with links to advanced settings and retry/goodbye message configuration.
-   Admins can decouple the Testing UI from the Assistant "Active" state. Testing can be initiated without activating the assistant, and the test button is enabled regardless of activation status.
-   Admins can turn off parametric memory by default for all assistants. Scripts auto-populate parametric memory policy, ensuring consistent behavior.
-   Admins can now create a switch to enable custom SIP options in communication channels. The custom SIP option appears in the UI when enabled.
-   ServiceNow Otto panel premium chat is the default for eligible new customers, with Now LLM restrictions. Premium chat uses V2 orchestrator, and eligibility checks prevent Now LLM selection when premium chat and V2 orchestrator are enabled.

Changed

-   Embedded script for Service Portal UI has been updated. Parameter names, OAuth client ID handling, call button visibility, and optional widget parameters have been revised for improved reliability and clarity.

Fixed

-   Search sources in Assistant Designer now correctly reflect the "Include in AI Response" profile configuration. The system pulls from the correct table column, opens links in new tabs, and passes unit tests.
-   Unified Recommendations now allow cross-scope calls for typeahead suggestions, improving integration reliability.
-   The "Response feedback" page now works for existing assistants after upgrade. Script fixes ensure feedback attributes are correctly handled.
-   The "View org chart" feature in ServiceNow Otto for Virtual Agent now loads correctly when accessed through a custom URL or domain. The system uses relative URLs and sets appropriate roles.
-   Doc QnA now marks deflection logs as "response provided/resolved" after uploading an attachment with a question. The fix extends to all relevant topic representations and ensures logs are updated when user input is provided.
-   Duplicate create asset modal components have been eliminated from the codebase. Only one shared modal component is used across conversation-studio and nowassist-va repositories.

Removed

-   The role-based configuration from the MCP Server page is removed. The role column and related logic have been eliminated, simplifying server management and ensuring backward compatibility.
-   The Web applications section in Assistant Designer is no longer controlled by a system property. The property has been removed, and the section is always available.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.6.4|2026-09-10|
|Advanced Approval Management AI|1.2.2|2026-09-10|
|Agentic Contact Center for Banking|1.4.5|2026-09-04|
|Agentic Contact Center for Insurance|1.3.3|2026-09-04|
|AI Admin Hub|10.3.4|2026-09-10|
|AI Agent Advisor|1.4.5|2026-09-10|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.12.3|2026-09-10|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for CSM - Complaint Case|1.5.1|2026-08-07|
|AI Agents for Customer Success Management|2.7.21|2026-09-10|
|AI Agents for Discovery|3.2.2|2026-09-10|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.4|2026-08-07|
|AI Agents for Enterprise|1.0.1|2026-09-10|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|AI Agents for Health Log Analytics|2.5.0|2026-09-10|
|AI Agents for HR Service Delivery|7.3.1|2026-09-10|
|AI Agents for ITAM|5.0.0|2026-09-10|
|AI Agents for Meetings|1.0.10|2026-09-10|
|AI Agents for Retail Service Management|1.6.0|2026-09-10|
|AI Agents for Service Exchange Provider|1.1.12|2026-08-13|
|AI agents for SLO|2.2.2|2026-09-10|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Talent|6.0.0|2026-08-07|
|AI Agents for Telecommunications, Media and Technology|6.2.1|2026-09-10|
|AI Agents for Universal Request|1.1.3|2026-09-10|
|AI Agents for Workplace Service Delivery|3.3.8|2026-08-07|
|AI Analytics|5.3.5|2026-09-10|
|AI Authoring for Catalog Builder|8.0.3|2026-09-10|
|AI Control Tower for Enterprise AI Foundation|1.9.2|2026-09-10|
|AI Control Tower for ServiceNow Otto|7.0.3|2026-09-10|
|AI Dashboard Insights|1.3.4|2026-08-07|
|AI Data Explorer|5.2.7|2026-09-10|
|AI Data Kit|9.0.4|2026-09-10|
|AI Desktop Actions|6.0.0|2026-09-10|
|AI Enhanced Recommended Actions|1.0.5|2026-08-07|
|AI Experience Framework Skills|1.4.4|2026-09-10|
|AI features for Deal Registration|1.0.2|2026-09-10|
|AI for document designer|23.0.3|2026-09-10|
|AI Help Framework|2.0.2|2026-09-10|
|AI Native Experience for AI Control Tower - ServicenowAI|4.0.1|2026-09-10|
|AI Platform skills|3.2.2|2026-09-10|
|AI Search RAG|7.0.3|2026-09-10|
|AI Skill Kit|10.0.5|2026-09-10|
|AI slot-filling for catalog items|1.4.5|2026-08-07|
|AI Specialists for Security Incident Response|1.0.10|2026-09-10|
|AI Troubleshooting|4.1.4|2026-08-07|
|AI Websearch|4.1.0|2026-06-16|
|AIOps Agentic Workforce|2.2.5|2026-09-10|
|AIS ZTSD Gemma|1.0.6|2026-09-10|
|Alert Assist|3.12.2|2026-09-10|
|Amazon Bedrock Spoke|1.5.1|2026-08-07|
|Analytics Generation|4.1.15|2026-07-09|
|APO - Foundation|2.0.0|2026-09-10|
|APO - Prime|2.0.0|2026-09-10|
|App Engine - Prime|29.1.8|2026-08-07|
|App Generation|28.3.12|2026-07-09|
|App Life Cycle AI Agents|29.5.2|2026-08-07|
|App Summary|29.4.0|2026-07-09|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.1.2|2026-09-10|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Build Agent Premium|1.6.0|2026-09-10|
|Business Continuity Management Advanced|2.0.3|2026-09-10|
|Business Continuity Management Foundation|2.0.3|2026-09-10|
|Care Team Operations AI agent collection|2.1.1|2026-09-10|
|Catalog Conversational Coverage|6.2.1|2026-09-10|
|Change Management AI Orchestrator|1.0.4|2026-09-10|
|Chat Recommendation|1.9.1|2026-09-10|
|Chat Summarization for Virtual Agent|1.12.7|2026-09-10|
|Cloud Cost Management Advanced|1.0.0|2026-09-10|
|CMDB MCP Server|2.0.0|2026-09-10|
|Collaborative Work Management - Advanced|2.2.1|2026-09-10|
|Common AI Framework|2.0.2|2026-08-07|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Content Understanding|7.1.4|2026-09-10|
|Contract Management Pro - Prime|1.0.21|2026-09-10|
|Conversation Evaluator|3.2.1|2026-09-10|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Conversational Catalog Requests|8.0.2|2026-09-10|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|12.0.7|2026-09-10|
|Conversational subflows and actions|30.0.4|2026-08-07|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced for Finance|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Advanced for Legal|3.3.2|2026-08-07|
|Core Business Suite Advanced for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Advanced for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite for Finance|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Human Resources|3.3.2|2026-08-07|
|Core Business Suite for Legal|3.3.2|2026-08-07|
|Core Business Suite For Source To Pay|3.3.2|2026-08-07|
|Core Business Suite For Workplace Service Delivery|3.3.3|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation for Finance|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Foundation for Legal|3.3.2|2026-08-07|
|Core Business Suite Foundation for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Foundation for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime for Finance|3.3.2|2026-08-07|
|Core Business Suite Prime for Health and Safety|3.3.3|2026-09-10|
|Core Business Suite Prime for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Prime for Legal|3.3.2|2026-08-07|
|Core Business Suite Prime for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Prime for Workplace Services|3.3.3|2026-08-07|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|3.0.0|2026-09-10|
|CPQ for Manufacturing Foundation|3.0.0|2026-09-10|
|Cryptographic Asset Compliance|1.0.2|2026-08-07|
|CSM - Advanced|2.1.2|2026-08-07|
|CSM - Foundation|2.1.2|2026-08-07|
|CSM - Prime|2.1.2|2026-08-07|
|CSM MCP Server|1.2.0|2026-08-07|
|CTO Voice AI Agents|2.1.0|2026-09-10|
|Custom App Record Summarization|30.1.1|2026-09-10|
|Customer Service Management AI agent collection|7.0.1|2026-09-10|
|Customer Service RMA AI Agents|1.1.4|2026-09-10|
|Cyber Physical Systems Control Tower Advanced|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Foundation|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Prime|1.0.2|2026-09-10|
|Cyber Physical Systems Operations Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Prime|1.0.5|2026-09-10|
|Cyber Physical Systems Security Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Security Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Security Prime|1.0.7|2026-09-10|
|Dashboard and visualization export|1.4.1|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Dynamic Guidance|28.5.1|2026-09-10|
|Employee Slate \(built for Now Assist\)|1.4.4|2026-09-10|
|Enhanced Features for IRM Enterprise|23.0.1|2026-09-10|
|Enhanced Features for IRM Professional|23.0.2|2026-09-10|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Asset Management Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for Healthcare Advanced|2.0.1|2026-09-10|
|Enterprise Data Transform|1.0.2|2026-09-10|
|External content connectors - ServiceNow Otto agent|1.2.0|2026-08-07|
|Field Service Management AI agent collection|4.1.0|2026-09-10|
|Finance and Procurement - Foundation|2.0.0|2026-09-10|
|Finance and Procurement - Prime|2.0.0|2026-09-10|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Flow Designer GenAI|30.1.4|2026-09-10|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.4.4|2026-08-07|
|Flow Summarization|29.4.4|2026-08-07|
|Flow troubleshooting agent|1.0.12|2026-09-10|
|Form data collector|2.3.1|2026-08-07|
|FSM - Advanced|2.1.2|2026-09-10|
|FSM - Foundation|2.1.2|2026-09-10|
|FSM Scheduling AI Agent Collection|2.0.4|2026-09-10|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Generative AI Controller|15.0.3|2026-09-10|
|Google Gemini Spoke|1.6.2|2026-08-07|
|GRC Common GenAI|23.0.5|2026-09-10|
|GRC Shared GenAI|23.0.2|2026-09-10|
|Group-Action Framework|8.0.6|2026-09-10|
|Hardware Asset Management - Advanced|1.0.11|2026-09-10|
|Hardware Asset Management - Prime|1.0.13|2026-09-10|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|Health and Safety - Advanced|1.0.6|2026-07-09|
|Health and Safety - Foundation|1.0.6|2026-07-09|
|Health and Safety - Prime|1.0.6|2026-07-09|
|HR Voice AI Agents|2.3.14|2026-09-10|
|HRSD - Advanced|2.2.5|2026-09-10|
|HRSD - Foundation|2.2.5|2026-09-10|
|HRSD - Prime|2.2.5|2026-09-10|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Insights Clustering Utils|3.4.1|2026-09-10|
|Integrated Risk Management Advanced|23.0.1|2026-09-10|
|Integrated Risk Management Foundation|23.0.0|2026-09-10|
|Integrated Risk Management Prime|23.0.1|2026-09-10|
|Intelligent Approvals|3.0.10|2026-09-10|
|IRM Compliance GenAI|23.0.3|2026-09-10|
|IRM Risk GenAI|23.0.2|2026-09-10|
|IT Service Management|3.3.1|2026-09-10|
|IT Service Management Advanced|3.3.1|2026-09-10|
|IT Service Management AI agent collection|11.2.2|2026-09-18|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|ITOM - Advanced|1.1.5|2026-09-10|
|ITOM - Prime|1.2.2|2026-09-10|
|ITOM AI Agents For Service Mapping|1.4.1|2026-08-07|
|ITSM - Advanced|2.3.16|2026-09-24|
|ITSM - Foundation|2.3.16|2026-09-24|
|ITSM - Prime|2.3.16|2026-09-24|
|ITSM Autonomous Workforce|1.1.7|2026-09-18|
|ITSM L1 AI Specialist|1.1.10|2026-09-18|
|Keyboard Shortcuts AI Skills|1.0.4|2026-08-07|
|Knowledge Center|31.26.5|2026-09-10|
|Knowledge Graph|8.3.3|2026-09-10|
|Knowledge Graph Affinity Signals|1.0.1|2026-09-10|
|LEAP|4.3.1|2026-09-10|
|Legal Service Delivery - Prime|1.0.17|2026-09-10|
|List AI Experience|3.1.4|2026-08-07|
|Manage Invoice Operations|1.3.0|2026-09-10|
|Manage Order Operations|2.2.0|2026-09-10|
|Manufacturing Commercial Operations Advanced|3.0.0|2026-09-10|
|Manufacturing Commercial Operations AI agents collection|4.1.0|2026-09-10|
|Manufacturing Commercial Operations Foundation|3.0.0|2026-09-10|
|Manufacturing Commercial Operations Prime|3.0.0|2026-09-10|
|MCP for Strategic Portfolio Management|1.4.0|2026-09-10|
|Metadata Search|1.2.1|2026-09-10|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.3|2026-08-07|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.6.0|2026-07-09|
|Model Context Protocol Client|2.4.4|2026-09-10|
|Model Context Protocol Server|1.8.0|2026-09-10|
|Notifications Email Agents|3.0.2|2026-09-10|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Prompt Assistance|6.0.7|2026-09-10|
|observ-ai-agents-app|6.3.1|2026-09-10|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|23.0.1|2026-09-10|
|Operational Sustainability Management Prime|23.0.3|2026-09-10|
|OT Asset Management Advanced|2.0.1|2026-09-10|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|PA AI Tools|1.0.4|2026-09-10|
|Platform AI Agents and Skills|14.0.10|2026-09-10|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.3.1|2026-09-10|
|Privacy Management Advanced|23.0.2|2026-09-10|
|Privacy Management Prime|23.0.2|2026-09-10|
|prompt-management|2.0.6|2026-07-09|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|2.0.4|2026-09-10|
|Query Generation|6.3.1|2026-09-10|
|Query Orchestrator|1.3.1|2026-08-07|
|Quote AI agent|3.0.8|2026-09-10|
|RAG for code generation|1.1.14|2026-09-10|
|Recommendation template|22.5.1|2026-08-07|
|Recommended Actions for Security Operations|2.3.6|2026-09-10|
|Retail MCP Server|1.0.0|2026-09-10|
|RSM - Advanced|1.1.1|2026-08-07|
|RSM - Foundation|1.1.1|2026-08-07|
|RSM - Prime|1.1.1|2026-08-07|
|Sales and Order Management for Technology Provider - Advanced|1.0.8|2026-09-10|
|Sales and Order Management for Technology Provider - Prime|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications - Advanced|2.3.2|2026-09-10|
|Sales and Order Management for Telecommunications - Prime|2.3.2|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.9|2026-09-10|
|Sales Development AI Agents|1.0.12|2026-09-10|
|Screen Summarization|1.2.6|2026-08-07|
|Security Incident Response - Advanced|1.0.10|2026-09-10|
|Security Incident Response - Foundation|1.0.10|2026-09-10|
|Security Incident Response - Prime|1.0.10|2026-09-10|
|Service Catalog AI Core|1.0.2|2026-09-10|
|Service Exchange - Advanced|1.1.13|2026-08-13|
|Service Exchange - Foundation|1.1.13|2026-08-13|
|Service Exchange - Prime|1.1.13|2026-08-13|
|ServiceNow AI Lens|8.1.1|2026-09-10|
|ServiceNow Otto Agents for requestor|3.7.6|2026-09-10|
|ServiceNow Otto AI Agents|9.0.11|2026-09-18|
|ServiceNow Otto AI web agent|33.0.3|2026-09-10|
|ServiceNow Otto context menu|3.9.2|2026-09-24|
|ServiceNow Otto Conversational Data Collection|10.2.22|2026-09-10|
|ServiceNow Otto for Accounts Payable Operations \(APO\)|9.0.0|2026-09-10|
|ServiceNow Otto for AI Control Tower|24.0.4|2026-09-10|
|ServiceNow Otto for AI Search|18.0.5|2026-09-10|
|ServiceNow Otto for AIRC|23.0.1|2026-09-10|
|ServiceNow Otto for App Engine|30.1.1|2026-09-10|
|ServiceNow Otto for Automation Center|1.3.0|2026-08-07|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Cloud Cost Management|1.0.0|2026-09-10|
|ServiceNow Otto for Code|28.5.32|2026-09-10|
|ServiceNow Otto for Collaborative Work Management \(CWM\)|7.0.2|2026-09-10|
|ServiceNow Otto for Configuration Management Database \(CMDB\)|4.4.1|2026-09-10|
|ServiceNow Otto for Contract Analysis|1.0.15|2026-08-07|
|ServiceNow Otto for Contract Management Pro|2.5.2|2026-09-10|
|ServiceNow Otto for Conversational Spokes|1.1.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for CPQ|1.1.8|2026-09-10|
|ServiceNow Otto for Creator|29.6.2|2026-09-10|
|ServiceNow Otto for CSM Complaint Case|2.2.1|2026-08-07|
|ServiceNow Otto for CSM Major Issue Management|1.2.4|2026-08-07|
|ServiceNow Otto for Customer Service Management \(CSM\)|15.0.1|2026-09-10|
|ServiceNow Otto for Digital End-user Experience \(DEX\)|5.2.10|2026-09-18|
|ServiceNow Otto for Document Voice|2.0.11|2026-09-10|
|ServiceNow Otto for Employee Experience|4.4.3|2026-08-07|
|ServiceNow Otto for Enterprise Architecture \(EA\)|7.5.2|2026-08-07|
|ServiceNow Otto for Enterprise Asset Management|2.0.1|2026-09-10|
|ServiceNow Otto for Error Framework|1.2.0|2026-09-10|
|ServiceNow Otto for Field Service Management|11.1.2|2026-09-10|
|ServiceNow Otto for Finance and Procurement|8.0.0|2026-09-10|
|ServiceNow Otto for Financial Services Operations \(FSO\)|3.4.3|2026-09-04|
|ServiceNow Otto for Hardware Asset Management|5.0.1|2026-09-10|
|ServiceNow Otto for Health and Safety|1.5.1|2026-08-07|
|ServiceNow Otto for HR Service Delivery \(HRSD\)|13.5.2|2026-09-10|
|ServiceNow Otto for HRSD - Galileo Inside|2.3.7|2026-09-10|
|ServiceNow Otto for ICW|1.1.0|2026-08-07|
|ServiceNow Otto for Impact|6.0.6|2026-09-10|
|ServiceNow Otto for Integrated Risk Management|23.0.4|2026-09-10|
|ServiceNow Otto for Integration Hub|2.3.2|2026-08-07|
|ServiceNow Otto for IT Operations Management \(ITOM\)|2.9.4|2026-09-10|
|ServiceNow Otto for IT Service Management \(ITSM\)|17.2.4|2026-09-24|
|ServiceNow Otto for Knowledge Management|31.6.6|2026-09-10|
|ServiceNow Otto for Legal Service Delivery|1.9.7|2026-09-10|
|ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)|4.1.0|2026-09-10|
|ServiceNow Otto for Operational Sustainability|23.0.1|2026-09-10|
|ServiceNow Otto for Opportunity Management|1.2.0|2026-09-10|
|ServiceNow Otto for Order Management|2.3.3|2026-09-10|
|ServiceNow Otto for OT Service Management|3.1.5|2026-08-07|
|ServiceNow Otto for Platform|13.0.1|2026-09-10|
|ServiceNow Otto for Platform Advanced|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Foundation|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Prime|3.0.1|2026-09-10|
|ServiceNow Otto for Privacy Management|23.0.2|2026-09-10|
|ServiceNow Otto for Process Mining|4.1.5|2026-09-10|
|ServiceNow Otto for Public Sector Digital Services \(PSDS\)|2.5.3|2026-09-10|
|ServiceNow Otto for Purchase Order Management \(POM\)|1.4.1|2026-09-10|
|ServiceNow Otto for Retail Service Management|1.6.0|2026-09-10|
|ServiceNow Otto for RPA Hub|5.1.1|2026-08-07|
|ServiceNow Otto for Sales and Order Management for Telecommunications|4.3.3|2026-09-10|
|ServiceNow Otto for Sales Automation|1.1.7|2026-09-10|
|ServiceNow Otto for Security Incident Response \(SIR\)|6.5.2|2026-09-10|
|ServiceNow Otto for Security Incident Response Integration Toolkit|1.2.5|2026-08-07|
|ServiceNow Otto for Service Exchange|1.1.12|2026-08-13|
|ServiceNow Otto for Service Quality|2.2.0|2026-09-10|
|ServiceNow Otto for Setup|5.0.20|2026-09-10|
|ServiceNow Otto for Setup Core|4.0.20|2026-09-10|
|ServiceNow Otto for Smart Assessment Engine|23.0.6|2026-09-10|
|ServiceNow Otto for Software Asset Management \(SAM\)|11.0.0|2026-09-10|
|ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)|11.0.0|2026-09-10|
|ServiceNow Otto for Spoke Generation|2.0.1|2026-08-07|
|ServiceNow Otto for Strategic Portfolio Management|9.11.0|2026-09-10|
|ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)|9.0.1|2026-09-10|
|ServiceNow Otto for Talent|1.9.2|2026-08-07|
|ServiceNow Otto for Telecommunications Service Management|2.3.1|2026-09-10|
|ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)|6.0.15|2026-09-10|
|ServiceNow Otto for Third-Party Risk Management|23.0.5|2026-09-10|
|ServiceNow Otto for Threat Intelligence Security Center|2.6.1|2026-09-10|
|ServiceNow Otto for Unified Security Exposure Management|5.2.3|2026-08-07|
|ServiceNow Otto for Vault|2.2.2|2026-08-07|
|ServiceNow Otto for Virtual Agent Configurations|16.0.5|2026-08-20|
|ServiceNow Otto for Voice Agents|6.0.5|2026-09-10|
|ServiceNow Otto for WDF|2.3.4|2026-08-07|
|ServiceNow Otto for Workplace Service Delivery \(WSD\)|1.1.20|2026-08-07|
|ServiceNow Otto for Wrap Up|1.0.4|2026-08-07|
|ServiceNow Otto for Zero Copy Connector|2.0.6|2026-08-07|
|ServiceNow Otto in Document Management|4.0.11|2026-09-18|
|SLO - Foundation|2.0.2|2026-09-10|
|SLO - Prime|2.0.0|2026-09-10|
|Software Asset Management AI Advanced|2.5.0|2026-09-10|
|Software Asset Management AI Prime|2.5.0|2026-09-10|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SOM for Manufacturing Advanced|3.0.0|2026-09-10|
|SOM for Manufacturing Prime|3.0.0|2026-09-10|
|SPO - Foundation|2.0.0|2026-09-10|
|SPO - Prime|2.0.0|2026-09-10|
|Standard ticket page summarization|1.3.3|2026-08-07|
|Strategic Portfolio Management - Advanced|1.3.0|2026-09-10|
|Strategic Portfolio Management - Prime|1.2.0|2026-09-10|
|Summarization for Order Management|2.2.4|2026-09-10|
|Task Plan Template AI Agents|2.0.1|2026-09-10|
|Technology Advanced|1.0.12|2026-09-10|
|Technology Foundation|1.0.15|2026-09-10|
|Technology Prime|1.0.12|2026-09-10|
|Telecommunications Advanced|2.3.1|2026-09-10|
|Telecommunications Foundation|2.3.1|2026-09-10|
|Telecommunications Prime|2.3.1|2026-09-10|
|Telecommunications, Media and Technology - Advanced|1.0.11|2026-09-10|
|Telecommunications, Media and Technology - Foundation|1.0.13|2026-09-10|
|Telecommunications, Media and Technology - Prime|1.0.11|2026-09-10|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Management Advanced|23.0.3|2026-09-10|
|Third-party Risk Management Professional Plus|23.0.3|2026-09-10|
|Threat Intelligence Security Center - Advanced|3.3.1|2026-09-10|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|TSOM - Advanced|2.3.0|2026-09-10|
|TSOM - Prime|2.3.0|2026-09-10|
|UI Generation|29.2.5|2026-05-05|
|Unified Security Exposure Management \(USEM\) - Advanced|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Foundation|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Prime|2.2.3|2026-08-07|
|Voice input for Now Assist|1.5.0|2026-07-09|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|Zero Touch Service Desk|3.2.8|2026-09-18|

## Suite version 30.0.20261001 - Brazil Patch 0 \(Early Availability\)

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Admin Center

</td><td>

6.0.9

</td><td>

Fixed : Updating the Self healing agent scheduled job to on-demand.

</td></tr><tr><td>

OpenAI Generative AI Spoke

</td><td>

3.4.0

</td><td>

Changed - Actions - Add Response Format input for all the actions

</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

22.0.18

</td><td>

New -   Admins can configure tool access permissions for Model Context Protocol \(MCP\) server integrations. When adding or editing an MCP server configuration, admins can select tools and set their access status as Allowed, Disallowed, or Require Approval. The interface supports bulk permission changes, search, authentication flows, and error handling for tool loading.
-   Admins can add Web applications as a communication channel under WebRTC. The WebRTC section supports adding new web applications, including an Engagement Messenger section with configuration links and read-only fields for Voice Service ID, Orchestrator Host URL, and WebSocket URL.
-   Admins can make retry attempts editable directly on the Caller Verification screen. The retry attempt value is now adjustable within the UI, improving workflow efficiency.
-   Caller verification supports a discard changes pop-up when refreshing configuration. Users are prompted to confirm before discarding unsaved changes during configuration refresh.
-   Caller verification includes a refresh configuration option. Admins can refresh configuration directly from the Assistant Designer page.
-   Caller verification now displays updated error messages for configuration issues. The UI provides clearer guidance for missing identification methods and factors.
-   Voice assistant handles form validation errors in Caller Verification. Mandatory fields not filled trigger a red card error, improving clarity.
-   Admins can select language input using DTMF or voice options. The Language and Voice page includes a new section for input selection, with links to advanced settings and retry/goodbye message configuration.
-   Admins can decouple the Testing UI from the Assistant "Active" state. Testing can be initiated without activating the assistant, and the test button is enabled regardless of activation status.
-   Admins can turn off parametric memory by default for all assistants. Scripts auto-populate parametric memory policy, ensuring consistent behavior.
-   Admins can now create a switch to enable custom SIP options in communication channels. The custom SIP option appears in the UI when enabled.
-   ServiceNow Otto panel premium chat is the default for eligible new customers, with Now LLM restrictions. Premium chat uses V2 orchestrator, and eligibility checks prevent Now LLM selection when premium chat and V2 orchestrator are enabled.

 Changed

-   Embedded script for Service Portal UI has been updated. Parameter names, OAuth client ID handling, call button visibility, and optional widget parameters have been revised for improved reliability and clarity.

Fixed

-   Search sources in Assistant Designer now correctly reflect the "Include in AI Response" profile configuration. The system pulls from the correct table column, opens links in new tabs, and passes unit tests.
-   Unified Recommendations now allow cross-scope calls for typeahead suggestions, improving integration reliability.
-   The "Response feedback" page now works for existing assistants after upgrade. Script fixes ensure feedback attributes are correctly handled.
-   The "View org chart" feature in ServiceNow Otto for Virtual Agent now loads correctly when accessed through a custom URL or domain. The system uses relative URLs and sets appropriate roles.
-   Doc QnA now marks deflection logs as "response provided/resolved" after uploading an attachment with a question. The fix extends to all relevant topic representations and ensures logs are updated when user input is provided.
-   Duplicate create asset modal components have been eliminated from the codebase. Only one shared modal component is used across conversation-studio and nowassist-va repositories.

Removed

-   The role-based configuration from the MCP Server page is removed. The role column and related logic have been eliminated, simplifying server management and ensuring backward compatibility.
-   The Web applications section in Assistant Designer is no longer controlled by a system property. The property has been removed, and the section is always available.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.6.4|2026-09-10|
|Access Analysis AI Agents|1.0.4|2026-09-10|
|Advanced Approval Management AI|1.2.2|2026-09-10|
|Agentic Contact Center for Banking|2.1.0|2026-09-10|
|Agentic Contact Center for Insurance|2.1.0|2026-09-10|
|AI Admin Hub|10.3.4|2026-09-10|
|AI Agent Advisor|1.4.5|2026-09-10|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.12.3|2026-09-10|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for CSM - Complaint Case|1.5.1|2026-08-07|
|AI Agents for Customer Success Management|2.7.21|2026-09-10|
|AI Agents for Discovery|3.2.2|2026-09-10|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.4|2026-08-07|
|AI Agents for Enterprise|1.0.1|2026-09-10|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|AI Agents for Health Log Analytics|2.5.0|2026-09-10|
|AI Agents for HR Service Delivery|7.3.1|2026-09-10|
|AI Agents for ITAM|5.0.0|2026-09-10|
|AI Agents for Meetings|1.0.10|2026-09-10|
|AI Agents for Retail Service Management|2.0.0|2026-09-10|
|AI Agents for Service Exchange Provider|1.1.12|2026-08-13|
|AI agents for SLO|2.2.2|2026-09-10|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Talent|6.0.0|2026-08-07|
|AI Agents for Telecommunications, Media and Technology|6.2.1|2026-09-10|
|AI Agents for Universal Request|1.1.3|2026-09-10|
|AI Agents for Workplace Service Delivery|3.3.8|2026-08-07|
|AI Analytics|5.3.5|2026-09-10|
|AI Authoring for Catalog Builder|8.0.3|2026-09-10|
|AI Control Tower for Enterprise AI Foundation|1.9.2|2026-09-10|
|AI Control Tower for ServiceNow Otto|7.0.3|2026-09-10|
|AI Dashboard Insights|1.3.4|2026-08-07|
|AI Data Explorer|5.2.7|2026-09-10|
|AI Data Kit|9.0.4|2026-09-10|
|AI Desktop Actions|6.0.0|2026-09-10|
|AI Enhanced Recommended Actions|1.0.5|2026-08-07|
|AI Experience Framework Skills|1.4.4|2026-09-10|
|AI features for Deal Registration|1.0.2|2026-09-10|
|AI for document designer|23.0.3|2026-09-10|
|AI Help Framework|2.0.2|2026-09-10|
|AI Native Experience for AI Control Tower - ServicenowAI|4.0.1|2026-09-10|
|AI Platform skills|3.2.2|2026-09-10|
|AI Search RAG|7.0.3|2026-09-10|
|AI Skill Kit|10.0.5|2026-09-10|
|AI slot-filling for catalog items|1.4.5|2026-08-07|
|AI Specialists for Security Incident Response|1.0.10|2026-09-10|
|AI Troubleshooting|4.1.4|2026-08-07|
|AI Websearch|4.1.0|2026-06-16|
|AIOps Agentic Workforce|2.2.5|2026-09-10|
|AIS ZTSD Gemma|1.0.6|2026-09-10|
|Alert Assist|3.12.2|2026-09-10|
|Amazon Bedrock Spoke|1.5.1|2026-08-07|
|Analytics Generation|4.1.15|2026-07-09|
|APO - Foundation|2.0.0|2026-09-10|
|APO - Prime|2.0.0|2026-09-10|
|App Engine - Prime|30.1.1|2026-09-10|
|App Generation|28.3.12|2026-07-09|
|App Life Cycle AI Agents|29.5.2|2026-08-07|
|App Summary|29.4.0|2026-07-09|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.1.2|2026-09-10|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Autonomous Engineer|30.0.0|2026-09-10|
|Build Agent Premium|1.6.0|2026-09-10|
|Business Continuity Management Advanced|2.0.3|2026-09-10|
|Business Continuity Management Foundation|2.0.3|2026-09-10|
|Care Team Operations AI agent collection|2.1.1|2026-09-10|
|Catalog Conversational Coverage|6.2.1|2026-09-10|
|Chat Recommendation|1.9.1|2026-09-10|
|Chat Summarization for Virtual Agent|1.12.7|2026-09-10|
|Cloud Cost Management Advanced|1.0.0|2026-09-10|
|CMDB MCP Server|2.0.0|2026-09-10|
|Collaborative Work Management - Advanced|2.2.1|2026-09-10|
|Common AI Framework|2.0.2|2026-08-07|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Content Understanding|7.1.4|2026-09-10|
|Contract Management Pro - Prime|1.0.21|2026-09-10|
|Conversation Evaluator|3.2.1|2026-09-10|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Conversational Catalog Requests|8.0.2|2026-09-10|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|12.0.7|2026-09-10|
|Conversational subflows and actions|30.0.4|2026-08-07|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced for Finance|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Advanced for Legal|3.3.2|2026-08-07|
|Core Business Suite Advanced for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Advanced for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite for Finance|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Human Resources|3.3.2|2026-08-07|
|Core Business Suite for Legal|3.3.2|2026-08-07|
|Core Business Suite For Source To Pay|3.3.2|2026-08-07|
|Core Business Suite For Workplace Service Delivery|3.3.3|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation for Finance|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Foundation for Legal|3.3.2|2026-08-07|
|Core Business Suite Foundation for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Foundation for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime for Finance|3.3.2|2026-08-07|
|Core Business Suite Prime for Health and Safety|3.3.3|2026-09-10|
|Core Business Suite Prime for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Prime for Legal|3.3.2|2026-08-07|
|Core Business Suite Prime for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Prime for Workplace Services|3.3.3|2026-08-07|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|3.1.0|2026-09-10|
|CPQ for Manufacturing Foundation|3.1.0|2026-09-10|
|Cryptographic Asset Compliance|1.0.2|2026-08-07|
|CSM - Advanced|2.1.2|2026-08-07|
|CSM - Foundation|2.1.2|2026-08-07|
|CSM - Prime|2.1.2|2026-08-07|
|CSM MCP Server|1.2.0|2026-08-07|
|CTO Voice AI Agents|2.1.0|2026-09-10|
|Custom App Record Summarization|30.1.1|2026-09-10|
|Customer Service Management AI agent collection|7.0.1|2026-09-10|
|Customer Service RMA AI Agents|1.1.4|2026-09-10|
|Cyber Physical Systems Control Tower Advanced|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Foundation|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Prime|1.0.2|2026-09-10|
|Cyber Physical Systems Operations Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Prime|1.0.5|2026-09-10|
|Cyber Physical Systems Security Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Security Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Security Prime|1.0.7|2026-09-10|
|Dashboard and visualization export|1.4.1|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Dynamic Guidance|28.5.1|2026-09-10|
|Employee Slate \(built for Now Assist\)|1.4.4|2026-09-10|
|Enhanced Features for IRM Enterprise|23.0.1|2026-09-10|
|Enhanced Features for IRM Professional|23.0.2|2026-09-10|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Asset Management Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for Healthcare Advanced|2.0.1|2026-09-10|
|Enterprise Data Transform|1.0.2|2026-09-10|
|External content connectors - ServiceNow Otto agent|1.2.0|2026-08-07|
|Field Service Management AI agent collection|4.1.0|2026-09-10|
|Finance and Procurement - Foundation|2.0.0|2026-09-10|
|Finance and Procurement - Prime|2.0.0|2026-09-10|
|Financial Services Operations AI agent collection|5.1.1|2026-09-10|
|Flow Designer GenAI|30.1.4|2026-09-10|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|30.0.10|2026-09-10|
|Flow Summarization|30.0.5|2026-09-10|
|Flow troubleshooting agent|1.0.12|2026-09-10|
|Form data collector|3.1.1|2026-09-10|
|FSM - Advanced|2.1.2|2026-09-10|
|FSM - Foundation|2.1.2|2026-09-10|
|FSM Scheduling AI Agent Collection|2.0.4|2026-09-10|
|FSO - Advanced|2.1.0|2026-09-10|
|FSO - Foundation|2.1.0|2026-09-10|
|FSO - Prime|2.1.0|2026-09-10|
|Generative AI Controller|15.0.3|2026-09-10|
|Google Gemini Spoke|1.6.2|2026-08-07|
|GRC Common GenAI|23.0.5|2026-09-10|
|GRC Shared GenAI|23.0.2|2026-09-10|
|Group-Action Framework|8.0.6|2026-09-10|
|Hardware Asset Management - Advanced|1.0.11|2026-09-10|
|Hardware Asset Management - Prime|1.0.13|2026-09-10|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|Health and Safety - Advanced|1.0.6|2026-07-09|
|Health and Safety - Foundation|1.0.6|2026-07-09|
|Health and Safety - Prime|1.0.6|2026-07-09|
|HR Voice AI Agents|2.3.14|2026-09-10|
|HRSD - Advanced|2.2.5|2026-09-10|
|HRSD - Foundation|2.2.5|2026-09-10|
|HRSD - Prime|2.2.5|2026-09-10|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Insights Clustering Utils|3.4.1|2026-09-10|
|Integrated Risk Management Advanced|23.0.1|2026-09-10|
|Integrated Risk Management Foundation|23.0.0|2026-09-10|
|Integrated Risk Management Prime|23.0.1|2026-09-10|
|Intelligent Approvals|3.0.10|2026-09-10|
|IRM Compliance GenAI|23.0.3|2026-09-10|
|IRM Risk GenAI|23.0.2|2026-09-10|
|IT Service Management|3.3.1|2026-09-10|
|IT Service Management Advanced|3.3.1|2026-09-10|
|IT Service Management AI agent collection|11.2.2|2026-09-18|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|ITOM - Advanced|1.1.5|2026-09-10|
|ITOM - Prime|1.2.2|2026-09-10|
|ITOM AI Agents For Service Mapping|1.4.1|2026-08-07|
|ITSM - Advanced|2.3.16|2026-09-24|
|ITSM - Foundation|2.3.16|2026-09-24|
|ITSM - Prime|2.3.16|2026-09-24|
|ITSM Autonomous Workforce|1.1.7|2026-09-18|
|ITSM L1 AI Specialist|1.1.10|2026-09-18|
|Keyboard Shortcuts AI Skills|1.0.4|2026-08-07|
|Knowledge Center|31.26.5|2026-09-10|
|Knowledge Graph|8.3.3|2026-09-10|
|Knowledge Graph Affinity Signals|1.0.1|2026-09-10|
|LEAP|4.3.1|2026-09-10|
|Legal Service Delivery - Prime|1.0.17|2026-09-10|
|List AI Experience|3.1.4|2026-08-07|
|Manage Invoice Operations|1.3.0|2026-09-10|
|Manage Order Operations|2.2.0|2026-09-10|
|Manufacturing Commercial Operations Advanced|3.1.0|2026-09-10|
|Manufacturing Commercial Operations AI agents collection|4.2.0|2026-09-10|
|Manufacturing Commercial Operations Foundation|3.1.0|2026-09-10|
|Manufacturing Commercial Operations Prime|3.1.0|2026-09-10|
|MCP for Strategic Portfolio Management|1.4.0|2026-09-10|
|Metadata Search|1.2.1|2026-09-10|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.3|2026-08-07|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.6.0|2026-07-09|
|Model Context Protocol Client|2.4.4|2026-09-10|
|Model Context Protocol Server|1.8.0|2026-09-10|
|Notifications Email Agents|3.0.2|2026-09-10|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Prompt Assistance|6.0.7|2026-09-10|
|observ-ai-agents-app|6.3.1|2026-09-10|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|23.0.1|2026-09-10|
|Operational Sustainability Management Prime|23.0.3|2026-09-10|
|OT Asset Management Advanced|2.0.1|2026-09-10|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|PA AI Tools|1.0.4|2026-09-10|
|Platform AI Agents and Skills|14.0.10|2026-09-10|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.3.1|2026-09-10|
|Privacy Management Advanced|23.0.2|2026-09-10|
|Privacy Management Prime|23.0.2|2026-09-10|
|prompt-management|2.0.6|2026-07-09|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|2.0.4|2026-09-10|
|Query Generation|6.3.1|2026-09-10|
|Query Orchestrator|2.1.3|2026-09-10|
|Quote AI agent|3.0.8|2026-09-10|
|RAG for code generation|1.1.14|2026-09-10|
|Recommended Actions for Security Operations|2.3.6|2026-09-10|
|RSM - Advanced|2.0.0|2026-09-10|
|RSM - Foundation|2.0.0|2026-09-10|
|RSM - Prime|2.0.0|2026-09-10|
|Sales and Order Management for Technology Provider - Advanced|1.0.8|2026-09-10|
|Sales and Order Management for Technology Provider - Prime|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications - Advanced|2.3.2|2026-09-10|
|Sales and Order Management for Telecommunications - Prime|2.3.2|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.9|2026-09-10|
|Sales Development AI Agents|1.0.12|2026-09-10|
|Screen Summarization|1.2.6|2026-08-07|
|Security Incident Response - Advanced|1.0.10|2026-09-10|
|Security Incident Response - Foundation|1.0.10|2026-09-10|
|Security Incident Response - Prime|1.0.10|2026-09-10|
|Service Catalog AI Core|1.0.2|2026-09-10|
|Service Exchange - Advanced|1.1.13|2026-08-13|
|Service Exchange - Foundation|1.1.13|2026-08-13|
|Service Exchange - Prime|1.1.13|2026-08-13|
|ServiceNow AI Lens|8.1.1|2026-09-10|
|ServiceNow Otto Agents for requestor|3.7.6|2026-09-10|
|ServiceNow Otto AI Agents|9.0.11|2026-09-18|
|ServiceNow Otto AI web agent|33.0.3|2026-09-10|
|ServiceNow Otto context menu|3.9.2|2026-09-24|
|ServiceNow Otto Conversational Data Collection|10.2.22|2026-09-10|
|ServiceNow Otto for Accounts Payable Operations \(APO\)|9.0.0|2026-09-10|
|ServiceNow Otto for AI Control Tower|24.0.4|2026-09-10|
|ServiceNow Otto for AI Search|18.0.5|2026-09-10|
|ServiceNow Otto for AIRC|23.0.1|2026-09-10|
|ServiceNow Otto for App Engine|30.1.1|2026-09-10|
|ServiceNow Otto for Automation Center|1.3.0|2026-08-07|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Cloud Cost Management|1.0.0|2026-09-10|
|ServiceNow Otto for Code|28.5.32|2026-09-10|
|ServiceNow Otto for Collaborative Work Management \(CWM\)|7.0.2|2026-09-10|
|ServiceNow Otto for Configuration Management Database \(CMDB\)|4.4.1|2026-09-10|
|ServiceNow Otto for Contract Analysis|1.0.15|2026-08-07|
|ServiceNow Otto for Contract Management Pro|2.5.2|2026-09-10|
|ServiceNow Otto for Conversational Spokes|1.1.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for CPQ|1.1.8|2026-09-10|
|ServiceNow Otto for Creator|30.0.1|2026-09-10|
|ServiceNow Otto for CSM Complaint Case|2.2.1|2026-08-07|
|ServiceNow Otto for CSM Major Issue Management|1.2.4|2026-08-07|
|ServiceNow Otto for Customer Service Management \(CSM\)|15.0.1|2026-09-10|
|ServiceNow Otto for Digital End-user Experience \(DEX\)|5.2.10|2026-09-18|
|ServiceNow Otto for Document Voice|2.0.11|2026-09-10|
|ServiceNow Otto for Employee Experience|4.4.3|2026-08-07|
|ServiceNow Otto for Enterprise Architecture \(EA\)|7.5.2|2026-08-07|
|ServiceNow Otto for Enterprise Asset Management|2.0.1|2026-09-10|
|ServiceNow Otto for Error Framework|1.2.0|2026-09-10|
|ServiceNow Otto for Field Service Management|11.1.2|2026-09-10|
|ServiceNow Otto for Finance and Procurement|8.0.0|2026-09-10|
|ServiceNow Otto for Financial Services Operations \(FSO\)|4.1.1|2026-09-10|
|ServiceNow Otto for Hardware Asset Management|5.0.1|2026-09-10|
|ServiceNow Otto for Health and Safety|1.5.1|2026-08-07|
|ServiceNow Otto for HR Service Delivery \(HRSD\)|13.5.2|2026-09-10|
|ServiceNow Otto for HRSD - Galileo Inside|2.3.7|2026-09-10|
|ServiceNow Otto for ICW|1.1.0|2026-08-07|
|ServiceNow Otto for Impact|6.0.6|2026-09-10|
|ServiceNow Otto for Integrated Risk Management|23.0.4|2026-09-10|
|ServiceNow Otto for Integration Hub|2.3.2|2026-08-07|
|ServiceNow Otto for IT Operations Management \(ITOM\)|2.9.4|2026-09-10|
|ServiceNow Otto for IT Service Management \(ITSM\)|17.2.4|2026-09-24|
|ServiceNow Otto for Knowledge Management|31.6.6|2026-09-10|
|ServiceNow Otto for Legal Service Delivery|1.9.7|2026-09-10|
|ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)|4.2.0|2026-09-10|
|ServiceNow Otto for Operational Sustainability|23.0.1|2026-09-10|
|ServiceNow Otto for Opportunity Management|1.2.0|2026-09-10|
|ServiceNow Otto for Order Management|2.3.3|2026-09-10|
|ServiceNow Otto for OT Service Management|3.1.5|2026-08-07|
|ServiceNow Otto for Platform|13.0.1|2026-09-10|
|ServiceNow Otto for Platform Advanced|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Foundation|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Prime|3.0.1|2026-09-10|
|ServiceNow Otto for Privacy Management|23.0.2|2026-09-10|
|ServiceNow Otto for Process Mining|4.1.5|2026-09-10|
|ServiceNow Otto for Public Sector Digital Services \(PSDS\)|2.5.3|2026-09-10|
|ServiceNow Otto for Purchase Order Management \(POM\)|1.4.1|2026-09-10|
|ServiceNow Otto for Retail Service Management|2.0.0|2026-09-10|
|ServiceNow Otto for RPA Hub|5.1.1|2026-08-07|
|ServiceNow Otto for Sales and Order Management for Telecommunications|4.3.3|2026-09-10|
|ServiceNow Otto for Sales Automation|1.1.7|2026-09-10|
|ServiceNow Otto for Security Incident Response \(SIR\)|6.5.2|2026-09-10|
|ServiceNow Otto for Security Incident Response Integration Toolkit|1.2.5|2026-08-07|
|ServiceNow Otto for Service Exchange|1.1.12|2026-08-13|
|ServiceNow Otto for Service Quality|2.2.0|2026-09-10|
|ServiceNow Otto for Setup|5.0.20|2026-09-10|
|ServiceNow Otto for Setup Core|4.0.20|2026-09-10|
|ServiceNow Otto for Smart Assessment Engine|23.0.6|2026-09-10|
|ServiceNow Otto for Software Asset Management \(SAM\)|11.0.0|2026-09-10|
|ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)|11.0.0|2026-09-10|
|ServiceNow Otto for Spoke Generation|2.0.1|2026-08-07|
|ServiceNow Otto for Strategic Portfolio Management|9.11.0|2026-09-10|
|ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)|9.0.1|2026-09-10|
|ServiceNow Otto for Talent|1.9.2|2026-08-07|
|ServiceNow Otto for Telecommunications Service Management|2.3.1|2026-09-10|
|ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)|6.0.15|2026-09-10|
|ServiceNow Otto for Third-Party Risk Management|23.0.5|2026-09-10|
|ServiceNow Otto for Threat Intelligence Security Center|2.6.1|2026-09-10|
|ServiceNow Otto for Unified Security Exposure Management|5.2.3|2026-08-07|
|ServiceNow Otto for Vault|3.0.0|2026-09-10|
|ServiceNow Otto for Virtual Agent Configurations|16.0.5|2026-08-20|
|ServiceNow Otto for Voice Agents|6.0.5|2026-09-10|
|ServiceNow Otto for WDF|2.3.4|2026-08-07|
|ServiceNow Otto for Workplace Service Delivery \(WSD\)|1.1.20|2026-08-07|
|ServiceNow Otto for Wrap Up|1.0.4|2026-08-07|
|ServiceNow Otto for Zero Copy Connector|2.0.6|2026-08-07|
|ServiceNow Otto in Document Management|4.0.11|2026-09-18|
|SLO - Foundation|2.0.2|2026-09-10|
|SLO - Prime|2.0.0|2026-09-10|
|Software Asset Management AI Advanced|2.5.0|2026-09-10|
|Software Asset Management AI Prime|2.5.0|2026-09-10|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SOM for Manufacturing Advanced|3.1.0|2026-09-10|
|SOM for Manufacturing Prime|3.1.0|2026-09-10|
|SPO - Foundation|2.0.0|2026-09-10|
|SPO - Prime|2.0.0|2026-09-10|
|Standard ticket page summarization|1.3.3|2026-08-07|
|Strategic Portfolio Management - Advanced|1.3.0|2026-09-10|
|Strategic Portfolio Management - Prime|1.2.0|2026-09-10|
|Summarization for Order Management|2.2.4|2026-09-10|
|Task Plan Template AI Agents|2.0.1|2026-09-10|
|Technology Advanced|1.0.12|2026-09-10|
|Technology Foundation|1.0.15|2026-09-10|
|Technology Prime|1.0.12|2026-09-10|
|Telecommunications Advanced|2.3.1|2026-09-10|
|Telecommunications Foundation|2.3.1|2026-09-10|
|Telecommunications Prime|2.3.1|2026-09-10|
|Telecommunications, Media and Technology - Advanced|1.0.11|2026-09-10|
|Telecommunications, Media and Technology - Foundation|1.0.13|2026-09-10|
|Telecommunications, Media and Technology - Prime|1.0.11|2026-09-10|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Management Advanced|23.0.3|2026-09-10|
|Third-party Risk Management Professional Plus|23.0.3|2026-09-10|
|Threat Intelligence Security Center - Advanced|3.3.1|2026-09-10|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|TSOM - Advanced|2.3.0|2026-09-10|
|TSOM - Prime|2.3.0|2026-09-10|
|UI Generation|29.2.5|2026-05-05|
|Unified Security Exposure Management \(USEM\) - Advanced|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Foundation|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Prime|2.2.3|2026-08-07|
|Voice input for Now Assist|1.5.0|2026-07-09|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|Zero Touch Service Desk|3.2.8|2026-09-18|


---
title: June 16 2026 Now Assist Suite release notes
description: Now Assist Suite version and compatibility information for the June 16 2026 release on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/na-suite-rn-2026-06-16.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 299
breadcrumb: [Now Assist Suite - June 2026 release notes, Now Assist Suite release notes]
---

# June 16 2026 Now Assist Suite release notes

Now Assist Suite version and compatibility information for the June 16 2026 release on the ServiceNow Store.

Note: Now Assist Suite versions are cumulative. For app version updates that have been carried forward from previous releases, refer to the release notes page for the application's "Last updated" date or the ServiceNow Store app listing. See [Now Assist suite versions in the Application Manager](https://www.servicenow.com/docs/r/platform-administration/application-manager/now-assist-suites-app-mgr.html) for more details.

## Suite version 29.0.20260611 - Australia Patch 0

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Agentic Desktop

</td><td>

1.0.0

</td><td>

New:-   Design desktop actions of type UI block by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block that include pre-built connectors to interact with various applications and system components.
-   Add the desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy and desktop applications without APIs.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session. Interact with the automation when human input is required.

</td></tr><tr><td>

AI Agents for ACC

</td><td>

1.0.0

</td><td>

Initial release of "Agent Client Collector \(ACC\) Diagnostic" agentic workflow

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.5.2

</td><td>

Fixed:-   Added roles and ACL to AI Agents
-   Fixed parsing and formatting errors across different LLMs

</td></tr><tr><td>

AI Agents for Discovery

</td><td>

1.0.2

</td><td>

New - Introducing Certificate Renewal Agent Workflow to help you renew the certificates that are nearing expiry with the help of an agent. The system tracks discovered certificates, monitors their expiry dates, creates renewal tasks for the certificates and proactively notifies PKI admin via email.Through the NowAssist panel in the Certificate Management workspace, administrators can engage with the agentic workflow with the usage of natural language conversation.

-   This intelligent agent allows the PKI admin to check for certificates nearing expiry with just a simple prompt and can initiate their renewal with minimal interaction.
-   By delegating these tasks to the agent, administrators can significantly reduce manual effort and time spent on renewals.
-   This real-time capability helps prevent certificate outages, streamlines certificate management, and ensures organizations can adapt to shorter renewal cycles.
-   Also in this process it auto-generates CSR and stores the private key in community edition of Hashi-Corp vault \(The auto generation of CSR is supported fromYP8 onwards\)

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.0.3

</td><td>

Updated to support the latest version of the dependent app.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

3.0.1

</td><td>

With the Now Assist for Hardware Asset Management \(HAM\) application, Hardware Asset Managers can streamline and automate the process of sourcing hardware assets by using AI agents included in the agentic workflow. The Now Assist for Hardware Asset Management \(HAM\) application contains agentic workflows to automate the sourcing, transfer, and procurement of assets upon request.

 -   Role masking in AI Agent Studio to execute agentic workflows, AI agents, and tools.
-   New security configuration pages in AI Agent Studio.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Store episodic memory of agentic conversations with agent learning.
-   Create and update UI actions for workflows.
-   Framework extensibility with new condition builder.
-   Add Desktop action as a tool to an AI agent.
-   Support for multilingual conversations.
-   MCP Client enhancements

</td></tr><tr><td>

AI agents for Observability

</td><td>

3.1.3

</td><td>

Added role mask of \`evt\_mgmt\_operator\` to all workflows and agents.

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.0.3

</td><td>

-   New:
    -   Workplace Insights for key indicators like floor utilization, attendance, reservation no-shows, and space inefficiencies are generated and surfaced on the landing dashboard in Workplace Central. Introduced a new Workplace Insights AI Skill that analyzes the data and generates the insights.
    -   Workplace Reservation Q and A Agent: Workplace Managers can ask natural language questions related to reservations from the Now Assist Panel and receive responses
-   Fixed:
    -   Sometimes, the reservation details could not be extracted from the case number when using the "Help manage workplace reservations" workflow
    -   Security fixes

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

2.0.1

</td><td>

No new changes

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

AIOps LEAP

</td><td>

2.3.2

</td><td>

December 2025 Release updates -

 -   LLM Models:Supporting Now-LLM LTS as a fifth model provider \(built with GPT-OSS and Apriel models\)
-   Platform mandated component updates
-   Quality and stability improvements

</td></tr><tr><td>

Alert Assist

</td><td>

3.5.2

</td><td>

Fixed: Added roles and ACL to skills

</td></tr><tr><td>

Analytics Generation

</td><td>

4.0.3

</td><td>

-   Skill moved under Data and Analytics Workflow \(Analytics product\) in Now Assist Admin
-   Extended querying capabilities to support:
    -   Stacked group chart \(e.g. show tasks grouped by state and stacked by priority\)
    -   Top/bottom X questions \(e.g. show top 5 assignment groups that has most number of open incidents\)
-   Bug fix

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

</td></tr><tr><td>

Catalog Conversational Coverage

</td><td>

5.2.5

</td><td>

New

 Included tailored recommendations to help you improve your catalog items for the conversational channel, making it easier for you to identify areas that need enhancement.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.5.4

</td><td>

-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   CRR Completness Metric
-   performance improvement fix

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.8.15

</td><td>

-   Honor In-Product roles in Sidebar Chat Summarization
-   Add new skill configuration for Standalone Sidebar Discussions
-   Support selection of portal in multiple skill configs in Agent Chat Summarization
-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   Defect fixes

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

Conversation Insights

</td><td>

2.0.2

</td><td>

New: Inferred CSAT segmented by Intent Displayed in AI Agent Analytics dashboard. Display top intents for the selected agentic workflows and/or AI agents. Display average CSAT for intents of selected AI assets.

</td></tr><tr><td>

Conversational Studio

</td><td>

6.0.6

</td><td>

-   New :
    -   "Assistant" module that includes the end-to-end admin configuration for Assistants
    -   Ability to change the visibility of individual Assets per Assistant
    -   Conversational settings modal within individual Assets
    -   Ability to bulk remove Assets from Assistants
    -   Ability to create new Assets \(including AI Agents, Subflows/Actions, Custom Skills, Topic\) from the Assistant Designer
    -   Voice Assistants
-   Changed: Test panel UX update, more data available
-   Fixed:
    -   Changing asset to inactive should not clear the visibility and discoverability configs
    -   Topic migration
    -   Misc. defects

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

28.2.11

</td><td>

N/A. Initial release.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

4.0.0

</td><td>

NewCustomer 360 is an AI-powered assistant for the human agent that answers natural language questions about customers, cases, products, and interactions. This feature helps agents quickly access critical information and resolve cases.

 Changed: Role configuration is required for Agentic workflows and AI agents.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

0.1.8

</td><td>

New application

</td></tr><tr><td>

Document Intelligence for Contract Management Content Pack

</td><td>

1.3.1

</td><td>

New: Added a predefined use case for the Obligation Extraction skill that includes definitions for extracting two distinct categories of obligations from contracts.

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

1.0.3

</td><td>

Create work order from text in NAP and NAVA.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New:-   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Flow Designer GenAI

</td><td>

28.2.3

</td><td>

New: Users will have an option to call an agent from workflow

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

GRC Common GenAI

</td><td>

21.1.8

</td><td>

-   New:
    -   Issue Submission Agent:
    -   The issue submission AI agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.
-   Changed:

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

21.1.8

</td><td>

-   New
    -   Control objective impact analyzer: This Gen AI skill analyzes changes in citations and identifies control objectives that should be reviewed based on the modified citation content.
    -   Control objective detail updater: For a given control objective, validate whether the description and supplemental guidance needs to be updated based on associated citations, and suggest new content when updates are required. This skill is triggered only by the AI agent, Control objective change agent.
    -   Control objective change agent: This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates.
    -   Enabled Now LLM LTS and Role masking support for the recommendation of similar control objectives and common control objective creation skills.
    -   Control objective requirements and control requirements are now considered in the Rationalization process for control objectives.
-   Changed: Rationalization process now automatically generates recommendations using the skill when you select Rationalize button in the Control objective page.

</td></tr><tr><td>

HR Service Delivery AI agent collection

</td><td>

5.0.9

</td><td>

-   New:
    -   Help resolve tuition reimbursement requests agentic workflow supports the post-completion reimbursement process. It automatically evaluates employee-submitted grades, transcripts, and documentation against company policies and returns a decision of approval, denial, or request for additional information
    -   Generate onboarding ramp-up plan workflow - Performance improvements for faster creation and manager review
    -   Resolve Non Critical HR Cases - Predicts the criticality of the HR case and sends the response to the employee if the HR case is non critical.
    -   Predict Service and Transfer HR cases - Predict the correct HR Service of the HR Case.
    -   Resolve Critical HR Cases - Provides the ability for the HR Agents to generate a step by step plan
-   Enhanced:
    -   Help resolve tuition requests agentic workflow - Performance improvements for faster policy evaluation and case resolution
    -   Security - Implemented role masking to strengthen AI agent security and protect sensitive employee information

</td></tr><tr><td>

HR Talent AI Agent Collection

</td><td>

3.0.0

</td><td>

Whats New The Employee feedback collection AI Agent streamlines the process of gathering employee feedback, ensuring managers receive timely, structured, and actionable input. Persona: ManagerThe agent:

 -   Suggests relevant collaborators of the employee using data from Employee Profile, Talent Development apps, and optional Microsoft Graph interaction insights \(using the Microsoft Exchange Online spoke\)
-   Sends requests as EC To-Dos for the feedback providers and sends automated reminders
-   Consolidates all feedback responses into a single view for easier evaluation

 Updates

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.0.5

</td><td>

No functional changes, only updates for Dec platform agents

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

21.1.6

</td><td>

New:-   Use AI-generated recommendations to identify which policies are impacted by a regulatory alert
-   Use the Get Regulatory Insights agentic workflow to enrich regulatory alerts with external context, classification, summarization, and recommended potentially impacted items
-   Use the Generate Regulatory Action Plan agentic workflow to convert regulatory insights into actionable compliance strategies, including structured tasks with clear ownership and timelines

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

21.1.6

</td><td>

\[New\] Now LLM LTS and Role masking support are now enabled for risk event summarization

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

5.0.3

</td><td>

See the Now Assist for IT Service Management \(ITSM\) release notes for more information.

New:-   Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow: ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent
-   Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow: Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent
-   Masking roles for controlled access to agentic workflows, AI agents, and skills

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.1.4

</td><td>

Now Assist for ITSM release notes \[Zurich\]

New: Initial release for ITSM Voice AI agent. See the Key features section for more details.

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.2.5

</td><td>

Changed: Added compatibility with the "Now Assist for Platform" app, version 10.0.3

</td></tr><tr><td>

Knowledge Center

</td><td>

31.0.8

</td><td>

The Knowledge Center centralized hub for Knowledge Admin and Manager:

 1. Is an entry point for KM Management personas to manage all capabilities and configurations 2. Guides users on the next-best actions to take by displaying actionable key insights 3. Is a suite of KM Tools for suggesting content creation, updates, duplicates, and article retirement

</td></tr><tr><td>

Manage Order Operations

</td><td>

1.0.2

</td><td>

Initial Release:

 -   Automate the process of creating order cases on the Business Portal.
-   Retrieve customer inputs in text or voice format, classify intent, and route them to the Virtual Agent for action.
-   Identify the earliest possible delivery date for expedited product delivery on a specific customer order.
-   Create an order case autonomously based on the inputs on the Now Assist panel.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.4.7

</td><td>

New:-   Long-Term Support \(LTS\) model that delivers regulatory alignment, predictable behavior, and lifecycle stability is now supported.
-   Added role based access control to the generation skill of mobile card.This access control only allows specific roles of delegated\_developer and sn\_mab\_api.admin to generate the mobile card.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

1.2.4

</td><td>

-   PRM\(Protected Resource Metadata\) support for MCP servers
-   reduced latency for few MCP servers

</td></tr><tr><td>

Notifications Email Agents

</td><td>

1.0.7

</td><td>

New: The email agentic workflow introduces enhanced capabilities to intelligently process incoming emails by:

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

</td></tr><tr><td>

Now Assist Analytics

</td><td>

3.0.5

</td><td>

Monitor usage, adoption, and engagement factors for Virtual Agent interactions and Now Assist panel engagements via AI Engagement Analytics.

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed: AI skill execution is now performed off glide

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

28.2.7

</td><td>

New: Use the custom app record summarization skill to generate AI summaries for tables in custom applications. You can generate summaries in-product and through chat in the Now Assist panel.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

4.0.1

</td><td>

-   New: Agile team members can now use Now Assist to generate acceptance criteria for a story based on the short description and description
-   Fixed: Performance improvement of Now Assist skills in CWM
-   Deprecated/Removed

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

2.5.2

</td><td>

Fixed: Security fixes

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

11.0.3

</td><td>

-   New
    -   Use the trending topics dashboard to get a comprehensive view of trending topics across cases, along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and see more into specific trends using customizable filters.
    -   Use sentiment trends analysis to access a unified view of customer sentiment across cases, accounts, and live agent interactions. The dashboard uses LLM-powered insights to explain sentiment changes and lets you see more to find root causeshelping teams take targeted actions that improve customer satisfaction.
    -   Use the activity response generation skill to automatically generate recommendations for work notes and comments. This feature helps agents quickly add meaningful updates to case records, improving efficiency, and interaction quality.
    -   Availability of Now Assist Context Menu Config setup for extended tables within resolution notes.
-   Changed
    -   Added sentiment scoring to both the case record page and list view across cases. The sentiment scale ranges from very positive, positive, neutral, negative to very negative.
    -   Skills cloned in Now Assist Admin console \(NAA\) can now be edited in Now Assist Skill Kit \(NASK\). This allows users to add headers, configure prompts, and manage GenAI skills in one location. The migration supports case summarization, resolution notes generation, and sentiment analysis.
    -   Define trigger step has been added to the case summarization flow that provides the option to choose how the skill will be triggered - User Trigger and Automatic.
    -   Enhanced email response skill with the option to generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

3.0.10

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Environmental, Social, and Governance \(ESG\)

</td><td>

21.1.6

</td><td>

New: Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions. The carbon calculations agentic workflow acts as a copilot for sustainability teams, streamlining carbon accounting workflows. It intelligently selects metric definitions and emission factors from the library, generates calculated metric definitions, and allows users to review and make adjustments before final use.

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

8.0.5

</td><td>

-   Added new feature to create work order from text in NAP and NAVA.
-   Included Smart Assessment / Questionnaire summary in work order task summarization.

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

5.0.0

</td><td>

New: Changed Prompt migration to NASK: Summarization skill prompts have been migrated into the Now Assist Skill Kit \(NASK\), enabling admins to configure, modify, and maintain summarization skills using the new OOB editable experience. This update preserves full administrative control while aligning skills to the modern, centralized prompt management framework.

</td></tr><tr><td>

Now Assist for Hardware Asset Management

</td><td>

3.0.1

</td><td>

In this release, users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

 -   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent
-   Hardware asset repair process \(patch\)

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

12.0.7

</td><td>

New / enhancements- The case summarization skill is enabled for the attachment summaries

 - The resolution notes skill is enabled with NACM for the shortening/elaborating resolution notes summary

 - On the Agent Workspace application, the resolution notes skill is enabled to auto-populate Close notes field

 Changed:

 - Enhanced security features revisit the ACL roles and access;Support to GPT OSS model

</td></tr><tr><td>

Now Assist for Impact

</td><td>

2.0.18

</td><td>

Consumption Report summary

 -   Produces an insightful, human-readable summary which highlights key business objectives with active and completed initiatives and accelerators.
-   The summary flags any concerning trends in severity \(P1/P2 dominance\).
-   It also reviews premium seat utilization and provides recommendations.
-   Ability to provide Feedback for the summary
-   Ability to refresh the summary
-   Ability to Copy summary

 Code Fix AI agent

 -   Eliminates technical debt backlog by deploying an embedded AI agent within the script editor that identifies issues in real-time and generates intelligent code fixes through Now Assist integration.\_
-   Removes specialized expertise barriers by enabling developers to interact conversationally with the AI agent for code modifications and apply or reject suggested fixes with feedback mechanisms.\_
-   Maintains development velocity by allowing immediate technical debt resolution within existing workflows without context switching or requiring specialized knowledge.

</td></tr><tr><td>

Now Assist for IRM

</td><td>

21.1.6

</td><td>

\[New\]

 Issue submission agent:

 The Issue Submission agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.

 Check product documentation for activation details.

 Suggest potential risks agentic workflow

 -   AI-driven risk identification Conversational AI automatically analyzes entity context and surfaces relevant risks from internal libraries, industry patterns, and optional external sources.
-   Consolidated risk view Generates a single, ready-to-triage risk list, reducing manual effort and duplication while ensuring comprehensive coverage.
-   Guided user experience Embedded in the Now Assist Panel, the workflow provides step-by-step guidance for risk domain selection, simplifying complex risk discovery.
-   Proactive intelligence for emerging risks External scanning capabilities deliver early warnings of new threats, helping organizations stay ahead of evolving regulations and trends.

 Control objective impact analyzer:

 The citation-driven impacted control objective identifier uses generative AI to analyze changes in citations and identify control objectives that should be reviewed based on the modified citation content. It intelligently matches changed citation requirements with existing COs to suggest potential updates, helping teams maintain alignment between citations and control objectives.

 Control objective change agent:

 This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates. Users can review and approve AI-suggested changes directly within the workflow, ensuring that control objectives always reflect the most current regulatory requirements and best practices.

 \[Changed\]

 -   Removed the issue summarization step from the issue resolution agentic workflow as part of performance improvements.
-   Added support for LTS models for previously released Now Assist IRM skills.
-   Enhanced security by implementing role masking.
-   Rationalization process now auto-generates recommendations using the skill when the Rationalize button is clicked on a control objective.
-   Added a quick summary view for each recommendation card and clarified task sequence during the analyze step of the rationalization process.
-   Control objective requirements and control requirements are now considered in the rationalization process for control objectives.

 \[Fixed\]

 -   Implemented a fix to skip redundant approvals in the rationalization process.
-   Resolved issues related to synchronizing impacted items and automatic refreshes.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

2.4.5

</td><td>

New:-   AI Agents for MID Server
-   AI Agents for ACC

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

12.0.6

</td><td>

See the Now Assist for IT Service Management \(ITSM\) release notes for more information.

 -   New -
    -   Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit
    -   Expanding attachment summarization capabilities to include additional document formats and language
    -   Creating a knowledge article in any incident state
    -   Edit a knowledge article when one article is attached to an incident
    -   Generating resolution notes using the Now Assist context menu
    -   Generating an activity response using the Now Assist context menu
    -   Selecting the desired knowledge base and template for creating knowledge articles using the new knowledge article interceptor page
    -   Masking roles for controlled access to agentic workflows, AI agents, and skills
-   Changed - For new users, some skills are active by default. For information, see Now Assist for IT Service Management \(ITSM\) release notes.
-   Fixed - n/a
-   Removed - n/a

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

Now Assist for Platform

</td><td>

10.0.3

</td><td>

Changed: Updated release dependencies

</td></tr><tr><td>

Now Assist for Platform for Requestor

</td><td>

2.0.6

</td><td>

-   Changed: Updated app dependencies
-   Fixed: App title is Now Assist for Platform for Requestor

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

21.1.4

</td><td>

New: Now Assist for Privacy Management leverages Gen AI to streamline privacy workflows by summarizing risk assessments, condensing issue details, and identifying and merging redundant control objectives into a common control objective.

</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

1.2.4

</td><td>

Now LLM LTS Support

 Java 21 Compliant

 Security Directive Compliance

</td></tr><tr><td>

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for RSM

</td><td>

1.2.0

</td><td>

Now Assist for Retail Service Management \(RSM\) highlights for the Zurich release The Store Inquiry AI agent enables retail HQ teams by:

-   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed: Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

8.0.0

</td><td>

New: Quote-to-request automation: Employees no longer need to manually copy information from vendor quotes into procurement request forms.They can now upload a quote file, and the system automatically extracts key details, such as supplier information, item descriptions, quantities, and pricing, to pre-fill the appropriate request form for quick review and submission.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.6.1

</td><td>

Non Glide Cobalt Raven ACLs added.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

8.0.0

</td><td>

Enhanced

 -   Project Insights Generation- Automatically track critical project signals such as delayed milestones, resource constraints, and task slippages and receive proactive insights either on a scheduled cadence or on-demand
-   Agile story generation - Convert epics into high-quality, actionable user stories faster and more intelligently through an improved, agentic, context-aware flow
-   New
    -   Acceptance criteria generation - Produce clear, consistent, and context-aware acceptance criteria using predefined templates and story-specific information
    -   Target generation - Generate measurable targets from goals information and optional context and automatically populate key fields in the target creation form
    -   Identify similar demands - Identify existing or related demand records during creation or editing to avoid duplication and ensure better demand hygiene

</td></tr><tr><td>

Now Assist for Talent

</td><td>

1.5.1

</td><td>

Implemented several directive changes.

</td></tr><tr><td>

Now Assist for Third-Party Risk Management

</td><td>

21.1.5

</td><td>

New: TPRM Issue summarization skill to enable third-party risk managers and assessors to review and edit AI summaries.

</td></tr><tr><td>

Now Assist for Voice

</td><td>

2.0.9

</td><td>

Now Assist Voice AIA 2.0 release notes Overview Now Assist Voice AIA transforms traditional Interactive Voice Response \(IVR\) systems into intelligent, conversational AI experiences. This application integrates with Contact Center as a Service \(CCaaS\) platforms to deliver natural, secure, and scalable voice interactions for enterprise workflows. Natural Voice Conversations Secure Authentication Framework CCaaS Integration Multi-lingual Support Voice AI Agent Configuration Analytics and Monitoring Business Benefits

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.5

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New:-   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

2.0.5

</td><td>

-   New
    -   Configurable AI powered obligation extraction to automatically extract key contractual obligations from contract documents for user to review and approve.
    -   Now Assist powered conversational search to query contract documents using natural language and dialogue driven queries
-   Fixed: The Question Group card component now appears correctly when creating or editing Contract analysis use cases in the Now Assist Admin console.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Knowledge Management

</td><td>

29.4.11

</td><td>

1. Knowledge Gaps

 2. Article optimization

 3. Create/update article using custom instructions

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New:-   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Now Assist in Virtual Agent Configurations

</td><td>

8.0.7

</td><td>

N/A

</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

2.3.2

</td><td>

Defect fixes

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

8.0.13

</td><td>

-   Changed
    -   Skill Search &amp; AIS Logging: Add backend support for metadata logging during skill search and execution.
    -   Remove OneExtend for LLAMA/GPT-4o: Eliminate follow-up logic for these models to simplify execution.
    -   Refactor Data Collector: Modularize into JavaScript files using Fluent for better structure and localization.
    -   Entity Extraction API \(Level 1\): Plan initial API for automated skill evaluation.
    -   Synthesized Response in Text Input: Enable text input to accept synthesized responses.
    -   Agentic Slot Fill Discovery: Use agentic slot fills when available to improve accuracy.
    -   Skippable Input Collector: Support skippable inputs and hide skip button dynamically.
-   Fixed: Fixed the defects to improve performance, slot-filling issues, catalog flows, dynamic translation, VA Designer test panel crashes, and other defects.

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Recommendation template

</td><td>

21.1.3

</td><td>

-   Changed
    -   Updated the quick summary view for each recommendation card.
    -   Clarified the sequence of tasks during the Analyze step of the Rationalization process.
-   Fixed
    -   Redundant approvals during the Rationalization process.
    -   Synchronization of impacted items and automatic refreshes.

</td></tr><tr><td>

RSM AI agent collection

</td><td>

1.2.0

</td><td>

The Store Inquiry AI agent enables retail HQ teams by:

 -   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

3.0.1

</td><td>

-   New
    -   Fill Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto fills the relevant fields in the form.
    -   Two new fields added in Lens actions to handle post processing timeout for previewing data in the standalone mode.
    -   Trigger ServiceNow AI Lens from Now Mobile application to extract data from artifacts and auto-fill forms on your mobile device.
-   Changed: The user interface of the scanner window is changed. When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

Summarization for Order Management

</td><td>

1.0.2

</td><td>

New: Order Summarization for Order Management provides agents and managers with a consolidated, role-aware, and stage-specific view of all key order information across the order lifecycle. Built on Now Assist record summarization capabilities, this feature eliminates the need to navigate multiple pages or manually piece together order details, task progress, and risks. Integrated directly into the Order Management workspace starting in Q4, Order Summarization empowers agents to understand an orders status, history, risks, and progress at a glancemaking it easier to take action, hand off work, or pick up in-progress orders without searching across multiple records or tabs.

</td></tr><tr><td>

Test Generation

</td><td>

4.0.11

</td><td>

Changed:-   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|2.1.4|2026-01-20|
|Agentic Desktop|1.0.0|2025-12-11|
|AI Agents for ACC|1.0.0|2025-12-11|
|AI Agents for AIOps|1.5.2|2025-12-11|
|AI Agents for Customer Success Management|2.6.6|2026-01-20|
|AI Agents for Discovery|1.0.2|2025-12-11|
|AI Agents for Employee Experience|2.0.3|2025-12-11|
|AI Agents for Health and Safety|1.2.0|2026-01-20|
|AI Agents for ITAM|3.0.1|2025-12-11|
|AI agents for Observability|3.1.3|2025-12-11|
|AI Agents for Service Exchange Provider|1.0.5|2026-02-05|
|AI Agents for Workplace Service Delivery|3.0.3|2025-12-11|
|AI Control Tower for Now Assist|2.0.1|2025-12-11|
|AI Data Explorer|3.0.14|2026-03-12|
|AIOps LEAP|2.3.2|2025-12-11|
|Alert Assist|3.5.2|2025-12-11|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.0.3|2025-12-11|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Build Agent Premium|1.0.14|2026-03-12|
|Catalog Conversational Coverage|5.2.5|2025-12-11|
|Chat Recommendation|1.5.4|2025-12-11|
|Chat Summarization for Virtual Agent|1.8.15|2025-12-11|
|Conversation Evaluator|2.0.5|2026-01-20|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|2.0.2|2025-12-11|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|6.0.6|2025-12-11|
|Conversational subflows and actions|28.2.7|2026-01-06|
|Custom App Record Summarization|28.2.11|2025-12-11|
|Customer Service Management AI agent collection|4.0.0|2025-12-11|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|0.1.8|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.3.1|2025-12-11|
|Field Service Management AI agent collection|1.0.3|2025-12-11|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|28.2.3|2025-12-11|
|Flow Generation|29.0.4|2026-03-12|
|Flow Summarization|29.0.3|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|12.0.17|2026-03-12|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|21.1.8|2025-12-11|
|GRC Shared GenAI|21.1.8|2025-12-11|
|Group-Action Framework|5.0.5|2026-05-05|
|HR Service Delivery AI agent collection|5.0.9|2025-12-11|
|HR Talent AI Agent Collection|3.0.0|2025-12-11|
|HR Voice AI Agents|2.0.5|2025-12-11|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|1.0.5|2026-05-05|
|IRM Compliance GenAI|21.1.6|2025-12-11|
|IRM Risk GenAI|21.1.6|2025-12-11|
|IT Service Management AI agent collection|5.0.3|2025-12-11|
|IT Service Management AI voice agent collection|1.1.4|2025-12-11|
|ITOM AI Agents For Service Mapping|1.2.5|2025-12-11|
|Knowledge Center|31.0.8|2025-12-11|
|Knowledge Graph|6.0.7|2026-04-09|
|List AI Experience|1.1.14|2026-01-20|
|Manage Order Operations|1.0.2|2025-12-11|
|Manufacturing Commercial Operations AI agents collection|1.0.1|2025-12-11|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.9.0|2026-03-12|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.7|2025-12-11|
|Model Context Protocol Client|1.2.4|2025-12-11|
|Model Context Protocol Server|1.1.3|2026-01-22|
|Notifications Email Agents|1.0.7|2025-12-11|
|Now Assist Admin Console|7.0.19|2026-02-05|
|Now Assist Agents for requestor|3.0.9|2026-01-20|
|Now Assist AI Agents|6.0.25|2026-03-19|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|3.0.5|2025-12-11|
|Now Assist context menu|3.1.1|2026-01-22|
|Now Assist Data Kit|6.0.8|2026-01-20|
|Now Assist for Accounts Payable Operations \(APO\)|6.0.2|2026-03-12|
|Now Assist for App Engine|28.2.7|2025-12-11|
|Now Assist for code generation|28.5.13|2026-03-12|
|Now Assist for Collaborative Work Management \(CWM\)|4.0.1|2025-12-11|
|Now Assist for Complaint Case \(CSM\)|1.0.3|2026-02-05|
|Now Assist for Configuration Management Database \(CMDB\)|2.5.2|2025-12-11|
|Now Assist for Creator|29.0.1|2026-03-12|
|Now Assist for Customer Service Management \(CSM\)|11.0.3|2025-12-11|
|Now Assist for Digital End-user Experience \(DEX\)|4.1.2|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|3.0.10|2025-12-11|
|Now Assist for Enterprise Architecture \(EA\)|7.0.3|2026-01-20|
|Now Assist for Environmental, Social, and Governance \(ESG\)|21.1.6|2025-12-11|
|Now Assist for Field Service Management \(FSM\)|8.0.5|2025-12-11|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|5.0.0|2025-12-11|
|Now Assist for Hardware Asset Management|3.0.1|2025-12-11|
|Now Assist for Health and Safety|1.2.0|2026-01-20|
|Now Assist for HR Service Delivery \(HRSD\)|12.0.7|2025-12-11|
|Now Assist for Impact|2.0.18|2025-12-11|
|Now Assist for IRM|21.1.6|2025-12-11|
|Now Assist for IT Operations Management \(ITOM\)|2.4.5|2025-12-11|
|Now Assist for IT Service Management \(ITSM\)|12.0.6|2025-12-11|
|Now Assist for Legal Service Delivery|1.5.6|2026-01-20|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|1.0.1|2025-12-11|
|Now Assist for Order Management|1.0.1|2026-01-20|
|Now Assist for Platform|10.0.3|2025-12-11|
|Now Assist for Platform for Requestor|2.0.6|2025-12-11|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|21.1.4|2025-12-11|
|Now Assist for Process Mining|3.0.6|2026-03-12|
|Now Assist for Prompt Assistance|2.0.7|2026-01-20|
|Now Assist for Public Sector Digital Services \(PSDS\)|1.2.4|2025-12-11|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.2.0|2025-12-11|
|Now Assist for Sales and Order Management \(SOM\)|1.0.6|2026-01-20|
|Now Assist for Sales and Order Management for Telecommunications|1.0.2|2026-01-20|
|Now Assist for Security Incident Response \(SIR\)|4.2.1|2026-01-20|
|Now Assist for Service Exchange|1.0.5|2026-02-05|
|Now Assist for Software Asset Management \(SAM\)|6.1.1|2026-03-12|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|8.0.0|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|8.0.0|2025-12-11|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|6.0.2|2025-12-24|
|Now Assist for Talent|1.5.1|2025-12-11|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|5.1.9|2026-02-05|
|Now Assist for Third-Party Risk Management|21.1.5|2025-12-11|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|2.0.9|2025-12-11|
|Now Assist for Vulnerability Response|4.0.0|2026-01-20|
|Now Assist for WDF|2.0.3|2026-03-12|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.5|2025-12-11|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|15.3.0|2026-02-05|
|Now Assist in Catalog Builder|6.0.7|2026-01-20|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.0.5|2025-12-11|
|Now Assist in Conversational Catalog Request|5.2.23|2026-01-20|
|Now Assist in Document Intelligence|5.0.10|2026-04-02|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|29.4.11|2025-12-11|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|13.0.12|2025-12-31|
|Now Assist in Virtual Agent Configurations|8.0.7|2025-12-11|
|Now Assist Platform Skills|2.3.2|2025-12-11|
|Now Assist Skill Discovery and Execution|8.0.13|2025-12-11|
|Now Assist Skill Kit|7.0.14|2026-03-03|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Platform AI Agents and Skills|11.5.6|2026-02-12|
|prompt-management|1.0.11|2026-03-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|4.0.6|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|21.1.3|2025-12-11|
|RSM AI agent collection|1.2.0|2025-12-11|
|Sales Development AI Agents|1.0.7|2025-12-11|
|ServiceNow AI Lens|3.0.1|2025-12-11|
|Summarization for Order Management|1.0.2|2025-12-11|
|Telecommunications Media and Technology AI agent collection|4.0.5|2026-01-20|
|Test Generation|4.0.11|2025-12-11|
|UI Generation|29.1.2|2026-03-12|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Zero Copy Connector Hub|3.0.1|2026-03-12|

## Suite version 29.1.20260611 - Australia Patch 1

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed: -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

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

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

7.2.0

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

ITSM - Advanced

</td><td>

1.0.8

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

ITSM - Foundation

</td><td>

1.0.8

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

ITSM - Prime

</td><td>

1.0.9

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New:
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed: AI skill execution is now performed off glide

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

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

13.2.0

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

Now Assist for Platform for Requestor

</td><td>

2.0.6

</td><td>

-   Changed: Updated app dependencies
-   Fixed: App title is Now Assist for Platform for Requestor

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed: Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.6.1

</td><td>

Non Glide Cobalt Raven ACLs added.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New -   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New -   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

Test Generation

</td><td>

4.0.11

</td><td>

Changed:-   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

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

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.1.3|2026-04-28|
|Agentic Contact Center for Banking|1.0.1|2026-04-09|
|Agentic Desktop|2.0.0|2026-03-12|
|AI Agent Advisor|1.0.2|2026-06-04|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.8.2|2026-03-12|
|AI Agents for Customer Success Management|2.7.2|2026-04-09|
|AI Agents for Discovery|2.0.4|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.2.1|2026-04-09|
|AI Agents for Health and Safety|1.3.1|2026-04-09|
|AI Agents for ITAM|4.1.0|2026-04-09|
|AI agents for Observability|5.0.4|2026-03-12|
|AI Agents for Service Exchange Provider|1.0.12|2026-04-09|
|AI agents for SLO|1.0.5|2026-03-12|
|AI Agents for Workplace Service Delivery|3.2.0|2026-04-09|
|AI Control Tower for Enterprise AI Foundation|1.0.2|2026-04-09|
|AI Control Tower for Now Assist|3.1.0|2026-04-09|
|AI Data Explorer|4.1.5|2026-05-05|
|AI Enhanced Recommended Actions|1.0.1|2026-03-12|
|AI-Native IT Service Management|2.0.2|2026-04-09|
|AIOps LEAP|3.2.1|2026-04-09|
|Alert Assist|3.8.1|2026-03-12|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.0.4|2026-03-12|
|APO - Foundation|1.0.0|2026-04-09|
|APO - Prime|1.0.0|2026-04-09|
|App Engine - Prime|29.1.3|2026-04-09|
|App Generation|28.3.11|2025-12-11|
|App Life Cycle AI Agents|29.1.4|2026-04-09|
|App Summary|28.2.6|2025-12-11|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Build Agent Premium|1.1.9|2026-04-28|
|Business Continuity Management Advanced|1.0.2|2026-04-09|
|Business Continuity Management Foundation|1.0.3|2026-04-09|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.1|2026-03-12|
|Chat Recommendation|1.6.3|2026-04-09|
|Chat Summarization for Virtual Agent|1.10.5|2026-04-09|
|Collaborative Work Management - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Contract Management Pro - Prime|1.0.5|2026-04-09|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.0.0|2026-03-12|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|7.1.5|2026-04-09|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Core Business Suite|3.0.4|2026-04-09|
|Core Business Suite Advanced|3.0.0|2026-04-09|
|Core Business Suite Advanced for Finance|3.0.0|2026-04-09|
|Core Business Suite Advanced for Health and Safety|3.0.1|2026-04-09|
|Core Business Suite Advanced for Human Resources|3.0.1|2026-04-09|
|Core Business Suite Advanced for Legal|3.0.0|2026-04-09|
|Core Business Suite Advanced for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Advanced for Workplace Services|3.0.1|2026-04-09|
|Core Business Suite AI Agent|3.0.2|2026-04-09|
|Core Business Suite for Finance|3.0.3|2026-04-09|
|Core Business Suite for Health and Safety|3.0.3|2026-04-09|
|Core Business Suite for Human Resources|3.0.3|2026-04-09|
|Core Business Suite for Legal|3.0.3|2026-04-09|
|Core Business Suite For Source To Pay|3.0.3|2026-04-09|
|Core Business Suite For Workplace Service Delivery|3.0.3|2026-04-09|
|Core Business Suite Foundation|3.0.0|2026-04-09|
|Core Business Suite Foundation for Finance|3.0.0|2026-04-09|
|Core Business Suite Foundation for Health and Safety|3.0.0|2026-04-09|
|Core Business Suite Foundation for Human Resources|3.0.1|2026-04-09|
|Core Business Suite Foundation for Legal|3.0.0|2026-04-09|
|Core Business Suite Foundation for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Foundation for Workplace Services|3.0.1|2026-04-09|
|Core Business Suite Prime|3.0.0|2026-04-09|
|Core Business Suite Prime for Finance|3.0.0|2026-04-09|
|Core Business Suite Prime for Health and Safety|3.0.3|2026-04-09|
|Core Business Suite Prime for Human Resources|3.0.2|2026-04-09|
|Core Business Suite Prime for Legal|3.0.1|2026-04-09|
|Core Business Suite Prime for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Prime for Workplace Services|3.0.2|2026-04-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|1.0.0|2026-04-09|
|CPQ for Manufacturing Foundation|1.0.0|2026-04-09|
|CSM - Advanced|1.0.0|2026-04-09|
|CSM - Foundation|1.0.0|2026-04-09|
|CSM - Prime|1.0.0|2026-04-09|
|CTO Voice AI Agents|1.0.3|2026-04-09|
|Custom App Record Summarization|29.1.2|2026-04-09|
|Customer Service Management AI agent collection|5.1.0|2026-04-09|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DCNAM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|DocIntel Vision AI Agent|1.0.2|2026-04-09|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Dynamic Guidance|28.2.15|2026-04-09|
|Enterprise Architecture - Advanced|1.0.0|2026-04-09|
|Enterprise Architecture - Prime|1.0.0|2026-04-09|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|External content connectors - Now assist agent|1.0.6|2026-05-21|
|Field Service Management AI agent collection|2.1.0|2026-04-09|
|Financial Services Operations AI agent collection|4.0.0|2026-04-09|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Form data collector|2.0.1|2026-04-09|
|FSC Common - Foundation|1.0.0|2026-04-09|
|FSC Common - Prime|1.0.0|2026-04-09|
|FSM - Advanced|1.0.0|2026-04-09|
|FSM - Foundation|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Generative AI Controller|13.1.2|2026-04-09|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|6.1.2|2026-04-09|
|Hardware Asset Management - Advanced|1.0.0|2026-04-09|
|HCLS - Advanced|1.0.1|2026-04-09|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|1.0.1|2026-04-09|
|Health and Safety - Advanced|1.0.3|2026-04-09|
|Health and Safety - Foundation|1.0.3|2026-04-09|
|Health and Safety - Prime|1.0.3|2026-04-09|
|HR Service Delivery AI agent collection|6.0.1|2026-04-09|
|HR Talent AI Agent Collection|4.1.0|2026-04-09|
|HRSD - Advanced|1.0.5|2026-04-17|
|HRSD - Prime|1.0.5|2026-04-17|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Prime|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Insights Clustering Utils|3.0.0|2026-05-05|
|Integrated Risk Management Advanced|22.2.0|2026-05-05|
|Integrated Risk Management Foundation|22.1.2|2026-04-09|
|Integrated Risk Management Prime|22.2.0|2026-05-05|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management AI voice agent collection|1.2.0|2026-04-09|
|ITOM - Advanced|1.0.7|2026-04-09|
|ITOM - Prime|1.0.3|2026-04-09|
|ITOM AI Agents For Service Mapping|1.2.6|2026-03-12|
|Knowledge Center|31.8.1|2026-04-09|
|Knowledge Graph|7.1.2|2026-04-09|
|Legal Service Delivery - Prime|1.0.4|2026-04-09|
|List AI Experience|2.0.8|2026-03-12|
|Manage Invoice Operations|1.0.2|2026-04-09|
|Manage Order Operations|1.0.4|2026-04-09|
|Manufacturing Commercial Operations Advanced|1.0.2|2026-04-09|
|Manufacturing Commercial Operations AI agents collection|2.1.2|2026-04-09|
|Manufacturing Commercial Operations Foundation|1.0.2|2026-04-09|
|Manufacturing Commercial Operations Prime|1.0.2|2026-04-09|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.11.1|2026-05-21|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.8|2026-04-09|
|Model Context Protocol Client|2.1.0|2026-03-12|
|Model Context Protocol Server|1.3.1|2026-04-09|
|Notifications Email Agents|2.0.1|2026-04-09|
|Now Assist Admin Console|9.0.5|2026-04-09|
|Now Assist Agents for requestor|3.3.0|2026-04-09|
|Now Assist AI Agents|7.2.11|2026-05-05|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|4.1.3|2026-04-09|
|Now Assist context menu|3.5.1|2026-05-05|
|Now Assist Data Kit|7.1.2|2026-04-09|
|Now Assist for Accounts Payable Operations \(APO\)|7.1.0|2026-04-09|
|Now Assist for App Engine|29.1.2|2026-04-09|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|1.0.4|2026-04-09|
|Now Assist for Collaborative Work Management \(CWM\)|5.0.3|2026-04-09|
|Now Assist for Complaint Case \(CSM\)|2.1.1|2026-04-09|
|Now Assist for Configuration Management Database \(CMDB\)|3.2.1|2026-04-09|
|Now Assist for Contract Analysis|1.0.8|2026-05-05|
|Now Assist For Core Business Suite|3.0.2|2026-04-09|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Creator|29.1.2|2026-04-09|
|Now Assist for Customer Service Management \(CSM\)|12.1.2|2026-04-23|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.1.1|2026-04-09|
|Now Assist for Enterprise Architecture \(EA\)|7.2.0|2026-04-09|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for Field Service Management \(FSM\)|9.1.0|2026-04-09|
|Now Assist for Financial Services Operations \(FSO\)|3.0.0|2026-04-09|
|Now Assist for FSC Common|6.1.0|2026-04-09|
|Now Assist for Hardware Asset Management|4.1.0|2026-04-09|
|Now Assist for Health and Safety|1.3.1|2026-04-09|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.1.3|2026-04-09|
|Now Assist for HRSD - Foundation|1.0.5|2026-04-17|
|Now Assist for Impact|3.1.3|2026-04-09|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.6.9|2026-04-09|
|Now Assist for Legal Service Delivery|1.6.5|2026-04-09|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.1.2|2026-04-09|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.0.7|2026-04-09|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|11.1.0|2026-04-09|
|Now Assist for Platform Advanced|1.0.0|2026-04-09|
|Now Assist for Platform for Requestor|2.0.6|2025-12-11|
|Now Assist for Platform Foundation|1.0.0|2026-04-09|
|Now Assist for Platform Prime|1.0.0|2026-04-09|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|3.0.6|2026-03-12|
|Now Assist for Prompt Assistance|4.0.3|2026-04-09|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.1.1|2026-04-09|
|Now Assist for Purchase Order Management \(POM\)|1.1.0|2026-04-09|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for Sales and Order Management for Telecommunications|2.0.7|2026-04-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.1|2026-04-09|
|Now Assist for Security Incident Response \(SIR\)|6.0.1|2026-05-05|
|Now Assist for Service Exchange|1.0.12|2026-04-09|
|Now Assist for Setup|2.0.7|2026-04-09|
|Now Assist for Setup Core|1.0.6|2026-04-09|
|Now Assist for Software Asset Management \(SAM\)|7.0.0|2026-04-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|9.1.0|2026-04-09|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.1.0|2026-04-09|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|7.1.0|2026-04-09|
|Now Assist for Talent|1.7.0|2026-04-09|
|Now Assist for Telecommunications|1.1.5|2026-04-09|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.6|2026-04-09|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|2.0.0|2026-04-09|
|Now Assist for Voice|4.1.2|2026-04-09|
|Now Assist for WDF|2.0.7|2026-05-05|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.8|2026-03-12|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|16.1.4|2026-05-29|
|Now Assist in Catalog Builder|7.1.0|2026-04-09|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.1.3|2026-04-09|
|Now Assist in Conversational Catalog Request|6.0.2|2026-03-12|
|Now Assist in Document Intelligence|6.0.10|2026-04-09|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|30.8.0|2026-04-09|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|17.0.12|2026-04-09|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|2.4.3|2026-03-12|
|Now Assist Skill Discovery and Execution|9.1.9|2026-04-09|
|Now Assist Skill Kit|8.1.3|2026-04-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|22.0.1|2026-04-09|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OT Manager Foundation|3.3.1|2026-04-09|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Platform AI Agents and Skills|12.1.10|2026-05-29|
|POM - Foundation|1.0.0|2026-04-09|
|POM - Prime|1.0.0|2026-04-09|
|Privacy Management Advanced|22.2.0|2026-05-05|
|prompt-management|1.0.11|2026-03-12|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|1.1.1|2026-04-09|
|Query Generation|5.1.1|2026-04-09|
|Query Orchestrator|1.0.0|2026-04-09|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|Sales and Order Management for Technology Provider - Advanced|1.0.2|2026-04-09|
|Sales and Order Management for Technology Provider - Prime|1.0.2|2026-04-09|
|Sales and Order Management for Telecommunications - Advanced|1.0.5|2026-04-09|
|Sales and Order Management for Telecommunications - Prime|1.0.5|2026-04-09|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.1|2026-04-09|
|Sales Development AI Agents|1.0.7|2025-12-11|
|Screen Summarization|1.0.10|2026-04-09|
|Security Incident Response - Advanced|1.0.4|2026-05-05|
|Security Incident Response - Foundation|1.0.4|2026-05-05|
|Security Incident Response - Prime|1.0.4|2026-05-05|
|Service Exchange - Advanced|1.0.1|2026-04-09|
|Service Exchange - Foundation|1.0.1|2026-04-09|
|Service Exchange - Prime|1.0.1|2026-04-09|
|ServiceNow AI Lens|4.0.0|2026-03-12|
|SLO - Foundation|1.0.0|2026-04-09|
|SLO - Prime|1.0.0|2026-04-09|
|Software Asset Management AI Advanced|1.0.4|2026-04-09|
|Software Asset Management AI Prime|1.0.4|2026-04-09|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SPO - Foundation|1.0.0|2026-04-09|
|SPO - Prime|1.0.0|2026-04-09|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Summarization for Order Management|2.0.1|2026-03-12|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Technology Advanced|1.0.3|2026-04-09|
|Technology Foundation|1.0.3|2026-04-09|
|Technology Prime|1.0.3|2026-04-09|
|Telecommunications Advanced|1.0.4|2026-04-09|
|Telecommunications Foundation|1.0.4|2026-04-09|
|Telecommunications Media and Technology AI agent collection|5.1.3|2026-04-09|
|Telecommunications Prime|1.0.4|2026-04-09|
|Telecommunications, Media and Technology - Advanced|1.0.2|2026-04-09|
|Telecommunications, Media and Technology - Foundation|1.0.3|2026-04-09|
|Telecommunications, Media and Technology - Prime|1.0.2|2026-04-09|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.0.4|2026-03-12|
|Third-party Risk Management Advanced|22.0.1|2026-04-09|
|TNI and DCNAM AI Content Collection|1.0.0|2026-04-09|
|TNI for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Prime|1.0.3|2026-04-09|
|UI Generation|29.1.2|2026-03-12|
|Universal Request AI agent collection|1.0.7|2026-04-09|
|Voice input for Now Assist|1.3.13|2025-12-11|
|WSD - Advanced|1.0.1|2026-04-09|
|WSD - Foundation|1.0.1|2026-04-09|
|WSD - Prime|1.0.1|2026-04-09|
|Zero Copy Connector Hub|3.0.1|2026-03-12|

## Suite version 29.2.20260611 - Australia Patch 2

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Agents for Health and Safety

</td><td>

1.3.3

</td><td>

Fixed: Missing xml field that were causing data quality tests to fail

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

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

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.3.2

</td><td>

Fixed:

 Updated the version for ServiceNow Docs Connector to fix dependency failures

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed: AI skill execution is now performed off glide

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

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Health and Safety

</td><td>

1.4.1

</td><td>

New: Contextual Action Planner sidebar in the Health and Safety Workspace: Create actions manually or from AI suggestions, and review them in context across incidents, observations, investigations, cases, audits, work permits, risk assessments, meetings, etc.

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed: Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.6.1

</td><td>

Non Glide Cobalt Raven ACLs added.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
-   Users can upload images or diagrams which contain a process flow/flow diagram. The Template AI agent reads these documents and analyzes the template and template items required.
-   The Template ai agent creates a draft template along with template items based on the document and provides draft template details which are verified by the user.

</td></tr><tr><td>

Test Generation

</td><td>

4.0.11

</td><td>

Changed -   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

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

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Universal Request AI agent collection

</td><td>

1.0.9

</td><td>

Fixed minor system defects

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.2.6|2026-05-05|
|Agentic Contact Center for Banking|1.1.0|2026-05-05|
|AI Agent Advisor|1.0.2|2026-06-04|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.8.5|2026-05-05|
|AI Agents for Customer Success Management|2.7.2|2026-04-09|
|AI Agents for Discovery|2.0.4|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.0|2026-05-05|
|AI Agents for ITAM|4.1.0|2026-04-09|
|AI agents for Observability|5.0.4|2026-03-12|
|AI Agents for Service Exchange Provider|1.0.12|2026-04-09|
|AI agents for SLO|1.0.7|2026-05-05|
|AI Agents for Workplace Service Delivery|3.2.0|2026-04-09|
|AI Control Tower for Enterprise AI Foundation|1.0.2|2026-04-09|
|AI Control Tower for Now Assist|3.2.2|2026-05-05|
|AI Dashboard Insights|1.0.6|2026-05-05|
|AI Data Explorer|4.1.5|2026-05-05|
|AI Desktop Actions|3.0.1|2026-05-05|
|AI Enhanced Recommended Actions|1.0.2|2026-05-05|
|AIOps LEAP|3.3.1|2026-05-15|
|Alert Assist|3.9.1|2026-05-05|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.0.4|2026-03-12|
|APO - Foundation|1.1.0|2026-05-05|
|APO - Prime|1.1.0|2026-05-05|
|App Engine - Prime|29.1.3|2026-04-09|
|App Generation|28.3.11|2025-12-11|
|App Life Cycle AI Agents|29.2.0|2026-05-05|
|App Summary|29.2.1|2026-05-05|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Build Agent Premium|1.2.6|2026-05-05|
|Business Continuity Management Advanced|1.0.2|2026-04-09|
|Business Continuity Management Foundation|1.0.3|2026-04-09|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Chat Recommendation|1.6.3|2026-04-09|
|Chat Summarization for Virtual Agent|1.10.5|2026-04-09|
|Collaborative Work Management - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Contract Management Pro - Prime|1.0.7|2026-05-05|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.0.0|2026-03-12|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|8.0.1|2026-05-05|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Core Business Suite|3.0.4|2026-04-09|
|Core Business Suite Advanced|3.0.0|2026-04-09|
|Core Business Suite Advanced for Finance|3.0.0|2026-04-09|
|Core Business Suite Advanced for Health and Safety|3.0.1|2026-04-09|
|Core Business Suite Advanced for Human Resources|3.0.1|2026-04-09|
|Core Business Suite Advanced for Legal|3.0.0|2026-04-09|
|Core Business Suite Advanced for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Advanced for Workplace Services|3.0.1|2026-04-09|
|Core Business Suite AI Agent|3.0.2|2026-04-09|
|Core Business Suite for Finance|3.0.3|2026-04-09|
|Core Business Suite for Health and Safety|3.0.3|2026-04-09|
|Core Business Suite for Human Resources|3.0.3|2026-04-09|
|Core Business Suite for Legal|3.0.3|2026-04-09|
|Core Business Suite For Source To Pay|3.0.3|2026-04-09|
|Core Business Suite For Workplace Service Delivery|3.0.3|2026-04-09|
|Core Business Suite Foundation|3.0.0|2026-04-09|
|Core Business Suite Foundation for Finance|3.0.0|2026-04-09|
|Core Business Suite Foundation for Health and Safety|3.0.0|2026-04-09|
|Core Business Suite Foundation for Human Resources|3.0.1|2026-04-09|
|Core Business Suite Foundation for Legal|3.0.0|2026-04-09|
|Core Business Suite Foundation for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Foundation for Workplace Services|3.0.1|2026-04-09|
|Core Business Suite Prime|3.0.0|2026-04-09|
|Core Business Suite Prime for Finance|3.0.0|2026-04-09|
|Core Business Suite Prime for Health and Safety|3.0.3|2026-04-09|
|Core Business Suite Prime for Human Resources|3.0.2|2026-04-09|
|Core Business Suite Prime for Legal|3.0.1|2026-04-09|
|Core Business Suite Prime for Source to Pay|3.0.0|2026-04-09|
|Core Business Suite Prime for Workplace Services|3.0.2|2026-04-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ for Manufacturing Advanced|1.0.0|2026-04-09|
|CPQ for Manufacturing Foundation|1.0.0|2026-04-09|
|CSM - Advanced|1.0.0|2026-04-09|
|CSM - Foundation|1.0.0|2026-04-09|
|CSM - Prime|1.0.0|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.1.2|2026-04-09|
|Customer Service Management AI agent collection|5.1.5|2026-05-05|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DCNAM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|DocIntel Vision AI Agent|1.0.2|2026-04-09|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Enterprise Architecture - Advanced|1.0.0|2026-04-09|
|Enterprise Architecture - Prime|1.0.0|2026-04-09|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|External content connectors - Now assist agent|1.0.6|2026-05-21|
|Field Service Management AI agent collection|2.1.0|2026-04-09|
|Financial Services Operations AI agent collection|4.0.0|2026-04-09|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Form data collector|2.0.1|2026-04-09|
|FSC Common - Foundation|1.1.0|2026-05-05|
|FSC Common - Prime|1.1.0|2026-05-05|
|FSM - Advanced|1.0.0|2026-04-09|
|FSM - Foundation|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Generative AI Controller|13.2.2|2026-05-05|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|6.1.2|2026-04-09|
|Hardware Asset Management - Advanced|1.0.0|2026-04-09|
|HCLS - Advanced|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|Health and Safety - Advanced|1.0.4|2026-05-05|
|Health and Safety - Foundation|1.0.4|2026-05-05|
|Health and Safety - Prime|1.0.4|2026-05-05|
|HR Service Delivery AI agent collection|6.1.3|2026-05-05|
|HR Talent AI Agent Collection|4.1.0|2026-04-09|
|HRSD - Advanced|1.0.5|2026-04-17|
|HRSD - Prime|1.0.5|2026-04-17|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Prime|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Insights Clustering Utils|3.0.0|2026-05-05|
|Integrated Risk Management Advanced|22.2.0|2026-05-05|
|Integrated Risk Management Foundation|22.1.2|2026-04-09|
|Integrated Risk Management Prime|22.2.0|2026-05-05|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management|2.1.0|2026-05-05|
|IT Service Management AI agent collection|8.0.3|2026-05-08|
|IT Service Management AI voice agent collection|1.2.0|2026-04-09|
|ITOM - Advanced|1.0.8|2026-05-05|
|ITOM - Prime|1.0.4|2026-05-05|
|ITOM AI Agents For Service Mapping|1.3.1|2026-05-05|
|ITSM - Advanced|1.1.6|2026-05-15|
|ITSM - Foundation|1.1.6|2026-05-15|
|ITSM - Prime|1.1.6|2026-05-15|
|Knowledge Center|31.9.9|2026-05-05|
|Knowledge Graph|7.2.1|2026-05-05|
|Legal Service Delivery - Prime|1.0.8|2026-05-05|
|List AI Experience|2.0.8|2026-03-12|
|Manage Invoice Operations|1.0.2|2026-04-09|
|Manage Order Operations|1.0.4|2026-04-09|
|Manufacturing Commercial Operations Advanced|1.0.2|2026-04-09|
|Manufacturing Commercial Operations AI agents collection|2.1.2|2026-04-09|
|Manufacturing Commercial Operations Foundation|1.0.2|2026-04-09|
|Manufacturing Commercial Operations Prime|1.0.2|2026-04-09|
|Metadata Search|1.0.11|2026-05-05|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.11.1|2026-05-21|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.8|2026-04-09|
|Model Context Protocol Client|2.1.0|2026-03-12|
|Model Context Protocol Server|1.4.2|2026-05-05|
|Notifications Email Agents|2.0.4|2026-05-05|
|Now Assist Admin Console|9.1.8|2026-05-05|
|Now Assist Agents for requestor|3.4.1|2026-05-05|
|Now Assist AI Agents|7.2.11|2026-05-05|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|30.0.6|2026-05-05|
|Now Assist Analytics|4.1.7|2026-05-05|
|Now Assist Center|3.0.5|2026-05-05|
|Now Assist context menu|3.5.1|2026-05-05|
|Now Assist Data Kit|7.2.3|2026-05-05|
|Now Assist for Accounts Payable Operations \(APO\)|7.2.1|2026-05-05|
|Now Assist for App Engine|29.1.2|2026-04-09|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for Collaborative Work Management \(CWM\)|5.0.3|2026-04-09|
|Now Assist for Complaint Case \(CSM\)|2.1.1|2026-04-09|
|Now Assist for Configuration Management Database \(CMDB\)|3.6.0|2026-05-05|
|Now Assist for Contract Analysis|1.0.8|2026-05-05|
|Now Assist For Core Business Suite|3.0.2|2026-04-09|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Creator|29.2.2|2026-05-05|
|Now Assist for Customer Service Management \(CSM\)|12.2.0|2026-05-05|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.2.0|2026-05-05|
|Now Assist for Enterprise Architecture \(EA\)|7.2.0|2026-04-09|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for Field Service Management \(FSM\)|9.1.0|2026-04-09|
|Now Assist for Financial Services Operations \(FSO\)|3.1.0|2026-05-05|
|Now Assist for FSC Common|6.2.1|2026-05-05|
|Now Assist for Hardware Asset Management|4.1.0|2026-04-09|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.1.5|2026-05-05|
|Now Assist for HRSD - Foundation|1.0.5|2026-04-17|
|Now Assist for ICW|1.0.0|2026-05-05|
|Now Assist for Impact|3.1.3|2026-04-09|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.6.12|2026-05-05|
|Now Assist for IT Service Management \(ITSM\)|14.0.6|2026-05-15|
|Now Assist for Legal Service Delivery|1.7.7|2026-05-05|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.1.2|2026-04-09|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.1.0|2026-05-05|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|11.2.0|2026-05-05|
|Now Assist for Platform Advanced|1.1.0|2026-05-05|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Platform Foundation|1.1.0|2026-05-05|
|Now Assist for Platform Prime|1.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|3.0.12|2026-05-05|
|Now Assist for Prompt Assistance|4.1.4|2026-05-05|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.1.1|2026-04-09|
|Now Assist for Purchase Order Management \(POM\)|1.1.0|2026-04-09|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for Sales and Order Management for Telecommunications|2.0.7|2026-04-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.1|2026-04-09|
|Now Assist for Security Incident Response \(SIR\)|6.0.1|2026-05-05|
|Now Assist for Service Exchange|1.0.12|2026-04-09|
|Now Assist for Setup|2.1.2|2026-05-05|
|Now Assist for Setup Core|1.1.2|2026-05-05|
|Now Assist for Software Asset Management \(SAM\)|7.0.0|2026-04-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|9.2.2|2026-05-05|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.4.0|2026-05-05|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|7.2.2|2026-05-05|
|Now Assist for Talent|1.7.0|2026-04-09|
|Now Assist for Telecommunications|1.1.5|2026-04-09|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.6|2026-04-09|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|2.0.0|2026-04-09|
|Now Assist for Voice|4.2.3|2026-05-05|
|Now Assist for WDF|2.0.7|2026-05-05|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.8|2026-03-12|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in AI Search|16.1.4|2026-05-29|
|Now Assist in Catalog Builder|7.1.2|2026-05-05|
|Now Assist in Catalog item forms|1.3.2|2026-05-05|
|Now Assist in Contract Management|2.1.10|2026-05-05|
|Now Assist in Conversational Catalog Request|7.0.2|2026-05-05|
|Now Assist in Document Intelligence|6.0.12|2026-05-05|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|30.9.2|2026-05-05|
|Now Assist in Standard Ticket Page|1.0.9|2026-05-05|
|Now Assist in Virtual Agent|18.0.13|2026-06-04|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|2.4.3|2026-03-12|
|Now Assist Service Quality|1.0.2|2026-05-05|
|Now Assist Skill Discovery and Execution|10.0.4|2026-05-05|
|Now Assist Skill Kit|8.2.9|2026-05-05|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|22.0.1|2026-04-09|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OT Manager Foundation|3.3.1|2026-04-09|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Platform AI Agents and Skills|12.2.7|2026-05-05|
|POM - Foundation|1.0.0|2026-04-09|
|POM - Prime|1.0.0|2026-04-09|
|Privacy Management Advanced|22.2.0|2026-05-05|
|prompt-management|1.0.11|2026-03-12|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|1.1.1|2026-04-09|
|Query Generation|5.2.0|2026-05-05|
|Query Orchestrator|1.0.0|2026-04-09|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|Sales and Order Management for Technology Provider - Advanced|1.0.2|2026-04-09|
|Sales and Order Management for Technology Provider - Prime|1.0.2|2026-04-09|
|Sales and Order Management for Telecommunications - Advanced|1.0.5|2026-04-09|
|Sales and Order Management for Telecommunications - Prime|1.0.5|2026-04-09|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.1|2026-04-09|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.11|2026-05-05|
|Security Incident Response - Advanced|1.0.4|2026-05-05|
|Security Incident Response - Foundation|1.0.4|2026-05-05|
|Security Incident Response - Prime|1.0.4|2026-05-05|
|Service Exchange - Advanced|1.0.1|2026-04-09|
|Service Exchange - Foundation|1.0.1|2026-04-09|
|Service Exchange - Prime|1.0.1|2026-04-09|
|ServiceNow AI Lens|5.0.0|2026-05-05|
|SLO - Foundation|1.1.0|2026-05-05|
|SLO - Prime|1.1.0|2026-05-05|
|Software Asset Management AI Advanced|1.0.4|2026-04-09|
|Software Asset Management AI Prime|1.0.4|2026-04-09|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|SPO - Foundation|1.1.0|2026-05-05|
|SPO - Prime|1.1.0|2026-05-05|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Technology Advanced|1.0.3|2026-04-09|
|Technology Foundation|1.0.3|2026-04-09|
|Technology Prime|1.0.3|2026-04-09|
|Telecommunications Advanced|1.0.4|2026-04-09|
|Telecommunications Foundation|1.0.4|2026-04-09|
|Telecommunications Media and Technology AI agent collection|5.1.3|2026-04-09|
|Telecommunications Prime|1.0.4|2026-04-09|
|Telecommunications, Media and Technology - Advanced|1.0.2|2026-04-09|
|Telecommunications, Media and Technology - Foundation|1.0.3|2026-04-09|
|Telecommunications, Media and Technology - Prime|1.0.2|2026-04-09|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Management Advanced|22.0.1|2026-04-09|
|TNI and DCNAM AI Content Collection|1.0.0|2026-04-09|
|TNI for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Prime|1.0.3|2026-04-09|
|UI Generation|29.2.5|2026-05-05|
|Voice input for Now Assist|1.3.13|2025-12-11|
|WSD - Advanced|1.0.1|2026-04-09|
|WSD - Foundation|1.0.1|2026-04-09|
|WSD - Prime|1.0.1|2026-04-09|
|Zero Copy Connector Hub|3.0.1|2026-03-12|

## Suite version 29.3.20260611 - Australia Patch 3

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

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

New Changed Fixed Removed Removed outdated terminology and legacy labels associated with prior AI workflow naming and activity actions.

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

AI Agent Advisor

</td><td>

1.1.0

</td><td>

-   New
    -   Discover automation opportunities across customer service interaction channels chat \(portal and messaging\), voice, and email in addition to incidents and cases.
    -   Transcript-based analysis infers customer intent and resolution steps from conversational language, surfacing automation opportunities that aren't captured in structured fields.
    -   Channel-specific agent matching recommends chat, voice, or email agents based on each opportunity's characteristics.
    -   Channel-appropriate agent generation when no suitable existing agent is found.
-   Changed
    -   Mining scope expanded beyond cases and incidents to include the Interaction table.
    -   Matching pulls from a unified agent registry so chat and voice agents are evaluated alongside existing agents and tools, with no separate setup per channel.
    -   Clustering now incorporates interaction type, transcript content, short description, and referenced knowledge base articles when ranking opportunities by impact.
-   Fixed
    -   Resolved a defect causing opportunity ranking to display in reverse order.
    -   Resolved an issue where asset counts did not match across the UI.

 Removed

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.9.0

</td><td>

New - -   AIOps AI Specialist \(limited availavilblity\) - The AIOps AI Specialist AI is ServiceNows purpose-built AI agent for IT Operations, designed to autonomously monitor, correlate, triage, and resolve infrastructure and application events at enterprise scale.
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

-   New: Added Splunk, AWS CloudWatch, ThousandEyes, SolarWinds, and Prometheus as supported investigation backends for the Analyze alert impact agentic workflow, expanding the alert insights available.
-   Changed
    -   Updated the Analyze alert impact agentic workflow to route all alert investigation through a single SRE Investigate AI Agent, delivering consistent behavior across all supported backends and simplifying the path for adding new vendor agents.
    -   Migrated New Relic and Datadog integrations to Model Context Protocol \(MCP\) agents, standardizing on vendor-maintained tool surfaces so the investigation workflows stay current as vendors ship updates.

 Deprecated

 Deprecated the Dynatrace Analysis AI Agent, superseded by the Dynatrace MCP Server Agent.

</td></tr><tr><td>

AI Agents for Service Exchange Provider

</td><td>

1.0.13

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

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

-   New
-   Changed: Workplace Utilization QnA Agent can now be used by users with the sn\_wsd\_spcmgmt.space\_planner role
-   Fixed: The AI Agent was not always able to block the location after submitting an emergency maintenance request
-   Removed

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
    -   Localization &amp; Performance issues are fixed.
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

AI Dashboard Insights

</td><td>

1.1.4

</td><td>

-   New
    -   Refine actions You can now refine generated summaries directly within the dashboard using built-in actions such as Elaborate and Shorten, giving you more control over how the summary is presented.
    -   Feedback on generated content Added thumbs up / thumbs down controls to the summary component, making it easy to share feedback on AI-generated summaries.
    -   Dashboard Summary for UI Builder Workspaces Dashboard Summary is now available out of the box in UI Builder Workspaces.
-   Fixed
    -   Consistent cache behavior across summary triggers Both the Refresh and Generate Summary buttons now apply the cache consistently, avoiding redundant AI calls.
    -   Dashboard Summary time zone aligned with user preference The Dashboard Summary now correctly applies the user's configured time zone rather than the system time zone, ensuring consistency with the data shown in dashboard widgets.

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

New -   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch to AI-assisted recording by selecting the new Record with AI \(recommended\) check box that replaces the previous capture modes in the Create desktop action modal.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the Shared and Mark As Sensitive fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.

</td></tr><tr><td>

AI Experience Framework Skills

</td><td>

1.1.0

</td><td>

New features for June Release:

 -   Improved error handling and internationalization \(i18n\) support
-   Added streaming capabilities for real-time data processing
-   Resolved critical defects and stability issues
-   Extended support for additional widget property types

</td></tr><tr><td>

AI for document designer

</td><td>

22.3.4

</td><td>

-   New
    -   AI for Document Designer A new AI-powered application that integrates with the Microsoft Word add-in, enabling users to generate and manage report content directly within Word documents using Now Assist.
    -   AI-powered Word content generation A custom AI skill that generates Microsoft Word report content through natural language prompts, allowing users to create document sections conversationally.
    -   Content insertion into Word documents Support for inserting AI-generated content \(HTML and OOXML formats\) directly into Word documents via sn-office-addin handlers.
    -   Multi-conversation document editing Ability to edit and refine document content across multiple conversations with the AI assistant, enabling iterative content development.
    -   Data model, ACLs, and roles Purpose-built data model with access controls and role definitions to secure AI-generated document content and manage user permissions.
-   Changed: AI agent accuracy and prompt enhancements Improved agent accuracy and refined prompts based on Architecture Review Board \(ARB\) feedback for higher quality content generation.
-   Fixed: AI agent icons updated in add-in Corrected the icons displayed for the AI agent within the Microsoft Word add-in.

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed:-   Addressed Brazil security directive
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

New:-   AIOps AI Specialist \(L1 AI Worker\): AI-powered first responder that autonomously triages alerts, reduces noise, enriches context, and provides remediation recommendations across the alert lifecycle.
    -   Context-rich alert investigation Enhanced alert analysis using CMDB topology, incident history, and operational signals to provide deeper insights and faster decision-making.
    -   Knowledge-driven investigation Integrated knowledge sources, including KB articles into the investigation workflow to improve accuracy and deflect incidents
    -   Remediation suggestions from existing subflows AI-generated remediation recommendations leveraging existing alert rules and subflows to accelerate resolution and ensure consistency.
    -   SRE AI Specialist integration Integrates seamlessly with the SRE AI Specialist for deeper investigation, including observability data analysis and root cause hypotheses
-   Dedicated AIOps Manager Homepage: New homepage for AIOps Managers and Event Management Admins to onboard, configure, and manage AI Specialists from a centralized command center.

</td></tr><tr><td>

Alert Assist

</td><td>

3.9.3

</td><td>

-   New: Proactive Grouping Recommendations AI-generated grouping recommendations help AIOps administrators identify alert correlation opportunities with greater speed and accuracy.
-   Changed: Updated supported LLM versions to GPT-4o Mini and Claude Haiku 4.5, bringing the latest model improvements to the platform.
-   Fixed: The Autonomous Operator was not automatically updating the description of HLA alerts. This has been corrected.

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

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

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

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

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

-   Changed
    -   Identify missing clauses in contract revisions with improved accuracy.
    -   Support for upgraded versions of third party LLMs has been provided.
-   Fixed
    -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
    -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.

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

Core Business Suite

</td><td>

3.2.1

</td><td>

Core Business Suite \(CBS\) brings together case and knowledge management applications for essential business functions including HR, Source-to-Pay, Finance, Workplace Services, Legal, and Health &amp; Safety. It enables organizations to standardize, manage, and streamline critical employee and business workflows on a single, unified platform.

</td></tr><tr><td>

Core Business Suite Advanced

</td><td>

3.0.5

</td><td>

-   Employee Slate is now the default experience - Core Business Suite now uses Employee Slate as the requester experience out-of -the-box, giving employees a single, consistent place to get help.
-   CBS Analytics Dashboard - A new dashboard gives a consolidated, cross-business-unit view of service performance, including open and unassigned cases, mean time to resolve, and self-service resolution.
-   Core Business Suite Advanced is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced applications.

</td></tr><tr><td>

Core Business Suite Advanced for Finance

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Finance is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced Finance applications.

</td></tr><tr><td>

Core Business Suite Advanced for Health and Safety

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Health and Safety is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced Health and Safety applications.

</td></tr><tr><td>

Core Business Suite Advanced for Human Resources

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Human Resources is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced HR applications.

</td></tr><tr><td>

Core Business Suite Advanced for Legal

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Legal is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced Legal applications.

</td></tr><tr><td>

Core Business Suite Advanced for Source to Pay

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Source to Pay is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced S2P applications.

</td></tr><tr><td>

Core Business Suite Advanced for Workplace Services

</td><td>

3.0.5

</td><td>

Core Business Suite Advanced for Workplace Services is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Advanced of Workplace Services.

</td></tr><tr><td>

Core Business Suite AI Agent

</td><td>

3.2.0

</td><td>

Updated to support the latest versions of the dependent apps.

</td></tr><tr><td>

Core Business Suite for Finance

</td><td>

3.2.0

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Finance. The goal is to give finance admins immediate visibility into existing rule configurations without manual setup, letting them review and understand what rules are active right out of the box.

</td></tr><tr><td>

Core Business Suite for Health and Safety

</td><td>

3.2.0

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Health and Safety. The goal is to give Health and Safety admins immediate visibility into existing rule configurations without manual setup, so they can review and understand which rules are active by default.

</td></tr><tr><td>

Core Business Suite for Human Resources

</td><td>

3.2.0

</td><td>

Core Business Suite for Human Resources delivers end\_to\_end Human Resources case and knowledge management, combined with other enterprise workflows.

</td></tr><tr><td>

Core Business Suite for Legal

</td><td>

3.2.0

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Legal. The goal is to give legal admins immediate visibility into existing rule configurations without manual setup, letting them review and understand what rules are active by default.

</td></tr><tr><td>

Core Business Suite For Source To Pay

</td><td>

3.2.0

</td><td>

The Core Business Suite For Source To Pay contains all Source To Pay-related code within this applications repository. This application will not be visible to customers on the ServiceNow Store and is intended solely to organize legal-related code within CBS.

</td></tr><tr><td>

Core Business Suite For Workplace Service Delivery

</td><td>

3.2.0

</td><td>

Shipped out-of-the-box \(OOB\) assignment rules for the Workplace Service Delivery administrators. This change surfaces the OOB rules in the admin interface, giving teams an immediate and accurate picture of the baseline configuration.

</td></tr><tr><td>

Core Business Suite Foundation

</td><td>

3.0.5

</td><td>

-   Employee Slate is now the default experience - Core Business Suite now uses Employee Slate as the requester experience out-of -the-box, giving employees a single, consistent place to get help. Install and configure it from the CBS admin setup, with support for both Moveworks and Now Assist.
-   Assignment rules for all business units - Route cases to the right team automatically with configurable assignment rules across HR, Legal, Finance, Source-to-Pay, Workplace Services, and Health &amp; Safety. Out-of-the-box rules are included for each business unit and can be created or edited from the CBS console.
-   CBS Analytics Dashboard - A new dashboard gives a consolidated, cross-business-unit view of service performance, including open and unassigned cases, mean time to resolve, and self-service resolution.

</td></tr><tr><td>

Core Business Suite Foundation for Finance

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Finance. The goal is to give finance admins immediate visibility into existing rule configurations without manual setup, so they can review and understand which rules are active by default.

</td></tr><tr><td>

Core Business Suite Foundation for Health and Safety

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Health and Safety. The goal is to give Health and Safety admins immediate visibility into existing rule configurations without manual setup, so they can review and understand which rules are active by default.

</td></tr><tr><td>

Core Business Suite Foundation for Human Resources

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite Foundation for Human Resources. The goal is to give HR admins immediate visibility into existing rule configurations without manual setup, so they can review and understand which rules are active by default.

</td></tr><tr><td>

Core Business Suite Foundation for Legal

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite for Legal. The goal is to give legal admins immediate visibility into existing rule configurations without manual setup, letting them review and understand what rules are active by default.

</td></tr><tr><td>

Core Business Suite Foundation for Source to Pay

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for the Core Business Suite Foundation for Source to Pay. The goal is to give S2P admins immediate visibility into existing rule configurations without manual setup, so they can review and understand which rules are active by default.

</td></tr><tr><td>

Core Business Suite Foundation for Workplace Services

</td><td>

3.0.5

</td><td>

Shipped out-of-the-box assignment rules for Core Business Suite for Workplace Services. The goal is to give Workplace Services admins immediate visibility into existing rule configurations without manual setup, letting them review and understand what rules are active right out of the box.

</td></tr><tr><td>

Core Business Suite Prime

</td><td>

3.0.5

</td><td>

-   Employee Slate is now the default experience - Core Business Suite now uses Employee Slate as the requester experience out-of -the-box, giving employees a single, consistent place to get help.
-   CBS Analytics Dashboard - A new dashboard gives a consolidated, cross-business-unit view of service performance, including open and unassigned cases, mean time to resolve, and self-service resolution.
-   Core Business Suite Prime is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime applications.

</td></tr><tr><td>

Core Business Suite Prime for Finance

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Finance is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime Finance applications.

</td></tr><tr><td>

Core Business Suite Prime for Health and Safety

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Health and Safety is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime Health and Safety applications.

</td></tr><tr><td>

Core Business Suite Prime for Human Resources

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Human Resources is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime HR applications.

</td></tr><tr><td>

Core Business Suite Prime for Legal

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Legal is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime Legal applications.

</td></tr><tr><td>

Core Business Suite Prime for Source to Pay

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Source to Pay is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime S2P applications.

</td></tr><tr><td>

Core Business Suite Prime for Workplace Services

</td><td>

3.0.5

</td><td>

Core Business Suite Prime for Workplace Services is now available for direct installation from the Product Hub. This enables one-click installation of all CBS Prime of Workplace Services.

</td></tr><tr><td>

CPQ for Manufacturing Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

CPQ for Manufacturing Foundation

</td><td>

1.1.0

</td><td>

 

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

Changed -   Added voice-driven case status retrieval and updates, enabling customers to check open case statuses and submit updates through guided voice interactions across Genesys, NICE, Five9, 3CLogic, and Amazon Connect, reducing live agent dependency.
-   Enhanced Provide Customer 360 Insights with Enterprise Graph and AI Agent deep research for richer, more contextual query results.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

2.0.1

</td><td>

New -   Agent renamed to "Vision AI Agent"
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

Employee Slate for Now Assist

</td><td>

1.1.3

</td><td>

This release provides the following enhancements and improvements.

 -   Enhanced accessibility support Performance improvements Support for L10n Enhanced telemetry support for tracking user behavior Enhanced the home page layout with auto-adjust flexibility based on the widgets count Enhanced Admin configuration to support Tasks and requests \(fka Inbox\), To-dos task type configurations
-   Enhanced AI Preferences to support Smart Prioritisation and AI-Generated Summarisation
-   Enhanced the option to load AI summary automatically or on demand on AI summary details page

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

New:-   Generate a business process map \(BPM\) diagram in the Enterprise Modeling &amp; Visualization by uploading an image of an existing process diagram.
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

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to ensure certification and release standards.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

 Fixed

 Removed

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

New -   Summarize flow execution details when flow reporting is off.
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

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to certify features.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

 Fixed

 Removed

</td></tr><tr><td>

FSM - Foundation

</td><td>

2.0.1

</td><td>

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content \(links, code, special characters\).
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins/analysts can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to certify that features meet release standards.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

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

-   New: Backend support for HR Knowledge Gaps. This capability will be taken up by the Knowledge Center team in a future release. No customer-facing updates in this release.
-   Changed: Nothing changed in this release.
-   Fixed: Various minor defects fixed.
-   Removed: Nothing removed in this release.

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

New: Added new skills for Interview health tracker.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

HRSD - Advanced

</td><td>

2.0.2

</td><td>

Changed: App and plugin dependencies have been updated.

</td></tr><tr><td>

HRSD - Foundation

</td><td>

2.0.2

</td><td>

Changed: App and plugin dependencies have been updated.

</td></tr><tr><td>

HRSD - Prime

</td><td>

2.0.2

</td><td>

Changed: App and plugin dependencies have been updated.

</td></tr><tr><td>

Industrial Control Tower Advanced

</td><td>

1.0.0

</td><td>

New: Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Foundation

</td><td>

1.0.0

</td><td>

New: Update to include AI native and risk calculator

</td></tr><tr><td>

Industrial Control Tower Prime

</td><td>

1.0.0

</td><td>

New: Update to include AI native and risk calculator

</td></tr><tr><td>

Insights Clustering Utils

</td><td>

3.1.0

</td><td>

-   New: Updates to support AI Agent Advisor.
-   Changed: Nothing changed in this release.
-   Fixed: Nothing fixed in this release.
-   Removed: Nothing removed in this release.

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

-   New: Implemented meta data changes to enable AI native support for all skills and agents in the Regulatory Change Management application.
-   Changed: Improved agent instructions and supporting tools for the Regulatory Alert Analysis and Recommendations agent to ensure more reliable and consistent responses.

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

22.3.2

</td><td>

Fixed: Risk Event Summary now generates correctly when a task is associated with a Risk Event.

</td></tr><tr><td>

IT Service Management

</td><td>

3.0.2

</td><td>

New:

 Employee experience

 Front door employee experience \(Employee Slate\): a conversation-first portal with a unified Activity Hub displaying open incidents and requested items, fulfillment progress, a Needs Attention area, and a simplified Request experience.

 Fulfiller experience

 Catalog tasks on the landing page: IT agents can track catalog tasks alongside incidents and requests on the fulfiller homepage.

 Admin experience

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

-   New: Fulfiller actions from an incident: Fulfillers can create a change request, propose a major incident, and create a problem record for an incident.
-   Changed
    -   Enhanced embedded Now Assist chat module card with contextual resolution actions: draft or attach a knowledge article, propose a major incident, create a change or problem, and send next steps to the requester.
    -   AI-assisted incident triage, resolution guidance, and summaries surfaced natively on the record.

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

9.0.0

</td><td>

1.  The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
2.  Knowledge feedback tasks are now deduplicated the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
3.  The Change Quality Agent now persists quality scores per change record including timestamps and contributing factors available for dashboards, audits, and risk-detection workflows.
4.  A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
5.  The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
6.  A new manager dashboard aggregates incidents into issue-based clusters with health metrics and drill-down views, giving incident managers a consolidated view of emerging problem areas.
7.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
8.  The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
9.  A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.

 1.  The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
2.  Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
3.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
4.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.

 -   Fixed- None
-   Removed - None

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.4.0

</td><td>

-   New: n/a
-   Changed: Security related enhancements on existing AI Voice agents
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

-   New
    -   Service Mapping supports the Model Context Protocol \(MCP\), providing a conversational interface for live application service data. Service Mapping admins can connect Claude Desktop to a ServiceNow instance and query service topology, server-to-service relationships, related CIs, and unmapped configuration items.
    -   Service Mapping Workspace widgets1. Business app linked to App services - Indicating the count of business applications that were linked to application services by the Business App Mapping AI Agent.2. Maps created by Now Assist - Indicating the count of the service maps created by Service Mapping AI Agent.
-   Changed
    -   The AI specialists for Service Mapping are renamed as AI Agents for Service Mapping.
    -   View the service map created by Service Mapping AI Agent through the AI Activity list.

</td></tr><tr><td>

ITSM - Advanced

</td><td>

2.0.3

</td><td>

1.  The Change Quality Agent now persists quality scores in a dedicated table linked to each change record, enabling persistent reporting and downstream use. Scores include metadata such as timestamps, scoring version, and contributing factors, and are available for dashboards, audits, and risk-detection workflows across the full change lifecycle.
2.  The Insights and Opportunities for Incident dashboard in Service Operations Workspace aggregates incidents into trend categories with AI-generated summaries, SLA performance, sentiment, channel adoption, and geographic distribution, giving incident managers a consolidated view of incident patterns with drill-down views into individual records.
3.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, replacing complex admin navigation. The guided agent walks administrators through key settings including approvals, risk scoring, and workflows via natural language, making Change Management configuration accessible to customers with limited ServiceNow expertise.

 1.  The Create Incident AI Agent has been migrated from VA topic-based orchestration to a Hierarchical Agent model, resolving hallucination, functional deviation, and rendering issues on the NextWave orchestrator. The agent now runs natively on NextWave without VA dependency, delivering a consistent and reliable incident creation experience for end users.
2.  The Create Incident AI Agent has been evaluated and updated for compatibility with the NextWave off-glide orchestrator. All hallucination and functional deviation issues identified during GA readiness testing have been resolved, ensuring consistent and accurate incident creation behavior across both VA-based and NextWave runtime environments.

 1.  An issue has been resolved where Platform skills were not appearing in the Now Assist Skills admin panel even when the ignoreFulfillerSubscriptionCheck system property was enabled. Administrators can now successfully view and activate Platform skills from the Now Assist admin interface.
2.  Several display and interaction issues in the Recommended Actions panel have been resolved, including a misaligned loading indicator on the search box, a non-functional full-view search icon, filter dropdowns obscured by the footer, and an incorrect hand cursor appearing on non-clickable KB article and AI action content.
3.  The Suggested Steps feature has been deprecated and removed from Now Assist for ITSM. Customers previously using Suggested Steps should transition to the AIOps LEAP recommendations available through updated Now Assist for ITSM capabilities.

</td></tr><tr><td>

ITSM - Foundation

</td><td>

2.0.3

</td><td>

1.  The Insights and Opportunities for Incident dashboard in Service Operations Workspace aggregates incidents into trend categories with AI-generated summaries, SLA performance, sentiment, channel adoption, and geographic distribution, giving incident managers a consolidated view of incident patterns with drill-down views into individual records.
2.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
3.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.
4.  Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
5.  Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.
6.  Suggested Steps has been deprecated and removed. Customers should transition to AI-driven recommendations in Now Assist for ITSM.

</td></tr><tr><td>

ITSM - Prime

</td><td>

2.0.3

</td><td>

1.  The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
2.  Knowledge feedback tasks are now deduplicated the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
3.  The Change Quality Agent now persists quality scores per change record including timestamps and contributing factors available for dashboards, audits, and risk-detection workflows.
4.  A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
5.  The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
6.  A new manager dashboard aggregates incidents into issue-based clusters with health metrics and drill-down views, giving incident managers a consolidated view of emerging problem areas.
7.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
8.  The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
9.  A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.

1.  The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
2.  Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
3.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
4.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.

1.  Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
2.  Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.

Suggested Steps has been deprecated and removed. Customers should transition to AIOps LEAP recommendations in Now Assist for ITSM.

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

-   Changed: Support for upgraded versions of third party LLMs has been provided.
-   Fixed: Legal request and matter summarization now delivers improved accuracy across all supported models

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

-   New: Delivery note upload for quantity disputes: Customers can upload delivery notes during case creation, enabling the invoice dispute intake assistant AI agent to validate and resolve quantity disputes without human intervention.
-   Changed: Order line quantity validation for disputes: The invoice dispute support assistant AI agent uses order line data when sold product records are unavailable such as new orders, non-serialized products, or services. It auto-approves valid disputes and escalates only when data is unclear.

</td></tr><tr><td>

Manage Order Operations

</td><td>

2.0.3

</td><td>

-   New
-   Automated email notifications for order cases: Send emails when the AI agent opens an order case from a Business Portal chat and when the case is resolved. Closure emails include resolution and quote details, if generated. Voice-created cases don't trigger emails.Scripted extension point for quote thresholds: A scripted extension point to integrate the manage order operations AI agent with your inventory, ERP, and quote systems for quote threshold evaluation. The AI agent generates a quote when a quantity-change request exceeds the configured price threshold.
-   Changed
-   Order exception support for quantity and shipping location: Customers can request quantity and shipping location updates, along with expedite requests via chat and voice channels.
-   Voice assistant intake for order exceptions: Customers can submit expedite, quantity, and shipping location requests via voice. Requests are captured and converted into order cases for resolution in CSM/FSM Configurable Workspace.
-   Unified extension point for feasibility checks: A single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) validates delivery, quantity, and shipping feasibility, replacing the earlier expedite-only ATP check.
-   Auto-populated account and contact on interactions: Account and Contact fields are populated during chat handoff, giving agents immediate customer context and improving summarization accuracy.
-   AI-generated summaries for agent handoff: Agents receive a concise AI-generated summary instead of full chat history, improving context and productivity.

</td></tr><tr><td>

Manufacturing Commercial Operations Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

2.2.0

</td><td>

New

 Detect claim anomaly - two new capabilities

 Auto-categorize Repair Claims capability

 GenAI summary on repair claims

</td></tr><tr><td>

Manufacturing Commercial Operations Foundation

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

Manufacturing Commercial Operations Prime

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

1.0.2

</td><td>

New: Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and reason about goals, portfolio plans, and projects. The following tools are available in this release: Tool Description get\_goals Retrieves goals and objectives. generate\_goal\_insights Generates AI-powered insights for goals and targets. get\_portfolio\_plans Retrieves portfolio plans. generate\_portfolio\_insights Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies. get\_projects Retrieves projects. generate\_project\_insights Detects project risks, analyzes status trajectory, and provides recommendations. identify\_project\_risks Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts. get\_ai\_status\_report Generates a RAG \(Red, Amber, Green\) status report across resources, cost, schedule, and scope.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.12.0

</td><td>

Removed : api-version query parameter from Create Response OEM action

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.5.0

</td><td>

New

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.2.0

</td><td>

Changed: Minor API changes for another app support internally

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

1.5.1

</td><td>

Performance improvements implemented, and third-party IDPs now allowed to be used.

</td></tr><tr><td>

Moveworks AIS Enabler

</td><td>

1.1.3

</td><td>

OOTB Search profile and related details for Moveworks

</td></tr><tr><td>

Notifications Email Agents

</td><td>

2.1.1

</td><td>

New -   Multi-intent identification support
-   Missing inputs extraction
-   email branding/template support for email generation

</td></tr><tr><td>

Now Assist Admin Console

</td><td>

10.0.11

</td><td>

Skill Archival Instance and system administrators can now archive custom skills directly from the Now Assist Skills page. Archiving is not supported for ServiceNow out-of-box \(OOB\) skills. Archived skills can be restored at any time.

 Skill Details Page View Detail button is now available alongside the Activate button for OOB skills on the Now Assist Skills page. The Skill detail view provides administrators and users with key information about a skill including its benefits, prerequisites, recommended model provider, and related skills enabling informed activation decisions.

 Prompt Injection Enhancements Prompt injection protection can now be configured at both the instance level and the product level \(CSM, ITSM, and others\), giving administrators more granular control over enforcement across workflows.

 Model Version Management Guided Tour Administrators can now launch a guided tour walkthrough directly from the " Manage Model Versions" section within Settings section in now assist admin. The guided tour provides a step-by-step introduction to the model version management workflow, helping admins understand version lifecycle, deprecation alerts, and available actions.

</td></tr><tr><td>

Now Assist Agents for requestor

</td><td>

3.5.0

</td><td>

Approval checklist generator skill accepts additional context parameter that is used to resolve checklists unknown items.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

8.0.10

</td><td>

-   New: AI Agent Extensibility: Customers can now add / remove AI agents or tools from OOTB agents while remaining on the upgrade path.
-   Changed: Orchestrator defaults to GPT-5.4: The orchestrator now uses GPT-5.4 as its default model when Azure OpenAI is the selected LLM.
-   Fixed
    -   Agent Execution
        -   Published version instructions not being applied to agents at runtime.
        -   Execution plan fetch timing out on instances with large numbers of execution plan records.
        -   Agentic workflow stuck at orchestrator step intermittently.
        -   VA transaction timeout and conversation stuck on "Thinking."
    -   Agent-to-Agent \(A2A\)
        -   Async handling of working state from secondary agent causing primary flow issues.
        -   Raw rich control output in agent response causing conversation to fault and close abruptly.
        -   input-required response sending empty message/parts block.
    -   Multilingual
        -   Tool names, agent names, and "Processing new information" untranslated in AI steps.
        -   Words not translated when user language differs from system language \(intermittent\).

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

31.0.5

</td><td>

Changed:-   Browser tabs that open during goal execution in adaptive desktop actions remain open after the goal completes. Use the keep\_tab\_open system property to turn this behavior on or off. The property is turned on by default.
-   Adaptive desktop actions is enhanced to improve execution efficiency.

</td></tr><tr><td>

Now Assist Analytics

</td><td>

5.0.3

</td><td>

New:-   Analytics dashboards pertaining to AI agents, AI assistants, and skills are consolidated inside Now Assist Center &gt; Monitor.
-   Executions dashboard in Now Assist Center: Deep dive into individual executions of assistants and agents to improve performance.
-   Business value dashboard in Now Assist Center: Analyze the impact of AI assets on time and cost savings and set formula for calculating value per AI asset \(skills, AI agents, agentic workflows\)

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

- Increased sample data input limit for SDG requests Users \(Data Kit Admin\) can now select up to 50 seed records from a data collection or table when submitting a Synthetic Data Generation request, up from the previous default of 3. The maximum sample size is also configurable by NADK Admins via sys\_property.

 - Plausibility Metrics for Synthetic Data Introduced plausibility scoring as a new data quality insight layer within the Generated Data view \(Data Kit &gt; Home &gt; Synthetic Data tab &gt; Open Generated Data &gt; Data Insight &gt; Plausibility\). Validates that generated field values are realistic, internally consistent, and free of garbage data.

 - OOB data sets

</td></tr><tr><td>

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

8.0.0

</td><td>

New: -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
-   Enhanced workflow to enable requesters to accept/reject the case resolution.

</td></tr><tr><td>

Now Assist for Advanced Work Assignment \(AWA\)

</td><td>

1.0.3

</td><td>

Changed: AI skill execution is now performed off glide

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

29.2.3

</td><td>

Changed: Updated versions of dependent apps.

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

Fixed: Security fixes

</td></tr><tr><td>

Now Assist for Contract Analysis

</td><td>

1.0.9

</td><td>

Existing feature: with latest third party model versions

</td></tr><tr><td>

Now Assist For Core Business Suite

</td><td>

3.2.0

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

29.2.5

</td><td>

-   New
    -   Build Agent
        -   Upload files to Build Agent to provide context: images \(PNG, JPEG, GIF, WEBP\), documents \(PDF, DOC, DOCX, XLS, XLSX\), and text/code files \(TS, JS, PY, JSON, MD, HTML, YAML, and more\)
        -   View update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab
        -   Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.
        -   Validate user interface output during app creation with the UI validation tool in Build Agent, now available in ServiceNow Studio.
        -   Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.
    -   Catalog Item Generation: Migrated Now Assist for Catalog Generation skill group \(Create Catalog Item and Refine Skill\) to Mosaic \(off-Glide GenAI Controller\) by enabling offglide routing via OneExtend
    -   Flow Execution Analysis: Net new app in Now Assist for Creator
    -   Playbook Generation: Playbooks now automatically generate a concise, AI-powered summary of a Playbook's purpose, structure, and logic, helping new process owners quickly understand existing workflows without manual documentation.
    -   Widget Generation and Widget Updation: Australia support
-   Changed: Build Agent
-   New MCP integrations in ServiceNow Studio: Added support for 12 connectors including Atlassian Rovo, DocuSign, Figma, GitHub, Linear, Miro, Prisma Postgres, and Zoom \(Chat, Docs, Revenue Accelerator, Whiteboard\)

</td></tr><tr><td>

Now Assist for CSM Major Issue Management

</td><td>

1.0.1

</td><td>

New: Introduces AI-driven similarity search and case correlation to automatically identify related cases, associate them with major cases, or propose new major case candidates.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

14.0.3

</td><td>

New

 Dependency on store app Now Assist for CSM Major Issue Management

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

4.3.0

</td><td>

\* Changed

 - Engagement tool for DEX agents to obtain employee approval before auto-triggering device actions. This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

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

New: -   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.
-   Generate a business process map \(BPM\) diagram in the Enterprise Modeling &amp; Visualization by uploading an image of an existing process diagram.

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

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to certify features.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

 Fixed

 Removed

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

 When the Code Fix Agent runs into a problem, you will now see a plain-language explanation of what went wrong and what to do next right on the remediation record. Select the links navigate directly to the relevant error record, so there's no need to hunt through system logs.

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

 -   -   The AI Investigation Report displayed an infinite loading spinner on timeout.
-   The Regenerate action in the AI Insights card was non-deterministic. The Express List also showed incorrect insight data when the first analysis run failed.
-   The Autonomous Operator was not updating descriptions on individual HLA alerts.
-   Alert Assist was logging unnecessary errors when no related changes passed the relevance threshold.
-   Alert Assist was logging null pointer exceptions during skill availability checks.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

15.0.1

</td><td>

1.  The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
2.  Knowledge feedback tasks are now deduplicated the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
3.  The Change Quality Agent now persists quality scores per change record including timestamps and contributing factors available for dashboards, audits, and risk-detection workflows.
4.  A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
5.  The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
6.  The Insights and Opportunities for Incident dashboard in Service Operations Workspace aggregates incidents into trend categories with AI-generated summaries, SLA performance, sentiment, channel adoption, and geographic distribution, giving incident managers a consolidated view of incident patterns with drill-down views into individual records.
7.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
8.  The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
9.  A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.

1.  The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
2.  Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
3.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
4.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.

1.  Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
2.  Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.

Suggested Steps has been deprecated and removed. Customers should transition to AI-driven recommendations in Now Assist for ITSM.

</td></tr><tr><td>

Now Assist for Legal Service Delivery

</td><td>

1.8.1

</td><td>

-   Changed: Support for upgraded versions of third party LLMs has been provided.
-   Fixed: Legal request and matter summarization now delivers improved accuracy across all supported models

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

2.2.0

</td><td>

New

 Detect claim anomaly - two new capabilities

 Auto-categorize Repair Claims capability

 GenAI summary on repair claims

</td></tr><tr><td>

Now Assist for Operational Sustainability

</td><td>

22.3.2

</td><td>

Changed

 - This release includes security enhancements that strengthen access controls across the application.

 Fixed

 - ESG business domain scope and knowledge graph tags for disclosure report Corrected the ESG business domain scope and updated knowledge graph tags for the ESG disclosure report to ensure accurate AI-assisted content generation.

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

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

22.3.1

</td><td>

-   New
    -   Implemented meta data changes to enable AI native support to all the skills and agents on regulatory change management product.
    -   All the plugin dependency &amp; role changes to enable AI Native capabilities are implemented as part of this application.
-   Changed: The Now Assist issue summarization skill includes new configuration records offering descriptions and guides for configuration and prompt customization, enhancing the administrator and end-user experience without requiring upgrade actions.

</td></tr><tr><td>

Now Assist for Prompt Assistance

</td><td>

5.0.4

</td><td>

-   New:
    -   Customers will be able to view latency numbers in evaluation run reports \(Agentic Evaluation\). Two latency scores will be available:
        -   Total session time: Measures the complete end-to-end task duration, including AI processing, tool usage, and user input delays.
        -   Agent processing time: Captures the time the AI agent spends working on the task, not counting user delays or waiting.
    -   Agent Instruction Optimization - added support for the latest third-party \(3P\) models, Hierarchical Agents, and Voice Agents.
    -   'Suggested Fixes' in Agentic Evaluation - added support for Hierarchical Agents.
    -   Added Skill Group capability to update LLM providers across all Agentic Judges simultaneously through Now Assist Admin.
-   Changed
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

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications

</td><td>

4.0.1

</td><td>

New:-   Fallout creation AI Agent - This will be automatically generate fallouts in the correct category depending on the Notes/Comments on the Task.
-   Document to Task plan template AI Agent - This Agent will be used to create a Task plan template using an document \( pdg, png,jpeg\) which contains the fulfilment view of the Specification.

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

 Changed

</td></tr><tr><td>

Now Assist for Security Incident Response integrations

</td><td>

1.2.1

</td><td>

Fixed: Adoption of AI Gradient UI for integration builder.

</td></tr><tr><td>

Now Assist for Service Exchange

</td><td>

1.0.13

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Now Assist for Setup

</td><td>

3.0.2

</td><td>

June Release Highlights

</td></tr><tr><td>

Now Assist for Setup Core

</td><td>

2.0.3

</td><td>

June Release Highlights

</td></tr><tr><td>

Now Assist for Smart Assessment Engine

</td><td>

22.3.5

</td><td>

-   New
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

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

10.0.0

</td><td>

New:-   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
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

New: -   Introduced Project Q&amp;A conversational capability to ask questions about your project in natural language and get instant, AI-generated answers directly from the project workspace, without having to manually analyze project data.
-   Use Portfolio insights to analyze planning items in a portfolio plan for execution delays, delayed starts, planned versus approved date misalignments, and projects at risk. View AI-generated root causes and recommended actions to mitigate identified risks and issues.
-   Get demands from Draft to Converted in minutes instead of weeks. The Demand Management AI Specialist reads your governance policies and does the intake work for you.\[Requires approval from Servicenow\]
-   Changed:
    -   Project insights now includes scope creep as an additional topic and considers work notes at the task level as additional context, providing richer and more actionable project visibility.
    -   Updated formatting for in-app insight widgets to improve readability and presentation within the project workspace.
    -   Project Risk Detection now includes clickable links in AI Rationale for quick navigation to referenced project records. Refined Mitigation plan formatting for a better reading experience.

</td></tr><tr><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

8.0.0

</td><td>

New:-   Ability to link emails to the created cases and the supplier records
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

New Changed Fixed

</td></tr><tr><td>

Now Assist for Threat Intelligence Security Center

</td><td>

2.0.0

</td><td>

Initial Release

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
-   Filler message delay is now configurable per deployment. Set the wait time before filler words are spoken during processing-intensive operations to control conversational pacing.
-   Voice assistants now support PSTN request processing. The system selects the appropriate request processor based on the active communication channel, enabling PSTN alongside existing providers.

 Changed

 -   Voice analytics dashboard now organises performance metrics across four tabs Overview, Performance, Insights, and Assist consumption with new metrics for resolution rate, authentication performance, tool execution, conversation sentiment signals, and AI agent assist consumption.
-   execute\_tool and execute\_tool\_guest API responses now include execution plan and task identifiers. Use these identifiers to track and troubleshoot tool executions.
-   Voice language configurations can now be deleted across application scopes. Only voice admins have permission to delete configurations from other scopes.
-   Execution latency metrics are now captured for agent evaluation. The system records execution time data for voice agent plans to support performance analysis.

 Fixed

 Corrected language selection prompts for secondary languages to align with voice-based language selection behavior.

 Removed

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.13

</td><td>

-   New
-   Changed
-   Fixed
-   Removed

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

17.0.7

</td><td>

-   Changed: Suggestion readers are now mapped automatically when Premium Chat is enabled for global search, a workspace, or a service portal, so suggested content surfaces without additional setup.
-   Fixed:
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

-   Changed
    -   Identify missing clauses in contract revisions with improved accuracy.
    -   Support for upgraded versions of third party LLMs has been provided.
-   Fixed
    -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
    -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

6.1.2

</td><td>

-   Changed
    -   Updated default model configuration per ServiceNow platform guidance
    -   Removed UI bounding box visualization feature to resolve node restart issues caused by memory contention during candidate mapping
-   Fixed
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

New Changed Fixed Removed

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

-   New: Auto QA Breakdown Dashboard
-   Changed:
    -   UX improvements
    -   Functional improvements in Admin UI
-   Fixed: UI Fixes related to data visualization

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

10.1.1

</td><td>

Fixed:-   Fixed an issue where the system got stuck in a loop during sensitive detection in topic execution.
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

 - Updated metadata for OSM AI Advanced Application metadata has been updated to reflect current AI capabilities and configurations.

</td></tr><tr><td>

Opportunity Management AI Features

</td><td>

1.0.3

</td><td>

New:-   Manage CRM records conversationally create, view, and update opportunities, contacts, leads, tasks, and accounts using natural language via a conversational interface. Use your MCP client to connect to the Sales CRM MCP server.
-   Get AI-generated summaries of opportunity activity, bringing together emails, tasks, meetings, and product details without manual review.

</td></tr><tr><td>

OT Manager Foundation

</td><td>

3.3.3

</td><td>

New: Certified for Australia Patch 3

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

13.0.8

</td><td>

-   New
    -   Agentic workflow to pro-actively identify escalations. The workflow evaluates various parameters like time remaining for SLA, urgency, priority, impact etc. to provides an escalation label \(Critical, High, Medium\) and reason for escalation.
    -   Skill to predict the next action including attaching relevant KBs, inking cases to Problem tickets, and updating form fields based on record context.
    -   Quick Wins skill that leverages an LLM to analyze task detailsincluding descriptions, short descriptions, journal fields, relevant KBs, and past resolution notesto determine if a task qualifies as a quick win
    -   Skill editing capabilities in NASK, providing a consistent editing experience across NAA and NASK
    -   Citations feature for summarization is now ready for uptake
-   Changed
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
    -   All the plugin dependency &amp; role changes to enable AI Native capabilities are implemented as part of this application.
-   Changed: The Now Assist issue summarization skill includes new configuration records offering descriptions and guides for configuration and prompt customization, enhancing the administrator and end-user experience without requiring upgrade actions.

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

Changed: Query range ACL's -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
-   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
-   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.

</td></tr><tr><td>

Recommended Actions for Security Operations

</td><td>

2.2.1

</td><td>

Changed: Updated the Query range ACL.

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

Sales and Order Management for Telecommunications - Advanced

</td><td>

2.0.2

</td><td>

New

 1. Image to Task plan template AU Agent- Allows users to convert a fulfilment flow image in a pdf, jpeg, png format to a task plan template.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Prime

</td><td>

2.0.2

</td><td>

Please refer to Advanced SKU

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

</td></tr><tr><td>

Security Incident Response - Foundation

</td><td>

1.0.7

</td><td>

Changed

</td></tr><tr><td>

Security Incident Response - Prime

</td><td>

1.0.7

</td><td>

Changed

</td></tr><tr><td>

Service Exchange - Advanced

</td><td>

1.0.2

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Service Exchange - Foundation

</td><td>

1.0.2

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Service Exchange - Prime

</td><td>

1.0.2

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

6.0.1

</td><td>

-   New: Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables: auto-map Excel column headers to ServiceNow table fields, auto-map Excel choice column values to ServiceNow choice field values, and auto-map Excel reference column values to ServiceNow reference field values.
-   Changed: ServiceNow AI Lens now uses visual gradient indicators to distinguish AI-filled form fields from manually entered data.

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

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

New feature:

</td></tr><tr><td>

Software Asset Management AI Prime

</td><td>

2.0.1

</td><td>

New feature:

 Entitlement creation error handling - This feature uses AI to suggest resolutions when users upload the standard Excel import template for entitlement creation.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

1.1.0

</td><td>

 

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

1.1.0

</td><td>

 

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

New -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
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

Test Generation

</td><td>

4.0.11

</td><td>

Changed -   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Third-party Risk Management Advanced

</td><td>

22.3.2

</td><td>

New Fixed

</td></tr><tr><td>

Third-party Risk Management Professional Plus

</td><td>

22.3.2

</td><td>

New Fixed

</td></tr><tr><td>

Threat Intelligence Security Center - Advanced

</td><td>

3.0.0

</td><td>

Initial Release

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

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

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

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
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Enhanced Recommended Actions|1.0.2|2026-05-05|
|App Generation|28.3.11|2025-12-11|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversational Help|2.0.3|2026-03-12|
|Conversational subflows and actions|29.2.2|2026-04-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ - Foundation|1.0.1|2026-04-09|
|CSM - Advanced|1.0.0|2026-04-09|
|CSM - Foundation|1.0.0|2026-04-09|
|CSM - Prime|1.0.0|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DCNAM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Form data collector|2.0.1|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|Google Gemini Spoke|1.6.0|2026-03-12|
|HCLS - Advanced|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|Health and Safety - Advanced|1.0.4|2026-05-05|
|Health and Safety - Foundation|1.0.4|2026-05-05|
|Health and Safety - Prime|1.0.4|2026-05-05|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW - Foundation|1.0.3|2026-05-05|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Prime|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Metadata Search|1.0.11|2026-05-05|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|MID Guardian|1.0.4|2025-12-11|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for ICW|1.0.0|2026-05-05|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Process Mining|3.0.12|2026-05-05|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for WDF|2.0.7|2026-05-05|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in Catalog item forms|1.3.2|2026-05-05|
|Now Assist in Conversational Catalog Request|7.0.2|2026-05-05|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|prompt-management|1.0.11|2026-03-12|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|RAG for code generation|1.1.8|2026-03-12|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.11|2026-05-05|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder AI|1.1.0|2026-05-05|
|TNI and DCNAM AI Content Collection|1.0.0|2026-04-09|
|TNI for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Advanced|1.0.3|2026-04-09|
|TSOM for Telecommunications, Media and Technology - Prime|1.0.3|2026-04-09|
|UI Generation|29.2.5|2026-05-05|
|Zero Copy Connector Hub|3.0.1|2026-03-12|

## Suite version 28.10.20260611 - Zurich Patch 10

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

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

New Changed Fixed Removed Removed outdated terminology and legacy labels associated with prior AI workflow naming and activity actions.

</td></tr><tr><td>

AI Agent Advisor

</td><td>

1.1.0

</td><td>

-   New
    -   Discover automation opportunities across customer service interaction channels chat \(portal and messaging\), voice, and email in addition to incidents and cases.
    -   Transcript-based analysis infers customer intent and resolution steps from conversational language, surfacing automation opportunities that aren't captured in structured fields.
    -   Channel-specific agent matching recommends chat, voice, or email agents based on each opportunity's characteristics.
    -   Channel-appropriate agent generation when no suitable existing agent is found.
-   Changed
    -   Mining scope expanded beyond cases and incidents to include the Interaction table.
    -   Matching pulls from a unified agent registry so chat and voice agents are evaluated alongside existing agents and tools, with no separate setup per channel.
    -   Clustering now incorporates interaction type, transcript content, short description, and referenced knowledge base articles when ranking opportunities by impact.
-   Fixed
    -   Resolved a defect causing opportunity ranking to display in reverse order.
    -   Resolved an issue where asset counts did not match across the UI.

 Removed

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.9.0

</td><td>

New - -   AIOps AI Specialist \(limited availavilblity\) - The AIOps AI Specialist AI is ServiceNows purpose-built AI agent for IT Operations, designed to autonomously monitor, correlate, triage, and resolve infrastructure and application events at enterprise scale.
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

-   New: Added Splunk, AWS CloudWatch, ThousandEyes, SolarWinds, and Prometheus as supported investigation backends for the Analyze alert impact agentic workflow, expanding the alert insights available.
-   Changed
    -   Updated the Analyze alert impact agentic workflow to route all alert investigation through a single SRE Investigate AI Agent, delivering consistent behavior across all supported backends and simplifying the path for adding new vendor agents.
    -   Migrated New Relic and Datadog integrations to Model Context Protocol \(MCP\) agents, standardizing on vendor-maintained tool surfaces so the investigation workflows stay current as vendors ship updates.

 Deprecated

 Deprecated the Dynatrace Analysis AI Agent, superseded by the Dynatrace MCP Server Agent.

</td></tr><tr><td>

AI Agents for Service Exchange Provider

</td><td>

1.0.13

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

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

-   New
-   Changed: Workplace Utilization QnA Agent can now be used by users with the sn\_wsd\_spcmgmt.space\_planner role
-   Fixed: The AI Agent was not always able to block the location after submitting an emergency maintenance request
-   Removed

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

4.0.0

</td><td>

This is a "marker app" with no new functionality added; its purpose is to automatically trigger installation of other apps.

</td></tr><tr><td>

AI Dashboard Insights

</td><td>

1.1.4

</td><td>

-   New
    -   Refine actions You can now refine generated summaries directly within the dashboard using built-in actions such as Elaborate and Shorten, giving you more control over how the summary is presented.
    -   Feedback on generated content Added thumbs up / thumbs down controls to the summary component, making it easy to share feedback on AI-generated summaries.
    -   Dashboard Summary for UI Builder Workspaces Dashboard Summary is now available out of the box in UI Builder Workspaces.
-   Fixed
    -   Consistent cache behavior across summary triggers Both the Refresh and Generate Summary buttons now apply the cache consistently, avoiding redundant AI calls.
    -   Dashboard Summary time zone aligned with user preference The Dashboard Summary now correctly applies the user's configured time zone rather than the system time zone, ensuring consistency with the data shown in dashboard widgets.

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

New -   Record desktop actions more accurately by using the new AI-powered recording mode when creating desktop actions.
-   Save time on manual setup by letting AI automatically insert anchors and generate screen context for each captured screen and add desktop action description after recording.
-   Switch to AI-assisted recording by selecting the new Record with AI \(recommended\) check box that replaces the previous capture modes in the Create desktop action modal.
-   Make desktop actions more flexible by configuring parameters for on-screen task desktop actions.
-   Pass dynamic values at runtime by mapping parameters in the Map parameters section in AI Agent Studio.
-   Control data visibility and security by using the Shared and Mark As Sensitive fields on the Desktop action parameter form.
-   Get a quick guidance on how to effectively use the recorder with the recorder tips modal.

</td></tr><tr><td>

AI Experience Framework Skills

</td><td>

1.1.0

</td><td>

New features for June Release:

 -   Improved error handling and internationalization \(i18n\) support
-   Added streaming capabilities for real-time data processing
-   Resolved critical defects and stability issues
-   Extended support for additional widget property types

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
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

 AIOps AI Specialist \(L1 AI Worker\): AI-powered first responder that autonomously triages alerts, reduces noise, enriches context, and provides remediation recommendations across the alert lifecycle.

 -   Context-rich alert investigation Enhanced alert analysis using CMDB topology, incident history, and operational signals to provide deeper insights and faster decision-making.
-   Knowledge-driven investigation Integrated knowledge sources, including KB articles into the investigation workflow to improve accuracy and deflect incidents
-   Remediation suggestions from existing subflows AI-generated remediation recommendations leveraging existing alert rules and subflows to accelerate resolution and ensure consistency.
-   SRE AI Specialist integration Integrates seamlessly with the SRE AI Specialist for deeper investigation, including observability data analysis and root cause hypotheses

 Dedicated AIOps Manager Homepage

 New homepage for AIOps Managers and Event Management Admins to onboard, configure, and manage AI Specialists from a centralized command center. \_

 \_

</td></tr><tr><td>

Alert Assist

</td><td>

3.9.3

</td><td>

-   New: Proactive Grouping Recommendations AI-generated grouping recommendations help AIOps administrators identify alert correlation opportunities with greater speed and accuracy.
-   Changed: Updated supported LLM versions to GPT-4o Mini and Claude Haiku 4.5, bringing the latest model improvements to the platform.
-   Fixed: The Autonomous Operator was not automatically updating the description of HLA alerts. This has been corrected.

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

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

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

Changed -   Added voice-driven case status retrieval and updates, enabling customers to check open case statuses and submit updates through guided voice interactions across Genesys, NICE, Five9, 3CLogic, and Amazon Connect, reducing live agent dependency.
-   Enhanced Provide Customer 360 Insights with Enterprise Graph and AI Agent deep research for richer, more contextual query results.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

2.0.1

</td><td>

New -   Agent renamed to "Vision AI Agent"
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

Employee Slate for Now Assist

</td><td>

1.0.7

</td><td>

This release provides the following enhancements and improvements.

 -   Enhanced accessibility support Performance improvements Support for L10n Enhanced telemetry support for tracking user behavior Enhanced the home page layout with auto-adjust flexibility based on the widgets count Enhanced Admin configuration to support Tasks and requests \(fka Inbox\), To-dos task type configurations
-   Enhanced AI Preferences to support Smart Prioritisation and AI-Generated Summarisation
-   Enhanced the option to load AI summary automatically or on demand on AI summary details page

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

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to ensure certification and release standards.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

 Fixed

 Removed

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

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

Group-Action Framework

</td><td>

7.0.1

</td><td>

-   New: Backend support for HR Knowledge Gaps. This capability will be taken up by the Knowledge Center team in a future release. No customer-facing updates in this release.
-   Changed: Nothing changed in this release.
-   Fixed: Various minor defects fixed.
-   Removed: Nothing removed in this release.

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

New: Added new skills for Interview health tracker.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

Insights Clustering Utils

</td><td>

3.1.0

</td><td>

-   New: Updates to support AI Agent Advisor.
-   Changed: Nothing changed in this release.
-   Fixed: Nothing fixed in this release.
-   Removed: Nothing removed in this release.

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

9.0.0

</td><td>

1.  The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
2.  Knowledge feedback tasks are now deduplicated the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
3.  The Change Quality Agent now persists quality scores per change record including timestamps and contributing factors available for dashboards, audits, and risk-detection workflows.
4.  A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
5.  The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
6.  A new manager dashboard aggregates incidents into issue-based clusters with health metrics and drill-down views, giving incident managers a consolidated view of emerging problem areas.
7.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
8.  The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
9.  A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.

 1.  The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
2.  Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
3.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
4.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.

 -   Fixed- None
-   Removed - None

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.4.0

</td><td>

-   New: n/a
-   Changed: Security related enhancements on existing AI Voice agents
-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.3.2

</td><td>

-   New
    -   Service Mapping supports the Model Context Protocol \(MCP\), providing a conversational interface for live application service data. Service Mapping admins can connect Claude Desktop to a ServiceNow instance and query service topology, server-to-service relationships, related CIs, and unmapped configuration items.
    -   Service Mapping Workspace widgets1. Business app linked to App services - Indicating the count of business applications that were linked to application services by the Business App Mapping AI Agent.2. Maps created by Now Assist - Indicating the count of the service maps created by Service Mapping AI Agent.
-   Changed
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

-   New: Delivery note upload for quantity disputes: Customers can upload delivery notes during case creation, enabling the invoice dispute intake assistant AI agent to validate and resolve quantity disputes without human intervention.
-   Changed: Order line quantity validation for disputes: The invoice dispute support assistant AI agent uses order line data when sold product records are unavailable such as new orders, non-serialized products, or services. It auto-approves valid disputes and escalates only when data is unclear.

</td></tr><tr><td>

Manage Order Operations

</td><td>

2.0.3

</td><td>

-   New
-   Automated email notifications for order cases: Send emails when the AI agent opens an order case from a Business Portal chat and when the case is resolved. Closure emails include resolution and quote details, if generated. Voice-created cases don't trigger emails.Scripted extension point for quote thresholds: A scripted extension point to integrate the manage order operations AI agent with your inventory, ERP, and quote systems for quote threshold evaluation. The AI agent generates a quote when a quantity-change request exceeds the configured price threshold.
-   Changed
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

New: Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and reason about goals, portfolio plans, and projects. The following tools are available in this release: Tool Description get\_goals Retrieves goals and objectives. generate\_goal\_insights Generates AI-powered insights for goals and targets. get\_portfolio\_plans Retrieves portfolio plans. generate\_portfolio\_insights Generates portfolio insights, including at-risk projects, delayed starts and ends, and dependencies. get\_projects Retrieves projects. generate\_project\_insights Detects project risks, analyzes status trajectory, and provides recommendations. identify\_project\_risks Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts. get\_ai\_status\_report Generates a RAG \(Red, Amber, Green\) status report across resources, cost, schedule, and scope.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.12.0

</td><td>

Removed : api-version query parameter from Create Response OEM action

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.5.0

</td><td>

New

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.2.0

</td><td>

Changed: Minor API changes for another app support internally

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

1.5.1

</td><td>

Performance improvements implemented, and third-party IDPs now allowed to be used.

</td></tr><tr><td>

Moveworks AIS Enabler

</td><td>

1.1.3

</td><td>

OOTB Search profile and related details for Moveworks

</td></tr><tr><td>

Notifications Email Agents

</td><td>

2.1.1

</td><td>

New -   Multi-intent identification support
-   Missing inputs extraction
-   email branding/template support for email generation

</td></tr><tr><td>

Now Assist Admin Console

</td><td>

10.0.11

</td><td>

Skill Archival Instance and system administrators can now archive custom skills directly from the Now Assist Skills page. Archiving is not supported for ServiceNow out-of-box \(OOB\) skills. Archived skills can be restored at any time.

 Skill Details Page View Detail button is now available alongside the Activate button for OOB skills on the Now Assist Skills page. The Skill detail view provides administrators and users with key information about a skill including its benefits, prerequisites, recommended model provider, and related skills enabling informed activation decisions.

 Prompt Injection Enhancements Prompt injection protection can now be configured at both the instance level and the product level \(CSM, ITSM, and others\), giving administrators more granular control over enforcement across workflows.

 Model Version Management Guided Tour Administrators can now launch a guided tour walkthrough directly from the " Manage Model Versions" section within Settings section in now assist admin. The guided tour provides a step-by-step introduction to the model version management workflow, helping admins understand version lifecycle, deprecation alerts, and available actions.

</td></tr><tr><td>

Now Assist Agents for requestor

</td><td>

3.5.0

</td><td>

Approval checklist generator skill accepts additional context parameter that is used to resolve checklists unknown items.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

8.0.10

</td><td>

-   New: AI Agent Extensibility: Customers can now add / remove AI agents or tools from OOTB agents while remaining on the upgrade path.
-   Changed: Orchestrator defaults to GPT-5.4: The orchestrator now uses GPT-5.4 as its default model when Azure OpenAI is the selected LLM.
-   Fixed
    -   Agent Execution
        -   Published version instructions not being applied to agents at runtime.
        -   Execution plan fetch timing out on instances with large numbers of execution plan records.
        -   Agentic workflow stuck at orchestrator step intermittently.
        -   VA transaction timeout and conversation stuck on "Thinking."
    -   Agent-to-Agent \(A2A\)
        -   Async handling of working state from secondary agent causing primary flow issues.
        -   Raw rich control output in agent response causing conversation to fault and close abruptly.
        -   input-required response sending empty message/parts block.
    -   Multilingual
        -   Tool names, agent names, and "Processing new information" untranslated in AI steps.
        -   Words not translated when user language differs from system language \(intermittent\).

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

31.0.5

</td><td>

Changed -   Browser tabs that open during goal execution in adaptive desktop actions remain open after the goal completes. Use the keep\_tab\_open system property to turn this behavior on or off. The property is turned on by default.
-   Adaptive desktop actions is enhanced to improve execution efficiency.

</td></tr><tr><td>

Now Assist Analytics

</td><td>

5.0.3

</td><td>

New -   Analytics dashboards pertaining to AI agents, AI assistants, and skills are consolidated inside Now Assist Center &gt; Monitor.
-   Executions dashboard in Now Assist Center: Deep dive into individual executions of assistants and agents to improve performance.
-   Business value dashboard in Now Assist Center: Analyze the impact of AI assets on time and cost savings and set formula for calculating value per AI asset \(skills, AI agents, agentic workflows\)

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

- Increased sample data input limit for SDG requests Users \(Data Kit Admin\) can now select up to 50 seed records from a data collection or table when submitting a Synthetic Data Generation request, up from the previous default of 3. The maximum sample size is also configurable by NADK Admins via sys\_property.

 - Plausibility Metrics for Synthetic Data Introduced plausibility scoring as a new data quality insight layer within the Generated Data view \(Data Kit &gt; Home &gt; Synthetic Data tab &gt; Open Generated Data &gt; Data Insight &gt; Plausibility\). Validates that generated field values are realistic, internally consistent, and free of garbage data.

 - OOB data sets

</td></tr><tr><td>

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

8.0.0

</td><td>

New -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
-   Enhanced workflow to enable requesters to accept/reject the case resolution.

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

29.2.3

</td><td>

Changed: Updated versions of dependent apps.

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

Fixed: Security fixes

</td></tr><tr><td>

Now Assist for Contract Analysis

</td><td>

1.0.9

</td><td>

Existing feature: with latest third party model versions

</td></tr><tr><td>

Now Assist for Creator

</td><td>

28.9.3

</td><td>

-   New
    -   Build Agent
        -   Upload files to Build Agent to provide context: images \(PNG, JPEG, GIF, WEBP\), documents \(PDF, DOC, DOCX, XLS, XLSX\), and text/code files \(TS, JS, PY, JSON, MD, HTML, YAML, and more\)
        -   View update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab
        -   Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.
        -   Validate user interface output during app creation with the UI validation tool in Build Agent, now available in ServiceNow Studio.
        -   Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.
    -   Catalog Item Generation: Migrated Now Assist for Catalog Generation skill group \(Create Catalog Item and Refine Skill\) to Mosaic \(off-Glide GenAI Controller\) by enabling offglide routing via OneExtend
    -   Playbook Generation: Playbooks now automatically generate a concise, AI-powered summary of a Playbook's purpose, structure, and logic, helping new process owners quickly understand existing workflows without manual documentation.
-   Changed: Build Agent: New MCP integrations in ServiceNow Studio: Added support for 12 connectors including Atlassian Rovo, DocuSign, Figma, GitHub, Linear, Miro, Prisma Postgres, and Zoom \(Chat, Docs, Revenue Accelerator, Whiteboard\)

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

13.0.3

</td><td>

Changed: -   Enhanced case insights card with customer details
-   Enabled sentiment analysis on email interactions.

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

4.3.0

</td><td>

\* Changed

 - Engagement tool for DEX agents to obtain employee approval before auto-triggering device actions. This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

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

-   New
    -   AI-powered mobile form auto-fill for field technicians.: Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
    -   Consistent AI visual indicators across applications.: AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
    -   Parts Debrief automation in NAP and NAVA.: Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
    -   Expanded AI summarization and knowledge workflows.: Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
    -   Create work order agent with enhanced persona coverage.: System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
    -   FSM AI Mandate features available on mobile and workspace.: FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
    -   Telemetry for AI feature usage.: Admins can track AI lens feature usage for FSM use cases.
    -   Skill refinement for FSM digital agents.: FSM agents enhanced for improved automation and workflow handling.
-   Changed
    -   Broadened test and validation coverage for FSM AI use cases.: Testing expanded across mobile/agent/NextWave experiences to certify features.
    -   Enhanced automation for AI SKU and agent studio test cases.: Remaining automation scenarios completed with monitoring on latest NAP version.
    -   Improved parts debrief workflow handling.: Better management of edge cases like unrecognized assets and invalid task states.
    -   Refined questionnaire answer validation in summarization workflows.: Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
    -   Performance testing for Q1 deliveries.: Testing conducted to ensure system stability and responsiveness.

 Fixed

 Removed

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

 When the Code Fix Agent runs into a problem, you will now see a plain-language explanation of what went wrong and what to do next right on the remediation record. Select the links navigate directly to the relevant error record, so there's no need to hunt through system logs.

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

 -   -   The AI Investigation Report displayed an infinite loading spinner on timeout.
-   The Regenerate action in the AI Insights card was non-deterministic. The Express List also showed incorrect insight data when the first analysis run failed.
-   The Autonomous Operator was not updating descriptions on individual HLA alerts.
-   Alert Assist was logging unnecessary errors when no related changes passed the relevance threshold.
-   Alert Assist was logging null pointer exceptions during skill availability checks.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

15.0.1

</td><td>

1.  The L1 Service Desk AI Specialist now detects knowledge gaps and automatically creates a Knowledge Feedback Task when KB search returns no results above the configured relevance threshold, enabling managers to create missing articles.
2.  Knowledge feedback tasks are now deduplicated the system checks for existing open tasks with matching category and subcategory within a lookback window before creating a new one, preventing task noise for gaps like password resets.
3.  The Change Quality Agent now persists quality scores per change record including timestamps and contributing factors available for dashboards, audits, and risk-detection workflows.
4.  A new KB article usage section on the AI Agent Studio Performance dashboard shows which articles the AI Specialist used during autonomous resolution.
5.  The AI Specialist now persists the Skill applied per incident evaluation onto the record. A new Skill filter on the AIS Performance Dashboard lets managers segment performance by capability area.
6.  The Insights and Opportunities for Incident dashboard in Service Operations Workspace aggregates incidents into trend categories with AI-generated summaries, SLA performance, sentiment, channel adoption, and geographic distribution, giving incident managers a consolidated view of incident patterns with drill-down views into individual records.
7.  IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, guided through approvals, risk scoring, and workflows via natural language.
8.  The ZTS AI L1 Service Desk Specialist now supports real-time conversational engagement via Microsoft Teams or Slack, replacing the asynchronous activity stream with a consent-driven experience.
9.  A new agentic solution for SharePoint access issues autonomously handles L1 scenarios including access requests, file failures, and permission mismatches, reducing resolution time from hours to minutes.

1.  The AI Specialist Performance Dashboard now includes revised productivity metrics measuring incidents attempted against total count for a more accurate resolution baseline.
2.  Targeted enhancements to the L1 Service Desk AI Specialist improve reliability and consistency based on quality feedback from recent releases.
3.  The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
4.  The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.

1.  Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
2.  Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.

Suggested Steps has been deprecated and removed. Customers should transition to AI-driven recommendations in Now Assist for ITSM.

</td></tr><tr><td>

Now Assist for Legal Service Delivery

</td><td>

1.8.1

</td><td>

-   Changed: Support for upgraded versions of third party LLMs has been provided.
-   Fixed: Legal request and matter summarization now delivers improved accuracy across all supported models

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

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Prompt Assistance

</td><td>

5.0.4

</td><td>

-   New:
    -   Customers will be able to view latency numbers in evaluation run reports \(Agentic Evaluation\). Two latency scores will be available:
        -   Total session time: Measures the complete end-to-end task duration, including AI processing, tool usage, and user input delays.
        -   Agent processing time: Captures the time the AI agent spends working on the task, not counting user delays or waiting.
    -   Agent Instruction Optimization - added support for the latest third-party \(3P\) models, Hierarchical Agents, and Voice Agents.
    -   'Suggested Fixes' in Agentic Evaluation - added support for Hierarchical Agents.
    -   Added Skill Group capability to update LLM providers across all Agentic Judges simultaneously through Now Assist Admin.
-   Changed
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

Now Assist for Sales and Order Management for Telecommunications

</td><td>

4.0.1

</td><td>

New -   Fallout creation AI Agent - This will be automatically generate fallouts in the correct category depending on the Notes/Comments on the Task.
-   Document to Task plan template AI Agent - This Agent will be used to create a Task plan template using an document \( pdg, png,jpeg\) which contains the fulfilment view of the Specification.

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

 Changed

</td></tr><tr><td>

Now Assist for Service Exchange

</td><td>

1.0.13

</td><td>

Connections tab in the Service Exchange Center

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting

 Group-based persona assignments for Remote Catalog

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Now Assist for Setup

</td><td>

3.0.2

</td><td>

June Release Highlights

</td></tr><tr><td>

Now Assist for Setup Core

</td><td>

2.0.3

</td><td>

June Release Highlights

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

8.0.1

</td><td>

New feature:

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

10.0.0

</td><td>

New -   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
-   The Savings Opportunity Discovery agentic workflow analyzes contracts, spend data, sourcing pipeline data, and supplier performance on a recurring schedule to automatically identify a prioritized list of savings opportunities. Category managers can review each opportunity in the Now Assist Panel and create a pipeline project or dismiss the opportunity directly from the panel.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

9.6.0

</td><td>

-   New:
    -   Introduced Project Q&amp;A conversational capability to ask questions about your project in natural language and get instant, AI-generated answers directly from the project workspace, without having to manually analyze project data.
    -   Use Portfolio insights to analyze planning items in a portfolio plan for execution delays, delayed starts, planned versus approved date misalignments, and projects at risk. View AI-generated root causes and recommended actions to mitigate identified risks and issues.
    -   Get demands from Draft to Converted in minutes instead of weeks. The Demand Management AI Specialist reads your governance policies and does the intake work for you.\[Requires approval from Servicenow\]
-   Changed:
    -   Project insights now includes scope creep as an additional topic and considers work notes at the task level as additional context, providing richer and more actionable project visibility.
    -   Updated formatting for in-app insight widgets to improve readability and presentation within the project workspace.
    -   Project Risk Detection now includes clickable links in AI Rationale for quick navigation to referenced project records. Refined Mitigation plan formatting for a better reading experience.

</td></tr><tr><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

8.0.0

</td><td>

New -   Ability to link emails to the created cases and the supplier records
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
-   Filler message delay is now configurable per deployment. Set the wait time before filler words are spoken during processing-intensive operations to control conversational pacing.
-   Voice assistants now support PSTN request processing. The system selects the appropriate request processor based on the active communication channel, enabling PSTN alongside existing providers.

 Changed

 -   Voice analytics dashboard now organises performance metrics across four tabs Overview, Performance, Insights, and Assist consumption with new metrics for resolution rate, authentication performance, tool execution, conversation sentiment signals, and AI agent assist consumption.
-   execute\_tool and execute\_tool\_guest API responses now include execution plan and task identifiers. Use these identifiers to track and troubleshoot tool executions.
-   Voice language configurations can now be deleted across application scopes. Only voice admins have permission to delete configurations from other scopes.
-   Execution latency metrics are now captured for agent evaluation. The system records execution time data for voice agent plans to support performance analysis.

 Fixed

 Corrected language selection prompts for secondary languages to align with voice-based language selection behavior.

 Removed

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.13

</td><td>

-   New
-   Changed
-   Fixed
-   Removed

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

17.0.7

</td><td>

-   Changed: Suggestion readers are now mapped automatically when Premium Chat is enabled for global search, a workspace, or a service portal, so suggested content surfaces without additional setup.
-   Fixed
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

-   Changed
    -   Identify missing clauses in contract revisions with improved accuracy.
    -   Support for upgraded versions of third party LLMs has been provided.
-   Fixed
    -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
    -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

6.1.2

</td><td>

-   Changed
    -   Updated default model configuration per ServiceNow platform guidance
    -   Removed UI bounding box visualization feature to resolve node restart issues caused by memory contention during candidate mapping
-   Fixed
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

New Changed Fixed Removed

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

-   New: Auto QA Breakdown Dashboard
-   Changed
    -   UX improvements
    -   Functional improvements in Admin UI
-   Fixed: UI Fixes related to data visualization

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

10.1.1

</td><td>

Fixed -   Fixed an issue where the system got stuck in a loop during sensitive detection in topic execution.
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

Opportunity Management AI Features

</td><td>

1.0.3

</td><td>

New -   Manage CRM records conversationally create, view, and update opportunities, contacts, leads, tasks, and accounts using natural language via a conversational interface. Use your MCP client to connect to the Sales CRM MCP server.
-   Get AI-generated summaries of opportunity activity, bringing together emails, tasks, meetings, and product details without manual review.

</td></tr><tr><td>

OT Manager Foundation

</td><td>

3.3.3

</td><td>

New: Certified for Australia Patch 3

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

13.0.8

</td><td>

-   New
    -   Agentic workflow to pro-actively identify escalations. The workflow evaluates various parameters like time remaining for SLA, urgency, priority, impact etc. to provides an escalation label \(Critical, High, Medium\) and reason for escalation.
    -   Skill to predict the next action including attaching relevant KBs, inking cases to Problem tickets, and updating form fields based on record context.
    -   Quick Wins skill that leverages an LLM to analyze task detailsincluding descriptions, short descriptions, journal fields, relevant KBs, and past resolution notesto determine if a task qualifies as a quick win
    -   Skill editing capabilities in NASK, providing a consistent editing experience across NAA and NASK
    -   Citations feature for summarization is now ready for uptake
-   Changed
    -   Ability to filter on additional fields from record table \(Asst group, Service, CI\) for Analyze Task Trends
    -   Update Resolution notes activity filtering to include ai activity \(include\_ai\_updates\) config
    -   Updates to Citations to include related records
    -   Filter on additional params from record table for IWIS
    -   Summary of the generated work plan
    -   Auto classification of records GAF and config for Analyze task trends

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

Recommended Actions for Security Operations

</td><td>

2.2.1

</td><td>

Changed: Updated the Query range ACL.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

6.0.1

</td><td>

-   New: Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables: auto-map Excel column headers to ServiceNow table fields, auto-map Excel choice column values to ServiceNow choice field values, and auto-map Excel reference column values to ServiceNow reference field values.
-   Changed: ServiceNow AI Lens now uses visual gradient indicators to distinguish AI-filled form fields from manually entered data.

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
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

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.4.0

</td><td>

Resolved an installation issue that prevented Voice Input from activating correctly on some instances.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Enhanced Recommended Actions|1.0.2|2026-05-05|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversational Help|2.0.3|2026-03-12|
|Conversational subflows and actions|29.2.2|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|Manufacturing Commercial Operations AI agents collection|2.0.2|2026-03-12|
|Metadata Search|1.0.11|2026-05-05|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|MID Guardian|1.0.4|2025-12-11|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Enterprise Architecture \(EA\)|7.1.0|2026-03-12|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.0.1|2026-03-12|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.8|2026-05-05|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in Catalog item forms|1.3.2|2026-05-05|
|Now Assist in Conversational Catalog Request|7.0.2|2026-05-05|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|prompt-management|1.0.11|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM AI agent collection|1.3.0|2026-03-12|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.11|2026-05-05|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.1.0|2026-05-05|
|UI Generation|28.2.14|2026-01-23|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|

## Suite version 28.5.20260611 - Zurich Patch 5

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Agentic Desktop

</td><td>

1.0.0

</td><td>

New-   Design desktop actions of type UI block by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block that include pre-built connectors to interact with various applications and system components.
-   Add the desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy and desktop applications without APIs.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session. Interact with the automation when human input is required.
-   Changed
-   Fixed
-   Removed

</td></tr><tr><td>

AI Agents for ACC

</td><td>

1.0.0

</td><td>

Initial release of "Agent Client Collector \(ACC\) Diagnostic" agentic workflow

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.6.3

</td><td>

CHANGED: Success analysis AI agent has been removed, and we have introduced a new skill for trend analysis. The skill name is Analyze metric data trend.NEW: Agentic workflows

Workflow: Trigger risk mitigation touchpoint workflow

-   1.Meeting Draft Creator AI Agent - \_\_Automates meeting draft creation using context and history, ensuring completeness and reducing manual effort
-   2.Draft Meeting Scheduler AI Agent - Automates virtual meeting scheduling by collecting invitee and provider details from the user.

Workflow: Support renewal and expansion

-   a. Renewal analysis AI Agent\_
-   b. Success insight AI Agent
-   c. Value realization assessor AI Agent

</td></tr><tr><td>

AI Agents for Discovery

</td><td>

1.0.2

</td><td>

New - Introducing Certificate Renewal Agent Workflow to help you renew the certificates that are nearing expiry with the help of an agent. The system tracks discovered certificates, monitors their expiry dates, creates renewal tasks for the certificates and proactively notifies PKI admin via email.Through the NowAssist panel in the Certificate Management workspace, administrators can engage with the agentic workflow with the usage of natural language conversation.

-   This intelligent agent allows the PKI admin to check for certificates nearing expiry with just a simple prompt and can initiate their renewal with minimal interaction.
-   By delegating these tasks to the agent, administrators can significantly reduce manual effort and time spent on renewals.
-   This real-time capability helps prevent certificate outages, streamlines certificate management, and ensures organizations can adapt to shorter renewal cycles.
-   Also in this process it auto-generates CSR and stores the private key in community edition of Hashi-Corp vault \(The auto generation of CSR is supported fromYP8 onwards\)

 Changed N/A \(Initial Release\) Fixed N/A \(Initial Release\) Removed N/A \(Initial Release\)

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.0.3

</td><td>

Updated to support the latest version of the dependent app.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

3.0.1

</td><td>

With the Now Assist for Hardware Asset Management \(HAM\) application, Hardware Asset Managers can streamline and automate the process of sourcing hardware assets by using AI agents included in the agentic workflow. The Now Assist for Hardware Asset Management \(HAM\) application contains agentic workflows to automate the sourcing, transfer, and procurement of assets upon request.

 -   Role masking in AI Agent Studio to execute agentic workflows, AI agents, and tools.
-   New security configuration pages in AI Agent Studio.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Store episodic memory of agentic conversations with agent learning.
-   Create and update UI actions for workflows.
-   Framework extensibility with new condition builder.
-   Add Desktop action as a tool to an AI agent.
-   Support for multilingual conversations.
-   MCP Client enhancements

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.0.3

</td><td>

-   New:
    -   Workplace Insights for key indicators like floor utilization, attendance, reservation no-shows, and space inefficiencies are generated and surfaced on the landing dashboard in Workplace Central.
    -   Introduced a new Workplace Insights AI Skill that analyzes the data and generates the insights. Workplace Reservation QnA Agent: Workplace Managers can ask natural language questions related to reservations from the Now Assist Panel and receive responses.
-   Changed: NA
-   Fixed:
    -   Sometimes, the reservation details could not be extracted from the case number when using the "Help manage workplace reservations" workflow
    -   Security fixes
-   Removed: NA

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

2.0.1

</td><td>

No new changes

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.3.2

</td><td>

Fixed: removed json.stringify for request

</td></tr><tr><td>

Analytics Generation

</td><td>

4.0.3

</td><td>

-   Skill moved under Data and Analytics Workflow \(Analytics product\) in Now Assist Admin
-   Extended querying capabilities to support:
    -   Stacked group chart \(e.g. show tasks grouped by state and stacked by priority\)
    -   Top/bottom X questions \(e.g. show top 5 assignment groups that has most number of open incidents\)
-   Bug fix

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

</td></tr><tr><td>

Catalog Conversational Coverage

</td><td>

5.2.5

</td><td>

New

 Included tailored recommendations to help you improve your catalog items for the conversational channel, making it easier for you to identify areas that need enhancement.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.5.4

</td><td>

-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   CRR Completness Metric
-   performance improvement fix

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.8.15

</td><td>

-   Honor In-Product roles in Sidebar Chat Summarization
-   Add new skill configuration for Standalone Sidebar Discussions
-   Support selection of portal in multiple skill configs in Agent Chat Summarization
-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   Defect fixes

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

Conversation Insights

</td><td>

2.0.2

</td><td>

New: Inferred CSAT segmented by Intent Displayed in AI Agent Analytics dashboard. Display top intents for the selected agentic workflows and/or AI agents. Display average CSAT for intents of selected AI assets.

</td></tr><tr><td>

Conversational Studio

</td><td>

6.0.6

</td><td>

-   New
    -   "Assistant" module that includes the end-to-end admin configuration for Assistants
    -   Ability to change the visibility of individual Assets per Assistant
    -   Conversational settings modal within individual Assets
    -   Ability to bulk remove Assets from Assistants
    -   Ability to create new Assets \(including AI Agents, Subflows/Actions, Custom Skills, Topic\) from the Assistant Designer
    -   Voice Assistants
-   Changed: Test panel UX update, more data available
-   Fixed
    -   Changing asset to inactive should not clear the visibility and discoverability configs
    -   Topic migration
    -   Misc. defects
-   Removed

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

28.2.11

</td><td>

N/A. Initial release.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

4.0.0

</td><td>

NewCustomer 360 is an AI-powered assistant for the human agent that answers natural language questions about customers, cases, products, and interactions. This feature helps agents quickly access critical information and resolve cases.

 Changed

 Role configuration is required for Agentic workflows and AI agents.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

0.1.8

</td><td>

New application

</td></tr><tr><td>

Document Intelligence for Contract Management Content Pack

</td><td>

1.3.1

</td><td>

New: Added a predefined use case for the Obligation Extraction skill that includes definitions for extracting two distinct categories of obligations from contracts.

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

1.0.3

</td><td>

Create work order from text in NAP and NAVA.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Flow Designer GenAI

</td><td>

28.2.3

</td><td>

New:

 Users will have an option to call an agent from workflow

</td></tr><tr><td>

Flow Generation

</td><td>

28.2.5

</td><td>

New: Support the Now LLM Long Term Stable models \(LTS\).

</td></tr><tr><td>

Flow Summarization

</td><td>

28.2.4

</td><td>

New: Support for the Now LLM Long Term Stable models \(LTS\).

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

Google Gemini Spoke

</td><td>

1.5.3

</td><td>

Fixed: removed json.stringify for request

</td></tr><tr><td>

GRC Common GenAI

</td><td>

21.1.8

</td><td>

New:

 Issue Submission Agent:

 The issue submission AI agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.

 Changed:

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

21.1.8

</td><td>

-   New
    -   Control objective impact analyzer: This Gen AI skill analyzes changes in citations and identifies control objectives that should be reviewed based on the modified citation content.
    -   Control objective detail updater: For a given control objective, validate whether the description and supplemental guidance needs to be updated based on associated citations, and suggest new content when updates are required. This skill is triggered only by the AI agent, Control objective change agent.
    -   Control objective change agent: This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates.
    -   Enabled Now LLM LTS and Role masking support for the recommendation of similar control objectives and common control objective creation skills.
    -   Control objective requirements and control requirements are now considered in the Rationalization process for control objectives.
-   Changed: Rationalization process now automatically generates recommendations using the skill when you select Rationalize button in the Control objective page.

</td></tr><tr><td>

HR Service Delivery AI agent collection

</td><td>

5.0.9

</td><td>

New -   Help resolve tuition reimbursement requests agentic workflow supports the post-completion reimbursement process. It automatically evaluates employee-submitted grades, transcripts, and documentation against company policies and returns a decision of approval, denial, or request for additional information
-   Generate onboarding ramp-up plan workflow - Performance improvements for faster creation and manager review
-   Resolve Non Critical HR Cases - Predicts the criticality of the HR case and sends the response to the employee if the HR case is non critical.
-   Predict Service and Transfer HR cases - Predict the correct HR Service of the HR Case.
-   Resolve Critical HR Cases - Provides the ability for the HR Agents to generate a step by step plan

Enhanced

-   Help resolve tuition requests agentic workflow - Performance improvements for faster policy evaluation and case resolution
-   Security - Implemented role masking to strengthen AI agent security and protect sensitive employee information

</td></tr><tr><td>

HR Talent AI Agent Collection

</td><td>

3.0.0

</td><td>

Whats New The Employee feedback collection AI Agent streamlines the process of gathering employee feedback, ensuring managers receive timely, structured, and actionable input. Persona: ManagerThe agent:

 -   Suggests relevant collaborators of the employee using data from Employee Profile, Talent Development apps, and optional Microsoft Graph interaction insights \(using the Microsoft Exchange Online spoke\)
-   Sends requests as EC To-Dos for the feedback providers and sends automated reminders
-   Consolidates all feedback responses into a single view for easier evaluation

 Updates

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.0.5

</td><td>

No functional changes, only updates for Dec platform agents

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

21.1.6

</td><td>

New -   Use AI-generated recommendations to identify which policies are impacted by a regulatory alert
-   Use the Get Regulatory Insights agentic workflow to enrich regulatory alerts with external context, classification, summarization, and recommended potentially impacted items
-   Use the Generate Regulatory Action Plan agentic workflow to convert regulatory insights into actionable compliance strategies, including structured tasks with clear ownership and timelines

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

21.1.6

</td><td>

\[New\]

 Now LLM LTS and Role masking support are now enabled for risk event summarization

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.1.4

</td><td>

Now Assist for ITSM release notes \[Zurich\]

 -   New: Initial release for ITSM Voice AI agent. See the Key features section for more details.
-   Changed: n/a
-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.2.5

</td><td>

Changed: Added compatibility with the "Now Assist for Platform" app, version 10.0.3

</td></tr><tr><td>

Knowledge Center

</td><td>

31.0.8

</td><td>

The Knowledge Center centralized hub for Knowledge Admin and Manager:

 1. Is an entry point for KM Management personas to manage all capabilities and configurations 2. Guides users on the next-best actions to take by displaying actionable key insights 3. Is a suite of KM Tools for suggesting content creation, updates, duplicates, and article retirement

</td></tr><tr><td>

Manage Order Operations

</td><td>

1.0.2

</td><td>

Initial Release:

 -   Automate the process of creating order cases on the Business Portal.
-   Retrieve customer inputs in text or voice format, classify intent, and route them to the Virtual Agent for action.
-   Identify the earliest possible delivery date for expedited product delivery on a specific customer order.
-   Create an order case autonomously based on the inputs on the Now Assist panel.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.8.1

</td><td>

New: Support responses actions for CUA.

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.4.7

</td><td>

New -   Long-Term Support \(LTS\) model that delivers regulatory alignment, predictable behavior, and lifecycle stability is now supported.
-   Added role based access control to the generation skill of mobile card.This access control only allows specific roles of delegated\_developer and sn\_mab\_api.admin to generate the mobile card.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

1.2.4

</td><td>

-   PRM\(Protected Resource Metadata\) support for MCP servers
-   reduced latency for few MCP servers

</td></tr><tr><td>

Notifications Email Agents

</td><td>

1.0.7

</td><td>

New: The email agentic workflow introduces enhanced capabilities to intelligently process incoming emails by:

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

28.2.7

</td><td>

New: Use the custom app record summarization skill to generate AI summaries for tables in custom applications. You can generate summaries in-product and through chat in the Now Assist panel.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

4.0.1

</td><td>

-   New: Agile team members can now use Now Assist to generate acceptance criteria for a story based on the short description and description
-   Changed
-   Fixed: Performance improvement of Now Assist skills in CWM

 Deprecated/Removed

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

3.0.10

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Environmental, Social, and Governance \(ESG\)

</td><td>

21.1.6

</td><td>

New: Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions. The carbon calculations agentic workflow acts as a copilot for sustainability teams, streamlining carbon accounting workflows. It intelligently selects metric definitions and emission factors from the library, generates calculated metric definitions, and allows users to review and make adjustments before final use.

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

8.0.5

</td><td>

-   Added new feature to create work order from text in NAP and NAVA.
-   Included Smart Assessment / Questionnaire summary in work order task summarization.

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

5.0.0

</td><td>

-   New
-   Changed: Prompt migration to NASK: Summarization skill prompts have been migrated into the Now Assist Skill Kit \(NASK\), enabling admins to configure, modify, and maintain summarization skills using the new OOB editable experience. This update preserves full administrative control while aligning skills to the modern, centralized prompt management framework.

</td></tr><tr><td>

Now Assist for Hardware Asset Management

</td><td>

3.0.1

</td><td>

In this release, users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

 -   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent
-   Hardware asset repair process \(patch\)

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

12.0.7

</td><td>

New / enhancements- The case summarization skill is enabled for the attachment summaries

 - The resolution notes skill is enabled with NACM for the shortening/elaborating resolution notes summary

 - On the Agent Workspace application, the resolution notes skill is enabled to auto-populate Close notes field

 Changed:

 - Enhanced security features revisit the ACL roles and access;Support to GPT OSS model

</td></tr><tr><td>

Now Assist for Impact

</td><td>

2.0.18

</td><td>

Consumption Report summary

 -   Produces an insightful, human-readable summary which highlights key business objectives with active and completed initiatives and accelerators.
-   The summary flags any concerning trends in severity \(P1/P2 dominance\).
-   It also reviews premium seat utilization and provides recommendations.
-   Ability to provide Feedback for the summary
-   Ability to refresh the summary
-   Ability to Copy summary

 Code Fix AI agent

 -   Eliminates technical debt backlog by deploying an embedded AI agent within the script editor that identifies issues in real-time and generates intelligent code fixes through Now Assist integration.\_
-   Removes specialized expertise barriers by enabling developers to interact conversationally with the AI agent for code modifications and apply or reject suggested fixes with feedback mechanisms.\_
-   Maintains development velocity by allowing immediate technical debt resolution within existing workflows without context switching or requiring specialized knowledge.

</td></tr><tr><td>

Now Assist for IRM

</td><td>

21.1.6

</td><td>

\[New\]

 Issue submission agent:

 The Issue Submission agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.

 Check product documentation for activation details.

 Suggest potential risks agentic workflow

 -   AI-driven risk identification Conversational AI automatically analyzes entity context and surfaces relevant risks from internal libraries, industry patterns, and optional external sources.
-   Consolidated risk view Generates a single, ready-to-triage risk list, reducing manual effort and duplication while ensuring comprehensive coverage.
-   Guided user experience Embedded in the Now Assist Panel, the workflow provides step-by-step guidance for risk domain selection, simplifying complex risk discovery.
-   Proactive intelligence for emerging risks External scanning capabilities deliver early warnings of new threats, helping organizations stay ahead of evolving regulations and trends.

 Control objective impact analyzer:

 The citation-driven impacted control objective identifier uses generative AI to analyze changes in citations and identify control objectives that should be reviewed based on the modified citation content. It intelligently matches changed citation requirements with existing COs to suggest potential updates, helping teams maintain alignment between citations and control objectives.

 Control objective change agent:

 This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates. Users can review and approve AI-suggested changes directly within the workflow, ensuring that control objectives always reflect the most current regulatory requirements and best practices.

 \[Changed\]

 -   Removed the issue summarization step from the issue resolution agentic workflow as part of performance improvements.
-   Added support for LTS models for previously released Now Assist IRM skills.
-   Enhanced security by implementing role masking.
-   Rationalization process now auto-generates recommendations using the skill when the Rationalize button is clicked on a control objective.
-   Added a quick summary view for each recommendation card and clarified task sequence during the analyze step of the rationalization process.
-   Control objective requirements and control requirements are now considered in the rationalization process for control objectives.

 \[Fixed\]

 -   Implemented a fix to skip redundant approvals in the rationalization process.
-   Resolved issues related to synchronizing impacted items and automatic refreshes.

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

Now Assist for OT Manager

</td><td>

3.1.0

</td><td>

New: Certified for Zurich

</td></tr><tr><td>

Now Assist for Platform

</td><td>

10.0.3

</td><td>

Changed: Updated release dependencies

</td></tr><tr><td>

Now Assist for Platform for Requestor

</td><td>

2.0.6

</td><td>

-   Changed: Updated app dependencies
-   Fixed: App title is Now Assist for Platform for Requestor

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

21.1.4

</td><td>

New: Now Assist for Privacy Management leverages Gen AI to streamline privacy workflows by summarizing risk assessments, condensing issue details, and identifying and merging redundant control objectives into a common control objective.

</td></tr><tr><td>

Now Assist for Process Mining

</td><td>

2.6.2

</td><td>

Additional support for various third party models.

</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

1.2.4

</td><td>

Now LLM LTS Support

 Java 21 Compliant

 Security Directive Compliance

</td></tr><tr><td>

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for RSM

</td><td>

1.2.0

</td><td>

Now Assist for Retail Service Management \(RSM\) highlights for the Zurich release The Store Inquiry AI agent enables retail HQ teams by:

-   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications

</td><td>

1.0.1

</td><td>

Changed

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

8.0.0

</td><td>

New: Quote-to-request automation: Employees no longer need to manually copy information from vendor quotes into procurement request forms.They can now upload a quote file, and the system automatically extracts key details, such as supplier information, item descriptions, quantities, and pricing, to pre-fill the appropriate request form for quick review and submission.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

8.0.0

</td><td>

Enhanced

 -   Project Insights Generation- Automatically track critical project signals such as delayed milestones, resource constraints, and task slippages and receive proactive insights either on a scheduled cadence or on-demand
-   Agile story generation - Convert epics into high-quality, actionable user stories faster and more intelligently through an improved, agentic, context-aware flow
-   New
    -   Acceptance criteria generation - Produce clear, consistent, and context-aware acceptance criteria using predefined templates and story-specific information
    -   Target generation - Generate measurable targets from goals information and optional context and automatically populate key fields in the target creation form
    -   Identify similar demands - Identify existing or related demand records during creation or editing to avoid duplication and ensure better demand hygiene

</td></tr><tr><td>

Now Assist for Talent

</td><td>

1.5.1

</td><td>

Implemented several directive changes.

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

5.1.7

</td><td>

The following is the list of features that we are shipping in the December Z Release:-

 Risk signal and Issue record summarisation: The Risk Signal and Issues Summary skill provides you with a summary of the risk signal and issues record, along with associated risk occurrences and solutions. This skill is available in the CSM/FSM Configurable Workspace and in Core UI.

</td></tr><tr><td>

Now Assist for Third-Party Risk Management

</td><td>

21.1.5

</td><td>

New: TPRM Issue summarization skill to enable third-party risk managers and assessors to review and edit AI summaries.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.5

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New -   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

2.0.5

</td><td>

-   New
    -   Configurable AI powered obligation extraction to automatically extract key contractual obligations from contract documents for user to review and approve.
    -   Now Assist powered conversational search to query contract documents using natural language and dialogue driven queries
-   Fixed: The Question Group card component now appears correctly when creating or editing Contract analysis use cases in the Now Assist Admin console.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Knowledge Management

</td><td>

29.4.11

</td><td>

1. Knowledge Gaps

 2. Article optimization

 3. Create/update article using custom instructions

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New -   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

2.3.2

</td><td>

Defect fixes

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

8.0.13

</td><td>

-   Changed
    -   Skill Search &amp; AIS Logging: Add backend support for metadata logging during skill search and execution.
    -   Remove OneExtend for LLAMA/GPT-4o: Eliminate follow-up logic for these models to simplify execution.
    -   Refactor Data Collector: Modularize into JavaScript files using Fluent for better structure and localization.
    -   Entity Extraction API \(Level 1\): Plan initial API for automated skill evaluation.
    -   Synthesized Response in Text Input: Enable text input to accept synthesized responses.
    -   Agentic Slot Fill Discovery: Use agentic slot fills when available to improve accuracy.
    -   Skippable Input Collector: Support skippable inputs and hide skip button dynamically.
-   Fixed: Fixed the defects to improve performance, slot-filling issues, catalog flows, dynamic translation, VA Designer test panel crashes, and other defects.

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Recommendation template

</td><td>

21.1.3

</td><td>

-   Changed
    -   Updated the quick summary view for each recommendation card.
    -   Clarified the sequence of tasks during the Analyze step of the Rationalization process.
-   Fixed
    -   Redundant approvals during the Rationalization process.
    -   Synchronization of impacted items and automatic refreshes.

</td></tr><tr><td>

RSM AI agent collection

</td><td>

1.2.0

</td><td>

The Store Inquiry AI agent enables retail HQ teams by:

 -   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

3.0.1

</td><td>

-   New
    -   Fill Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto fills the relevant fields in the form.
    -   Two new fields added in Lens actions to handle post processing timeout for previewing data in the standalone mode.
    -   Trigger ServiceNow AI Lens from Now Mobile application to extract data from artifacts and auto-fill forms on your mobile device.
-   Changed: The user interface of the scanner window is changed. When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.

</td></tr><tr><td>

Summarization for Order Management

</td><td>

1.0.2

</td><td>

New: Order Summarization for Order Management provides agents and managers with a consolidated, role-aware, and stage-specific view of all key order information across the order lifecycle. Built on Now Assist record summarization capabilities, this feature eliminates the need to navigate multiple pages or manually piece together order details, task progress, and risks. Integrated directly into the Order Management workspace starting in Q4, Order Summarization empowers agents to understand an orders status, history, risks, and progress at a glancemaking it easier to take action, hand off work, or pick up in-progress orders without searching across multiple records or tabs.

</td></tr><tr><td>

Telecommunications Media and Technology AI agent collection

</td><td>

4.0.4

</td><td>

Changed

</td></tr><tr><td>

Test Generation

</td><td>

4.0.11

</td><td>

Changed -   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|2.1.4|2026-01-20|
|Agentic Desktop|1.0.0|2025-12-11|
|AI Agents for ACC|1.0.0|2025-12-11|
|AI Agents for AIOps|1.7.2|2026-02-05|
|AI Agents for Customer Success Management|2.6.3|2025-12-11|
|AI Agents for Discovery|1.0.2|2025-12-11|
|AI Agents for Employee Experience|2.0.3|2025-12-11|
|AI Agents for Health and Safety|1.2.0|2026-01-20|
|AI Agents for ITAM|3.0.1|2025-12-11|
|AI agents for Observability|4.0.4|2026-01-20|
|AI Agents for Service Exchange Provider|1.0.5|2026-02-05|
|AI Agents for Workplace Service Delivery|3.0.3|2025-12-11|
|AI Control Tower for Now Assist|2.0.1|2025-12-11|
|AI Data Explorer|1.22.5|2025-12-16|
|AIOps LEAP|3.0.0|2026-01-20|
|Alert Assist|3.7.2|2026-02-05|
|Amazon Bedrock Spoke|1.3.2|2025-12-11|
|Analytics Generation|4.0.3|2025-12-11|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Catalog Conversational Coverage|5.2.5|2025-12-11|
|Chat Recommendation|1.5.4|2025-12-11|
|Chat Summarization for Virtual Agent|1.8.15|2025-12-11|
|Conversation Evaluator|2.0.5|2026-01-20|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|2.0.2|2025-12-11|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|6.0.6|2025-12-11|
|Conversational subflows and actions|28.2.7|2026-01-06|
|Custom App Record Summarization|28.2.11|2025-12-11|
|Customer Service Management AI agent collection|4.0.0|2025-12-11|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|0.1.8|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.3.1|2025-12-11|
|Field Service Management AI agent collection|1.0.3|2025-12-11|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|28.2.3|2025-12-11|
|Flow Generation|28.2.5|2025-12-11|
|Flow Summarization|28.2.4|2025-12-11|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|12.0.16|2026-01-23|
|Google Gemini Spoke|1.5.3|2025-12-11|
|GRC Common GenAI|21.1.8|2025-12-11|
|GRC Shared GenAI|21.1.8|2025-12-11|
|Group-Action Framework|5.0.5|2026-05-05|
|HR Service Delivery AI agent collection|5.0.9|2025-12-11|
|HR Talent AI Agent Collection|3.0.0|2025-12-11|
|HR Voice AI Agents|2.0.5|2025-12-11|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|1.0.5|2026-05-05|
|IRM Compliance GenAI|21.1.6|2025-12-11|
|IRM Risk GenAI|21.1.6|2025-12-11|
|IT Service Management AI agent collection|5.1.2|2026-01-20|
|IT Service Management AI voice agent collection|1.1.4|2025-12-11|
|ITOM AI Agents For Service Mapping|1.2.5|2025-12-11|
|Knowledge Center|31.0.8|2025-12-11|
|Knowledge Graph|6.1.0|2026-01-20|
|List AI Experience|1.1.14|2026-01-20|
|Manage Order Operations|1.0.2|2025-12-11|
|Manufacturing Commercial Operations AI agents collection|1.0.1|2025-12-11|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.8.1|2025-12-11|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.7|2025-12-11|
|Model Context Protocol Client|1.2.4|2025-12-11|
|Model Context Protocol Server|1.1.3|2026-01-22|
|Notifications Email Agents|1.0.7|2025-12-11|
|Now Assist Admin Console|7.0.19|2026-02-05|
|Now Assist Agents for requestor|3.0.9|2026-01-20|
|Now Assist AI Agents|6.1.12|2026-03-19|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|3.2.0|2026-01-20|
|Now Assist context menu|3.1.1|2026-01-22|
|Now Assist Data Kit|6.0.8|2026-01-20|
|Now Assist for Accounts Payable Operations \(APO\)|6.0.2|2026-03-12|
|Now Assist for App Engine|28.2.7|2025-12-11|
|Now Assist for code generation|28.5.13|2026-03-12|
|Now Assist for Collaborative Work Management \(CWM\)|4.0.1|2025-12-11|
|Now Assist for Complaint Case \(CSM\)|1.0.3|2026-02-05|
|Now Assist for Configuration Management Database \(CMDB\)|2.5.3|2026-01-20|
|Now Assist for Creator|28.6.1|2026-02-05|
|Now Assist for Customer Service Management \(CSM\)|11.1.0|2026-01-20|
|Now Assist for Digital End-user Experience \(DEX\)|4.1.2|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|3.0.10|2025-12-11|
|Now Assist for Enterprise Architecture \(EA\)|7.0.3|2026-01-20|
|Now Assist for Environmental, Social, and Governance \(ESG\)|21.1.6|2025-12-11|
|Now Assist for Field Service Management \(FSM\)|8.0.5|2025-12-11|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|5.0.0|2025-12-11|
|Now Assist for Hardware Asset Management|3.0.1|2025-12-11|
|Now Assist for Health and Safety|1.2.0|2026-01-20|
|Now Assist for HR Service Delivery \(HRSD\)|12.0.7|2025-12-11|
|Now Assist for Impact|2.0.18|2025-12-11|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|21.1.6|2025-12-11|
|Now Assist for IT Operations Management \(ITOM\)|2.5.1|2026-02-05|
|Now Assist for IT Service Management \(ITSM\)|12.1.1|2026-01-20|
|Now Assist for Legal Service Delivery|1.5.6|2026-01-20|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|1.0.1|2025-12-11|
|Now Assist for Order Management|1.0.1|2026-01-20|
|Now Assist for OT Manager|3.1.0|2025-12-11|
|Now Assist for Platform|10.0.3|2025-12-11|
|Now Assist for Platform for Requestor|2.0.6|2025-12-11|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|21.1.4|2025-12-11|
|Now Assist for Process Mining|2.6.2|2025-12-11|
|Now Assist for Prompt Assistance|2.0.7|2026-01-20|
|Now Assist for Public Sector Digital Services \(PSDS\)|1.2.4|2025-12-11|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.2.0|2025-12-11|
|Now Assist for Sales and Order Management \(SOM\)|1.0.6|2026-01-20|
|Now Assist for Sales and Order Management for Telecommunications|1.0.1|2025-12-11|
|Now Assist for Security Incident Response \(SIR\)|4.2.1|2026-01-20|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.0.5|2026-02-05|
|Now Assist for Software Asset Management \(SAM\)|5.2.5|2026-02-19|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|8.0.0|2025-12-11|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|8.0.0|2025-12-11|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|6.0.2|2025-12-24|
|Now Assist for Talent|1.5.1|2025-12-11|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|5.1.7|2025-12-11|
|Now Assist for Third-Party Risk Management|21.1.5|2025-12-11|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|2.1.6|2026-01-20|
|Now Assist for Vulnerability Response|4.0.0|2026-01-20|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.5|2025-12-11|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|15.1.0|2026-01-20|
|Now Assist in Catalog Builder|6.0.7|2026-01-20|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.0.5|2025-12-11|
|Now Assist in Conversational Catalog Request|5.2.23|2026-01-20|
|Now Assist in Document Intelligence|5.0.10|2026-04-02|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|29.4.11|2025-12-11|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|14.0.1|2026-01-20|
|Now Assist in Virtual Agent Configurations|8.0.8|2026-02-05|
|Now Assist Platform Skills|2.3.2|2025-12-11|
|Now Assist Skill Discovery and Execution|8.0.13|2025-12-11|
|Now Assist Skill Kit|7.0.14|2026-03-03|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Platform AI Agents and Skills|11.5.6|2026-02-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|4.0.6|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|21.1.3|2025-12-11|
|RSM AI agent collection|1.2.0|2025-12-11|
|Sales Development AI Agents|1.0.7|2025-12-11|
|ServiceNow AI Lens|3.0.1|2025-12-11|
|Summarization for Order Management|1.0.2|2025-12-11|
|Telecommunications Media and Technology AI agent collection|4.0.4|2025-12-11|
|Test Generation|4.0.11|2025-12-11|
|UI Generation|28.2.14|2026-01-23|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|

## Suite version 28.6.20260611 - Zurich Patch 6

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Agentic Desktop

</td><td>

1.0.0

</td><td>

New-   Design desktop actions of type UI block by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block that include pre-built connectors to interact with various applications and system components.
-   Add the desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy and desktop applications without APIs.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session. Interact with the automation when human input is required.
-   Changed
-   Fixed
-   Removed

</td></tr><tr><td>

AI Agents for ACC

</td><td>

1.0.0

</td><td>

Initial release of "Agent Client Collector \(ACC\) Diagnostic" agentic workflow

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.6.3

</td><td>

CHANGED: Success analysis AI agent has been removed, and we have introduced a new skill for trend analysis. The skill name is Analyze metric data trend.NEW: Agentic workflows

Workflow: Trigger risk mitigation touchpoint workflow

-   1.Meeting Draft Creator AI Agent - \_\_Automates meeting draft creation using context and history, ensuring completeness and reducing manual effort
-   2.Draft Meeting Scheduler AI Agent - Automates virtual meeting scheduling by collecting invitee and provider details from the user.

Workflow: Support renewal and expansion

-   a. Renewal analysis AI Agent\_
-   b. Success insight AI Agent
-   c. Value realization assessor AI Agent

</td></tr><tr><td>

AI Agents for Discovery

</td><td>

1.0.2

</td><td>

New - Introducing Certificate Renewal Agent Workflow to help you renew the certificates that are nearing expiry with the help of an agent. The system tracks discovered certificates, monitors their expiry dates, creates renewal tasks for the certificates and proactively notifies PKI admin via email.Through the NowAssist panel in the Certificate Management workspace, administrators can engage with the agentic workflow with the usage of natural language conversation.

-   This intelligent agent allows the PKI admin to check for certificates nearing expiry with just a simple prompt and can initiate their renewal with minimal interaction.
-   By delegating these tasks to the agent, administrators can significantly reduce manual effort and time spent on renewals.
-   This real-time capability helps prevent certificate outages, streamlines certificate management, and ensures organizations can adapt to shorter renewal cycles.
-   Also in this process it auto-generates CSR and stores the private key in community edition of Hashi-Corp vault \(The auto generation of CSR is supported fromYP8 onwards\)

 Changed N/A \(Initial Release\) Fixed N/A \(Initial Release\) Removed N/A \(Initial Release\)

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2.0.3

</td><td>

Updated to support the latest version of the dependent app.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

3.0.1

</td><td>

With the Now Assist for Hardware Asset Management \(HAM\) application, Hardware Asset Managers can streamline and automate the process of sourcing hardware assets by using AI agents included in the agentic workflow. The Now Assist for Hardware Asset Management \(HAM\) application contains agentic workflows to automate the sourcing, transfer, and procurement of assets upon request.

 -   Role masking in AI Agent Studio to execute agentic workflows, AI agents, and tools.
-   New security configuration pages in AI Agent Studio.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Store episodic memory of agentic conversations with agent learning.
-   Create and update UI actions for workflows.
-   Framework extensibility with new condition builder.
-   Add Desktop action as a tool to an AI agent.
-   Support for multilingual conversations.
-   MCP Client enhancements

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.0.3

</td><td>

-   New:
    -   Workplace Insights for key indicators like floor utilization, attendance, reservation no-shows, and space inefficiencies are generated and surfaced on the landing dashboard in Workplace Central.
    -   Introduced a new Workplace Insights AI Skill that analyzes the data and generates the insights. Workplace Reservation QnA Agent: Workplace Managers can ask natural language questions related to reservations from the Now Assist Panel and receive responses.
-   Changed: NA
-   Fixed:
    -   Sometimes, the reservation details could not be extracted from the case number when using the "Help manage workplace reservations" workflow
    -   Security fixes
-   Removed: NA

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

2.0.1

</td><td>

No new changes

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.3.2

</td><td>

Fixed: removed json.stringify for request

</td></tr><tr><td>

Analytics Generation

</td><td>

4.0.3

</td><td>

-   Skill moved under Data and Analytics Workflow \(Analytics product\) in Now Assist Admin
-   Extended querying capabilities to support:
    -   Stacked group chart \(e.g. show tasks grouped by state and stacked by priority\)
    -   Top/bottom X questions \(e.g. show top 5 assignment groups that has most number of open incidents\)
-   Bug fix

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

ATF troubleshooting agent

</td><td>

1.0.3

</td><td>

See RCA and steps to fix your failed ATF test

 Changed: none

 Fixed: none

 Removed: none

</td></tr><tr><td>

Catalog Conversational Coverage

</td><td>

5.2.5

</td><td>

New

 Included tailored recommendations to help you improve your catalog items for the conversational channel, making it easier for you to identify areas that need enhancement.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.5.4

</td><td>

-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   CRR Completness Metric
-   performance improvement fix

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.8.15

</td><td>

-   Honor In-Product roles in Sidebar Chat Summarization
-   Add new skill configuration for Standalone Sidebar Discussions
-   Support selection of portal in multiple skill configs in Agent Chat Summarization
-   NowLLM - Apriel Model changes
-   Add NowLLM LTS as an Additional Provider to Support LTS
-   Defect fixes

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

Conversation Insights

</td><td>

2.0.2

</td><td>

New: Inferred CSAT segmented by Intent Displayed in AI Agent Analytics dashboard. Display top intents for the selected agentic workflows and/or AI agents. Display average CSAT for intents of selected AI assets.

</td></tr><tr><td>

Conversational Studio

</td><td>

6.0.6

</td><td>

-   New
    -   "Assistant" module that includes the end-to-end admin configuration for Assistants
    -   Ability to change the visibility of individual Assets per Assistant
    -   Conversational settings modal within individual Assets
    -   Ability to bulk remove Assets from Assistants
    -   Ability to create new Assets \(including AI Agents, Subflows/Actions, Custom Skills, Topic\) from the Assistant Designer
    -   Voice Assistants
-   Changed: Test panel UX update, more data available
-   Fixed
    -   Changing asset to inactive should not clear the visibility and discoverability configs
    -   Topic migration
    -   Misc. defects
-   Removed

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

28.2.11

</td><td>

N/A. Initial release.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

4.0.0

</td><td>

NewCustomer 360 is an AI-powered assistant for the human agent that answers natural language questions about customers, cases, products, and interactions. This feature helps agents quickly access critical information and resolve cases.

 Changed

 Role configuration is required for Agentic workflows and AI agents.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

0.1.8

</td><td>

New application

</td></tr><tr><td>

Document Intelligence for Contract Management Content Pack

</td><td>

1.3.1

</td><td>

New: Added a predefined use case for the Obligation Extraction skill that includes definitions for extracting two distinct categories of obligations from contracts.

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

1.0.3

</td><td>

Create work order from text in NAP and NAVA.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Flow Designer GenAI

</td><td>

28.2.3

</td><td>

New:

 Users will have an option to call an agent from workflow

</td></tr><tr><td>

Flow Generation

</td><td>

28.2.5

</td><td>

New: Support the Now LLM Long Term Stable models \(LTS\).

</td></tr><tr><td>

Flow Summarization

</td><td>

28.2.4

</td><td>

New: Support for the Now LLM Long Term Stable models \(LTS\).

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

Google Gemini Spoke

</td><td>

1.5.3

</td><td>

Fixed: removed json.stringify for request

</td></tr><tr><td>

GRC Common GenAI

</td><td>

21.1.8

</td><td>

New:

 Issue Submission Agent:

 The issue submission AI agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.

 Changed:

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

21.1.8

</td><td>

New -   Control objective impact analyzer: This Gen AI skill analyzes changes in citations and identifies control objectives that should be reviewed based on the modified citation content.
-   Control objective detail updater: For a given control objective, validate whether the description and supplemental guidance needs to be updated based on associated citations, and suggest new content when updates are required. This skill is triggered only by the AI agent, Control objective change agent.
-   Control objective change agent: This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates.
-   Enabled Now LLM LTS and Role masking support for the recommendation of similar control objectives and common control objective creation skills.
-   Control objective requirements and control requirements are now considered in the Rationalization process for control objectives.

Changed: Rationalization process now automatically generates recommendations using the skill when you select Rationalize button in the Control objective page.

</td></tr><tr><td>

HR Service Delivery AI agent collection

</td><td>

5.0.9

</td><td>

New -   Help resolve tuition reimbursement requests agentic workflow supports the post-completion reimbursement process. It automatically evaluates employee-submitted grades, transcripts, and documentation against company policies and returns a decision of approval, denial, or request for additional information
-   Generate onboarding ramp-up plan workflow - Performance improvements for faster creation and manager review
-   Resolve Non Critical HR Cases - Predicts the criticality of the HR case and sends the response to the employee if the HR case is non critical.
-   Predict Service and Transfer HR cases - Predict the correct HR Service of the HR Case.
-   Resolve Critical HR Cases - Provides the ability for the HR Agents to generate a step by step plan

Enhanced

-   Help resolve tuition requests agentic workflow - Performance improvements for faster policy evaluation and case resolution
-   Security - Implemented role masking to strengthen AI agent security and protect sensitive employee information

</td></tr><tr><td>

HR Talent AI Agent Collection

</td><td>

3.0.0

</td><td>

Whats New The Employee feedback collection AI Agent streamlines the process of gathering employee feedback, ensuring managers receive timely, structured, and actionable input. Persona: ManagerThe agent:

 -   Suggests relevant collaborators of the employee using data from Employee Profile, Talent Development apps, and optional Microsoft Graph interaction insights \(using the Microsoft Exchange Online spoke\)
-   Sends requests as EC To-Dos for the feedback providers and sends automated reminders
-   Consolidates all feedback responses into a single view for easier evaluation

 Updates

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

21.1.6

</td><td>

New -   Use AI-generated recommendations to identify which policies are impacted by a regulatory alert
-   Use the Get Regulatory Insights agentic workflow to enrich regulatory alerts with external context, classification, summarization, and recommended potentially impacted items
-   Use the Generate Regulatory Action Plan agentic workflow to convert regulatory insights into actionable compliance strategies, including structured tasks with clear ownership and timelines

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

21.1.6

</td><td>

\[New\]

 Now LLM LTS and Role masking support are now enabled for risk event summarization

</td></tr><tr><td>

IT Service Management AI voice agent collection

</td><td>

1.1.4

</td><td>

Now Assist for ITSM release notes \[Zurich\]

 -   New: Initial release for ITSM Voice AI agent. See the Key features section for more details.
-   Changed: n/a
-   Fixed: n/a
-   Removed: n/a

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.2.5

</td><td>

Changed: Added compatibility with the "Now Assist for Platform" app, version 10.0.3

</td></tr><tr><td>

Knowledge Center

</td><td>

31.0.8

</td><td>

The Knowledge Center centralized hub for Knowledge Admin and Manager:

 1. Is an entry point for KM Management personas to manage all capabilities and configurations 2. Guides users on the next-best actions to take by displaying actionable key insights 3. Is a suite of KM Tools for suggesting content creation, updates, duplicates, and article retirement

</td></tr><tr><td>

Manage Order Operations

</td><td>

1.0.2

</td><td>

Initial Release:

 -   Automate the process of creating order cases on the Business Portal.
-   Retrieve customer inputs in text or voice format, classify intent, and route them to the Virtual Agent for action.
-   Identify the earliest possible delivery date for expedited product delivery on a specific customer order.
-   Create an order case autonomously based on the inputs on the Now Assist panel.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.8.1

</td><td>

New: Support responses actions for CUA.

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.4.7

</td><td>

New -   Long-Term Support \(LTS\) model that delivers regulatory alignment, predictable behavior, and lifecycle stability is now supported.
-   Added role based access control to the generation skill of mobile card.This access control only allows specific roles of delegated\_developer and sn\_mab\_api.admin to generate the mobile card.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

1.2.4

</td><td>

-   PRM\(Protected Resource Metadata\) support for MCP servers
-   reduced latency for few MCP servers

</td></tr><tr><td>

Notifications Email Agents

</td><td>

1.0.7

</td><td>

New: The email agentic workflow introduces enhanced capabilities to intelligently process incoming emails by:

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

28.2.7

</td><td>

New: Use the custom app record summarization skill to generate AI summaries for tables in custom applications. You can generate summaries in-product and through chat in the Now Assist panel.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

4.0.1

</td><td>

-   New: Agile team members can now use Now Assist to generate acceptance criteria for a story based on the short description and description
-   Changed
-   Fixed: Performance improvement of Now Assist skills in CWM

 Deprecated/Removed

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Employee Experience

</td><td>

3.0.10

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Now Assist for Environmental, Social, and Governance \(ESG\)

</td><td>

21.1.6

</td><td>

New: Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions.The carbon calculations agentic workflow acts as a copilot for sustainability teams, streamlining carbon accounting workflows. It intelligently selects metric definitions and emission factors from the library, generates calculated metric definitions, and allows users to review and make adjustments before final use.

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

8.0.5

</td><td>

-   Added new feature to create work order from text in NAP and NAVA.
-   Included Smart Assessment / Questionnaire summary in work order task summarization.

</td></tr><tr><td>

Now Assist for FSC Common

</td><td>

5.0.0

</td><td>

New: Changed: Prompt migration to NASK: Summarization skill prompts have been migrated into the Now Assist Skill Kit \(NASK\), enabling admins to configure, modify, and maintain summarization skills using the new OOB editable experience. This update preserves full administrative control while aligning skills to the modern, centralized prompt management framework.

</td></tr><tr><td>

Now Assist for Hardware Asset Management

</td><td>

3.0.1

</td><td>

In this release, users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

 -   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent
-   Hardware asset repair process \(patch\)

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

12.0.7

</td><td>

New / enhancements- The case summarization skill is enabled for the attachment summaries

 - The resolution notes skill is enabled with NACM for the shortening/elaborating resolution notes summary

 - On the Agent Workspace application, the resolution notes skill is enabled to auto-populate Close notes field

 Changed:

 - Enhanced security features revisit the ACL roles and access;Support to GPT OSS model

</td></tr><tr><td>

Now Assist for Impact

</td><td>

2.0.18

</td><td>

Consumption Report summary

 -   Produces an insightful, human-readable summary which highlights key business objectives with active and completed initiatives and accelerators.
-   The summary flags any concerning trends in severity \(P1/P2 dominance\).
-   It also reviews premium seat utilization and provides recommendations.
-   Ability to provide Feedback for the summary
-   Ability to refresh the summary
-   Ability to Copy summary

 Code Fix AI agent

 -   Eliminates technical debt backlog by deploying an embedded AI agent within the script editor that identifies issues in real-time and generates intelligent code fixes through Now Assist integration.\_
-   Removes specialized expertise barriers by enabling developers to interact conversationally with the AI agent for code modifications and apply or reject suggested fixes with feedback mechanisms.\_
-   Maintains development velocity by allowing immediate technical debt resolution within existing workflows without context switching or requiring specialized knowledge.

</td></tr><tr><td>

Now Assist for IRM

</td><td>

21.1.6

</td><td>

\[New\]

 Issue submission agent:

 The Issue Submission agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.

 Check product documentation for activation details.

 Suggest potential risks agentic workflow

 -   AI-driven risk identification Conversational AI automatically analyzes entity context and surfaces relevant risks from internal libraries, industry patterns, and optional external sources.
-   Consolidated risk view Generates a single, ready-to-triage risk list, reducing manual effort and duplication while ensuring comprehensive coverage.
-   Guided user experience Embedded in the Now Assist Panel, the workflow provides step-by-step guidance for risk domain selection, simplifying complex risk discovery.
-   Proactive intelligence for emerging risks External scanning capabilities deliver early warnings of new threats, helping organizations stay ahead of evolving regulations and trends.

 Control objective impact analyzer:

 The citation-driven impacted control objective identifier uses generative AI to analyze changes in citations and identify control objectives that should be reviewed based on the modified citation content. It intelligently matches changed citation requirements with existing COs to suggest potential updates, helping teams maintain alignment between citations and control objectives.

 Control objective change agent:

 This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates. Users can review and approve AI-suggested changes directly within the workflow, ensuring that control objectives always reflect the most current regulatory requirements and best practices.

 \[Changed\]

 -   Removed the issue summarization step from the issue resolution agentic workflow as part of performance improvements.
-   Added support for LTS models for previously released Now Assist IRM skills.
-   Enhanced security by implementing role masking.
-   Rationalization process now auto-generates recommendations using the skill when the Rationalize button is clicked on a control objective.
-   Added a quick summary view for each recommendation card and clarified task sequence during the analyze step of the rationalization process.
-   Control objective requirements and control requirements are now considered in the rationalization process for control objectives.

 \[Fixed\]

 -   Implemented a fix to skip redundant approvals in the rationalization process.
-   Resolved issues related to synchronizing impacted items and automatic refreshes.

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

1.0.1

</td><td>

New: Create recall corrective actions AI agent

</td></tr><tr><td>

Now Assist for OT Manager

</td><td>

3.1.0

</td><td>

New: Certified for Zurich

</td></tr><tr><td>

Now Assist for Platform

</td><td>

10.0.3

</td><td>

Changed: Updated release dependencies

</td></tr><tr><td>

Now Assist for Platform for Requestor

</td><td>

2.0.6

</td><td>

-   Changed: Updated app dependencies
-   Fixed: App title is Now Assist for Platform for Requestor

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

21.1.4

</td><td>

New: Now Assist for Privacy Management leverages Gen AI to streamline privacy workflows by summarizing risk assessments, condensing issue details, and identifying and merging redundant control objectives into a common control objective.

</td></tr><tr><td>

Now Assist for Process Mining

</td><td>

2.6.2

</td><td>

Additional support for various third party models.

</td></tr><tr><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

1.2.4

</td><td>

Now LLM LTS Support

 Java 21 Compliant

 Security Directive Compliance

</td></tr><tr><td>

Now Assist for RPA Hub

</td><td>

5.0.2

</td><td>

New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

</td></tr><tr><td>

Now Assist for RSM

</td><td>

1.2.0

</td><td>

Now Assist for Retail Service Management \(RSM\) highlights for the Zurich release The Store Inquiry AI agent enables retail HQ teams by:

-   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications

</td><td>

1.0.1

</td><td>

Changed

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

8.0.0

</td><td>

New: Quote-to-request automation: Employees no longer need to manually copy information from vendor quotes into procurement request forms.They can now upload a quote file, and the system automatically extracts key details, such as supplier information, item descriptions, quantities, and pricing, to pre-fill the appropriate request form for quick review and submission.

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

8.0.0

</td><td>

Enhanced

 -   Project Insights Generation- Automatically track critical project signals such as delayed milestones, resource constraints, and task slippages and receive proactive insights either on a scheduled cadence or on-demand
-   Agile story generation - Convert epics into high-quality, actionable user stories faster and more intelligently through an improved, agentic, context-aware flow
-   New
    -   Acceptance criteria generation - Produce clear, consistent, and context-aware acceptance criteria using predefined templates and story-specific information
    -   Target generation - Generate measurable targets from goals information and optional context and automatically populate key fields in the target creation form
    -   Identify similar demands - Identify existing or related demand records during creation or editing to avoid duplication and ensure better demand hygiene

</td></tr><tr><td>

Now Assist for Talent

</td><td>

1.5.1

</td><td>

Implemented several directive changes.

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

5.1.7

</td><td>

The following is the list of features that we are shipping in the December Z Release:-

 Risk signal and Issue record summarisation: The Risk Signal and Issues Summary skill provides you with a summary of the risk signal and issues record, along with associated risk occurrences and solutions. This skill is available in the CSM/FSM Configurable Workspace and in Core UI.

</td></tr><tr><td>

Now Assist for Third-Party Risk Management

</td><td>

21.1.5

</td><td>

New: TPRM Issue summarization skill to enable third-party risk managers and assessors to review and edit AI summaries.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

1.1.5

</td><td>

The release notes of the related plugins can be viewed on the respective plugin's release notes.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New -   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

2.0.5

</td><td>

-   New
    -   Configurable AI powered obligation extraction to automatically extract key contractual obligations from contract documents for user to review and approve.
    -   Now Assist powered conversational search to query contract documents using natural language and dialogue driven queries
-   Fixed: The Question Group card component now appears correctly when creating or editing Contract analysis use cases in the Now Assist Admin console.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Knowledge Management

</td><td>

29.4.11

</td><td>

1. Knowledge Gaps

 2. Article optimization

 3. Create/update article using custom instructions

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New -   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Now Assist Platform Skills

</td><td>

2.3.2

</td><td>

Defect fixes

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Recommendation template

</td><td>

21.1.3

</td><td>

-   Changed
    -   Updated the quick summary view for each recommendation card.
    -   Clarified the sequence of tasks during the Analyze step of the Rationalization process.
-   Fixed
    -   Redundant approvals during the Rationalization process.
    -   Synchronization of impacted items and automatic refreshes.

</td></tr><tr><td>

RSM AI agent collection

</td><td>

1.2.0

</td><td>

The Store Inquiry AI agent enables retail HQ teams by:

 -   Searching intelligently across knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
-   Providing AI-generated resolution steps and prompting agents to accept, edit, or reject the suggestions to reduce manual effort and speed up decision-making.
-   Learning continuously from resolved queries to offer more accurate and relevant suggestions over time.

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

3.0.1

</td><td>

-   New
    -   Fill Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto fills the relevant fields in the form.
    -   Two new fields added in Lens actions to handle post processing timeout for previewing data in the standalone mode.
    -   Trigger ServiceNow AI Lens from Now Mobile application to extract data from artifacts and auto-fill forms on your mobile device.
-   Changed: The user interface of the scanner window is changed. When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.

</td></tr><tr><td>

Summarization for Order Management

</td><td>

1.0.2

</td><td>

New: Order Summarization for Order Management provides agents and managers with a consolidated, role-aware, and stage-specific view of all key order information across the order lifecycle. Built on Now Assist record summarization capabilities, this feature eliminates the need to navigate multiple pages or manually piece together order details, task progress, and risks. Integrated directly into the Order Management workspace starting in Q4, Order Summarization empowers agents to understand an orders status, history, risks, and progress at a glancemaking it easier to take action, hand off work, or pick up in-progress orders without searching across multiple records or tabs.

</td></tr><tr><td>

Telecommunications Media and Technology AI agent collection

</td><td>

4.0.4

</td><td>

Changed

</td></tr><tr><td>

Test Generation

</td><td>

4.0.11

</td><td>

Changed -   Security fixes
-   Users can now enter Japanese into Test Generation

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|2.1.4|2026-01-20|
|Agentic Desktop|1.0.0|2025-12-11|
|AI Agents for ACC|1.0.0|2025-12-11|
|AI Agents for AIOps|1.7.2|2026-02-05|
|AI Agents for Customer Success Management|2.6.3|2025-12-11|
|AI Agents for Discovery|1.0.2|2025-12-11|
|AI Agents for Employee Experience|2.0.3|2025-12-11|
|AI Agents for Health and Safety|1.2.0|2026-01-20|
|AI Agents for ITAM|3.0.1|2025-12-11|
|AI agents for Observability|4.0.4|2026-01-20|
|AI Agents for Service Exchange Provider|1.0.5|2026-02-05|
|AI Agents for Workplace Service Delivery|3.0.3|2025-12-11|
|AI Control Tower for Now Assist|2.0.1|2025-12-11|
|AI Data Explorer|1.22.5|2025-12-16|
|AIOps LEAP|3.0.0|2026-01-20|
|Alert Assist|3.7.2|2026-02-05|
|Amazon Bedrock Spoke|1.3.2|2025-12-11|
|Analytics Generation|4.0.3|2025-12-11|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Catalog Conversational Coverage|5.2.5|2025-12-11|
|Chat Recommendation|1.5.4|2025-12-11|
|Chat Summarization for Virtual Agent|1.8.15|2025-12-11|
|Conversation Evaluator|2.0.5|2026-01-20|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|2.0.2|2025-12-11|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|6.0.6|2025-12-11|
|Conversational subflows and actions|28.2.7|2026-01-06|
|Custom App Record Summarization|28.2.11|2025-12-11|
|Customer Service Management AI agent collection|4.0.0|2025-12-11|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|0.1.8|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.3.1|2025-12-11|
|Field Service Management AI agent collection|1.0.3|2025-12-11|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|28.2.3|2025-12-11|
|Flow Generation|28.2.5|2025-12-11|
|Flow Summarization|28.2.4|2025-12-11|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|12.1.2|2026-02-05|
|Google Gemini Spoke|1.5.3|2025-12-11|
|GRC Common GenAI|21.1.8|2025-12-11|
|GRC Shared GenAI|21.1.8|2025-12-11|
|Group-Action Framework|5.0.5|2026-05-05|
|HR Service Delivery AI agent collection|5.0.9|2025-12-11|
|HR Talent AI Agent Collection|3.0.0|2025-12-11|
|HR Voice AI Agents|2.1.4|2026-02-05|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|1.0.5|2026-05-05|
|IRM Compliance GenAI|21.1.6|2025-12-11|
|IRM Risk GenAI|21.1.6|2025-12-11|
|IT Service Management AI agent collection|5.1.2|2026-01-20|
|IT Service Management AI voice agent collection|1.1.4|2025-12-11|
|ITOM AI Agents For Service Mapping|1.2.5|2025-12-11|
|Knowledge Center|31.0.8|2025-12-11|
|Knowledge Graph|6.1.0|2026-01-20|
|List AI Experience|1.1.14|2026-01-20|
|Manage Order Operations|1.0.2|2025-12-11|
|Manufacturing Commercial Operations AI agents collection|1.0.1|2025-12-11|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.8.1|2025-12-11|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.7|2025-12-11|
|Model Context Protocol Client|1.2.4|2025-12-11|
|Model Context Protocol Server|1.1.3|2026-01-22|
|Notifications Email Agents|1.0.7|2025-12-11|
|Now Assist Admin Console|7.0.19|2026-02-05|
|Now Assist Agents for requestor|3.1.2|2026-02-05|
|Now Assist AI Agents|6.2.12|2026-03-19|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|3.2.0|2026-01-20|
|Now Assist context menu|3.1.1|2026-01-22|
|Now Assist Data Kit|6.0.8|2026-01-20|
|Now Assist for Accounts Payable Operations \(APO\)|6.0.2|2026-03-12|
|Now Assist for App Engine|28.2.7|2025-12-11|
|Now Assist for code generation|28.5.13|2026-03-12|
|Now Assist for Collaborative Work Management \(CWM\)|4.0.1|2025-12-11|
|Now Assist for Complaint Case \(CSM\)|1.0.3|2026-02-05|
|Now Assist for Configuration Management Database \(CMDB\)|2.5.3|2026-01-20|
|Now Assist for Creator|28.6.1|2026-02-05|
|Now Assist for Customer Service Management \(CSM\)|11.1.0|2026-01-20|
|Now Assist for Digital End-user Experience \(DEX\)|4.1.2|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|3.0.10|2025-12-11|
|Now Assist for Enterprise Architecture \(EA\)|7.0.3|2026-01-20|
|Now Assist for Environmental, Social, and Governance \(ESG\)|21.1.6|2025-12-11|
|Now Assist for Field Service Management \(FSM\)|8.0.5|2025-12-11|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|5.0.0|2025-12-11|
|Now Assist for Hardware Asset Management|3.0.1|2025-12-11|
|Now Assist for Health and Safety|1.2.0|2026-01-20|
|Now Assist for HR Service Delivery \(HRSD\)|12.0.7|2025-12-11|
|Now Assist for Impact|2.0.18|2025-12-11|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|21.1.6|2025-12-11|
|Now Assist for IT Operations Management \(ITOM\)|2.5.1|2026-02-05|
|Now Assist for IT Service Management \(ITSM\)|12.1.1|2026-01-20|
|Now Assist for Legal Service Delivery|1.5.6|2026-01-20|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|1.0.1|2025-12-11|
|Now Assist for Order Management|1.0.1|2026-01-20|
|Now Assist for OT Manager|3.1.0|2025-12-11|
|Now Assist for Platform|10.0.3|2025-12-11|
|Now Assist for Platform for Requestor|2.0.6|2025-12-11|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|21.1.4|2025-12-11|
|Now Assist for Process Mining|2.6.2|2025-12-11|
|Now Assist for Prompt Assistance|2.0.7|2026-01-20|
|Now Assist for Public Sector Digital Services \(PSDS\)|1.2.4|2025-12-11|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.2.0|2025-12-11|
|Now Assist for Sales and Order Management \(SOM\)|1.0.6|2026-01-20|
|Now Assist for Sales and Order Management for Telecommunications|1.0.1|2025-12-11|
|Now Assist for Security Incident Response \(SIR\)|4.2.1|2026-01-20|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.0.5|2026-02-05|
|Now Assist for Software Asset Management \(SAM\)|5.2.5|2026-02-19|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|8.0.0|2025-12-11|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|8.0.0|2025-12-11|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|6.0.2|2025-12-24|
|Now Assist for Talent|1.5.1|2025-12-11|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|5.1.7|2025-12-11|
|Now Assist for Third-Party Risk Management|21.1.5|2025-12-11|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|3.0.2|2026-02-05|
|Now Assist for Vulnerability Response|4.0.0|2026-01-20|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.5|2025-12-11|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|15.3.0|2026-02-05|
|Now Assist in Catalog Builder|6.0.7|2026-01-20|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.0.5|2025-12-11|
|Now Assist in Conversational Catalog Request|5.2.23|2026-01-20|
|Now Assist in Document Intelligence|5.0.10|2026-04-02|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|29.4.11|2025-12-11|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|15.0.8|2026-02-20|
|Now Assist in Virtual Agent Configurations|8.0.8|2026-02-05|
|Now Assist Platform Skills|2.3.2|2025-12-11|
|Now Assist Skill Discovery and Execution|8.1.3|2026-02-20|
|Now Assist Skill Kit|7.0.14|2026-03-03|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Platform AI Agents and Skills|11.5.6|2026-02-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|4.0.6|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|21.1.3|2025-12-11|
|RSM AI agent collection|1.2.0|2025-12-11|
|Sales Development AI Agents|1.0.7|2025-12-11|
|ServiceNow AI Lens|3.0.1|2025-12-11|
|Summarization for Order Management|1.0.2|2025-12-11|
|Telecommunications Media and Technology AI agent collection|4.0.4|2025-12-11|
|Test Generation|4.0.11|2025-12-11|
|UI Generation|28.2.14|2026-01-23|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|

## Suite version 28.7.20260611 - Zurich Patch 7

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Agents for ACC

</td><td>

1.0.0

</td><td>

Initial release of "Agent Client Collector \(ACC\) Diagnostic" agentic workflow

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

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

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

28.2.11

</td><td>

N/A. Initial release.

</td></tr><tr><td>

DocIntel Vision AI Agent

</td><td>

0.1.8

</td><td>

New application

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

Manage Order Operations

</td><td>

1.0.2

</td><td>

Initial Release:

 -   Automate the process of creating order cases on the Business Portal.
-   Retrieve customer inputs in text or voice format, classify intent, and route them to the Virtual Agent for action.
-   Identify the earliest possible delivery date for expedited product delivery on a specific customer order.
-   Create an order case autonomously based on the inputs on the Now Assist panel.

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.4.7

</td><td>

New -   Long-Term Support \(LTS\) model that delivers regulatory alignment, predictable behavior, and lifecycle stability is now supported.
-   Added role based access control to the generation skill of mobile card.This access control only allows specific roles of delegated\_developer and sn\_mab\_api.admin to generate the mobile card.

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

28.2.7

</td><td>

New: Use the custom app record summarization skill to generate AI summaries for tables in custom applications. You can generate summaries in-product and through chat in the Now Assist panel.

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New -   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New -   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.0.9|2026-03-12|
|Agentic Desktop|2.0.0|2026-03-12|
|AI Agents for ACC|1.0.0|2025-12-11|
|AI Agents for AIOps|1.8.2|2026-03-12|
|AI Agents for Customer Success Management|2.6.8|2026-03-12|
|AI Agents for Discovery|1.0.3|2026-03-12|
|AI Agents for Employee Experience|2.1.0|2026-03-12|
|AI Agents for Health and Safety|1.3.0|2026-03-12|
|AI Agents for ITAM|4.0.0|2026-03-12|
|AI agents for Observability|5.0.4|2026-03-12|
|AI Agents for Service Exchange Provider|1.0.9|2026-03-12|
|AI agents for SLO|1.0.5|2026-03-12|
|AI Agents for Workplace Service Delivery|3.1.0|2026-03-12|
|AI Control Tower for Now Assist|3.0.2|2026-03-12|
|AI Data Explorer|4.0.5|2026-03-12|
|AI Enhanced Recommended Actions|1.0.1|2026-03-12|
|AIOps LEAP|3.1.2|2026-03-12|
|Alert Assist|3.8.1|2026-03-12|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.0.4|2026-03-12|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Catalog Conversational Coverage|6.0.1|2026-03-12|
|Chat Recommendation|1.6.0|2026-03-12|
|Chat Summarization for Virtual Agent|1.10.3|2026-03-12|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.0.0|2026-03-12|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|7.0.3|2026-03-12|
|Conversational subflows and actions|29.1.1|2026-03-12|
|Custom App Record Summarization|28.2.11|2025-12-11|
|Customer Service Management AI agent collection|5.0.0|2026-03-12|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|0.1.8|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Field Service Management AI agent collection|2.0.2|2026-03-12|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|13.0.4|2026-04-02|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|6.0.5|2026-03-12|
|HR Service Delivery AI agent collection|5.1.3|2026-03-12|
|HR Talent AI Agent Collection|4.0.1|2026-03-12|
|HR Voice AI Agents|2.1.4|2026-02-05|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|2.0.2|2026-03-12|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management AI agent collection|6.0.8|2026-03-12|
|IT Service Management AI voice agent collection|1.1.6|2026-03-12|
|ITOM AI Agents For Service Mapping|1.2.6|2026-03-12|
|Knowledge Center|31.1.3|2026-03-12|
|Knowledge Graph|7.0.2|2026-03-12|
|List AI Experience|2.0.8|2026-03-12|
|Manage Invoice Operations|1.0.1|2026-03-12|
|Manage Order Operations|1.0.2|2025-12-11|
|Manufacturing Commercial Operations AI agents collection|2.0.2|2026-03-12|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.9.0|2026-03-12|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.7|2025-12-11|
|Model Context Protocol Client|2.1.0|2026-03-12|
|Model Context Protocol Server|1.2.2|2026-03-12|
|Notifications Email Agents|1.0.10|2026-03-12|
|Now Assist Admin Console|8.0.7|2026-03-12|
|Now Assist Agents for requestor|3.2.0|2026-03-12|
|Now Assist AI Agents|7.0.11|2026-05-08|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|4.0.2|2026-03-12|
|Now Assist context menu|3.2.10|2026-04-17|
|Now Assist Data Kit|7.0.7|2026-03-12|
|Now Assist for Accounts Payable Operations \(APO\)|7.0.0|2026-03-12|
|Now Assist for App Engine|28.2.7|2025-12-11|
|Now Assist for Automation Center|1.0.5|2026-03-12|
|Now Assist for code generation|28.5.13|2026-03-12|
|Now Assist for Collaborative Work Management \(CWM\)|5.0.1|2026-03-12|
|Now Assist for Complaint Case \(CSM\)|2.0.2|2026-03-12|
|Now Assist for Configuration Management Database \(CMDB\)|3.0.2|2026-03-12|
|Now Assist for CPQ|1.0.1|2026-03-12|
|Now Assist for Creator|28.7.1|2026-03-12|
|Now Assist for Customer Service Management \(CSM\)|12.0.0|2026-03-12|
|Now Assist for Digital End-user Experience \(DEX\)|4.1.2|2026-04-09|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.0.6|2026-03-12|
|Now Assist for Enterprise Architecture \(EA\)|7.1.0|2026-03-12|
|Now Assist for Field Service Management \(FSM\)|9.0.3|2026-03-12|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|6.0.1|2026-03-12|
|Now Assist for Hardware Asset Management|4.0.0|2026-03-12|
|Now Assist for Health and Safety|1.3.0|2026-03-12|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.0.4|2026-03-12|
|Now Assist for Impact|3.0.3|2026-03-12|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.6.0|2026-03-12|
|Now Assist for IT Service Management \(ITSM\)|12.2.7|2026-03-12|
|Now Assist for Legal Service Delivery|1.6.2|2026-03-12|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.0.1|2026-03-12|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.0.3|2026-03-12|
|Now Assist for OT Manager|3.3.0|2026-03-12|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|11.0.1|2026-03-12|
|Now Assist for Platform for Requestor|3.0.1|2026-03-12|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.5|2026-03-12|
|Now Assist for Prompt Assistance|3.0.2|2026-03-12|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.0.3|2026-03-12|
|Now Assist for Purchase Order Management \(POM\)|1.0.1|2026-03-12|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Sales and Order Management for Telecommunications|2.0.4|2026-03-12|
|Now Assist for Sales Force Automation \(SFA\)|1.1.0|2026-03-12|
|Now Assist for Security Incident Response \(SIR\)|4.3.1|2026-03-12|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.0.9|2026-03-12|
|Now Assist for Software Asset Management \(SAM\)|5.3.3|2026-03-12|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|9.0.0|2026-03-12|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.0.1|2026-03-12|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|7.0.0|2026-03-12|
|Now Assist for Talent|1.6.2|2026-03-12|
|Now Assist for Telecommunications|1.0.5|2026-03-12|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.2|2026-03-12|
|Now Assist for Third-Party Risk Management|22.0.8|2026-03-12|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|4.0.3|2026-03-12|
|Now Assist for Vulnerability Response|4.0.0|2026-01-20|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.8|2026-03-12|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|16.0.8|2026-03-12|
|Now Assist in Catalog Builder|7.0.1|2026-03-12|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.1.0|2026-03-12|
|Now Assist in Conversational Catalog Request|6.0.2|2026-03-12|
|Now Assist in Document Intelligence|6.0.5|2026-03-12|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|30.7.3|2026-03-12|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|16.0.5|2026-03-12|
|Now Assist in Virtual Agent Configurations|11.0.5|2026-03-12|
|Now Assist Platform Skills|2.4.3|2026-03-12|
|Now Assist Skill Discovery and Execution|9.0.2|2026-03-12|
|Now Assist Skill Kit|8.0.5|2026-03-12|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Platform AI Agents and Skills|12.0.12|2026-03-12|
|prompt-management|1.0.11|2026-03-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|5.0.0|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM AI agent collection|1.3.0|2026-03-12|
|Sales Development AI Agents|1.0.7|2025-12-11|
|ServiceNow AI Lens|4.0.0|2026-03-12|
|Summarization for Order Management|2.0.1|2026-03-12|
|Summarization for Quote Management|1.0.1|2026-03-12|
|Telecommunications Media and Technology AI agent collection|5.0.1|2026-03-12|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.0.4|2026-03-12|
|UI Generation|28.2.14|2026-01-23|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|

## Suite version 28.8.20260611 - Zurich Patch 8

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

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

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

7.2.0

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

</td></tr><tr><td>

Now Assist AI web agent

</td><td>

29.0.7

</td><td>

-   New
    -   Native elements support \(dropdown, calendar\)
    -   Take/Give-back control
-   Update: Minor bug fixes

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

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

13.2.0

</td><td>

Defect fixes and plugin upgrade issue fixed.

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist for Zero Copy Connector

</td><td>

1.0.9

</td><td>

-   Discover ERP database table information and identify relevant ERP Data Product models using the ERP Data Product Explorer agentic AI workflow.
-   Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.
-   Identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill.
-   Ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.2.5

</td><td>

New -   Introduced GenAI-powered slot-fill capability for catalog item forms
-   Enabled natural language to structured form conversion
-   Added intelligent field auto-population and suggestion engine

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.0.6

</td><td>

New -   Initial release of ticket summarization on the standard ticket page
-   Added AI-driven summary generation for opened tickets
-   Introduced automatic action item extraction for quick follow-up

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

1.0.7

</td><td>

Extended the support for Now LLM LTS model

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.1.3|2026-04-28|
|Agentic Desktop|2.0.0|2026-03-12|
|AI Agent Advisor|1.0.2|2026-06-04|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.8.2|2026-03-12|
|AI Agents for Customer Success Management|2.7.2|2026-04-09|
|AI Agents for Discovery|2.0.4|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.2.1|2026-04-09|
|AI Agents for Health and Safety|1.3.1|2026-04-09|
|AI Agents for ITAM|4.1.0|2026-04-09|
|AI agents for Observability|5.0.4|2026-03-12|
|AI Agents for Service Exchange Provider|1.0.12|2026-04-09|
|AI agents for SLO|1.0.5|2026-03-12|
|AI Agents for Workplace Service Delivery|3.2.0|2026-04-09|
|AI Control Tower for Now Assist|3.1.0|2026-04-09|
|AI Data Explorer|4.1.5|2026-05-05|
|AI Enhanced Recommended Actions|1.0.1|2026-03-12|
|AIOps LEAP|3.2.1|2026-04-09|
|Alert Assist|3.8.1|2026-03-12|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.1.4|2026-04-09|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Build Agent Premium|1.1.9|2026-04-28|
|Care Team Operations AI agent collection|1.0.2|2026-04-09|
|Catalog Conversational Coverage|6.0.1|2026-03-12|
|Chat Recommendation|1.6.3|2026-04-09|
|Chat Summarization for Virtual Agent|1.10.5|2026-04-09|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.0.0|2026-03-12|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|7.1.5|2026-04-09|
|Conversational subflows and actions|29.2.2|2026-04-09|
|CTO Voice AI Agents|1.0.2|2026-04-09|
|Custom App Record Summarization|29.1.2|2026-04-09|
|Customer Service Management AI agent collection|5.1.0|2026-04-09|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|1.0.2|2026-04-09|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Dynamic Guidance|28.2.15|2026-04-09|
|External content connectors - Now assist agent|1.0.6|2026-05-21|
|Field Service Management AI agent collection|2.1.0|2026-04-09|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|13.1.2|2026-04-09|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|6.1.2|2026-04-09|
|HR Service Delivery AI agent collection|6.0.1|2026-04-09|
|HR Talent AI Agent Collection|4.1.0|2026-04-09|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|3.0.0|2026-05-05|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management AI voice agent collection|1.2.0|2026-04-09|
|ITOM AI Agents For Service Mapping|1.2.6|2026-03-12|
|Knowledge Center|31.8.1|2026-04-09|
|Knowledge Graph|7.1.2|2026-04-09|
|List AI Experience|2.0.8|2026-03-12|
|Manage Invoice Operations|1.0.2|2026-04-09|
|Manage Order Operations|1.0.4|2026-04-09|
|Manufacturing Commercial Operations AI agents collection|2.0.2|2026-03-12|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.11.1|2026-05-21|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.8|2026-04-09|
|Model Context Protocol Client|2.1.0|2026-03-12|
|Model Context Protocol Server|1.3.1|2026-04-09|
|Notifications Email Agents|2.0.1|2026-04-09|
|Now Assist Admin Console|9.0.5|2026-04-09|
|Now Assist Agents for requestor|3.3.0|2026-04-09|
|Now Assist AI Agents|7.2.11|2026-05-05|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|29.0.7|2025-12-11|
|Now Assist Analytics|4.1.3|2026-04-09|
|Now Assist context menu|3.5.1|2026-05-05|
|Now Assist Data Kit|7.1.2|2026-04-09|
|Now Assist for Accounts Payable Operations \(APO\)|7.1.0|2026-04-09|
|Now Assist for App Engine|29.1.2|2026-04-09|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|1.0.3|2026-04-09|
|Now Assist for Collaborative Work Management \(CWM\)|5.0.1|2026-03-12|
|Now Assist for Complaint Case \(CSM\)|2.1.1|2026-04-09|
|Now Assist for Configuration Management Database \(CMDB\)|3.2.1|2026-04-09|
|Now Assist for Contract Analysis|1.0.8|2026-05-05|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Creator|28.8.2|2026-04-09|
|Now Assist for Customer Service Management \(CSM\)|12.1.2|2026-04-23|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.1.1|2026-04-09|
|Now Assist for Enterprise Architecture \(EA\)|7.1.0|2026-03-12|
|Now Assist for Field Service Management \(FSM\)|9.1.0|2026-04-09|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|6.1.0|2026-04-09|
|Now Assist for Hardware Asset Management|4.1.0|2026-04-09|
|Now Assist for Health and Safety|1.3.1|2026-04-09|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.1.3|2026-04-09|
|Now Assist for Impact|3.1.3|2026-04-09|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.6.9|2026-04-09|
|Now Assist for Legal Service Delivery|1.6.5|2026-04-09|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.0.1|2026-03-12|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.0.7|2026-04-09|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|11.1.0|2026-04-09|
|Now Assist for Platform for Requestor|3.0.1|2026-03-12|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.5|2026-03-12|
|Now Assist for Prompt Assistance|4.0.3|2026-04-09|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.0.3|2026-03-12|
|Now Assist for Purchase Order Management \(POM\)|1.1.0|2026-04-09|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Sales and Order Management for Telecommunications|2.0.7|2026-04-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.1|2026-04-09|
|Now Assist for Security Incident Response \(SIR\)|4.3.1|2026-03-12|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.0.12|2026-04-09|
|Now Assist for Setup|2.0.7|2026-04-09|
|Now Assist for Setup Core|1.0.6|2026-04-09|
|Now Assist for Software Asset Management \(SAM\)|7.0.0|2026-04-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|9.1.0|2026-04-09|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.1.0|2026-04-09|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|7.1.0|2026-04-09|
|Now Assist for Talent|1.7.0|2026-04-09|
|Now Assist for Telecommunications|1.1.5|2026-04-09|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.6|2026-04-09|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|4.1.2|2026-04-09|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.8|2026-03-12|
|Now Assist for Zero Copy Connector|1.0.9|2025-12-11|
|Now Assist in AI Search|16.1.4|2026-05-29|
|Now Assist in Catalog Builder|7.1.0|2026-04-09|
|Now Assist in Catalog item forms|1.2.5|2025-12-11|
|Now Assist in Contract Management|2.1.3|2026-04-09|
|Now Assist in Conversational Catalog Request|6.0.2|2026-03-12|
|Now Assist in Document Intelligence|6.0.10|2026-04-09|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|30.8.0|2026-04-09|
|Now Assist in Standard Ticket Page|1.0.6|2025-12-11|
|Now Assist in Virtual Agent|17.0.12|2026-04-09|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|2.4.3|2026-03-12|
|Now Assist Skill Discovery and Execution|9.1.9|2026-04-09|
|Now Assist Skill Kit|8.1.3|2026-04-09|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|OT Manager Foundation|3.3.1|2026-04-09|
|Platform AI Agents and Skills|12.1.10|2026-05-29|
|prompt-management|1.0.11|2026-03-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|5.1.1|2026-04-09|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM AI agent collection|1.3.0|2026-03-12|
|Sales Development AI Agents|1.0.7|2025-12-11|
|Screen Summarization|1.0.10|2026-04-09|
|ServiceNow AI Lens|4.0.0|2026-03-12|
|Summarization for Order Management|2.0.1|2026-03-12|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Telecommunications Media and Technology AI agent collection|5.1.3|2026-04-09|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.0.4|2026-03-12|
|UI Generation|28.2.14|2026-01-23|
|Universal Request AI agent collection|1.0.7|2026-04-09|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|

## Suite version 28.9.20260611 - Zurich Patch 9

**Note:** These versions have been withdrawn. See [June 18 2026 Now Assist Suite release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/na-suite-rn-2026-06-18.md) for the June release versions.

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

AI Agents for Health and Safety

</td><td>

1.3.3

</td><td>

Fixed: Missing xml field that were causing data quality tests to fail

</td></tr><tr><td>

AI Search RAG

</td><td>

6.1.0

</td><td>

Fixed -   Addressed Brazil security directive
-   Honoured document\_match\_count in the Uber RAG instead of default.
-   Updated default chunking mode to STB\(Small to big\) instead of Fixed Size.

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.0

</td><td>

Changed: Deprecated searching and scraping functionality.

</td></tr><tr><td>

App Generation

</td><td>

28.3.11

</td><td>

Removed: Removed now.assist.creator role

</td></tr><tr><td>

App Summary

</td><td>

28.2.6

</td><td>

Removed: Removed now.assist.creator role

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

Conversation Evaluator

</td><td>

3.0.4

</td><td>

Performance improvement.

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.3.2

</td><td>

Fixed:

 Updated the version for ServiceNow Docs Connector to fix dependency failures

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

3.0.3

</td><td>

New -   Role Masking: Added role masking security for all AI Agent usecases, agents, and skills.
-   New AI agents added for ACH Processing: Merchant analysis for disputes AI agent, Nacha operating guidelines check AI agent, ACH dispute return recommendation AI agent and Dispute communication AI agent.

</td></tr><tr><td>

Form data collector

</td><td>

2.0.0

</td><td>

-   New: Added scripted extension point to allow dynamic replacement of choice values based on table and field name.
-   Changed: Updated topic to check if extension point implementation is required.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.3.6

</td><td>

Fixed: AI Agent records view was affected due to an AI Native ACL issue

</td></tr><tr><td>

MID Guardian

</td><td>

1.0.4

</td><td>

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem / ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. Mid Guardian Agent intelligently analyzes logs, signals, and runtime behaviors. It offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server. - Root cause analysis \(RCA\) with Agentic AI - Correlation of symptoms from various telemetry sources \(e.g., logs, errors\) - Automated execution of corrective actions \(e.g., restarting services\) - Playbook-driven or Agentic AI-led remediation strategies - Action recommendations for unresolved or partially resolved issues, utilizing web searches - Self-learning from previous resolutions and human interventions

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

Now Assist for Employee Center Pro

</td><td>

1.1.9

</td><td>

Added support for Now Assist Suite to enhance the installation/upgrade experience.

</td></tr><tr><td>

Now Assist for Health and Safety

</td><td>

1.4.1

</td><td>

New: Contextual Action Planner sidebar in the Health and Safety Workspace: Create actions manually or from AI suggestions, and review them in context across incidents, observations, investigations, cases, audits, work permits, risk assessments, meetings, etc.

</td></tr><tr><td>

Now Assist for Playbook

</td><td>

28.0.1

</td><td>

Changed: Updated with enhanced security for your data

</td></tr><tr><td>

Now Assist for Spoke Generation

</td><td>

1.5.10

</td><td>

Patch release with a bug fix.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.0.0

</td><td>

New:

 The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data across all types of findings within USEM.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

2.0.5

</td><td>

-   New
    -   Q&amp;A: Allows users to ask specific questions about the content within a document
    -   FAQ: Displays frequently asked questions derived from the document
-   Changed: Summary: Provides a concise summary of the document

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

1.0.10

</td><td>

Made app compliant with December security directives

 NowLLM LTS Support

</td></tr><tr><td>

Setup Hub

</td><td>

1.0.1

</td><td>

June Release Highlights -   Tiered SKU Support for AI Native ITSM &amp; CBSAdded support for Advanced and Prime SKUs across AI Native ITSM and CBS, including associated entitlement-driven flows and experiences.
-   Product Hub UX EnhancementsIntroduced targeted UX improvements to Product Hubs, including updates to the Resources section and guided content refinements based on leadership and customer feedback to create a more intuitive onboarding experience.
-   LitJS Component Adoption in NAPEnabled the ability to import and leverage LitJS components within NAP, helping establish a more scalable and consistent component framework.
-   Admin Home Banner UpdatesUpdated Admin Home banners and messaging to better guide users through setup, actions, and key implementation milestones.
-   Zero-Touch ImplementationExpanded Zero-Touch Implementation capabilities to deliver provisioned instances with entitled plugins and apps fully enabled, giving customers a value-ready environment from day one.
-   Intelligent Configuration Update TrackingBuilt on the April GA release with smarter tracking of configuration updates and changes, helping customers stay informed of new capabilities and recommended actions.
-   Targeted UI ImprovementsDelivered incremental UI enhancements across the experience, informed directly by customer and leadership feedback to improve usability and flow.
-   Common Component Adoption Across ConsolesContinued adoption of shared/common components to create a more consistent and unified experience across consoles.
-   Hierarchical Agents, Phase 1Introduced Phase 1 of the hierarchical agent orchestration layer, laying the foundation for more intelligent, coordinated experiences.
-   Impact BU UptakeExpanded onboarding and enablement to support Impact BU adoption and uptake of the platform and implementation capabilities.

</td></tr><tr><td>

Task Plan Template AI Agents

</td><td>

1.0.0

</td><td>

New -   Business users create templates to manage process so that all tasks are standardized across the organization. The template AI agent helps in creating templates from their current existing documents.
-   Users can upload images or diagrams which contain a process flow/flow diagram. The Template AI agent reads these documents and analyzes the template and template items required.
-   The Template ai agent creates a draft template along with template items based on the document and provides draft template details which are verified by the user.

</td></tr><tr><td>

Universal Request AI agent collection

</td><td>

1.0.9

</td><td>

Fixed minor system defects

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.3.13

</td><td>

Defects fixed:

 1.  Fixed now-voice-input to display browser's microphone as active and shows recording only when needed.
2.  Fixed the issue where now-voice-input can be disabled when needed.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@servicenow/sn-ai-engagement-experience|3.2.6|2026-05-05|
|AI Agent Advisor|1.0.2|2026-06-04|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.8.5|2026-05-05|
|AI Agents for Customer Success Management|2.7.2|2026-04-09|
|AI Agents for Discovery|2.0.4|2026-04-09|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.0|2026-05-05|
|AI Agents for ITAM|4.1.0|2026-04-09|
|AI agents for Observability|5.0.4|2026-03-12|
|AI Agents for Service Exchange Provider|1.0.12|2026-04-09|
|AI agents for SLO|1.0.7|2026-05-05|
|AI Agents for Workplace Service Delivery|3.2.0|2026-04-09|
|AI Control Tower for Now Assist|3.2.2|2026-05-05|
|AI Data Explorer|4.1.5|2026-05-05|
|AI Desktop Actions|3.0.1|2026-05-05|
|AI Enhanced Recommended Actions|1.0.2|2026-05-05|
|AI Experience Framework Skills|1.0.4|2026-05-05|
|AIOps LEAP|3.3.1|2026-05-15|
|Alert Assist|3.9.1|2026-05-05|
|Amazon Bedrock Spoke|1.4.0|2026-03-12|
|Analytics Generation|4.1.6|2026-05-05|
|App Generation|28.3.11|2025-12-11|
|App Summary|28.2.6|2025-12-11|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Build Agent Premium|1.2.6|2026-05-05|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|Chat Recommendation|1.6.3|2026-04-09|
|Chat Summarization for Virtual Agent|1.10.5|2026-04-09|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.0.0|2026-03-12|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Studio|8.0.1|2026-05-05|
|Conversational subflows and actions|29.2.2|2026-04-09|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.1.2|2026-04-09|
|Customer Service Management AI agent collection|5.1.5|2026-05-05|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Dashboard and visualization export|1.3.5|2026-01-20|
|DocIntel Vision AI Agent|1.0.2|2026-04-09|
|Document Intelligence for Contract Management Content Pack|1.4.1|2026-03-12|
|Employee Slate for Now Assist|1.0.2|2026-05-05|
|External content connectors - Now assist agent|1.0.6|2026-05-21|
|Field Service Management AI agent collection|2.1.0|2026-04-09|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
|Form data collector|2.0.0|2025-12-11|
|Generative AI Controller|13.2.2|2026-05-05|
|Google Gemini Spoke|1.6.0|2026-03-12|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Group-Action Framework|6.1.2|2026-04-09|
|HR Service Delivery AI agent collection|6.1.3|2026-05-05|
|HR Talent AI Agent Collection|4.1.0|2026-04-09|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Insights Clustering Utils|3.0.0|2026-05-05|
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|IT Service Management AI agent collection|8.0.3|2026-05-08|
|IT Service Management AI voice agent collection|1.2.0|2026-04-09|
|ITOM AI Agents For Service Mapping|1.3.1|2026-05-05|
|Knowledge Center|31.9.9|2026-05-05|
|Knowledge Graph|7.2.1|2026-05-05|
|List AI Experience|2.0.8|2026-03-12|
|Manage Invoice Operations|1.0.2|2026-04-09|
|Manage Order Operations|1.0.4|2026-04-09|
|Manufacturing Commercial Operations AI agents collection|2.0.2|2026-03-12|
|Metadata Search|1.0.11|2026-05-05|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.11.1|2026-05-21|
|MID Guardian|1.0.4|2025-12-11|
|Mobile Builder AI|27.4.8|2026-04-09|
|Model Context Protocol Client|2.1.0|2026-03-12|
|Model Context Protocol Server|1.4.2|2026-05-05|
|Notifications Email Agents|2.0.4|2026-05-05|
|Now Assist Admin Console|9.1.8|2026-05-05|
|Now Assist Agents for requestor|3.4.1|2026-05-05|
|Now Assist AI Agents|7.2.11|2026-05-05|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|30.0.6|2026-05-05|
|Now Assist Analytics|4.1.7|2026-05-05|
|Now Assist Center|3.0.5|2026-05-05|
|Now Assist context menu|3.5.1|2026-05-05|
|Now Assist Data Kit|7.2.3|2026-05-05|
|Now Assist for Accounts Payable Operations \(APO\)|7.2.1|2026-05-05|
|Now Assist for App Engine|29.1.2|2026-04-09|
|Now Assist for Automation Center|1.1.2|2026-04-09|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for Collaborative Work Management \(CWM\)|5.0.1|2026-03-12|
|Now Assist for Complaint Case \(CSM\)|2.1.1|2026-04-09|
|Now Assist for Configuration Management Database \(CMDB\)|3.6.0|2026-05-05|
|Now Assist for Contract Analysis|1.0.8|2026-05-05|
|Now Assist for CPQ|1.0.3|2026-04-09|
|Now Assist for Creator|28.9.2|2026-05-05|
|Now Assist for Customer Service Management \(CSM\)|12.2.0|2026-05-05|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.2.0|2026-05-05|
|Now Assist for Enterprise Architecture \(EA\)|7.1.0|2026-03-12|
|Now Assist for Field Service Management \(FSM\)|9.1.0|2026-04-09|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|6.2.1|2026-05-05|
|Now Assist for Hardware Asset Management|4.1.0|2026-04-09|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for HR Service Delivery \(HRSD\)|13.1.5|2026-05-05|
|Now Assist for Impact|3.1.3|2026-04-09|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for IT Operations Management \(ITOM\)|2.6.12|2026-05-05|
|Now Assist for IT Service Management \(ITSM\)|14.0.6|2026-05-15|
|Now Assist for Legal Service Delivery|1.7.7|2026-05-05|
|Now Assist for Manufacturing Commercial Operations \(MCO\)|2.0.1|2026-03-12|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for Order Management|2.1.0|2026-05-05|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform|11.2.0|2026-05-05|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.8|2026-05-05|
|Now Assist for Prompt Assistance|4.1.4|2026-05-05|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.0.3|2026-03-12|
|Now Assist for Purchase Order Management \(POM\)|1.1.0|2026-04-09|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Sales and Order Management for Telecommunications|2.0.7|2026-04-09|
|Now Assist for Sales Force Automation \(SFA\)|1.1.1|2026-04-09|
|Now Assist for Security Incident Response \(SIR\)|4.3.1|2026-03-12|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Exchange|1.0.12|2026-04-09|
|Now Assist for Setup|2.1.2|2026-05-05|
|Now Assist for Setup Core|1.1.2|2026-05-05|
|Now Assist for Software Asset Management \(SAM\)|7.0.0|2026-04-09|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|9.2.2|2026-05-05|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Strategic Portfolio Management \(SPM\)|9.4.0|2026-05-05|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|7.2.2|2026-05-05|
|Now Assist for Talent|1.7.0|2026-04-09|
|Now Assist for Telecommunications|1.1.5|2026-04-09|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.6|2026-04-09|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Voice|4.2.3|2026-05-05|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.8|2026-03-12|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in AI Search|16.1.4|2026-05-29|
|Now Assist in Catalog Builder|7.1.2|2026-05-05|
|Now Assist in Catalog item forms|1.3.2|2026-05-05|
|Now Assist in Contract Management|2.1.10|2026-05-05|
|Now Assist in Conversational Catalog Request|7.0.2|2026-05-05|
|Now Assist in Document Intelligence|6.0.12|2026-05-05|
|Now Assist in Document Management|2.0.5|2025-12-11|
|Now Assist in Knowledge Management|30.9.2|2026-05-05|
|Now Assist in Standard Ticket Page|1.0.9|2026-05-05|
|Now Assist in Virtual Agent|18.0.13|2026-06-04|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|2.4.3|2026-03-12|
|Now Assist Service Quality|1.0.2|2026-05-05|
|Now Assist Skill Discovery and Execution|10.0.4|2026-05-05|
|Now Assist Skill Kit|8.2.9|2026-05-05|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|OT Manager Foundation|3.3.1|2026-04-09|
|Platform AI Agents and Skills|12.2.7|2026-05-05|
|prompt-management|1.0.11|2026-03-12|
|Public Sector Digital Services AI Agent Collection|1.0.10|2025-12-11|
|Query Generation|5.2.0|2026-05-05|
|RAG for code generation|1.1.8|2026-03-12|
|Recommendation template|22.0.1|2026-03-12|
|RSM AI agent collection|1.3.0|2026-03-12|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Screen Summarization|1.1.11|2026-05-05|
|ServiceNow AI Lens|5.0.0|2026-05-05|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Telecommunications Media and Technology AI agent collection|5.1.3|2026-04-09|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.1.0|2026-05-05|
|UI Generation|28.2.14|2026-01-23|
|Voice input for Now Assist|1.3.13|2025-12-11|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|


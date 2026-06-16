---
title: Now Assist for ITOM release notes
description: Version history for the Now Assist for ITOM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-now-assist-itom.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Now Assist for ITOM release notes

Version history for the Now Assist for ITOM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.16 - June 2026**
    -   New:
        -   AIOps AI Specialist — Autonomous Alert Management\(Limited Availability\) The AIOps AI Specialist is ServiceNow's purpose-built AI agent for IT Operations. It autonomously monitors, triages, and resolves infrastructure and application alerts, executing the full NOC workflow without requiring human intervention on every event. In this release, the AI Specialist can:
            -   Automatically pick up alerts based on configurable scope and filter rules
            -   Run alert analysis, investigation, and impact assessment autonomously
            -   Collaborate with the SRE Agent for deep-level investigation using A2A integration with observability tools and hyperscalers
            -   Hand off to a remediation agent to execute subflow-based fixes
            -   Close alerts determined to be insignificant noise
            -   Be triggered manually by assigning an alert directly to the AI Worker user
        -   Onboarding Experience for the AIOps AI Specialist – A guided setup flow helps NOC team managers configure and activate the AI Specialist quickly and consistently.
        -   Remediation Agent – A new remediation agent works alongside the AIOps AI Specialist to automatically identify and execute the appropriate remediation subflow for an alert.
        -   Proactive Grouping Recommendations – Alert Assist now proactively analyzes incoming alerts and recommends grouping candidates before a NOC operator opens a case. The engine uses intelligent field selection to identify the most relevant alert attributes, supports all LLM types, and handles high-cardinality and verbose alert data gracefully. Recommendations are refreshed every 5 minutes via a scheduled job.
        -   AI Resolution Attribution – When the AIOps AI Specialist closes an alert, the system records it as "Closed by AI," capturing which alerts were fully handled autonomously. This enables NOC teams to measure automation rate and track AI-driven closure trends over time.
        -   Text to Configuration Agent – Available out of the box, the Text to Configuration Agent allows operators to configure AIOps settings using natural language — no form-filling required.
    -   Changed:
        -   The AI Worker alert management rule now supports coexistence with autonomous mode.
        -   The auto-close path for insignificant noise alerts has been updated for more reliable handling.
        -   Autonomous Styled Output now generates a remediation anchor to support downstream remediation workflows.
        -   LLM Model Upgrades – Alert Assist skills have been updated to use gpt-4o-mini\(previously gpt-small\) and Claude Haiku 4.5\(previously claude-small\), improving output quality and aligning with current model availability.
    -   Fixed:
        -   The AI Investigation Report displayed an infinite loading spinner on timeout.
        -   The Regenerate action in the AI Insights card was non-deterministic. The Express List also showed incorrect insight data when the first analysis run failed.
        -   The Autonomous Operator was not updating descriptions on individual HLA alerts.
        -   Alert Assist was logging unnecessary errors when no related changes passed the relevance threshold.
        -   Alert Assist was logging null pointer exceptions during skill availability checks.
-   **Version 2.6.12 - May 2026**

    New: Introducing the ITOM MCP Server, available through the MCO Console Admin. The ITOM MCP server enables seamless integration with your ServiceNow instance, allowing you to connect to and manage alerts efficiently. This capability extends to leveraging any 3rd-party AI tool such as Claude, ChatGPT, and others, to retrieve information, perform analysis, investigate, and access additional skills to streamline your workflow.

-   **Version 2.6.9 - April 2026**

    Added support to Australia release

-   **Version 2.6.0 - March 2026**
    -   New:
        -   AI Analysis for Automated Alert Groups.
        -   Noise Alert Classification. A new LLM-based classifier automatically evaluates same-alert groups matched by CI/node and metric name, and determines whether each group represents noise or requires operator action.
        -   Text-to-Configuration AI Agent for Alert Grouping. Event Management administrators can now describe alert grouping automation rules in plain language through the Now Assist panel in Service Operations Workspace. The agent interprets intent, asks clarifying questions for any missing details, presents a full preview of the proposed rule, and creates it as an inactive configuration ready to activate, save, or simulate.
        -   AI Alert Insights: Rich HTML Formatted Output. The Autonomous Operator workflow now generates HTML-formatted insights rendered through the now-rich-text component.
        -   AI Insights Card Embedded in UI16 Alert Form. The AI Insights card is now embedded directly in the UI16 Alert Form, giving operators immediate access to contextual AI analysis without navigating to the Service Operations Workspace or Now Assist panel.
        -   Service Observability Dashboard Summarization. The Autonomous Operator workflow now incorporates Service Observability dashboard health analysis for services associated with an alert, enriching AI summaries with broader observability context before surfacing results to the operator.
-   **Version 2.5.1 - February 2026**
    -   Fixed:
        -   Fixing automatic execution in new instances
        -   Fixing knowledge summarization and probable root cause with Now LLM
        -   Fixing skill group definition for ITOM skills
-   **Version 2.5.0 - January 2026**
    -   New:
        -   Manage alert autonomously agentic workflow
        -   Datadog analysis AI Agent
        -   Google Cloud Observability analysis AI Agent
        -   AIOps LEAP
            -   Create Knowledge Base articles with embedded command snippets
            -   Guided chat workflow to create and manage Playbooks and KBs
            -   Break automation opportunities with large number of records into targeted sub-groups using GenAI
            -   Generate comprehensive resolution steps from multiple web sources
            -   Regenerate resolutions when new data sources are enabled
    -   Changed:
        -   AIOps LEAP
            -   AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation
            -   Playbooks appear natively in Service Operations Workspace module
            -   Status information for records grouping job run, with support KB content
            -   New interface to configure opportunity savings and reporting
            -   Surface optimization opportunities and knowledge gaps for architects
            -   Show analyzed data date range on Opportunities page for automation teams to be aware of time-ranges of analysis
            -   Enterprise security compliance with role masking mandate implemented
-   **Version 2.4.5 - December 2025**
    -   New:
        -   AI Agents for MID Server
        -   AI Agents for ACC
-   **Version 2.3.3 - October 2025**

    Fixed: Aligned application dependencies for Yokohama and Zurich.

-   **Version 1.3.6 - October 2025**

    Changed: Certified Now Assist for ITOM with Xanadu, including security fixes for compliance and stability.

-   **Version 2.3.0 - September 2025**
    -   New:
        -   New AI Agents for Service Mapping
        -   New AI Agents for Discovery
        -   An updated Analyze Alert Impact workflow with additional AI agents
-   **Version 2.2.1 - August 2025**

    New: Certify 4 LLM for Now Assist Skills and AI Agents.

-   **Version 1.3.5 - June 2025**
    -   New:
        -   AI Agents for AIOps
        -   AI Agents for Observability
        -   AIOps LEAP
-   **Version 2.0.0 - May 2025**
    -   New:
        -   AI Agents for AIOps
        -   AI Agents for Observability
        -   AIOps LEAP
-   **Version 1.5.0 - February 2025**
    -   New:
        -   Leveraging RAG AIS to identify more relevant incidents for Alert Investigation.
        -   Alert group analysis, and alert group description update for Network Traffic Connection groups.
    -   Changed: Synced Express List selection and Now Assist Panel for faster record selection and improved user effectiveness.
-   **Version 1.2.0 - November 2024**
    -   New:
        -   Alert Investigation Skill - Helps users analyze related incidents with targeted insights, including relevant assignees and assigned teams, incident timelines, and resolutions.
        -   The Alert Analysis skill is now accessible directly from the Now Assist Panel, providing quick, insightful alert overviews.
        -   Edit Alert Group Descriptions with Now Assist - Enables users to generate and refine alert group descriptions through the Alert Analysis skill, improving clarity and contextual relevance.
    -   Fixed:
        -   Minor UI fixes
        -   Fixed domain separation for Alert Assist skills
        -   Fixed alert analysis for Tag Based groups
-   **Version 1.1.1 - September 2024**

    Fixed: Fixing deployment issues on Xanadu release.

-   **Version 1.0.4 - June 2024**

    New: Alert group analysis - Helps users understand the context of the alert group, and provides a technical analysis on the alert group level.

-   **Version 1.0.1 - March 2024**

    Now Assist for IT Operations Management represents a groundbreaking application within the ServiceNow ecosystem, integrating cutting-edge Gen AI capabilities into IT operations products. Among its innovative features, Alert Assist stands out as a cornerstone functionality. Leveraging advanced generative AI technology, Alert Assist revolutionizes the management of alerts by providing human-readable descriptions that succinctly convey the essence of each alert. Moreover, it enriches these descriptions with an alert analysis section, furnishing technical details crucial for understanding and addressing the underlying issues. By seamlessly integrating with ServiceNow's IT operations suite, Now Assist enhances operational efficiency and empowers IT teams to proactively tackle challenges, thereby elevating the performance and resilience of organizational IT infrastructure.



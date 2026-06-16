---
title: AIOps LEAP release notes
description: Version history for the AIOps LEAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-leap.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# AIOps LEAP release notes

Version history for the AIOps LEAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026**
    -   New:
        -   Discover and execute Ansible playbooks from LEAP automation opportunities to promote faster incident resolution
        -   Track missed automation opportunities in LEAP to identify gaps in automation coverage
        -   Auto-generate resolution steps for all critical and high severity automation opportunities post initial run
        -   Improved resolution step relevance as irrelevant steps filtered out by group problem description
        -   LEAP available with Now Assist for ITSM
    -   Changed:
        -   Product renamed from AIOps LEAP toLEAP \(Learning-Enhanced Automation Platform\)
        -   AI-enhanced and structured knowledge base articles published to the Knowledge Center
    -   Fixed:
        -   Automation Opportunities page load time reduced from 3+ seconds
        -   Value Dashboard page load time reduced from 4+ seconds
        -   Resolved stale resolution steps reappearing in record metric table after SOW Flow updates
        -   Fixed sharp-edged AI Gradient button for Regenerate in AO Details to match default theme
        -   Fixed UI issues on resolution steps filter in LEAP Settings page
        -   Fixed missing help content on LEAP Installer Skill Activation page
        -   Reverted unintended default UI filter that auto-generated resolution steps
        -   Fixed Maintenance ACL Roles being overridable by Admins in LEAP Automation Playbooks
-   **Version 3.3.0 - May 2026**
    -   New: Added support for GPT 5.4, OpenAI's latest large language model, for LEAP automation recommendations and AI-assisted workflows.
    -   Changed:
        -   The following default models are updated: claude\_large→ Claude Sonnet 4.6, claude\_small→ Claude Haiku 4.5, gpt\_small→ GPT 5.2 mini,
        -   Prior versions remain available for customer selection. New model: gpt\_large→ GPT 5.4.
-   **Version 3.2.1 - April 2026**

    New: Support new third-party model, Claude Sonnet 4.6

-   **Version 3.1.2 - March 2026**

    New: Expanded 3P AI Model Support - Introduced additional model options across Small \(OpenAI GPT-4o mini, Claude Haiku 4.5, Gemini 2.0 Flash\) and Large \(OpenAI GPT-4o, Claude Sonnet 4.5, Gemini 2.0 Pro\) tracks; existing model defaults remain unchanged and customers can opt in via new prompt configurations.

-   **Version 3.0.0 - January 2025**
    -   New:
        -   KB Artifacts: Create Knowledge Base articles with embedded command snippets
        -   Hierarchical Clustering: Break large groups into targeted sub-groups using GenAI
        -   Resolution Mining: Generate comprehensive resolution steps from multiple web sources
        -   KB Artifacts: Auto-create Knowledge Base articles with embedded command snippets
        -   Persistent Regeneration: Regenerate resolutions when new data sources are enabled
        -   LEAP Agent: Guided chat workflow to create and manage Playbooks and KBs
    -   Changed:
        -   Platform Rebranding: AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation
        -   SOW Integration: Playbooks appear natively in Service Operations Workspace module
        -   Improved Skill Setup: Status information for records grouping job run, with support KB content
        -   Properties UI: New interface to configure opportunity savings and reporting
        -   Action Insights: Surface optimization opportunities and knowledge gaps for architects
        -   Data Range Display: Show analyzed data date range on Opportunities page for automation teams to be aware of time-ranges of analysis
        -   Role Masking: Enterprise security compliance with role masking mandate implemented
    -   Note: From August 2025, AIOps LEAP is available as part of the Now Assist for ITOM package rather than as a standalone product. For details about the Now Assist for ITOM package and included features, see [Now Assist for ITOM](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-now-assist-itom.html).
-   **Version 2.0.0 - May 2025**
    -   New:
        -   Automation feedback and tracking.
        -   Pin Automation Opportunities.
        -   Customize filters for Automation Opportunities and published playbooks.
        -   Customize columns on the Automation Opportunities and published playbook pages.
        -   Use published LEAP in SOW to resolve a new incident quickly.
        -   Use value dashboard for performance analysis and improvement.

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)


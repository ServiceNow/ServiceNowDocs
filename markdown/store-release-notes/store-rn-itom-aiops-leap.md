---
title: LEAP release notes
description: Version history for the LEAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-leap.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - ITOM AIOps version history release notes, ServiceNow Store - IT Operations Management version history release notes, ServiceNow Store version history release notes]
---

# LEAP release notes

Version history for the LEAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.3.1 - September 2026**
    -   New:
        -   Knowledge base article improvements
            -   Admins can configure eligible knowledge bases and default KB/category for article creation. The Settings page allows selection of eligible knowledge bases, default knowledge base, and default KB category, which are automatically applied during agent-driven KB article creation.
            -   Users can select the knowledge base and category when creating KB articles. A configurable modal prompts users to choose the target KB and category, with metadata and author fields auto-populated for improved search and traceability.
        -   LEAP value dashboard
            -   The LEAP value dashboard surfaces metrics for all automation outcome types. The dashboard includes new sections and cards for Ansible executions, KB articles, problem records, and outcome breakdowns, with savings attribution by outcome type and Now Assist consumption metrics.
            -   Metrics dashboard tabs for artifacts are introduced. Users can view tabular metrics for KB articles, ServiceNow playbooks, Ansible playbooks, Problem records, and an overview of all artifacts, with project-level and system-wide calculations.
        -   Automation projects
            -   LEAP supports automation projects across multiple incident taxonomies. Admins can configure LEAP to ingest and cluster incidents from multiple taxonomies, producing unified insights and automation opportunities spanning all configured taxonomies.
        -   LEAP MCP tool
            -   LEAP MCP tool for app setup status is introduced for external AI clients to use LEAP's setup and grouping-pipeline readiness before invoking other tools.
        -   Manage archived automation opportunities
            -   Admins can view and manage archived automation opportunities\(AOs\). Old AOs with resolution steps are hidden by default after GAF re-runs, and successor/predecessor relationships are surfaced on the AO detail page.
        -   AI Sparkle indicator is shown for discovered Ansible playbooks.
            -   The LEAP homepage AO list includes an additional column to visually identify playbooks created with AI.
    -   Changed:
        -   LEAP value dashboard layout is updated to tabular format. Artifacts are presented in dedicated tabs with consistent layout and improved clarity.
        -   Playbook and Ansible metrics are filtered by automation source. Aggregate metrics now distinguish between ServiceNow playbooks and Ansible playbooks for accurate reporting.
        -   Archived flag is backfilled for legacy stranded AOs. Upgrade scripts ensure previously stranded AOs are correctly marked as archived, aligning UI visibility and actions.
        -   Default AO list and homepage filters exclude archived AOs. The homepage and list views now show only active, non-archived AOs.
        -   KB article creation options and modal labels are revised. The create/view KB article actions are renamed to "Draft KB article," and modal info text is clarified.
        -   Job status and troubleshooting actions are scoped per Automation project. Job status lookups and fix-the-error navigation are filtered by the selected project.
        -   Properties reads are project-scoped with fallback to global defaults. Changing a property on one project does not affect others.
-   **Version 4.2.1 - August 2026**

    Changed: Now Assist is renamed to 'ServiceNowOtto'.

-   **Version 4.1.0 - July 2026**
    -   New:
        -   Autonomous AI Agent that scans incident clusters and automatically generates draft knowledge base articles and problem records based on configurable incident count and severity thresholds
        -   Agent-generated artifacts display with an AI icons on LEAP home page with hover cards linking to related records for visibility. The Action Insights panel on the automation opportunity details page of agent-generated artifact uses gradient styling.
        -   Ansible Connector integration now available on LEAP Home page with dedicated help section
        -   Three new generative AI models now supported: Gemini 3.5 Flash, GPT 5.4 mini, and GPT 5.1
    -   Changed: Now LLM Service is no longer the default model provider for new or inactive AI assets. Third-party LLM is selected by default, while existing configurations using Now LLM service continue to remain unchanged and are available for manual selection.
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

**Parent Topic:**[ServiceNow Store - ITOM AIOps version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)


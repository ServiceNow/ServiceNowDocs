---
title: AI Admin Center release notes
description: Version history for the ServiceNow AI Admin Center application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-now-assist-center.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# AI Admin Center release notes

Version history for the ServiceNow® AI Admin Center application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.0.7 - September 2026**
    -   Agent Advisor UI enhancements improve opportunity resolution and filtering.
    -   Automation Opportunity page experience enhancements.
    -   Agent miner data set supports removal of custom data sets.
    -   Daily recommendation feature removed from Agent Advisor.
    -   Multiple cost profiles support removed; only a single cost profile is available.
-   **Version 5.1.9 - August 2026**
    -   New:
        -   Generally available: New public API \(script include\) exposes automation-opportunity data globally.
        -   New Lit.JS user experience only \(selected users\)
            -   AI readiness: Single hub for all activation-ready skills and AI agents; filter by type, metrics with change indicators, activate, expand for details, re-run assessment.
            -   Monitor tab: Cross-repo analytics in a new sidebar entry \(Overview, Performance Explorer, Business Value widgets\).
            -   System property registry: Browse/search/filter AI properties by domain and editability; view details; edit eligible single-value and boolean properties in-UI with audit logging \(masked, multi-value excluded\).
            -   Upgrade readiness pre-check: AI-specific impact report vs target releases — at-risk customizations, changed behaviors, deprecated features, new config options, with remediation and exports.
            -   AI Agent Advisor: Create/edit custom data sets, define cost profiles, new views for OOTB agents and clusters, including step pages.
            -   AI Search integrated into the discover flow.
            -   Self-healing AI agent skill support added to AI Agent Advisor.
            -   Automation opportunity backend wired into shared AI Readiness and Asset Inventory components for ready-to-activate.
    -   Changed:
        -   Generally available: Otto rebranding: all Now Assist Center references updated to AI Admin Center.
        -   Lit.JS only \(selected users\)
            -   AI Optimization renamed to AI Readiness, with updated filters, components, and design across Health, Ready-to-Activate, Data Quality tabs.
            -   Ready-to-Activate table refactored with snow-list.
            -   Plan Upgrade adopts snow-list and August UI tweaks; category filter pills removed, sub-filter pills retained.
            -   Customizations tab \(Upgrade Pre-Check\): Action-button nav to file details, more filters, breadcrumb mapping, better consistency.
            -   Instance Health stream shows all inactive agents and OOTB skills ready to activate.
            -   Data Quality tab adds an Estimated Effort column.
            -   Localization standardized via aiux-services i18n.
            -   Accessibility verified and fixed across all pages.
            -   Typography tokens and rules established.
            -   Snow-design-system components made Horizon 2.0-compliant on Home, Agent Advisor, Opportunity Detail.
            -   Now Assist Admin refactored for Lit.JS/Horizon 2.0 — Model Mgmt/Versions, Experiences, Edit Model Providers, DT Languages.
            -   Sidebar adopts latest karuna side-nav and top header \(navigation, logout, impersonate, scope-picker\).
            -   "New version available" indicator added to the AI Readiness page.
            -   Agent Advisor resolution steps and modal updates for OOTB agents.
            -   AI Agent Advisor settings/list pages show updated timestamps, cost-profile fields, cluster mapping.
            -   AI Readiness Overview tab adds graph components for Health, Data Quality, Ready-to-Activate metrics.
            -   System Property Registry supports cross-scope edits with scope-aware, role-accurate UI.
            -   Upgrade Pre-Check supports async run orchestration and per-file review.
    -   Fixed:
        -   Generally available: NAA KAA Auth dependency removed; Skills config now uses SkillConfig instead of the REST API.
            -   Lit.JS only \(selected users\)
                -   UI/stability: Blank-page loads, broken AI Solution page, dark theme, missing nav loaders, Otto Panel images, "Loading Now Assist…" hang.
                -   Navigation: Failing menu/workspace redirection and a broken Home "View All" control.
                -   AI Readiness/Instance Health: disabled Re-Run Assessment button, missing AI Solution count, skill-activation and rapid-action-card display issues.
                -   Agent Advisor/Agent-Miner/Automation Opportunity: Page-load latency, missing Activate button for inactive configs, savings-projection count error, minor list/resolution defects.
                -   Asset Inventory: Asset details not displaying and skill-type asset-page rendering.
                -   Localization: Translation gaps and 5.1 localization warnings across Lit and UI Builder.
                -   Access/roles: Updated nac\_user access on settings sub-pages; Agent-miner role scoping.
    -   Removed:
        -   Generally available: Platform-app dependencies eliminated; platform apps now function independently.
        -   Lit.JS only \(selected users\): Pre-built automation workflows no longer accessible or visible.
-   **Version 4.0.2 - June 2026**
    -   AI asset inventory. A new Asset Inventory page provides a single, consolidated view of every AI asset deployed across the instance including AI agents, agentic workflows, skills, subflows, actions, data assets, virtual assistants, topics, catalog items, and knowledge graphs. Each asset type surfaces active/inactive status, and the list supports column personalization so administrators can tailor the view to their needs. Assets from AI Agent Studio, Data Kit, and the platform catalog are unified in a single browsable surface.
    -   AI readiness assessment. Administrators can now validate their instance's readiness for AI adoption directly within Now Assist Center. The new AI Readiness page supports on-demand and scheduled assessment execution across both Now Assist and Agentic AI assessment types. Results are surfaced in a dedicated Assessment Details page with historical tracking, enabling teams to identify configuration gaps, measure readiness over time, and accelerate the path to their first production AI solution.
    -   AI Agent Advisor enhancements. The AI Agent Advisor experience has been refined based on feedback from the May release. Updates include an improved automation opportunities list page with better filtering and layout, redesigned Agent Advisor cards, a refreshed home page CTA experience that surfaces opportunities at a glance, a new Agent Advisor settings page, and stack metrics page improvements. These changes reduce friction in the discovery-to-deployment journey and improve the quality of agent recommendations surfaced to administrators.
    -   Expanded OOTB skill configuration. The conversational administration experience now surfaces additional out-of-the-box skill configuration paths, including skill availability configuration and display experience settings extending the reach of guided, in-product setup to more of the Now Assist skill catalog.
-   **Version 3.0.5 - May 2026**

    AI Admin Center is an AI-enablement workspace that helps customers accelerate and maximize adoption of AI throughout the ServiceNow platform. It acts as a centralized hub for AI administration, solution design, and deployment — consolidating the tools, guidance, and insights AI administrators and practitioners need into a single, unified experience on their instance.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)


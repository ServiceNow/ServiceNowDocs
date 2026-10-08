---
title: ITSM - Foundation release notes
description: Version history for the ServiceNow ITSM - Foundation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-foundation.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# ITSM - Foundation release notes

Version history for the ServiceNow® ITSM - Foundation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.4.2 - October 2026**
    -   New
        -   Incident Analyzer
            -   An agentic capability that automatically investigates new incidents and writes a summary to the incident work notes.
            -   The summary covers:
                -   What happened and the likely cause, with supporting evidence.
                -   Who to contact and proposed assignment groups.
                -   Potentially responsible CIs and changes.
                -   Related active and historical incidents, events and alerts.
                -   Investigation gaps.
            -   Ships inactive. Admins can activate it and configure trigger conditions, with P1 and P2 incidents as the default scope.
            -   Sections are left out when the underlying data is not available on the instance, such as Major Incident Management or event and alert tables.
            -   Each run consumes 4 assists.
    -   Changed
        -   Create and Edit Knowledge in the AI-native fulfiller experience
            -   Create Knowledge and Edit Knowledge are now compatible with UI 26.
            -   Fulfillers working incidents and requests in this experience can create and update knowledge articles without leaving it.
        -   Gemma 4 model support and Now LLM deprecation
            -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model for Now Assist for ITSM skills and agents, including self-hosted deployments.
            -   Gemma 4 is not set as the default model.
            -   Gemma 4 replaces GPT-OSS for Guardian moderation. By default:
                -   Guardian is on in logging-only mode for agents and conversations.
                -   Guardian is on in blocking mode for skills.
            -   The Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.
    -   Fixed
        -   Investigate and resolve ITSM incidents workflow
            -   The workflow now runs after being duplicated to a subdomain with global scope.
            -   Runs no longer end in a Terminated state.
            -   The workflow no longer fails with a generic error asking the user to try again later.
            -   The work notes tool no longer updates the wrong incident when duplicate incident numbers exist.
            -   Output no longer leaves information out with certain model configurations. This affected Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German.
            -   Workflow instructions now reference the same AI agent that is configured in the workflow.
        -   Incident classification and triage
            -   The Classify service and CI AI agent no longer overwrites a populated Service, Service offering, or Configuration item field on an incident.
                -   This includes cases where the agent could not read the referenced record.
            -   The out-of-box Triage and Categorize agentic workflow no longer occasionally asks the user for input.
        -   Requested Item Summarization
            -   Summaries now match the requested item being viewed.
            -   Summaries are no longer empty when the session language is Portuguese \(Brazil\) and Now LLM is in use.
        -   Incident record experience
            -   The Assign button in the Record Information panel in Service Operations Workspace now generates hyperlinks in its output.
            -   The Now Assist modal now reflects the Assigned to field's mandatory state after a UI policy makes the field optional.
                -   Previously this blocked saving the form in Service Operations Workspace.
                -   Previously the mandatory state was shown inconsistently in the native UI.
            -   Bullet-point formatting in work notes no longer breaks when a field such as Assignment group is changed and the record is saved.
            -   Incident Assist agentic workflow options now display in Japanese when the user's language is set to Japanese.
            -   Post Incident Report generation now responds faster.
-   **Version 2.3.3 - August 2026**
    -   New: Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.2.6 - August 2026**
    -   New: Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.1.4 - August 2026 \(Zurich\)**
    -   New: Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.1.2 - July 2026 \(Zurich\)**

    No release notes.

-   **Version 1.3.1 - July 2026 \(Zurich\)**

    No release notes.

-   **Version 2.2.3 - July 2026**
    -   New: In-form ticket deflection in Service Portal — An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.
    -   Changed:
        -   Conversational Analytics dashboard \(Phase 2\) — Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
        -   Default model change — Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).
-   **Version 2.0.3 - June 2026**
    -   New: A new manager dashboard experience aggregates all incidents under a manager responsibility and organizes them into issue-based clusters. The dashboard provides high-level health metrics with drill-down into cluster-specific views, giving incident managers a consolidated and actionable view of incident health and emerging problem areas in a single interface.
    -   Changed:
        -   The Create Incident AI Agent has been migrated to a Hierarchical Agent model, resolving hallucination and rendering issues on NextWave and removing the VA dependency.
        -   The Create Incident AI Agent has been updated for full NextWave off-glide orchestrator compatibility, resolving functional deviation issues from GA readiness testing.
    -   Fixed:
        -   Platform skills not appearing in the Now Assist Skills admin panel \(even with ignoreFulfillerSubscriptionCheck enabled\) have been resolved.
        -   Display and interaction issues in the Recommended Actions panel have been resolved: misaligned loading indicator, non-functional search icon, footer-obscured filters, and incorrect cursor on non-clickable content.
    -   Removed: Suggested Steps has been deprecated and removed. Customers should transition to AI-driven recommendations in Now Assist for ITSM.
-   **Version 1.0.8 - June 2026**

    Defect fixes and plugin upgrade issue fixed.

-   **Version 1.1.4 - May 2026**

    No functional changes in this release. Version incremented to align with the platform release cadence.

-   **Version 1.0.5 - May 2026 \(Zurich, Australia\)**
    -   New:
        -   Incident Assist Agentic Workflow -New conversational experience for incident investigation. Incident Assist is capable of answering context-based queries by accessing multiple related tables \(incident, change, problem, SLA, CI, outage\) through NAP
        -   Generate summaries of Request Management records - Summarization skills for Requests, Requested Items, and Catalog tasks in both Core UI and Service Operations Workspace
        -   Activity Response Generation for Requests - Activity response generation skills for Requests and Requested Items in both Core UI and Service Operations Workspace
-   **Version 1.0.3 - April 2026**

    Foundation is the entry point into ServiceNow's AI-native ITSM experience, designed to give requesters faster answers and fulfillers a head start on every case. It delivers out-of-the-box GenAI skills and AI Agents that help your team work smarter — not replace them. On the requester side, Moveworks deflects requests at the point of ask before anything reaches the service desk, surfacing answers from 25K+ indexed knowledge articles and resolving requests through natural language across Slack, Teams, and web. On the fulfiller side, Now Assist speeds up resolution from the moment a case is created — summarizing incidents so agents start with full context, and cutting triage time with AI that suggests next steps and routes work automatically. Core capabilities include summarization, pattern recognition, categorization, and task-based assistance.


**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


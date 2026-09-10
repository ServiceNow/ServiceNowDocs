---
title: ITSM - Advanced release notes
description: Version history for the ServiceNow ITSM - Advanced application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-advanced.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# ITSM - Advanced release notes

Version history for the ServiceNow® ITSM - Advanced application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 3.3.1 - September 2026**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.

-   **Version 2.3.3 - August 2026**
    -   New:
        -   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
        -   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat — requesting coverage or leave, and asking questions like "who is on call" or "when is my next shift."
        -   Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
        -   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed a date-formatting issue in the Change Outage Assistant AI agent.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.2.5 - August 2026**
    -   New:
        -   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
        -   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat — requesting coverage or leave, and asking questions like "who is on call" or "when is my next shift."
        -   Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
        -   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed a date-formatting issue in the Change Outage Assistant AI agent.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.1.4 - August 2026 \(Zurich\)**
    -   New:
        -   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
        -   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat — requesting coverage or leave, and asking questions like "who is on call" or "when is my next shift."
        -   Employees creating a ticket in Service Portal now see an AI-generated suggestion — drawn from relevant knowledge articles and catalog items — before they submit, based on the ticket description and their hardware, location, and department.
    -   Changed:
        -   Now Assist, Moveworks, and "AI Experience" branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
        -   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
        -   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
        -   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
    -   Fixed:
        -   Fixed an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
        -   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
        -   Fixed an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
        -   Fixed a date-formatting issue in the Change Outage Assistant AI agent.
        -   Fixed an issue where the incident investigation and resolution workflow could fail with an "incident search/read service unavailable" error.
        -   Fixed an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
        -   Improved the error message shown for the Resolution Notes generation skill when the "display in product desktop" setting is turned off
        -   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete
        -   Fixed an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform
        -   Fixed an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users
        -   Fixed an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own
    -   Removed: No items removed in this release
-   **Version 2.1.2 - July 2026 \(Zurich\)**

    No release notes.

-   **Version 1.3.1 - July 2026 \(Zurich\)**

    No release notes.

-   **Version 3.1.1 - July 2026**

    No changes.

-   **Version 2.2.2 - July 2026**
    -   New: In-form ticket deflection in Service Portal — An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.
    -   Changed:
        -   Conversational Analytics dashboard \(Phase 2\) — Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
        -   Default model change — Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).
-   **Version 3.0.1 - June 2026**
    -   New: Fulfiller actions from an incident: Fulfillers can create a change request, propose a major incident, and create a problem record for an incident.
    -   Changed:
        -   Enhanced embedded Now Assist chat module card with contextual resolution actions: draft or attach a knowledge article, propose a major incident, create a change or problem, and send next steps to the requester.
        -   AI-assisted incident triage, resolution guidance, and summaries surfaced natively on the record.
-   **Version 2.0.3 - June 2026**
    -   New:
        -   The Change Quality Agent now persists quality scores in a dedicated table linked to each change record, enabling persistent reporting and downstream use. Scores include metadata such as timestamps, scoring version, and contributing factors, and are available for dashboards, audits, and risk-detection workflows across the full change lifecycle.
        -   A new manager dashboard experience aggregates all incidents under a manager responsibility and organizes them into issue-based clusters. The dashboard provides high-level health metrics with drill-down into cluster-specific views, giving incident managers a consolidated and actionable view of incident health and emerging problem areas in a single interface.
        -   IT administrators can now configure Change Management through an AI-native conversational agent in the Product Console, replacing complex admin navigation. The guided agent walks administrators through key settings including approvals, risk scoring, and workflows via natural language, making Change Management configuration accessible to customers with limited ServiceNow expertise.
    -   Changed:
        -   The Create Incident AI Agent has been migrated from VA topic-based orchestration to a Hierarchical Agent model, resolving hallucination, functional deviation, and rendering issues on the NextWave orchestrator. The agent now runs natively on NextWave without VA dependency, delivering a consistent and reliable incident creation experience for end users.
        -   The Create Incident AI Agent has been evaluated and updated for compatibility with the NextWave off-glide orchestrator. All hallucination and functional deviation issues identified during GA readiness testing have been resolved, ensuring consistent and accurate incident creation behavior across both VA-based and NextWave runtime environments.
    -   Fixed:
        -   An issue has been resolved where Platform skills were not appearing in the Now Assist Skills admin panel even when the ignoreFulfillerSubscriptionCheck system property was enabled. Administrators can now successfully view and activate Platform skills from the Now Assist admin interface.
        -   Several display and interaction issues in the Recommended Actions panel have been resolved, including a misaligned loading indicator on the search box, a non-functional full-view search icon, filter dropdowns obscured by the footer, and an incorrect hand cursor appearing on non-clickable KB article and AI action content.
    -   Removed: The Suggested Steps feature has been deprecated and removed from Now Assist for ITSM. Customers previously using Suggested Steps should transition to the AIOps LEAP recommendations available through updated Now Assist for ITSM capabilities.
-   **Version 1.0.8 - June 2026**

    Defect fixes and plugin upgrade issue fixed.

-   **Version 1.1.4 - May 2026**

    No functional changes in this release. Version incremented to align with the platform release cadence.

-   **Version 1.0.5 - May 2026 \(Zurich, Australia\)**
    -   New:
        -   Incident Assist Agentic Workflow -New conversational experience for incident investigation. Incident Assist is capable of answering context-based queries by accessing multiple related tables \(incident, change, problem, SLA, CI, outage\) through NAP
        -   Activity Response Generation for Requests - Activity response generation skills now available for Requests and Requested Items in both Core UI and Service Operations Workspace
        -   Zoom Call Diagnostics \(DEX Integration\) - Diagnose and resolve Zoom call quality issues with device-level root cause analysis and suggested resolutions
        -   Device Boot Time Monitoring - Monitor device boot time and use Now Assist to quickly diagnose startup delays with actionable resolutions
        -   DEX Issue Diagnosis Agentic Workflow - Integration of Zoom call diagnostics in the agentic workflow to enable service desk agents to diagnose Zoom call quality issues.
    -   Changed:
        -   Change Request Risk Explanation - Skill configuration moved to NASK
        -   Change Request Summarization - Skill configuration moved to NASK
-   **Version 1.0.3 - April 2026**

    Advanced moves beyond assistance into automation, designed to deflect complex requests upfront and automate what reaches the desk. AI doesn't just help — it does some of the work by understanding context, applying domain knowledge, and automating entire processes end-to-end through out-of-the-box agentic workflows. On the requester side, Moveworks handles domain-specific IT and HR requests at the point of conversation before they become tickets, deflecting nuanced requests using OOTB Specialized Assistants and guiding employees through policy-aware responses. On the fulfiller side, Now Assist starts resolving cases the moment they land so fulfillers spend less time on setup and more time closing — executing multi-step workflows autonomously using OOTB agentic workflows for IT and HR. Specialized Assistants for IT and HR are coming in H2 2026.


**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


---
title: ITSM - Prime release notes
description: Version history for the ServiceNow ITSM - Prime application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-prime.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# ITSM - Prime release notes

Version history for the ServiceNow® ITSM - Prime application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.0.9 - June 2026**

    Defect fixes and plugin upgrade issue fixed.

-   **Version 2.0.3 - June 2026**
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
    -   Removed: Suggested Steps has been deprecated and removed. Customers should transition to AIOps LEAP recommendations in Now Assist for ITSM.
-   **Version 1.1.4 - May 2026**

    No functional changes in this release. Version incremented to align with the platform release cadence.

-   **Version 1.0.6 - May 2026 \(Zurich, Australia\)**
    -   New:
        -   For L1Service Desk AI Specialist
            -   Give admins tighter control over how incidents are understood and handled by the L1 SDS. Teams can now tailor which incident fields are classified, such as category, assignment group, or configuration item, so AI-driven triage aligns more closely with their data model and operational standards. This helps improve classification relevance and downstream routing accuracy. This capability is available with the L1 SDS installed.
            -   Reduce manual rework when AI cannot fully resolve an incident. Service Desk Managers can define a fallback assignment group so unresolved incidents are automatically routed to the right team, ensuring faster handoff and fewer stalled tickets. This capability is available with the L1 SDS installed.
            -   Close the loop on stalled conversations and keep queues clean. Incidents placed On Hold while waiting for a requester’s response will now automatically resolve after 2 days of inactivity, helping teams reduce backlog noise and focus on active work. This scheduled behavior activates with the L1 SDS installed.
            -   Improve confidence in configuration item predictions. A new configurable confidence threshold allows teams to fine-tune how aggressively the AI predicts CIs, balancing automation with accuracy based on their environment and data quality. This capability is available with the L1 SDS installed.
            -   Gain clearer visibility into AI performance. Updated dashboard metrics give Service Desk Managers better insight into how the L1 Service Desk AI Specialist is performing, supporting data-driven tuning and ongoing optimization. This capability is available with the L1 SDS installed
        -   Incident Assist Agentic Workflow -New conversational experience for incident investigation. Incident Assist is capable of answering context-based queries by accessing multiple related tables \(incident, change, problem, SLA, CI, outage\) through NAP
        -   Activity Response Generation for Requests - Activity response generation skills now available for Requests and Requested Items in both Core UI and Service Operations Workspace
        -   Zoom Call Diagnostics \(DEX Integration\) - Diagnose and resolve Zoom call quality issues with device-level root cause analysis and suggested resolutions
        -   Device Boot Time Monitoring - Monitor device boot time and use Now Assist to quickly diagnose startup delays with actionable resolutions
        -   DEX Issue Diagnosis and Resolution Agentic Workflow - Integration of Zoom call diagnostics in the agentic workflow to enable service desk agents to diagnose Zoom call quality issues.
    -   Changed:
        -   Change Request Risk Explanation - Skill configuration moved to NASK
        -   Change Request Summarization - Skill configuration moved to NASK
        -   L1 SDS Avatar Update — Updated to align with design standards for a more cohesive visual presence across configuration pages and incident records.
-   **Version 1.0.4 - April 2026**

    Prime is the top tier for organizations ready to put AI to work independently, enabling requesters to build the assistants they need and fulfillers to onboard AI Specialists that own entire jobs. AI completes work end-to-end — fully independent, making decisions, and operating with role-based expertise through custom AI Specialists, Agents, and Skills. On the requester side, Moveworks provides a conversational layer purpose-built for each team and use case, with the ability to build custom Specialized Assistants tailored to any domain and connect any enterprise system with custom plugins. On the fulfiller side, Now Assist onboards AI Specialists to the service desk that handle entire jobs from start to finish — deploying AI specialists trained on your L1 workflows and building custom AI Specialists, Agents, and Skills scoped to specific L1 roles. Prime is for organizations that want fulfillers focused only on the work that truly requires human judgment.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


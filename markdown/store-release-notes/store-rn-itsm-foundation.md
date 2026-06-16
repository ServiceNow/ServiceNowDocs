---
title: ITSM - Foundation release notes
description: Version history for the ServiceNow ITSM - Foundation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-foundation.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# ITSM - Foundation release notes

Version history for the ServiceNow® ITSM - Foundation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

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


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


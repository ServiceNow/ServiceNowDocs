---
title: ITSM MCP Server release notes
description: Version history for the ServiceNow ITSM MCP Server application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-mcp-server.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# ITSM MCP Server release notes

Version history for the ServiceNow® ITSM MCP Server application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.3.2 - October 2026**
    -   New:
        -   Attach a knowledge article to an incident \(incident.attach\_kb\) — Ask your AI assistant to attach a relevant KB article to an incident, so the guidance that resolved it is captured on the record without leaving the conversation.
        -   Knowledge article details \(incident.get\_kb\_details\) — Ask for the full content of a knowledge article and get the complete context back in the conversation, not just a title and link.
        -   Find similar knowledge articles \(incident.search\_similar\_kb\) — Describe a problem in your own words and get semantically matched KB articles, without needing to know the right keywords or article numbers.
        -   Catalog item lookup \(lookup\_catalog\) — Ask your AI assistant to find the right service catalog item by describing what you need, instead of browsing the catalog yourself.
        -   Change related records \(change.relation\) — Ask what's connected to a change and get its approvals, change tasks, affected CIs and services, linked incidents, and outages in one response.
        -   Approval decisions \(task\_approval\_decision\) — Approve or reject change and request tasks directly through your AI assistant, across both change and request approvals.
    -   Changed:
        -   Requester identity in knowledge graph queries \(itsm\_knowledge\_graph\) — Knowledge graph queries now capture requester identity accurately, so questions scoped to your own incidents and requests return the right records.
        -   Faster escalations \(escalate\_incident\) — Escalating an incident no longer requires the assistant to call other tools first, so the escalation completes in fewer steps.
        -   Multi-criteria change search \(change.query\) — Search changes across several criteria in a single call instead of chaining separate queries, replacing the previous separate search and aggregate operations.
        -   Incident tools available without the itil role — Incident tools now work for identities holding only incident read or incident write roles, so requesters and read-only stakeholders can use them without elevated access.
        -   Group lookup by name — Ask your AI assistant to find an assignment group by name rather than needing its identifier.
        -   Broader AI client support for change tools — Change management tools are validated against additional clients including Claude Desktop, Codex, and Copilot.
    -   Fixed:
        -   Assigning an incident by user identifier through the Modify Incident tool no longer skips the assignment eligibility check that already applied to name-based lookups.
        -   Knowledge graph queries involving catalog items and requested items no longer intermittently return empty results for repeated identical questions.
        -   Requesting incident details no longer fails with an error for callers who hold only incident read or incident write roles and cannot read work notes.
        -   Labels and date formatting in the on-call next shift response are corrected.
        -   Work notes and comments passed to the change task update operation are now saved to the record.
-   **Version 3.2.2 - September 2026**
    -   ITSM MCP Server is built on the ServiceNow platform framework that exposes incident, change, and request management capabilities to any MCP-compatible AI client. The server is packaged as an ITSM MCP plugin with a dependency on Now Assist, providing a standardized integration surface for external AI tools.
    -   Key Design Principles
        -   Tiered rollout: Start with Incident Management \(minimum commitment\), expand to Change and Request Management
        -   Platform-native: Built on ServiceNow's platform framework, leveraging existing APIs and security model
        -   Clear server purpose: Descriptive server identity and tool descriptions so MCP clients \(e.g., Claude, CoPilot\) can effectively discover and match capabilities
        -   Now Assist for ITSM dependency: Plugin requires Now Assist capabilities, aligning with the ServiceNow AI platform strategy
        -   Existing tool reuse: Incorporate existing incident-related tools from prior work \(Now Assist skills, Moveworks Service Operations Assistant for Fulfillers\) and extend with change/request tools
    -   MCP client should be able to query any information within the context of an incident.

**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


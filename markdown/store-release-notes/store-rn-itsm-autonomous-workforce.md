---
title: ITSM Autonomous Workforce release notes
description: Version history for the ServiceNow ITSM Autonomous Workforce application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-autonomous-workforce.html
release: store
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# ITSM Autonomous Workforce release notes

Version history for the ServiceNow® ITSM Autonomous Workforce application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.3.0 - November 2026**
    -   New:
        -   Service Desk Managers get a Rate trend chart on the AI Specialist Performance dashboard plotting the durable auto-resolve and coverage rates over time, with each day's incidents a click away.
        -   Service Desk Managers get a four-step funnel on the Overview tab, from incidents assigned to eligible groups to incidents durably resolved, with drill-down and cards explaining each rate.
        -   Service Desk Managers get a chart of what the service desk did with cross-group reassignment recommendations: adopted, overridden, or awaiting a decision.
        -   AI Admins can set the portal that knowledge and catalog links open for requesters, while Service Desk Agents keep platform links in work notes.
        -   Requesters see the catalog item variables the AI Specialist submitted in the Solution Proposed comment.
    -   Changed:
        -   Requesters are asked fewer catalog questions, because the AI Specialist fills variables from the incident and the caller's details and shows what it already captured.
        -   Requesters receive catalog follow-up questions composed from instruction-mode templates, with the fixed template as a fallback.
        -   Service Desk Agents see a knowledge article in Attached Knowledge only once the incident it resolved is closed.
        -   Service Desk Managers can apply the Assignment Group and AI Specialist filters together on the All incident outcomes chart.
        -   Service Desk Managers on non-English instances see the Catalog tab, funnel, cross-group outcomes, and catalog indicators in their own language, in up to 24 locales.
    -   Fixed:
        -   Access control gaps let users or prompt-injected tool calls read records beyond their permissions through the Catalog Agent and the AI Specialist's tools, and let generative AI steps run without checking the triggering user's access.
        -   Cited knowledge articles were dropped from requester comments by a faulty access check, and were missing from work notes after a low-confidence fallback or reassignment.
        -   Saving activity notes failed when research included an uncited result from a table the AI Specialist cannot read.
        -   Knowledge and catalog links in Helpful References opened the platform view instead of the portal.
        -   Resolution notes were cut off at the Helpful References section when none of its links remained.
        -   A knowledge feedback task was created for incidents resolved with a catalog item.
        -   Incidents stayed In Progress when the Solution proposed state was mapped to Resolved or Closed.
        -   A requester comment arriving just after work started could start a duplicate run on the same incident.
        -   The closing note after a requester confirmed the fix was always written in English.
        -   Canadian French was treated as French.
        -   Notes could post with template slots unfilled. The AI Specialist now retries and hands off to a person after three failures.
        -   The AI Specialist could ignore the operating system of the computer linked to the incident.
        -   Reloading a dashboard drilldown page failed, and unused article links opened a not found page.
        -   After an upgrade to version 1.2.2, the dashboard could be missing earlier improvements and show identical first two routing journey metrics.
        -   Attachment summarization did not work out of the box, because its service URL property shipped empty.
        -   A deprecated AI agent could run instead of the AI Specialist agent after an upgrade.
    -   Removed:
        -   The Routing journey count cards are gone from the Detailed view, replaced by the Overview funnel.
        -   The unused Research depth setting is gone.
        -   The Pre resolution condition setting is gone, and incidents are no longer checked against it.
-   **Version 1.2.1 - October 2026**
    -   The L1 IT Service Desk AI specialist will autonomously resolve high-volume, routine issues by triaging the incident, identifying the issue, researching the resolution, and resolving it end-to-end. It runs inside ServiceNow workflows you already operate, follows the policies and guardrails you set, and reassigns the moment something falls outside what it's cleared to handle.
    -   Getting Started:
        -   Implement with a ServiceNow expert. Please reach out to your account representative to plan your implementation with a ServiceNow professional implementation expert. This will ensure proper configuration of triage, knowledge sources, confidence thresholds, and governance to make autonomous resolution safe and effective in your environment.
        -   Identify the right candidates first. Before deployment, use the to determine which clusters are primed for autonomous resolution. It assesses your environment and pinpoints where the AI Specialist will perform well based on your KB and catalog coverage, so you start with high-confidence use cases and expand from there.

**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


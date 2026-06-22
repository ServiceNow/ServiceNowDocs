---
title: Ask questions about an incident by using the Now Assist panel
description: Quickly obtain common incident related information conversationally within the incident record by asking questions in the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-incident-assist.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Ask questions about an incident by using the Now Assist panel

Quickly obtain common incident related information conversationally within the incident record by asking questions in the Now Assist panel.

## Before you begin

Role required: itil

## About this task

**Important:** Starting with the Australia Patch 2, the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.

\[DEPRECATED\] Incident assist topics in the Now Assist panel include:

-   Caller's assets
    -   A caller must be associated with the incident to retrieve caller's assets.
    -   Incident number must be provided, unless triggered from the incident record.
-   Caller's recent incidents \(within the past 7 days\)
    -   A caller must be associated with the incident to retrieve caller's recent incidents.
    -   Incident number must be provided, unless triggered from the incident record.
-   On-call experts from support groups
    -   Ability to search on-call experts that are in any support group.
    -   Group members are configured in **On-Call Scheduling** &gt; **On-Call Schedules**.
-   Similar resolved incidents
    -   Similar incidents must be resolved or closed.
    -   Incident number must be provided, unless triggered from the incident record.

You can ask questions about an incident by using the Now Assist panel in Core UI and Service Operations Workspace for ITSM.

## Procedure

1.  In Core UI or Service Operations Workspace for ITSM, open an incident that is assigned to you.

2.  From the header menu, select the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Now assist icon. to open the Now Assist panel.

    \[Omitted image "now-assist-itsm-inc-assist-pnl.png"\] Alt text: Incident assist panel in Service Operations Workspace.

3.  In the Now Assist panel, either type in a question related to an incident assist topic, or select **Answer questions about an incident** and select an \[DEPRECATED\] Incident assist topic to ask about.

    **Note:** Incident assist uses index sources for which incidents, problems, and change requests are indexed. Similar resolved incidents are retrieved by comparing an incoming incident with past resolved incidents for smarter resolution. Similar past active incidents are displayed in the Now Assist panel and also in the Incident form via related search. For information on indexed sources, see [Managing indexed sources from the AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ais-managing-indexed-source.md).

    \[Omitted image "now-assist-itsm-inc-assist-pan.png"\] Alt text: Incident assist panel in Service Operations Workspace in an incident.

    Information requested about the incident is shown.

    \[Omitted image "now-assist-itsm-inc-assist-tpc.png"\] Alt text: Incident assist panel topic in Service Operations Workspace.



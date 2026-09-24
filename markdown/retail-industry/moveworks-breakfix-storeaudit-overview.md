---
title: ServiceNow Otto for Break-Fix and Store Audit overview
description: The ServiceNow Otto conversational interface connects to Break-Fix Case Management and Store Audit Plans workflows. Store staff can submit, troubleshoot, and track cases without accessing the RSM portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/moveworks-breakfix-storeaudit-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# ServiceNow Otto for Break-Fix and Store Audit overview

The ServiceNow Otto conversational interface connects to Break-Fix Case Management and Store Audit Plans workflows. Store staff can submit, troubleshoot, and track cases without accessing the RSM portal.

## How ServiceNow Otto relates to Break-Fix and Store Audit

-   **ServiceNow Otto as frontend interface**

    ServiceNow Otto is an alternative conversational UI to the RSM portal for Break-Fix and Store Audit case operations. All data flows to and from the existing ServiceNow RSM backend \(no new system required\).

-   **Break-Fix integration**

    Store staff submit equipment failure cases via ServiceNow Otto chat \(natural language\) instead of RSM portal forms. ServiceNow Otto automatically extracts metadata \(store ID, equipment type, severity\) and creates RSM break-fix cases with correct categorization. HQ support receives cases with full context in RSM workspace.

-   **Store Audit integration**

    Store staff track Store Audit plan progress via ServiceNow Otto chat. After a plan is published and audit cases auto-generated in RSM, auditors can ask ServiceNow Otto about plan status, completion progress, and Pass/Fail results without logging into the RSM portal.


## Break-Fix and Store Audit: workflows: portal vs ServiceNow Otto

|Workflow|RSM Portal \(Original\)|ServiceNow Otto|
|--------|-----------------------|---------------|
|Break-Fix Case Creation|Navigate portal → Select from dropdowns → Fill structured form → Submit|Open ServiceNow Otto → Describe issue → Answer clarifying questions → ServiceNow Otto creates case|
|Break-Fix Troubleshooting|Search KB separately, then submit case|ServiceNow Otto surfaces KB steps in chat before case creation|
|Break-Fix Tracking|Log in to the portal, click each case individually|Ask ServiceNow Otto "Show my cases" → Consolidated view + actions in chat|
|Store Audit Tracking|Log in to the portal, navigate to the Track plan tab|Ask ServiceNow Otto about plan progress → View Pass/Fail summary in chat|

## Multi-channel deployment

Both Break-Fix and Store Audit workflows are accessible through the following channels:

-   **ServiceNow Otto web portal**

    Standalone access

-   **Microsoft Teams**

    Organizational chat

-   **Slack**

    Organizational chat

-   **Embedded retail portal**

    Chatbot widget within the familiar portal


Store staff use their preferred channel for all case operations.

## Backend systems unchanged

-   **Break-Fix**

    Cases are still created in ServiceNow RSM, triaged by HQ support in RSM workspace, using the same workflows and business logic. Only the submission interface changes from the portal form to the ServiceNow Otto chat.

-   **Store Audit**

    Plans are still created in RSM, published to auto-generate cases, and auditors still complete tasks on mobile. ServiceNow Otto adds an optional tracking interface for status checks.

-   **Data sync**

    ServiceNow Otto reads from and writes to RSM via the NOW MCP server. All data resides in ServiceNow \(no replication\).


## Integrated benefits

-   **Unified experience**

    Store staff use a single conversational interface for Break-Fix case operations and Store Audit tracking. No need to toggle between the portal and ServiceNow Otto.

-   **Reduced portal login**

    Staff no longer need RSM portal login for routine operations \(submit cases, check status, add comments, view audit progress\).

-   **Natural language**

    Describe equipment issues naturally \("printer won't print"\) and audit queries \("what's my audit progress?"\) instead of using structured forms.

-   **Contextual intelligence**

    ServiceNow Otto surfaces troubleshooting steps for Break-Fix before escalation, reducing unnecessary cases and floor downtime.

-   **Faster triage**

    HQ support receives Break-Fix cases with proper categorization and full context .


## What stays the same

-   Break-Fix case category, priority, and resolution workflows remain identical
-   HQ support triage, dispatch, and resolution process unchanged
-   Store Audit plan creation, task definition, and execution unchanged
-   Mobile app for auditors executing Store Audit tasks unchanged
-   ServiceNow RSM as system of record for all data

## Related topics

-   [Submit and track Break-Fix cases via ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-case-operations.md)
-   [Track Store Audit progress via ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-storeaudit-tracking.md)
-   [ServiceNow Otto integration technical reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-reference.md)
-   [Break-Fix Case Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/breakfix-overview.md)
-   [Store Audit Plans overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-store-audit-overview.md)

-   **[Submit and track break-fix cases via Moveworks Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-case-operations.md)**  
Use Moveworks as an alternative to the RSM portal to submit, troubleshoot, and track break-fix cases using natural language in chat.
-   **[Track Store Audit Progress Using Moveworks Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-storeaudit-tracking.md)**  
After Store Audit plans are published and audit cases are created in RSM, auditors can ask Moveworks about plan progress, task completion status, and Pass/Fail results without accessing the RSM portal.
-   **[Configure the ServiceNow Otto webhook connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_configure-moveworks-webhook.md)**  
Configure the otto\_webhook Connection &amp; Credential Alias so ServiceNow can deliver webhook events to the ServiceNow Otto listener.
-   **[ServiceNow Otto integration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_moveworks-integration-overview.md)**  
The ServiceNow Otto integration sends outbound webhook events to the ServiceNow Otto listener when a Break-Fix case changes to a key state. This enables ServiceNow Otto to proactively notify store associates on their desktop messaging platform.
-   **[Components Moveworks Integration for Break-Fix and Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/moveworks-breakfix-storeaudit-reference.md)**  
Technical details on data flow, integration points, API usage, and supported operations for Moveworks with Break-Fix Case Management and Store Audit Plans.
-   **[Components for ServiceNow Otto integration for break-fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/r_moveworks-integration-reference.md)**  
Technical reference for webhook events, authentication types, platform artifacts, and troubleshooting.


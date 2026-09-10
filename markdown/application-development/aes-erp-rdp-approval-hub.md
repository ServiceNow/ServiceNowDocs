---
title: Approval Hub Rapid Deployment Pack
description: Approval Hub is the centralized interface where requests from MDM Orchestrator and journal entries converge for business approval. Approvers have one view of all pending actions, regardless of the originating rapid deployment pack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-approval-hub.html
release: australia
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 1
keywords: [app, engine, sap, erp, rapid, deployment, pack, approve, approval, agentic, manufactur, operation, template, templatized, business, workflow]
breadcrumb: [Explore, App Engine ERP Rapid Deployment Packs, Building low-code applications, Developing your application, Building applications]
---

# Approval Hub Rapid Deployment Pack

Approval Hub is the centralized interface where requests from MDM Orchestrator and journal entries converge for business approval. Approvers have one view of all pending actions, regardless of the originating rapid deployment pack.

## Approval Hub role in the workflow

Approval Hub doesn't have its own request workflow. Every request created in MDM Orchestrator, such as a new customer or a bulk upload, and every journal entry passes through Approval Hub after enrichment and governance review.

## Why Approval Hub matters

In traditional systems, approvers move between multiple applications and approval queues and lose visibility into what is pending, stalled, or urgent. Approval Hub addresses these issues in the following ways:

-   Consolidating all pending requests in a single interface.
-   Displaying request metadata, such as domain, type, age, and priority, so approvers can quickly identify what needs action.
-   Providing approve and reject controls without leaving the interface.
-   Integrating a virtual agent to help prioritize work and identify requests that breach their service level agreement \(SLA\).

## Approval Hub features

The Approval Hub interface includes:

-   A dashboard showing pending requests grouped by domain, such as MDM and manual journal entry, with counts and status breakdowns.
-   SLA breach indicators and in-progress task summaries.
-   A consolidated list of all requests awaiting approval, sortable by domain, type, and priority.
-   Virtual Agent integration to query pending items, identify stalled requests, and display prioritization suggestions.
-   Inline approve and reject controls in the Virtual Agent conversation, so approvers can act without opening the record.

\[Omitted image "aes-erp-rdp-approval-hub.png"\] Alt text: Approval Hub with MDM Dashboard open showing charts and graphs of approval information.

**Parent Topic:**[Exploring App Engine ERP Rapid Deployment Packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-explore.md)


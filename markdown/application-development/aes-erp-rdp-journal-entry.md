---
title: Journal Entry Portal rapid deployment pack
description: The Journal Entry Portal App Engine for ERP rapid deployment pack helps you create, validate, and submit journal entries for month-end account closing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-journal-entry.html
release: australia
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, journal, entry]
breadcrumb: [Explore, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Journal Entry Portal rapid deployment pack

The Journal Entry Portal App Engine for ERP rapid deployment pack helps you create, validate, and submit journal entries for month-end account closing.

## Journal Entry Portal capabilities

The Journal Entry Portal provides an interface for creating, reviewing, and submitting journal entries. Use the portal to manage journal entry workflows.

-   Period-end journal entries: Finance teams use the portal to create and submit closing entries at the end of an accounting period, with built-in review steps to verify accuracy before ERP submission.
-   Adjustment entries: Users submit corrective journal entries to adjust previously posted transactions, with the portal enforcing required documentation and approvals.

**Note:** To use the Journal Entry Portal, you must have access to create journal entries.

## Key benefits

The Journal Entry Portal provides the following benefits:

-   Centralizes journal entry creation and review in a single interface, reducing navigation overhead for finance users.
-   Supports structured submission workflows that enforce data completeness before entries reach the ERP system.
-   Integrates with the App Engine for ERP rapid deployment packs framework to align journal entry handling with other ERP deployment workflows.

\[Omitted image "aes-erp-rdp-journal-entry.png"\] Alt text: Journal entry task dashboard showing charts and graphs with task metrics.

## Journal Entry Portal workflow

The Journal Entry Portal operates as the user-facing layer of the journal entry process within the ERP rapid deployment framework:

-   A user accesses the Journal Entry Portal and initiates a new journal entry record.
-   The user completes the required fields and attaches any supporting documentation.
-   The portal validates the entry data and routes it through the configured approval or review workflow.
-   On approval, the journal entry is submitted to the connected ERP system for processing.

**Parent Topic:**[Exploring App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-explore.md)


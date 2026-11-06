---
title: ServiceNow Otto for Software Asset Management \(SAM\) release notes
description: The ServiceNow Otto for Software Asset Management \(SAM\) application brings agentic AI to Software Asset Management. See the following sections for release notes by version.This release adds AI-powered analysis of software spend transactions and software spend detection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/servicenow-otto-sam-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for Software Asset Management \(SAM\) release notes

The ServiceNow Otto for Software Asset Management \(SAM\) application brings agentic AI to Software Asset Management. See the following sections for release notes by version.

## About ServiceNow Otto for Software Asset Management \(SAM\)

-   Automatically match software entitlements to installations and usage data, and flag over-deployment and unused licenses so asset managers aren’t reconciling spreadsheets by hand.
-   Route license requests, installs, and upgrades to the right approvers and fulfillment steps, cutting response and provisioning time for employees.
-   Link publishers, contracts, entitlements, and install records into one view, then use AI analysis to flag renewal risks, shelfware, and reclaim opportunities.

See  for more information.

**Important:** For Now LLM Service model updates for each release, see .

## Activation and other requirements

-   **Activation information**

    Install ServiceNow Otto for Software Asset Management \(SAM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/it-asset-management-rn-landing.md)

## Version 11.0.0

This release adds AI-powered analysis of software spend transactions and software spend detection.

### What's new

-   **Analyze software spend transactions with AI in the Software Asset Workspace**

    Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.

-   **Resolve entitlement import errors by using ServiceNow Otto for Software Asset Management \(SAM\)**

    Resolve unmatched publisher and product data that blocks bulk entitlement imports in the Software Asset Workspace using the 5 new AI-powered skills that normalize publisher and product values:

    -   Publisher Search Tags Generation
    -   Product Search Tags Generation
    -   Publisher Match Review
    -   Product Match Review
    -   Product Resolution

### What's changed

-   **Software Spend Detection Core UI**

    The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.



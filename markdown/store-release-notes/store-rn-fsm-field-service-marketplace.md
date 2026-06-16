---
title: Field Service Marketplace release notes
description: Version history for the ServiceNow Field Service Marketplace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-field-service-marketplace.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Field Service Marketplace release notes

Version history for the ServiceNow® Field Service Marketplace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.0.3 - April 2026**
    -   Fixed:
        -   System properties shipped with the FSM Marketplace app have been updated to require the marketplace\_admin role for read and write access. With this change, only users with the marketplace\_adminrole can read and modify these system property values, while system admin and maintenance users retain access as per standard platform behavior.
        -   Corrected Work Order Task state transitions for work orders that are created in bulk through data loader with auto-push configured. Work Order Task state now transitions from Pending Dispatch to Pushed to Marketplace.
-   **Version 30.0.1 - March 2026**
    -   Field Service Marketplace gives dispatchers and contractor managers a structured way to source, evaluate, and assign work to external providers — without the back-and-forth that slows response times.
    -   Internal teams post work opportunities with defined criteria, contractors receive instant notifications and submit bids directly in the platform, and managers can compare responses and assign work in a single workflow. Bid visibility is controlled, timelines are tracked, and every step from task posting to award is documented.
    -   The result: faster contractor sourcing, fewer coordination gaps, and a clear audit trail so external work gets done with the same discipline as work handled internally.

**Parent Topic:**[ServiceNow Store - Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)


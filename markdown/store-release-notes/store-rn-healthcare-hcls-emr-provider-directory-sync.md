---
title: EMR Provider Directory Sync release notes
description: Version history for the ServiceNow EMR Provider Directory Sync application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-hcls-emr-provider-directory-sync.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# EMR Provider Directory Sync release notes

Version history for the ServiceNow® EMR Provider Directory Sync application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.0 - July 2026**
    -   Healthcare IT and clinical operations teams rely on ServiceNow to route support requests and coordinate care team work — but that only works if location, organization, and practitioner data stays current with the EMR. Manually reconciling provider directory changes across systems is slow, and stale data leads to cases routed to the wrong unit, department, or practitioner.
    -   EMR Provider Directory Sync connects to your EMR's FHIR-based provider directory and automatically imports Locations, Organizations, Practitioners, and PractitionerRoles into ServiceNow. Locations import with normalized addresses and parent/child hierarchy so facility structure matches your EMR. Organizations import with paired Business Locations to support Customer Service Management case routing. Practitioners and their roles sync into ServiceNow users and care team assignments, so practitioners are available for care team membership and case routing without manual setup.
    -   A configurable scheduled flow orchestrates the sync end-to-end, with delta sync so only changed records are processed after the initial load, and a dedicated sync log gives administrators visibility into every run for troubleshooting and audit.

**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)


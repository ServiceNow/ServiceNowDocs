---
title: Impact Value Management - CSM release notes
description: Version history for the Impact Value Management - CSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-impact-value-mgmt.html
release: store
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Impact Value Management - CSM release notes

Version history for the Impact Value Management - CSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - February 2025**
    -   Fixed: Metrics involving active user counts \(or other queries that rely on a change of state\) are now excluded from historical data collection for periods exceeding one month. This change ensures data accuracy, as such metrics cannot be reliably captured using point-in-time queries.
    -   Fixed: Date-based filter conditions are now applied directly to source indicators in CSM products. This update improves system stability, reduces errors, and improves analytics performance for users with large datasets. Existing users will experience no disruption.
    -   Compatible: Washington DC, Xanadu, Yokohama
-   **Version 2.0.0 - December 2024**
    -   The Impact Value Management Data Collection Dashboard for Customer Service Management \(CSM\) gives Impact customers an automated solution for gathering standard ServiceNow value metrics, enhancing their value journey.
    -   Sharing Metrics with ServiceNow ServiceNow's integration gathers value metrics from customer instances on a monthly basis. Please note that integration with ServiceNow's centralized Impact instance is not available for Regulated customers \(Standalone and SSP\) and may necessitate granting user access for instances using the ServiceNow SNC security plugin. The Data Collection Apps will remain functional even if the integration with ServiceNow is unavailable; however, Metrics Data will need to be transferred manually in such cases.


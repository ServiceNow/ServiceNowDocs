---
title: Impact Value Management - CSM release notes
description: Version history for the Impact Value Management - CSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-impact-value-mgmt.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Customer Service Management version history release notes, ServiceNow Store version history release notes]
---

# Impact Value Management - CSM release notes

Version history for the Impact Value Management - CSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.4 - October 2026**
    -   This release upgrades the Data Collection App for Customer Service Management \(CSM\) with an expanded set of value-measurement metrics.
    -   All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.
    -   For the complete list of new metrics, please refer to the Supporting Document.
    -   Enhanced Metrics:
        -   Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.
        -   Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.
        -   To make Enhanced Metric data available on the Impact Delivery Instance, customers must:
            -   Install the Impact In-Platform App, and
            -   Enable ServiceBridge.
            -   Configure the Estimated data definition against the enhanced metrics
        -   All the steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.
        -   Compatible: Zurich, Australia, Brazil
-   **Version 2.2.0 - September 2026**

    Compatible: Zurich, Australia, Brazil

-   **Version 2.1.0 - February 2025**
    -   Fixed: Metrics involving active user counts \(or other queries that rely on a change of state\) are now excluded from historical data collection for periods exceeding one month. This change ensures data accuracy, as such metrics cannot be reliably captured using point-in-time queries.
    -   Fixed: Date-based filter conditions are now applied directly to source indicators in CSM products. This update improves system stability, reduces errors, and improves analytics performance for users with large datasets. Existing users will experience no disruption.
    -   Compatible: Washington DC, Xanadu, Yokohama
-   **Version 2.0.0 - December 2024**
    -   The Impact Value Management Data Collection Dashboard for Customer Service Management \(CSM\) gives Impact customers an automated solution for gathering standard ServiceNow value metrics, enhancing their value journey.
    -   Sharing Metrics with ServiceNow ServiceNow's integration gathers value metrics from customer instances on a monthly basis. Please note that integration with ServiceNow's centralized Impact instance is not available for Regulated customers \(Standalone and SSP\) and may necessitate granting user access for instances using the ServiceNow SNC security plugin. The Data Collection Apps will remain functional even if the integration with ServiceNow is unavailable; however, Metrics Data will need to be transferred manually in such cases.


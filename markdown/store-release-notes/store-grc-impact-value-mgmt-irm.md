---
title: Impact Value Management - IRM release notes
description: Version history for the Impact Value Management - IRM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-impact-value-mgmt-irm.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Impact Value Management - IRM release notes

Version history for the Impact Value Management - IRM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.3 - December 2025**

    Compatible: Yokohama, Zurich.

-   **Version 2.1.0 - February 2025**
    -   Fixed: Metrics involving active user counts \(or other queries that rely on a change of state\) are now excluded from historical data collection for periods exceeding one month. This change ensures data accuracy, as such metrics cannot be reliably captured using point-in-time queries.
    -   Compatible: Washington DC, Xanadu, Yokohama
-   **Version 2.0.0 - December 2024**
    -   The Impact Value Management Data Collection Dashboard for Integrated Risk Management \(IRM\) gives Impact customers an automated solution for gathering standard ServiceNow value metrics, enhancing their value journey.
    -   Sharing Metrics with ServiceNow ServiceNow's integration gathers value metrics from customer instances on a monthly basis. Please note that integration with ServiceNow's centralized Impact instance is not available for Regulated customers \(Standalone and SSP\) and may necessitate granting user access for instances using the ServiceNow SNC security plugin. The Data Collection Apps will remain functional even if the integration with ServiceNow is unavailable; however, Metrics Data will need to be transferred manually in such cases.

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)


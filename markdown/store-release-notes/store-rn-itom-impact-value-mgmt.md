---
title: Impact Value Management - ITOM release notes
description: Version history for the Impact Value Management - ITOM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-impact-value-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Impact Value Management - ITOM release notes

Version history for the Impact Value Management - ITOM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.1 - December 2025**
    -   The ITOM Data Definition "Impact VM - ITOM - \# of Unplanned Outages This Month" in ITOM Performance Analytics Data Collection Apps was using an incorrect filter, which led to non-outage events \(such as service degradations\) being included in the calculation. The definition has now been updated to apply the correct outage criteria, ensuring that only valid outage events are counted. This fix improves the accuracy and reliability of the reported performance metrics.
    -   Compatible: Yokohama, Zurich
-   **Version 2.1.0 - February 2025**
    -   Fixed: Metrics involving active user counts \(or other queries that rely on a change of state\) are now excluded from historical data collection for periods exceeding one month. This change ensures data accuracy, as such metrics cannot be reliably captured using point-in-time queries.
    -   Compatible: Washington DC, Xanadu, Yokohama
-   **Version 2.0.0 - December 2024**
    -   The Impact Value Management Data Collection Dashboard for ITOM gives Impact customers an automated solution for gathering standard ServiceNow value metrics, enhancing their value journey.
    -   Sharing Metrics with ServiceNow ServiceNow's integration gathers value metrics from customer instances on a monthly basis. Please note that integration with ServiceNow's centralized Impact instance is not available for Regulated customers \(Standalone and SSP\) and may necessitate granting user access for instances using the ServiceNow SNC security plugin. The Data Collection Apps will remain functional even if the integration with ServiceNow is unavailable; however, Metrics Data will need to be transferred manually in such cases.


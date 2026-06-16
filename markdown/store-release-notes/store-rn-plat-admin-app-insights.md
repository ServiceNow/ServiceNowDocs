---
title: Application Insights release notes
description: Version history for the Application Insights application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-admin-app-insights.html
release: store
topic_type: reference
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Admin release notes, ServiceNow Store release notes]
---

# Application Insights release notes

Version history for the Application Insights application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.1 - August 2023**
    -   New:
        -   API Metrics - tabular view of API resources \(endpoints\) with respective performance metrics
        -   API Method:
            -   GET
            -   POST
            -   PUT
            -   PATCH
            -   DELETE
        -   Response time \(ms\)
        -   Requests per minute
        -   Payload size \(bytes\)
        -   Failure rate %
        -   Response time visualization for each resource
        -   Scatter plot time series showing API requests over time
        -   95th percentile, median, and 1-day moving average
    -   Fixed:
        -   Metric threshold trigger flow error on compilation step
        -   Table view on visualization not updating when day filter is applied
        -   Table view sorting \(asc and desc\) not working appropriately due to fields being of type 'string'
-   **Version 2.2.1 - February 2023**
    -   New:
        -   Tabular view of event queue metrics for individual event queues
            -   Processed events
            -   Unprocessed events
            -   Average processing duration
            -   Logged events
            -   Queued events
    -   Fixed:
        -   The "Retrieve metric logs" Flow Action from a Flow created via Application Insights error
        -   Error loading ECC QUEUE tab caused by empty ECC queue output and/or input graph
        -   Updated security permissions for REST APIs to require sn\_app\_insights.admin
-   **Version 2.1.3 - July 2022**
    -   Fixed:
        -   When one of the semphores that is tracked that has a different name than expected, a null pointer exception occurs
        -   Diagnostic events not displaying consistently
-   **Version 2.1.2 - February 2022**
    -   New:
        -   Add database throughput metric graph
        -   Overview graphs now have day range picker
        -   Overview graphs now have diagnostic events
        -   NOW icon in top left redirects to the platform
        -   For related slow scripts/queries and scripts, show the order in which they appear in the stack trace
    -   Changed: When MetricBase error occurs, show message specific to the issue to user instead of a general error message
    -   Fixed: User with sn\_app\_insights.admin role cannot create a new threshold, gets error message: There was a problem copying the template flow
-   **Version 2.0.3 - November 2021**

    Fixed: Intermittent 500/503 errors on App Insights UI


**Parent Topic:**[ServiceNow Store - Admin release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-admin.md)


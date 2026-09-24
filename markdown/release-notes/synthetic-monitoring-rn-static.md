---
title: Synthetic Monitoring release notes
description: The ServiceNow Synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring was enhanced and updated in the Brazil release.The ServiceNow Synthetic monitoring application was enhanced and updated in the Brazil release to support monitoring endpoint for multiple services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/synthetic-monitoring-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ITOM AIOps release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Synthetic Monitoring release notes

The ServiceNow® Synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring was enhanced and updated in the Brazil release.

## About Synthetic monitoring

-   Get real-time notifications for outages before they impact users.
-   Visualize synthetic test results.
-   Update monitors to match your business needs.

See [Exploring synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exploring-synthetic-monitoring.md) for more information.

## Activation and other requirements

**Note:** Synthetic monitoring is available in the ServiceNow Store.

**Parent Topic:**[ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-aiops-rn.md)

## Version 1.9.2

The ServiceNow® Synthetic monitoring application was enhanced and updated in the Brazil release to support monitoring endpoint for multiple services.

### Synthetic monitoring highlights for the Brazil release

-   Tag HTTP endpoints and discovered APIs to multiple application services to reduce duplicate checks and preserve CMDB relationships.
-   Prevent the ECC queue from growing unbounded with a new scheduled cleanup job for Synthetic Monitoring messages.

See [Exploring synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exploring-synthetic-monitoring.md) for more information.

**Important:** Synthetic monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

### New in the Brazil release

-   **[Multi-service tagging for endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/multi-service-monitoring.md)**

    Tag a single HTTP endpoint or discovered API to multiple application services. One check represents every team that depends on that shared endpoint. The underlying CMDB relationships between the endpoint and each application service are preserved rather than replaced when a new service is added.


### UI changes

-   **[Create a synthetic monitor for a discovered API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-synthetic-monitor-for-discovered-api.md)Related services**

    HTTP endpoint and discovered API forms now display a Related services list that shows every application service tagged to the endpoint. This list is read-only and removes duplicate entries so teams can see which other services share the same endpoint.


### Changed in the Brazil release

-   **[ECC queue auto purge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/ecc-queue-auto-purge.md)**

    Prevent the ECC queue from growing unbounded. A new scheduled job removes old Synthetic Monitoring messages from the ECC queue and flags stuck or orphaned messages so that stale entries aren't mistaken for pending work. To enable this cleanup, grant **Can Delete** application access on the ECC Queue \[ecc\_queue\] table.

-   **[Monitor result accuracy for HTTP error responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/view-a-monitor-s-test-results.md)**

    MID Server-executed checks now correctly show a Responded status when the endpoint returns an HTTP error status code, such as 401 or 503. Previously, these checks could incorrectly show no response despite a valid error being returned.


### Additional requirements

-   API Insights
-   CMDB CI Class Models
-   Can Delete application access on the ECC Queue \[ecc\_queue\] table, required to enable the ECC queue auto-purge cleanup job.


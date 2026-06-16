---
title: Service Graph Connector for Jamf release notes
description: Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Jamf integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-jamf.html
release: store
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Jamf release notes

Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Jamf integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.14.4 - September 2025**

    Fixed: Fixed the discovery source in samp\_sw\_usage for SG-JAMF.

-   **Version 2.14.2 - June 2025**
    -   Fixed:
        -   Fixed transforms for printer data.
        -   The Software Usage data source now reads the last run datetime correctly.
-   **Version 2.14.1 - February 2025**
    -   New:
        -   Automated the flow for verifying the Jamf API version for the mobile use case.
        -   Implemented delta \(incremental\) pull for computers and mobile devices.
    -   Fixed:
        -   Fixed the getSoftwareUsageDataSourceId error for the Software Usage data source.
        -   Fixed the 401 error for the Software Usage data source when OAuth is set up.
        -   Fixed the OAuth token retrieval flow when it is set up for the first time.
        -   Fixed the creation and removal of OS-related records added to the cmdb\_sam\_sw\_install table.
-   **Version 2.13.0 - November 2024**

    New: Added support for client credential authentication.

-   **Version 2.12.2 - July 2024**

    Fixed: Updating Auth API from '/uapi/auth/tokens' to '/api/v1/auth/token' for JAMF Pro 10.35 or higher.

-   **Version 2.12.1 - March 2024**
    -   Fixed:
        -   Business rule "Jamf Connection Removal" is now triggered in the Service Graph Connector for Jamf application scope.
        -   Fixed cleansed\_last\_inventory\_update\_utc mapping in Extract Transform Load \(ETL\) entities.
        -   Fixed creation of the incorrect usage record by the JAMFSoftwareUsagesUtil script include, which is used by the SG-Jamf Software Usage data source to obtain software usage details.
-   **Version 2.12.0 - July 2023**
    -   New: Support for authorization with bearer tokens when using the Jamf Pro 10.35 or higher version
    -   Fixed: No longer need to refresh the token for the SG-Jamf Computers data source when resolving the 401 unauthorized error
-   **Version 2.11.0 - December 2022**
    -   New:
        -   Support Mobile software removals.
        -   Mapped 'Last Inventory Update' to 'Most recent discovery' for Handheld device CI.
    -   Fixed: Fixed the connection issue when updating the connector from 2.7.1 to 2.9
-   **Version 2.10.0 - July 2022**
    -   Fixed:
        -   Software usages should use sys\_properties "glide.discovery.assigned\_user\_match\_field" to match the user.
        -   Manufacturer is populating correctly for computers.
        -   Fixed the "SG-Jamf Remove Software" data source API dependency.
-   **Version 2.9.0 - June 2022**

    Fixed: Resolved a problem with MID server support.

-   **Version 2.8.0 - May 2022**

    Change: Support the Classic API to accept Bearer Token authentication.

-   **Version 2.7.1 - February 2022**
    -   Fixed:
        -   Ability to handle large payloads from mobile devices.
        -   When Jamf Pro API is used, the username and email\_address information is at the correct level in the data source.
        -   Prevent partial and incomplete payloads when imported data is missing required attributes.
-   **Version 2.7.0 - October 2021**

    New: Added the ability to filter out "personal" apps when discovering software inventory on mobile devices. By default, the integration only imports data for apps managed by the corporation.

-   **Version 2.6.3 - September 2021**
    -   New:
        -   Support for Extended attributes.
        -   Support for multiple instances of Jamf. Included use iTunes Search API to improve the fidelity of publisher and software title information.
        -   Changed last\_discovered field to reflect the date Jamf last scanned the asset.
    -   Changed:
        -   The licensing requirement for this plugin has expanded to include both IT Asset Management as well the existing IT Operations Managment visibility and discovery.
        -   This will allow customers with IT Asset Management to use this application without requiring an IT Operations Management SKU.
        -   Software usage information is now gathered from the Jamf attribute "Foreground" rather than "Open".
    -   Removed: Delta detection on ingestion has been deprecated.
-   **Version 2.5.0 - April 2021**
    -   New:
        -   Added optional support for Jamf Pro API which provides higher data import throughput for Computer data. The improved performance is the result of pagination support in the Jamf Pro API.
        -   Jamf Classic API continues to be supported and remains the default configuration.
-   **Version 2.4.0 - February 2021**

    Fixed: Support for multiple instances \(endpoints\) of Jamf now works as documented.

-   **Version 2.3.2 - January 2021**
    -   New: Support for software usage tracking to enable Software Asset Management use cases.
    -   Changed:
        -   Improved MID Server configuration.
        -   Use of IntegrationHub across all APIs.
-   **Version 2.2.0 - October 2020**
    -   New:
        -   Added support for iOS device discovery \(hardware and applications\)
        -   Added support for detection of removed software for computers only that enables Software Asset Management Pro to reclaim software licenses
-   **Version 2.1.1 - September 2020**

    This is a CMDB-certified integration with Jamf. Use the integration to sync your computer inventory \(primarily MacOS hardware\) and software packages \(installed and in-use\) to the ServiceNow Configuration Management Database \(CMDB\). This integration allows for periodic data synchronization using Jamf Classic API. The data is mapped and stored in the appropriate classes in the CMDB data model so that it can be used in various Service Management and Asset Management applications.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)


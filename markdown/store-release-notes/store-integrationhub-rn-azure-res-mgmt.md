---
title: Microsoft Azure Resource Management spoke release notes
description: Version history for the Integration Hub Microsoft Azure Resource Management spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-res-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Resource Management spoke release notes

Version history for the Integration Hub Microsoft Azure Resource Management spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 2.0.0 - November 2024**
    -   New:
        -   New connection &amp; credential alias: Microsoft Azure Resource Management \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   Authentication Template for easy spoke setup
        -   New actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Metadata Retrieval
                -   Look up Databases \(look\_up\_databases\)
                -   Look up Elastic Pools \(look\_up\_elastic\_pools\)
                -   Look up Locations \(look\_up\_locations\)
                -   Look up Operational Status of Resource \(look\_up\_operational\_status\_of\_resource\)
                -   Look up Resource Groups \(look\_up\_resource\_groups\)
                -   Look up SQL Servers \(look\_up\_sql\_servers\)
    -   Removed:
        -   Deprecated old credential alias Azure\_Resource\_Mangement \(sn\_azure\_rm\_spoke.Azure\_Resource\_Mangement\)
        -   Deprecated Actions making use of old credential alias:
            -   Get Databases \(get\_databases\_\_dynamic\)
            -   Get Elasticpools \(get\_elasticpools\_\_dynamic\)
            -   Get Location \(get\_location\)
            -   Get Operational Status of Resource \(get\_operational\_status\_of\_resource\)
            -   Get Resources \(get\_resources\_\_dynamic\)
            -   Get SQL Servers \(get\_servers\_\_dynamic\)
-   **Version 1.1.2 - September 2023**

    Fixed: The license requirements.

-   **Version 1.1.1 - April 2023**

    Fixed: Improve installation performance of spoke.

-   **Version 1.1.0 - October 2021**

    Fixed: Security bug.

-   **Version 1.0.5 - July 2020**

    Patch release of the Azure Resource Management spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields and Rome compatibility.

-   **Version 1.0.3 - June 2020**

    Patch release of Microsoft Azure Resource Management spoke for IntegrationHub.

-   **Version 1.0.1 - March 2020**

    Provides actions to automate Microsoft Azure Resource Management.



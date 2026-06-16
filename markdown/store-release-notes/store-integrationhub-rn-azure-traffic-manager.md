---
title: Microsoft Azure Traffic Manager spoke release notes
description: Version history for the Integration Hub Microsoft Azure Traffic Manager spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-traffic-manager.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Traffic Manager spoke release notes

Version history for the Integration Hub Microsoft Azure Traffic Manager spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Traffic Manager Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Endpoint Management: Create Endpoint \(create\_endpoint\_v2\), Delete Endpoint \(delete\_endpoint\), Look up Endpoint \(look\_up\_endpoint\), Update Endpoint \(update\_endpoint\_v2\)
            -   Profile Management: Create Profile \(create\_profile\_v2\), Delete Profile \(delete\_profile\_v2\), Look up DNS Name Availability \(look\_up\_dns\_name\_availability\), Look up Profile \(look\_up\_profile\), Look up Profiles by Resource Group \(look\_up\_profiles\_by\_resource\_group\),Look up Profiles by Subscription ID \(look\_up\_profiles\_by\_subscription\_id\),Update Profile \(update\_profile\)
    -   Removed:
        -   Deprecated old credential alias Azure\_Traffic\_Manager \(sn\_azure\_tmgr\_spke.Azure\_Traffic\_Manager\)
        -   Deprecate actions that make use of old credential alias:
            -   Endpoint Management: Create Endpoint \(Deprecated\) \(create\_endpoint1\),Delete Endpoint \(Deprecated\) \(create\_endpoint\),Get Endpoint \(Deprecated\) \(get\_endpoint\),Update Endpoint \(Deprecated\) \(update\_endpoint\)
            -   Profile Management: Check DNS Availability \(Deprecated\) \(check\_dns\_availability\),Create Profile \(Deprecated\) \(create\_profile\),Delete Profile \(Deprecated\) \(delete\_profile\),Get Profile \(Deprecated\) \(get\_profile\),Look up Profiles By Resource Group \(Deprecated\) \(list\_profile\_by\_resource\_group\),Look up Profiles By Subscription \(Deprecated\) \(look\_up\_profiles\_by\_subscription\),Update Profile \(Deprecated\) \(update\_profile1\)
-   **Version 1.0.3 - May 2023**

    Changed: Spoke name.

-   **Version 1.0.2 - September 2022**

    Fixed: Patch version of Azure Traffic Manager Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.0.1 - July 2021**

    Patch release of the Azure Traffic Manager spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields and Rome compatibility.

-   **Version 1.0.0 - August 2020**

    Provides actions to automate the management of profiles and endpoints in Azure Traffic Manager.



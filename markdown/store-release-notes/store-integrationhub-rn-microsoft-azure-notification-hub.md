---
title: Microsoft Azure Notification Hub spoke release notes
description: Version history for the Integration Hub Microsoft Azure Notification Hub spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-microsoft-azure-notification-hub.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Notification Hub spoke release notes

Version history for the Integration Hub Microsoft Azure Notification Hub spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Notification Hub Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New connection &amp; credential alias: Microsoft Azure Notification Management \(sn\_ms\_notification.Microsoft\_Azure\_Notification\_Hub\_SAS\)
        -   Authentication Template for easy spoke setup
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the updated connection &amp; credential alias:
            -   Installation Management: Create or Update Installation \(create\_or\_update\_installation\),Delete Installation \(delete\_installation\),Look up Installation \(look\_up\_installation\),Update Installation \(update\_installation\_v2\)
            -   Namespace Management: Create or Update Namespace \(create\_or\_update\_namespace\_v2\),Delete Namespace \(delete\_namespace\_v2\),Get Namespace Properties \(Metadata\) \(get\_namespace\_properties\_metadata\),Get Namespaces by Resource Group \(Metadata\) \(get\_namespaces\_by\_resource\_group\_metadata\),Get SKU Properties \(Metadata\) \(get\_sku\_properties\_metadata\),Look up Namespace \(look\_up\_namespace\),Look up Namespaces Stream by Resource Group \(look\_up\_namespaces\_stream\_by\_resource\_group\),Look up Namespaces Stream by Subscription ID \(look\_up\_namespaces\_stream\_by\_subscription\_id\),Update Namespace \(update\_namespace\_v2\)
            -   Notification Hub Management: Create or Update Notification Hub \(create\_or\_update\_notification\_hub\_v2\),Delete Notification Hub \(delete\_notification\_hub\_v2\),Get Notification Hub Properties \(Metadata\) \(get\_notification\_hub\_properties\_metadata\),Get Notification Hubs by Namespace \(Metadata\) \(get\_notification\_hubs\_by\_namespace\_metadata\),Look up Notification Hub \(look\_up\_notification\_hub\),Look up Notification Hubs Stream by Namespace \(look\_up\_notification\_hubs\_stream\_by\_namespace\)
            -   Notification Management: Send APNS Native Notification \(send\_apns\_native\_notification\_v2\),Send GCM Native Notification \(send\_gcm\_native\_notification\_v2\),Send Notification to Device Handle \(send\_notification\_to\_device\_handle\)
            -   Registration Management: Create APNS Registration \(create\_apns\_registration\_v2\),Create GCM Registration \(create\_gcm\_registration\_v2\),Create Registration ID \(create\_registration\_id\),Delete Registration \(delete\_registration\),Look up Registration \(look\_up\_registration\),Look up Registrations Stream \(look\_up\_registrations\_stream\),Update APNS Registration \(update\_apns\_registration\),Update GCM Registration \(update\_gcm\_registration\)
    -   Removed:
        -   Deprecated old credential alias NotificationHub \(sn\_ms\_notification.NotificationHub\) and NotificationHub\_SAS \(sn\_ms\_notification.NotificationHub\_SAS\)
        -   Deprecated Actions making use of the old credential alias:
            -   Installation Management: Delete Installation \(Deprecated\) \(delete\_an\_installation\),Get Installation \(Deprecated\) \(get\_installation\),Update Installation \(Deprecated\) \(update\_installation\),Upsert Installation \(Deprecated\) \(create\_or\_overwrite\_an\_installation\)
            -   Metadata Retrieval: Get PNS Credentials \(Deprecated\) \(get\_namespace\_pns\_credentials\),Get Properties - Namespace Management \(Deprecated\) \(get\_properties\_\_namespace\_management\),Get Properties - Notification Hub \(Deprecated\) \(get\_properties\_\_notification\_hub\),Sku - Notifications \(Deprecated\) \(sku\_\_notifications\)
            -   Namespace Management: Delete Namespace \(Deprecated\) \(delete\_namespace\),Get Namespace \(Deprecated\) \(get\_namespace\),Look up Namespaces By Resource Group \(Deprecated\) \(list\_namespace\),Look up Namespaces By Subscription ID \(Deprecated\) \(list\_all\_namespaces\),Update Namespace \(Deprecated\) \(update\_namespace\),Upsert Namespace \(Deprecated\) \(create\_or\_update\_namespace\)
            -   Notification Hub Management: Delete Notification Hub \(Deprecated\) \(delete\_notification\_hub\),Get Notication Hub \(Deprecated\) \(get\_notication\_hub\),Look up Notification Hubs \(Deprecated\) \(look\_up\_notification\_hubs\),Send APNS Native Notification \(Deprecated\) \(send\_apns\_native\_notification\),Send GCM Native Notification \(Deprecated\) \(send\_gcm\_native\_notification\),Send Notification to Device Handle \(Deprecated\) \(direct\_send\),Upsert Notification Hub \(Deprecated\) \(create\_or\_update\_notification\_hub\)
            -   Registration Management: Create APNS Registration \(Deprecated\) \(create\_apns\_registration\),Create GCM Registration \(Deprecated\) \(create\_gcm\_registration\),Create Registration ID \(Deprecated\) \(create\_a\_registration\_id\),Delete Registration \(Deprecated\) \(delete\_a\_registration\),Get Registration \(Deprecated\) \(read\_a\_registration\),Look up Registrations \(Deprecated\) \(read\_all\_registration\),Update APNS Registration \(Deprecated\) \(update\_\_apns\_registration\),Update GCM Registration \(Deprecated\) \(update\_\_gcm\_registration\)
-   **Version 1.0.3 - September 2023**

    Fixed: The license requirements.

-   **Version 1.0.2 - September 2022**

    Fixed: Patch version of Microsoft Azure Notification Hub Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.0.1 - July 2021**

    Patch release of the Azure Notification Hub spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields and Rome compatibility.

-   **Version 1.0.0 - August 2020**

    Provides actions to automate the management of namespaces, installation, and registrations in Azure Notification Hub.



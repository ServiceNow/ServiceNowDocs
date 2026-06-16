---
title: Microsoft Azure Managed Storage spoke release notes
description: Version history for the Integration Hub Microsoft Azure Managed Storage spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-microsoft-azure-managed-storage.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Managed Storage spoke release notes

Version history for the Integration Hub Microsoft Azure Managed Storage spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.1 - November 2024**
    -   New:
        -   Microsoft Azure Managed Storage Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Disk Management: Create Managed Disk \(create\_managed\_disk\_v2\), Create Managed Disk from Snapshot \(create\_managed\_disk\_from\_snapshot\_v2\), Create Managed Upload Disk \(create\_managed\_upload\_disk\_v2\), Delete Disk \(delete\_disk\_v2\), Get Disks by Resource Group \(Metadata\) \(get\_disks\_by\_resource\_group\_metadata\), Grant Access to Disk \(grant\_access\_to\_disk\_v2\), Look up Disk \(look\_up\_disk\_v2\), Look up Disks Stream by Resource Group \(look\_up\_disks\_stream\_by\_resource\_group\), Look up Disks Stream by Subscription ID \(look\_up\_disks\_stream\_by\_subscription\_id\), Revoke Access from Disk \(revoke\_access\_from\_disk\_v2\), Set Disk Tags \(set\_disk\_tags\_v2\), Update Disk Size \(update\_disk\_size\_v2\), Update Disk Storage Account \(update\_disk\_storage\_account\_v2\)
            -   Disk Snapshot Management: Create Snapshot \(create\_snapshot\_v2\), Delete Snapshot \(delete\_snapshot\_v2\), Get Snapshots by Resource Group \(Metadata\) \(get\_snapshots\_by\_resource\_group\_metadata\), Get Snapshots by Subscription ID \(Metadata\) \(get\_snapshots\_by\_subscription\_id\_metadata\), Grant Access to Snapshot \(grant\_access\_to\_snapshot\_v2\), Look up Snapshot \(look\_up\_snapshot\_v2\), Look up Snapshots Stream by Resource Group \(look\_up\_snapshots\_stream\_by\_resource\_group\), Look up Snapshots Stream by Subscription ID \(look\_up\_snapshots\_stream\_by\_subscription\_id\), Revoke Access from Snapshot \(revoke\_access\_from\_snapshot\_v2\), Set Snapshot Tags \(set\_snapshot\_tags\_v2\), Update Snapshot Size \(update\_snapshot\_size\_v2\), Update Snapshot Storage Account \(update\_snapshot\_storage\_account\_v2\)
    -   Removed:
        -   Deprecated old credential alias Azure\_Managed\_Storage \(sn\_azure\_ms\_spoke.Azure\_Managed\_Storage\)
        -   Deprecated actions that make use of old credential alias:
            -   Disk Management: Create Managed Disk \(Deprecated\) \(create\_empty\_disk\),Create Managed Disk From Snapshot \(Deprecated\) \(create\_disk\_from\_snapshot\),Create Managed Upload Disk \(Deprecated\) \(create\_a\_managed\_upload\_disk\),Delete Disk \(Deprecated\) \(delete\_disk\), Get Disk Information \(Deprecated\) \(get\_information\_about\_disk\), Grant Access to Disk Data \(Deprecated\) \(grant\_access\),List Disk Names by ResourceGroup \(Deprecated\) \(list\_disk\_names\_by\_resourcegroup\),Look up Disks by Resource Group \(Deprecated\) \(list\_disks\_by\_resourcegroup\),Look up Disks by Subscription \(Deprecated\) \(list\_disks\_by\_subscription\),Revoke Access From Disk Data \(Deprecated\) \(revoke\_access\_from\_disk\_data\),Set Disk Tags \(Deprecated\) \(update\_disk\_tags\),Update Disk Size \(Deprecated\) \(update\_disk\),Update Disk Storage Account \(Deprecated\) \(update\_disk\_storage\_account\)
            -   Disk Snapshot Management: Create Snapshot \(Deprecated\) \(create\_snapshot\),Delete Snapshot \(Deprecated\) \(delete\_snapshot\),Get Snapshot Information \(Deprecated\) \(get\_snapshot\_information\),Grant Access to Disk Snapshot \(Deprecated\) \(grant\_access\_for\_disk\_snapshot\),List Snapshot Names by ResourceGroup \(Deprecated\) \(list\_snapshot\_names\_by\_resourcegroup\),Look up Snapshot By Resource Group \(Deprecated\) \(list\_by\_resourcegroup\),Look up Snapshot By Subscription \(Deprecated\) \(list\_by\_subscription\),Revoke Access From Snapshot \(Deprecated\) \(revoke\_access\_snapshot\),Set Snapshot Tags \(Deprecated\) \(update\_snapshot\_tags\),Update Snapshot Size \(Deprecated\) \(update\_snapshot\),Update Snapshot Storage Account \(Deprecated\) \(update\_snapshot\_storage\_account\_type\)
-   **Version 1.0.8 - September 2023**

    Fixed: The license requirements.

-   **Version 1.0.7 - April 2023**

    Fixed: Improve installation performance of spoke.

-   **Version 1.0.6 - July 2021**

    Patch release of the Azure Managed Storage spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields and Rome compatibility.

-   **Version 1.0.5 - October 2020**

    Patch release of Microsoft Azure Managed Storage spoke for IntegrationHub.

-   **Version 1.0.4 - July 2020**

    Patch release of Microsoft Azure Managed Storage spoke for IntegrationHub.

-   **Version 1.0.2 - June 2020**

    Provides actions to automate the management of disks and snapshots in Azure.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)


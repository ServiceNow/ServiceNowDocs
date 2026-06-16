---
title: Microsoft Azure Blob Storage spoke release notes
description: Version history for the Integration Hub Microsoft Azure Blob Storage spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-blob-storage.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Blob Storage spoke release notes

Version history for the Integration Hub Microsoft Azure Blob Storage spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   New connection &amp; credential alias: Microsoft Azure Blob Storage \(sn\_azure\_blob\_spke.Microsoft\_Azure\_Blob\_Storage\)
        -   Authentication Template for easy spoke setup
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Blob Management: Attach Blob to ServiceNow Record \(attach\_blob\_to\_servicenow\_record\_v2\),Copy Blob \(copy\_blob\_v2\),Delete Blob \(delete\_blob\_v2\),Lease Blob \(lease\_blob\_v2\),Look up Blob \(look\_up\_blob\),Look up Blobs \(look\_up\_blobs\),Parse Blob JSON \(parse\_blob\_json\),Release Lease on Blob \(release\_lease\_on\_blob\_v2\),Snapshot Blob \(snapshot\_blob\_v2\),Upload Attachment to Container \(upload\_attachment\_to\_container\)
            -   Container Management: Create Container \(create\_container\_v2\),Delete Container \(delete\_container\_v2\),Lease Container \(lease\_container\_v2\),Look up Container \(look\_up\_container\),Look up Containers \(look\_up\_containers\),Parse Container JSON \(parse\_container\_json\),Release Lease on Container \(release\_lease\_on\_container\_v2\)
        -   New subflows
            -   Blob Management: Look up Blobs Stream \(look\_up\_blobs\_stream\),Move Blob \(move\_blob\_v2\),Rename Blob \(rename\_blob\_v2\)
            -   Container Management: Look up Containers Stream \(look\_up\_containers\_stream\)
    -   Removed:
        -   Deprecate old credential alias for the spoke Azure\_Blob\_Storage \(sn\_azure\_blob\_spke.Azure\_Blob\_Storage\) and Azure\_Blob\_Storage\_SAS \(sn\_azure\_blob\_spke.Azure\_Blob\_Storage\_SAS\).
        -   Deprecated Actions that make use of old credential alias:
            -   Blob Management: Attach Blob To ServiceNow Record \(Deprecated\) \(attach\_blob\_to\_servicenow\_record\),Copy Blob \(Deprecated\) \(copy\_blob\),Delete Blob \(Deprecated\) \(delete\_blob\),Get Blob Details \(Deprecated\) \(get\_blob\_details\),Lease Blob \(Deprecated\) \(lease\_blob\),Look up Blob \(Deprecated\) \(list\_blobs\),Release Lease On Blob \(Deprecated\) \(release\_lease\_on\_blob\),Snapshot Blob \(Deprecated\) \(snapshot\_blob\),Upload ServiceNow Attachment To Container \(Deprecated\) \(upload\_servicenow\_attachment\_to\_container\)
            -   Container Management: Create Container \(Deprecated\) \(create\_container\),Delete Container \(Deprecated\) \(delete\_container\),Get Container Details \(Deprecated\) \(get\_container\_details\),Lease Container \(Deprecated\) \(lease\_container\),Look up Container \(Deprecated\) \(list\_containers\),Release Lease On Container \(Deprecated\) \(release\_lease\_on\_container\)
        -   Deprecated subflows
            -   Blob Management: Rename Blob \(Deprecated\) \(rename\_blob\),Move Blob \(Deprecated\) \(move\_blob\)
-   **Version 1.0.6 - May 2023**

    Changed: Spoke name.

-   **Version 1.0.5 - September 2022**

    Fixed: Improve installation performance of spoke

-   **Version 1.0.4 - July 2021**

    Patch release of Azure Blob Storage spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields, and Rome compatibility

-   **Version 1.0.3 - September 2020**

    Patch release of Azure Blob Storage spoke for IntegrationHub.

-   **Version 1.0.2 - July 2020**

    New: This version includes an updated icon for the actions.

-   **Version 1.0.1 - June 2020**

    Provides actions to automate the management of blobs and containers in Azure.



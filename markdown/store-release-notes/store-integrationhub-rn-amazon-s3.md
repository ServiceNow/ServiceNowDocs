---
title: Amazon S3 spoke release notes
description: Version history for the Integration Hub Amazon S3 spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-amazon-s3.html
release: store
topic_type: reference
last_updated: "2024-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Amazon S3 spoke release notes

Version history for the Integration Hub Amazon S3 spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.1 - September 2024**

    Fix: For Upload ServiceNow Attachment To S3 action fails to upload file when more than two "\(\)" are included in the file name.

-   **Version 1.2.0 - September 2023**
    -   New: Added Upload ServiceNow Attachment To S3 \(upload\_file\_to\_bucket\_v2\) to return ETag.
    -   Fixed: The license requirements.
    -   Removed: Deprecated Upload ServiceNow Attachment To S3 \(upload\_file\_to\_bucket\).
-   **Version 1.1.2 - September 2022**

    Patch release of Amazon S3 Spoke for IntegrationHub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.1.1 - June 2022**

    Fixed: Patch release of Amazon S3 Spoke. This version fixes an issue with the Delete S3 object within a folder.

-   **Version 1.1.0 - May 2022**
    -   New: Minor release for Amazon S3 Spoke. This version includes a new action 'Look up Objects by Bucket Stream'
    -   Fixed: Fix for Download Attachment to handle special characters in object names.
-   **Version 1.0.2 - February 2022**

    Fixed: Patch release of Amazon S3 spoke for IntegrationHub. This version adds a fix to the error observed when an s3 object with a key including special characters is downloaded.

-   **Version 1.0.1 - September 2020**

    Patch release of Amazon S3 spoke for IntegrationHub.

-   **Version 1.0.0 - March 2020**

    Provides actions to automate the management of Buckets and Objects in Amazon S3.



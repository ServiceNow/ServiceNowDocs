---
title: CSC Content Pack release notes
description: Version history for the CSC Content Pack application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-csc-content-pack.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# CSC Content Pack release notes

Version history for the CSC Content Pack application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.8.0 - June 2026**
    -   Fixed:
        -   Schedule Profile variable incorrectly appearing for GitHub Action catalog when stack-level operations are supported
        -   GitHub Actions update set import breaks normal provisioning of GitHub template provisions and JSON catalog
        -   Missing catalog-to-flow mappings in the Cloud Catalog Items table after upgrading CSC Content Pack to v1.6.0
        -   Manage access through predefined query access controls for all Cloud Service Catalog tables
-   **Version 1.7.0 - December 2025**

    New: Integrated GitHub Actions workflows to dynamically generate catalog items from YAML files, map and validate pipeline variables, and enable workflow triggering and status tracking in ServiceNow.

-   **Version 1.6.0 - May 2025**
    -   Changed: CSC Out-of-box catalogs are updated to use PAD for Day1 and Day2 activities
    -   Fixed: Improved cloud catalog speed by using reference qualifiers to dynamically filter data based on linked tables
-   **Version 1.5.5 - November 2024**

    Changed: Applied routine security updates and policies.

-   **Version 1.4.4 - May 2024**

    New: OOB Content for Google Cloud Catalogs.

-   **Version 1.3.0 - November 2023**
    -   This application provides content for use with the Cloud Services Catalog application.
    -   In this release of the app, meant for sub-production use \(Innovation Labs\) the content comprises of readymade catalog items suitable for use, with inbuilt governance policies and actions to deliver end-to-end governed deployment workflow.


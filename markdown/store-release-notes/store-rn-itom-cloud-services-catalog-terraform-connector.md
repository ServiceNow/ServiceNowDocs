---
title: Cloud Services Catalog Terraform Connector release notes
description: Version history for the Cloud Services Catalog Terraform Connector application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-services-catalog-terraform-connector.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ITOM Cloud Accelerate release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Services Catalog Terraform Connector release notes

Version history for the Cloud Services Catalog Terraform Connector application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**

    Fixed: Manage access through predefined query access controls for all Cloud Services Catalog tables

-   **Version 1.9.1 - December 2025**
    -   New: Introduced granular, feature-specific admin roles to replace the broad 'admin' role, significantly enhancing security by minimizing excess access. These new roles are seamlessly integrated into the standard administrative experience.
    -   Changed: Enabled end-to-end support for PowerShell operations across MID Servers and Windows remote machines. The system now automatically detects and selects the most appropriate PowerShell version, defaulting to PowerShell 7 where available, to ensure more consistent and reliable execution of scripts.
    -   Fixed: Implemented Read-Only Field Remediation by introducing a new ChoiceList, 'read\_only\_option,' to replace the previous 'read\_only' field \(which was prone to unauthorized client-side updates\). This change prevents client-side manipulation of read-only fields and significantly mitigates security risks across all applications.
-   **Version 1.8.0 - May 2025**

    CPG Terraform Connector is now available as Cloud Services Catalog Terraform Connector.



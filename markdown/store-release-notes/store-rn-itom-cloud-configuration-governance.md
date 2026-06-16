---
title: Cloud Configuration Governance release notes
description: Version history for the Cloud Configuration Governance application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-configuration-governance.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM Cloud Accelerate release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Configuration Governance release notes

Version history for the Cloud Configuration Governance application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.0 - June 2026**

    Fixed: Manage access through predefined query access controls for all Cloud Configuration Governance tables

-   **Version 1.6.0 - December 2025**
    -   New: Introduced granular, feature-specific admin roles to replace the broad 'admin' role, significantly enhancing security by minimizing excess access. These new roles are seamlessly integrated into the standard administrative experience.
    -   Fixed: Implemented Read-Only Field Remediation by introducing a new ChoiceList, 'read\_only\_option,' to replace the previous 'read\_only' field \(which was prone to unauthorized client-side updates\). This change prevents client-side manipulation of read-only fields and significantly mitigates security risks across all applications.
-   **Version 1.5.0 - November 2024**

    Fixed: Applied security and policy updates.

-   **Version 1.4.3 - January 2024**

    This quality release addresses issues with the empty 'no-rule' ACL. The appropriate roles are added to all the empty ACLs for tables to avoid unauthenticated access.

-   **Version 1.4.2 - May 2023**
    -   New: CCG pages support dark theme in Next Experience mode
    -   Changed: CCG Audit results now return non-violating \(compliant\) resources also. Prior to this, only violating resources were listed in Audit results. This change was done to aid GRC/ CSPM use-case.
    -   Fixed:
        -   Issues with running CCG Scan through API
        -   Security issue
-   **Version 1.3.10 - February 2023**
    -   Changed: Security improvements for report view ACLs
    -   Fixed: Fixed the license counting scripts to avoid duplicate CI counting.
-   **Version 1.3.7 - August 2022**
    -   New:
        -   Use the AWS assume role to scan member accounts from the management account.
        -   Use the new remediation dialog \(UI\) to run multiple remediations for multiple violations.
        -   Use the record producer to create custom remediations with additional inputs.
    -   Removed: Moved all the default base-system CCG contents to the CCG Content pack available with this release.
-   **Version 1.2.1 - May 2022**

    New: CI resource linking

-   **Version 1.0.5 - February 2022**

    When you have sensitive data in the cloud or use the public cloud heavily, it is essential to establish norms for configuring cloud resources. Failure to set up and follow these norms can prove costly for the business. Cloud Configuration Governance \(CCG\) helps set policies for cloud resources, validate these policies, identify the violators, and run remediation to fix invalid configurations. For instance, you can turn on encryption for object storage or prevent misuse, turn off VMs with wide network access settings, create any number of rules, and also set up configurations to run scans on a specific or a generic set of cloud resources. Remediations are available out of the box, and more remediations can be built using Automation Engine. Use CCG to get your cloud resource costs, security, and availability under control for building a better cloud-integrated business.



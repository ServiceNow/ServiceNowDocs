---
title: GRC: SOX content pack release notes
description: Version history for the Governance, Risk, and Compliance Sarbanes-Oxley \(SOX\) content pack on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-sox-kingston.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: SOX content pack release notes

Version history for the Governance, Risk, and Compliance Sarbanes-Oxley \(SOX\) content pack on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
        -   Post-upgrade review for customized ACLs:
            -   If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
    -   Changed: Validated plugin dependencies to prevent ACLs from referencing roles provided by uninstalled optional plugins.
-   **Version 22.0.1 - March 2026**

    Changed: Updated control objective content records with Record nature field as Current version and State as Published.

-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed: Added read-only attribute to read-only fields for enhanced security

-   **Version 5.0.2 \(Kingson, London\) - October 2018**
    -   The Sarbanes-Oxley \(SOX\) Content Pack includes the following content elements:
        -   Pre-defined profile type and profiles
        -   SOX policies
        -   Policy statements and controls
        -   SOX control attestation template
        -   Risk statements and risks
        -   Indicator templates and indicators
        -   SOX audit engagement
        -   Audit tasks
        -   Test templates and test plans
        -   Reports and dashboards
    -   The following relationships are also established:
        -   Policy statements to policies
        -   Controls to policies \(through policy statements\)
        -   Indicators to controls
        -   Risks to risk statements
        -   Risks to profiles
        -   Risks to controls \(mitigating controls\)
        -   Test plans to controls for control testing
    -   Other GRC roles:
        -   Compliance Reader \(sn\_compliance\_reader\) can read **SOX Compliance Dashboard** and **SOX Processes**
        -   Compliance Manager \(sn\_compliance\_manager\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and edit **SOX Processes**
        -   Compliance Admin \(sn\_compliance\_admin\) can read **SOX Risk Dashboard** and edit **SOX Compliance Dashboard** and **SOX Processes**
        -   Risk Reader \(sn\_risk\_reader\) can read **SOX Risk Dashboard** and **SOX Processes**
        -   Risk Manager \(sn\_risk\_manager\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and edit **SOX Processes**
        -   Risk Admin \(sn\_risk\_admin\) can read **SOX Compliance Dashboard** and edit **SOX Risk Dashboard** and **SOX Processes**
        -   Audit User \(sn\_audit\_user\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and **SOX Processes**
        -   Audit Admin \(sn\_audit\_admin\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and edit **SOX Audit Dashboard** and **SOX Processes**


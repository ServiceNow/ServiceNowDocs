---
title: GRC: Privacy Case Management integration with RadarFirst release notes
description: Version history for the GRC: Privacy Case Management integration with RadarFirst application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-privacy-case-mgmt-int-radarfirst.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Privacy Case Management integration with RadarFirst release notes

Version history for the GRC: Privacy Case Management integration with RadarFirst application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   Changed:
        -   Query range ACL's
            -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 21.1.0 - December 2025**
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 20.1.1 - May 2025**

    Fixed security issues as part of platform security directive initiative.

-   **Version 19.1.0 - November 2024**

    Changed: Enabled Now unit &amp; localisation for this app.

-   **Version 19.0.0 - August 2024**

    Changed: Updated the application version to keep it in sync with dependent application.

-   **Version 18.1.0 - June 2024**

    Changed: Updated dependency of this app to latest version \(18.1.1\) of GRC: Privacy Case Management.

-   **Version 18.0.2 - February 2024**

    The Privacy Case Management integration for RadarFirst enables the privacy teams to swiftly conduct risk assessments on breach incidents, generating prompt and actionable insights into regulatory notification obligations aligned with global regulations. It also suggests resolution, corrective action, and notification based on the breach assessment details.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)


---
title: Vulnerability Response Integration with Agile Management release notes
description: Version history for the Vulnerability Response Integration with Agile Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-agile-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Agile Management release notes

Version history for the Vulnerability Response Integration with Agile Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.3 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs are bundled with the Agile integration to align with ServiceNow Platform Security guidance.
        -   Dictionary fields for the Agile integration tables are read-only.
        -   Agile files renamed to prevent cross-plugin update set conflicts with Vulnerability Response plugins.
-   **Version 1.2.2 - August 2025**
    -   Fixed:
        -   Stabilized the JIRA integration by enforcing mandatory project selection check, improving UI messages in some of the flows, and refining field mapping validations.
        -   Updated Agile Tool configuration annotations to include information about an OOB system property - 'sn\_vul\_agile.display\_table' and ensured correct handling of default field mappings.
        -   Fixed state sync issues and validated UI actions for Agile Issue creation and synchronization as part of this release.
-   **Version 1.1.2 - November 2024**

    Minor fixes for this release.

-   **Version 1.0.4 - October 2023**

    Fixed: Added null check during creation of Jira issue.

-   **Version 1.0.3 - August 2023 \(Vancouver\)**

    This app provides the framework for integrating Vulnerability Response with Agile Management tools to create issues or tickets corresponding to Remediation Tasks.

    New:

    -   Integrate Vulnerability Response with Agile Management tools to create issues or tickets corresponding to Remediation Tasks.
    -   Choose between automatic versus manual creation of issues or tickets.
    -   Track remediation progress by syncing status from the Agile Management tool to VR.


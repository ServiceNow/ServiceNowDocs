---
title: Security Case Management common workspace components release notes
description: Version history for the Security Operations Security Case Management common workspace components on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-security-case-mgmt-common-ws-components.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Case Management common workspace components release notes

Version history for the Security Operations Security Case Management common workspace components on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**

    Fixed: Resolved a WCAG 1.4.11 non-text contrast issue where the remove tag button and its keyboard focus indicator on security tag pills did not meet the required 3:1 contrast ratio in the Security Incident Response Workspace.

-   **Version 1.4.4 - March 2026**
    -   Fixed:
        -   Fixed an issue in the SIR Post Implementation Review Assessment where saving the assessment caused an "Unparseable date" error when the system date format was configured as dd/MM/yyyy.
        -   Fixed an issue in the Security Incident Response Workspace where uploading a secure attachment displayed an error message and the upload failed.
-   **Version 1.4.1 - January 2026**

    Changed: Changes to support read-only security directive.

-   **Version 1.3.10 - August 2025**

    Fixed: Related Record number is not getting updated automatically when we perform link/unlink actions.

-   **Version 1.3.4 - June 2025**

    Fixed: Bug related to dark theme in the Post Incident review section.

-   **Version 1.3.3 - May 2025**

    Bug fixes with respect to ACL bypass.

-   **Version 1.3.1 - February 2025**

    Fixed: Accessibility issues addressed.

-   **Version 1.2.4 - November 2024**

    Fixed: Addressed accessibility issues.

-   **Version 1.2.3 - August 2024**

    New: Added Native sidebar chat.

-   **Version 1.2.1 - May 2024**

    New: Added Risk Score Calculator.

-   **Version 1.1.2 - February 2024**
    -   Changed: Updated the dependency on sn\_si.read role for graphQLschema "relatedListGroups"
    -   Fixed: The Related List Count wasn't getting updated when records were linked or unlinked.
-   **Version 1.0.8 - November 2023**
    -   Changed: Migrated Security Case Management common workspace components pages to Layout 3.0 to support accessibility.
    -   Fixed: The Security Incident Response workspace's related list personalization was not persistent and was getting applied to all users.
-   **Version 1.0.6 - August 2023**

    Changed: Supports Telemetry Usage queries.

-   **Version 1.0.5 - May 2023**

    Changed: Updated to support the Security Incident Response workspace.

-   **Version 1.0.3 - April 2023**

    Changed: Updated to support this application on the Security Incident Response workspace.

-   **Version 1.0.0 - February 2023**

    This application will serve as a base application holding common artifacts that will be used by all Security Case Management Workspaces.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


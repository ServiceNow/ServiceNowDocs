---
title: DLP Incident Response Integration with Symantec release notes
description: Version history for the DLP Incident Response integration with Symantec application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-dlp-incident-response-integration-symantec.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# DLP Incident Response Integration with Symantec release notes

Version history for the DLP Incident Response integration with Symantec application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.2 - June 2026**
    -   Fixed:
        -   Fixed the issue of the bi-directional synchronization not functioning correctly from ServiceNow to Symante
        -   Resolved the issue of Symantec DLP MID scripts failing under iPKI environments due to
        -   Implemented fixes related to Cobalt Raven Non-Glide Query ACL directives, ensuring proper ACL enforcement for non-Glide query operations.
-   **Version 1.3.1 - January 2026**

    Fixed: Fixed ACL on the Match Content field in the Detected Sensitive Info table.

-   **Version 1.2.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only, to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 1.1.30 - October 2025**

    Fixed issue by ensuring execution occurs only after Q entry record updates to prevent DLP incidents from being created without proper metadata.

-   **Version 1.1.21 - June 2025**

    Fixed: Unnecessary error logs that were generated on clicking the Sensitive Information tab in the Workspace.

-   **Version 1.1.20 - February 2025**
    -   New:
        -   Symantec Evidence File External Storage Implementation:
            -   Implemented external storage for Symantec evidence files, ensuring secure, scalable, and efficient storage of evidence data outside the core system.
-   **Version 1.1.18 - November 2024**
    -   Fixed:
        -   Security defects including the misconfiguration of Access Control Lists \(ACL\) to improve the system protection.
        -   The integration performed across all worker threads during a flood of events to ensure more stable and efficient processing.
-   **Version 1.1.15 - August 2024**
    -   New: Symantec is now compatible with the DLP core migration changes such as incident status.
    -   Fixed: Custom attributes is now visible on the enduser lookup rules page whenever a configuration tile is created for Symantec.
-   **Version 1.1.13 - June 2024**
    -   Fixed:
        -   Missing Server or Detector field on the DLP incident.
        -   Symantec DLP staging table was not importing all fields on the source.
        -   Symantec DLP Integration: User Justification is showing numerical data and DetectionServer was missing.
        -   Fetch of customAttribute fails and no retry happens.
        -   Detection date was lesser than the sent date for DLP incidents.
-   **Version 1.1.12 - April 2024**
    -   Fixed:
        -   Couple of ACLs.
        -   Symantec API indexing delay.
-   **Version 1.1.11 - February 2024**
    -   New:
        -   Added correlation ID mapping for DLP incidents in the transform map.
        -   Added support for the DLP incidents archival.
    -   Fixed:
        -   The field values now contains the special characters to support the data import from Symantec.
        -   Improved the Detected Sensitive Information records creation performance during the DLP incident ingestion process.
-   **Version 1.1.9 - December 2023**
    -   Fixed:
        -   Resolved the issue where the Sharepoint and File permissions were merged into the File permissions field of the DLP incidents.
        -   Fixed the problem of missing the batch file permissions if one incident in a batch of 100 REST calls fails.
        -   Addressed the issue where queue entries are moved to an error state if the processing had exceeded 1 hour.
        -   Resolved the performance issues caused by the incident transformation due to a new change for detected sensitive info per incident in the August store release.
        -   Fixed the problem where the Integration Configuration tile was not working for some combinations of passwords.
        -   Upgraded to code signing snc-app-parent version for the patch.
        -   Resolved the issue where the Since Date validation in the Profile was failing when the user was using a different date-time format.
        -   Fixed the problem where the file permissions were broken in the v16 API.
        -   Addressed the security bugs related to the misconfiguration of table/field ACLs within the com.snc.sym\_dlp plugin.
-   **Version 1.1.8 - November 2023**

    Fixed: The Performance issues are now fixed which occurred due to the changes that were made to the Match Content field on the DLP incident form view, which was released in the previous store version.

-   **Version 1.1.6 - August 2023**

    Fixed:

    -   Previously, the data was not transforming correctly for the Last Accessed field in the DLP Incident table.
    -   The existing Non-ASCII characters transform issue for some of the Symantec DLP fields is now resolved.
-   **Version 1.1.4 - July 2023**

    Fixed: Fixed the Jsession ID \(which was not deprecated properly\).

-   **Version 1.1.1 - June 2023**
    -   Fixed:
        -   The changes in the global date-time format impacted the data transformation process. This issue is now resolved.
        -   The Refresh Custom Attributes BR was triggered on any column update in the Symantec profile. This issue is now resolved.
        -   The polling interval for the DLP Symantec integration is now changed from hours to minutes.
        -   Some of the DLP Incident fields did not properly handle unicode and non-English characters in the response. This issue is now fixed.
-   **Version 1.1.0 - May 2023**
    -   Fixed:
        -   Ingestion was not working for Symantec 16.0.
        -   DLP Symantec integration mapping issue.
        -   Incident Profile Button's view is not proper.
        -   DLP profile gets stuck in a Running state due to a time zone issue.
        -   DLP Symantec - Multiple profiles issue.
        -   DLP Symantec Severity mapping is not proper.
        -   Fetching incidents in CSV format is broken in Symantec if the connection is via the cloud.
-   **Version 1.0.8 - August 2022**
    -   New: Allow Setting from DLP core whether to display matched content on form or not for intergration
    -   Fixed:
        -   Refactor Match content endpoint to avoid logging the response
        -   Trailing slash included in the Symantec incident ingestion endpoint
        -   Accessibility issues

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


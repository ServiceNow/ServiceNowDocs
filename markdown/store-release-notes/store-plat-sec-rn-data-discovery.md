---
title: Data Discovery release notes
description: Version history for the Data Discovery on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-plat-sec-rn-data-discovery.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ServiceNow AI Platform Security version history release notes, ServiceNow Store version history release notes]
---

# Data Discovery release notes

Version history for the Data Discovery on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.2 - September 2026**
    -   New:
        -   Admins can now configure real-time sensitive data discovery from image attachments using OCR. Image files \(.jpeg, .png\) uploaded to the platform are scanned for sensitive data using optical character recognition, enabling alerting, blocking, or reporting based on admin-defined policies.
        -   Granular findings are now tracked and accessible for Data Discovery jobs. Customers can review the exact records flagged for sensitive data, filter and search findings in the UI, and export results for offline review.
        -   Default Data Discovery jobs are now automatically created and run for Vault trial and licensed customers. The system scans recent records across key business tables for sensitive data and sends a summary email to admins, requiring no manual configuration.
        -   Automated email notifications are sent to Data Discovery admins upon job completion. The notification includes a link to the job summary and details of findings, with default subscription and opt-out options.
        -   A default Data Discovery policy is now available and assigned to all relevant patterns and tables. The policy is read-only, visible only to admins and designated roles, and supports trial period tracking.
        -   UI enhancements allow users to view granular findings and attachment findings in Scheduled Discovery. Related lists and tabs present findings filtered by workflow and grouped for easier review.
        -   Admins can now manage sensitive data discovery roles for Otto-branded features. A new role is available parallel to the previous Now Assist role for Data Privacy administration.
        -   Licensing alerts are shown in the UI for sensitive data discovery from images. Users are redirected to install required components to enable OCR scanning.
    -   Changed:
        -   The 'Generate Regex' and 'Regenerate Regex' UI buttons have been updated to reflect Otto branding. Button labels now communicate AI-assisted configuration actions, aligned with new naming guidelines.
        -   Default Data Discovery job scheduling has been revised to run during Saturday night off-peak hours. The job respects instance time zones and avoids overlapping with existing jobs, retrying weekly if needed.
        -   Default scan types for Data Discovery jobs now limit scans to 1,000 records or 30 days, whichever comes first. This scan type is not selectable in the UI and is used only for automated default jobs.
        -   Backward compatibility is supported for Data Discovery 9.0 changes with Australia. The system ensures consistent behavior across regions.
        -   Scheduled Discovery and Sources tabs now support optional URL parameters for subsection navigation. Deep-linking and bookmarking are improved, with graceful fallback for invalid parameters.
        -   All OOTB regex-based data patterns are applied to default jobs, excluding NER-based patterns. The default job is editable and becomes inactive after the trial period, with clear messaging.
        -   Email notifications for default Data Discovery jobs now include sensitive data visibility reports. The summary details record counts and types of sensitive data detected.
        -   Vault license checks are added as a condition for running default discovery jobs. Only licensed instances trigger automated scans.
-   **Version 8.1.3 - August 2026**

    Service now Otto Directive Changes.

-   **Version 7.1.4 - April 2026**
    -   No New functionality
    -   Patch release to handle defects
-   **Version 8.1.0 - March 2026**
    -   New Named Entity Recognition \(NER\) model data patterns - Address, City, State, Country, Job Position, and Salary - to detect and anonymize sensitive data.
    -   New OOB Regular Expression \(RegEx\) data patterns - 13 new data patterns
-   **Version 7.1.2 - January 2026**
    -   No new functionality
    -   Patch release to handle defects
-   **Version 7.1.1 - December 2025**
    -   No new functionality
    -   Patch release to add support for NowLLM LTS for GenAI capabilities
-   **Version 7.1.0 - September 2025**
    -   Text to generate Regex feature using Now Assist prompts to generate regex to discover sensitive data.
    -   Revamped Data Discovery user interface.
-   **Version 7.0.0 - August 2025**
    -   Revamped Data Discovery user interface to improve the Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first time users
    -   AI/ML based data patterns for intelligent discovery of sensitive data that is already on the platform
    -   Text to generate Regex feature using Now Assist prompts to generate regex to discover sensitive data
    -   Data discovery policies to streamline configurations to discover sensitive data
    -   Additional support for Excel and .CSV files for discovery and reporting of sensitive data from attachments
    -   Full scan and incremental scan support for data discovery jobs
    -   Column-level discovery of sensitive data
-   **Version 6.0.2 - July 2025**
    -   AI/ML based data patterns for intelligent discovery of sensitive data that doesn't follow a pattern like name, address, etc.
    -   Discovery and reporting of sensitive data from attachments.
-   **Version 6.0.1 - February 2025**
    -   AI/ML based data patterns for intelligent discovery of sensitive data that doesn't follow a pattern like name, address, etc.
    -   Discovery and reporting of sensitive data from attachments.
-   **Version 5.0.1 - August 2024**

    Data Discovery for Real time, support for journal fields.

-   **Version 3.0.1 - February 2024**
    -   Data pattern discovery using keywords and keyword proximity
    -   Real time Data Discovery APIs support
-   **Version 2.0.0 - November 2023**
    -   New:
        -   Full scan on the targeted tables.
        -   Anonymization of users by group
        -   Consolidate findings
    -   Changed:
        -   Users can now select a start date for data discovery jobs
        -   Bug fixes
-   **Version 1.0.0 - May 2023**

    Data Discovery gives you the ability to discover sensitive data using out-of-the-box data patterns or by creating custom regex patterns to act on: For example, to classify, report, or view. It provides sensitive data with visibility and cataloging which is an essential first step towards preventing data loss or exposure. This enables organizations to implement appropriate security measures and increase their security posture.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform Security version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-sec.md)


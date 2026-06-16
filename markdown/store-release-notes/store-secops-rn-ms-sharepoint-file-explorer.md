---
title: Microsoft SharePoint File Explorer Connector for Security Incident Response integration release notes
description: Version history for the Microsoft SharePoint File Explorer Connector for Security Incident Response integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-ms-sharepoint-file-explorer.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft SharePoint File Explorer Connector for Security Incident Response integration release notes

Version history for the Microsoft SharePoint File Explorer Connector for Security Incident Response integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.1 - March 2026**

    Fixed: When a folder is deleted from SharePoint, the deletion event appears in the Activity Section of ServiceNow. However, the user identified as having performed the deletion is incorrect.

-   **Version 1.3.0 - December 2025**

    Fixed: Resolved an issue where the Modified by field was being set to the actual user instead of the system user during SharePoint integration updates. The field now correctly reflects the system user for automated modifications.

-   **Version 1.2.10 - August 2025**

    Fixed: Added error handling for HTTP 410 \(Gone\) responses in the Get File Metadata flow. This error occurs when the service and instance are out of sync or when files are no longer accessible.

-   **Version 1.2.6 - May 2025**

    Fixed the processing of SharePoint notifications for Major Security Incident.

-   **Version 1.2.5 - November 2024**

    Fixed: Ensuring successful authentication by resolving an issue where a 401 error occurred while attempting to obtain an OAuth token when SharePoint were configured in MSIM.

-   **Version 1.2.4 - May 2024**

    Fixed: Empty ACLs and Report view ACLs.

-   **Version 1.2.2 - February 2023**

    Changed: Added changes to include certificate-based authentication.

-   **Version 1.2.0 - March 2022**

    Fixed: Bug fixes.

-   **Version 1.1.1 - December 2021**

    Manage SharePoint files and folders using file explorer.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


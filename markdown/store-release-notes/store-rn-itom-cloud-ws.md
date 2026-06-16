---
title: Cloud Workspace release notes
description: Version history for the ServiceNow Cloud Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-ws.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Workspace release notes

Version history for the ServiceNow® Cloud Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.4.0 - June 2026**
    -   New: Added support for special characters in tags \(Department, Cost Center, BU, Project/Application Service, Business Application\) for AWS provision requests
    -   Fixed:
        -   Duplicate tabs open when clicking an account name
        -   Cloud Workspace incorrectly allows the onboarding of retired or closed accounts and displays an incorrect status
        -   CAM AWS Account Creation Request fails when tags contain special characters
        -   Long account IDs overflow the card container and overlap fields in Card view
        -   Incorrect count displays for cloud accounts
        -   The home page for Asset Viewer displays no data
        -   Cloud Assets Name field is not clickable on the Australia platform family
        -   Azure provision request gets stuck in a progress state when special characters are passed in the account alias
        -   Number concatenation with strings causes grammatical errors in OOTB target languages \(i18n\)
        -   Arabic text overlaps with numbers, impacting readability in Cloud Workspace \(i18n\)
        -   Inconsistent border on the Compliance Dashboard widget for accounts with critical security findings
        -   Duplicate LDC entries appear in Cloud Workspace Asset Explorer
        -   Manage access through predefined query access controls for all Cloud Workspace tables
-   **Version 2.3.1 - March 2026**
    -   New: Introduced Cloud Cost findings in the Cloud Workspace, surfacing cloud account budget and spend data for accounts with a CCM license to provide visibility into budget compliance and variance for better cost governance.
    -   Changed: Updated the Cloud Workspace to display both budget and spend data per cloud account for green field accounts. Accounts created through the Cloud Workspace with a specified budget allow you to track spend against the defined budget and monitor parameters such as variance.
-   **Version 2.2.0 - December 2025**
    -   Cloud Workspace provides a centralized, consistent experience for managing all ServiceNow cloud solutions as part of the Cloud Governance Suite. It uses a unified data model to ensure that different cloud features work seamlessly together and share the same information, reducing silos and improving visibility.
    -   One of the key features in Cloud Workspace is Cloud Account Management \(CAM\), which is available through the ITOM Cloud Accelerate offering. CAM focuses on automating the entire cloud account lifecycle—from requesting and provisioning new cloud accounts to managing their governance, suspension, reactivation, and certification.
    -   By using CAM, organizations can significantly reduce the time and manual effort required to onboard and manage cloud accounts. It automates critical processes like CMDB population with cloud ownership data and service mapping, ensuring that every cloud resource is properly tracked, owned, and aligned with the organization’s compliance and governance policies.
    -   In addition to automation, CAM brings business context to cloud operations by linking cloud accounts to application services and business applications. This improves transparency and helps stakeholders understand how cloud usage supports broader business goals.
    -   Overall, Cloud Workspace with Cloud Account Management empowers IT teams to manage cloud accounts at scale, improve compliance, and deliver cloud services more efficiently using automation and dashboards designed for both cloud managers and account owners.

**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)


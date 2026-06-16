---
title: Microsoft Exchange Online for Security Operations release notes
description: Version history for the Microsoft Exchange Online for Security Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-ms-online.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft Exchange Online for Security Operations release notes

Version history for the Microsoft Exchange Online for Security Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.7.4 - June 2026**

    Fixed: Email search by subject line keywords returned no results because the Hunting API query used exact match \(==\) instead of keyword match \(has\) for the Subject field.

-   **Version 10.7.3 - March 2026**
    -   Fixed:
        -   Comments entered while rejecting email requests are now correctly reflected in the associated Security Incident Response.
        -   Email search requests no longer fail when the subject query contains quotation marks.
-   **Version 10.7.2 - January 2026**

    Fixed: Fixed an incorrect “email search is still running” message shown during the deletion approval step.

-   **Version 10.7.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.6.5 - May 2025**

    Fixed: Remove/hide unsupported email fields from the email search criteria.

-   **Version 10.6.3 - February 2025**

    Changed: Migrated workflows to flow designer.

-   **Version 10.6.2 - March 2024**
    -   Fixed:
        -   Supports non-ANSI characters in Threat-Hunting API query.
        -   Supports Graph URL configuration for Federal customers.
-   **Version 10.5.5 - December 2023**

    Fixed: Addressed the misconfiguration of table/field ACLs within the com.snc.secops.ms.exchange.online plugin.

-   **Version 10.5.2 - November 2021**
    -   Fixed:
        -   Added additional password-related policies.
        -   Failure of Email search, if the Exchange Module V2 is not present in MID server.
        -   Termination of Email search workflow because of an activity count limit.
        -   Improved PowerShell error logging for proper stack trace if an error is seen in the processing.
-   **Version 10.5.0 - August 2021**
    -   New: Support for Multi Factor Authentication \(MFA\) at the Tenant Level
    -   Fixed: Ability to delete emails from the email server through the UI action - 'Delete Emails from Exchange Online' that is present under the Email Search Results section
-   **Version 10.4.2 - February 2021**

    Fixed: This release includes a fix from double encoding a query to single encoding, to address the functionality change by Microsoft Graph API. Microsoft Graph API has modified their functionality which causes no results to appear when running a query. For example, if the subject contains a space, then results don't appear. Only the count of emails is returned. A system property sn\_sec\_ms\_ex\_on.single\_encode has been added to specify the use of single encoded or double encoded search queries. It defaults to single encoded queries.

-   **Version 10.4.1 - December 2020**
    -   New:
        -   A security tag is applied to a security incident, and a work note is created when the search and delete action fails.
        -   An error email notification is sent to a group, and a work note is created when the Microsoft Exchange Online OAuth credentials expire.
    -   Changed:
        -   Email Search and delete action includes junk folder for matching phishing emails and deletes them.
        -   Email Search Result record is created when the search and delete action fails.
-   **Version 10.3.2 - June 2020**
    -   New: Additional setting Email Result Threshold for Approvals
    -   Changed: Threshold configuration for Request Delete Approvals
-   **Version 10.0.1 - March 2020**
    -   New:
        -   Introduced troubleshooting capabilities by adding diagnostics tests that provide the ability to isolate issues with the integration
        -   New system property added to increase debug level logging
    -   Fixed: UI alignment of buttons present on the Microsoft Exchange Online configuration settings
-   **Version 8.0.3 - September 2019**

    Fixed:

    -   Improved error handling for unsupported characters
    -   Fixed support for valid special characters such as apostrophes, double quotations, and colons \(PRB1358086\)
-   **Version 8.0.2 - August 2019**
    -   New:
        -   Additional Settings parameters for Maximum Search Duration and Search Completion Notification
        -   MID Server Routing Changes: Provides ability to selectively route the integration searches to designated MID Servers that have the necessary MID Server capabilities enabled \(instead of all MID Servers\)
    -   Changed:
        -   Application tile configuration modifications: With the MID Server routing changes in this update, it is no longer necessary to designate a MID Server during the initial authentication set-up. In addition, there is a new status indicator for the MID Server Ready that will distinguish an authentication credential problem from a MID Server availability issue.
        -   Approval rejection notes are now posted to the work notes when an approval is rejected and the approver provides a reason to the SOC analyst.
        -   Email search results now contain the full message details, including the subject field that was missing with some platform versions.
    -   Fixed: Searches were previously not able to retrieve matching messages when the subject contained special characters, such as \#. Special characters are now supported in the email subject parameter for searches.
-   **Version 5.0.0 - March 2019**
    -   Configure search criteria for phishing threats in Security Incident Response based on combinations of the sender, recipient, and subject fields on email messages.
    -   For large and lengthy email searches, the security incident analyst is notified via email when a search is successfully completed, along with the number of matched messages.
    -   Status for individual messages informs you if recipients have read or deleted suspicious emails.
    -   If configured, optional approval processes ensure that suspicious emails are not deleted without prior approval.
    -   A complete audit trail for delete requests that includes the number of deleted emails is logged in the work notes of security incidents.
    -   If tagging is configured, security tags record when email search and delete workflows are initiated and successfully completed on security incidents.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


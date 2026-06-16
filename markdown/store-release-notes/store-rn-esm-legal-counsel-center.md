---
title: Legal Counsel Center release notes
description: Version history for the Legal Counsel Center application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-counsel-center.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Legal Counsel Center release notes

Version history for the Legal Counsel Center application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - June 2026**

    Changed: Security enhancements

-   **Version 2.1.0 - May 2026**

    Fixed: The 'Assign to me' button in legal requests now responds faster with an optimized business rule.

-   **Version 2.0.2 - March 2026**
    -   Fixed:
        -   General legal requests can no longer be transferred to the same category they currently belong to.
        -   Latest instructions on legal matter tasks are now displayed correctly while editing the instructions.
        -   The 'Select user' field in the Initiate Approval window correctly displays matching results when you enter a user name.
        -   When you select multiple legal requests on the Legal Counsel Center and then select Start Work, the status of all associated contract requests is correctly updated.
-   **Version 1.11.2 - January 2026**
    -   Fixed:
        -   Displays relevant message when users attempt to open any matter or matter artifact records without proper permissions.
        -   Resolved an issue to display legal matter draft emails with predefined filters.
-   **Version 1.11.0 - December 2025**
    -   Changed:
        -   Added notifications for Legal requests \(request assigned, comment added, request closed\). The notifications are inactive by default.
        -   The Request Type column now appears in the listing view of legal requests and related lists under parent records.
        -   The Initiate Approval modal for matters now filters the user and user group selection lists to show only those with the sn\_lg\_ops.legal\_user role.
    -   Fixed:
        -   The Knowledge Category tree picker now works correctly in Legal Counsel Center when adding or editing knowledge articles.
        -   The attachment panel is now hidden in the side panel when external storage is enabled for artifacts.
        -   Auto-refresh now works as expected when adding signatories to legal records.
        -   Users with the sn\_lg\_ops\_matter\_fulfiller role can now create matters from the Legal Counsel Center.
        -   UI improvements.
        -   Security fixes.
-   **Version 1.10.0 - September 2025**
    -   Changed: Legal Contract repository view on the Legal Counsel Center has been improved. The view has been updated to show the additional fields related to contracts, also additional related lists \(e.g. Obligations, Playbook, Executed contracts etc\) been added to show.
    -   Fixed:
        -   Localization issues have been fixed.
        -   On the All Requests listing page of the Legal Counsel Center, selecting the New action displayed matter-related intake form options instead of only request intake forms. This has been fixed.
-   **Version 1.8.5 - August 2025**
    -   New: Company field is displayed in contract request listing page in legal counsel center
    -   Changed: Enhanced all listing pages in the legal counsel center workspace to support presentation lists.
    -   Fixed: Added the required RCA and cross-scope functionality within Legal apps.
-   **Version 1.7.9 - June 2025**
    -   Fixed:
        -   The AI nudge alert in Contract Workspace now appears only when the request is in Work in Progress state, the user has the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role, and Now Assist skill is activated. Previously, the alert was shown to any watch list user regardless of state or role.
        -   For a digital forensic request, a legal matter for could not be created. This has been fixed.
        -   For an ethics compliant request, a legal user could not map Involved parties to Allegations. This has been fixed
-   **Version 1.7.6 - May 2025**
    -   Fixed:
        -   The metadata extraction results page fails to load after initiating metadata extraction and selecting Review metadata extraction. This issue has been fixed.
        -   The related list checkbox is not displayed for a legal matter. This issue has been fixed.
        -   The "Page not found" error was displayed while viewing scorecards in the Analytics Center of the Legal Counsel Center. This issue has been fixed.
        -   The "Sync document" functionality was not working. This issue has been fixed.
        -   The alert messages were displayed twice. This issue has been fixed.
        -   UI issues.
        -   Localization issues.
-   **Version 1.6.0 - February 2025**
    -   New: The system property, sn\_lg\_cf\_workspace.workspace\_typeahead\_list\_count has been added where you can specify the number of records that should appear in the suggestion list of a typehead component in Legal Service Delivery.
    -   Fixed:
        -   When adding and saving a link in the Checklist panel of a legal request, the link does not appear. This has been fixed.
        -   Dashboards on the Legal Counsel Center were not available. This has been fixed.
        -   Performance issues
        -   To create a new legal matter, go to the Matters list in Legal Counsel Center. Copy and paste the URL into a new browser tab. When selecting the option to create a new matter, the options to create a legal request appeared. This has been fixed.
        -   In legal workspace, the draft emails did not load in email composer when trying to open them. This has been fixed.
        -   Message to initiate contract analysis using Now Assist was displayed in all states of contract request instead of showing it in work in progress state. This has been fixed.
-   **Version 1.5.1 - November 2024**
    -   Fixed:
        -   In the Legal Counsel Center workspace, you were able to close complete a legal request even when information was not provided in the mandatory fields. This is now fixed.
        -   In the Legal Counsel Center workspace, when you select the Configure Workspace under the user menu, you were incorrectly redirected to the UX App Configuration of the CSM/FSM Configurable Workspace App Config. This is now fixed.
        -   Security fixes
-   **Version 1.4.1 - August 2024**
    -   Fixed:
        -   Counsel assist was not available for Sales contract requests.
        -   Translation issues observed in Create Revision pop-up in the contract request.
-   **Version 1.3.3 - May 2024**
    -   New: The filters in Legal Counsel Center have been updated to display Contract Requests and Legal Requests listings based on request state and user role.
    -   Fixed:
        -   On Legal Matter form, the Compose email action wasn't opening the pop-up window.
        -   The Comments and Compose fields do not appear on the Approval form.
        -   On the pending approval requests, the form doesn't display Comments field.
-   **Version 1.2.2 - March 2024**
    -   Fixed:
        -   Cancel approval for contracts is not working.
        -   Counsel Assist - "Flag Article" translation not shown correctly.
        -   Comments &amp; Compose fields missing on Pending Approval form.
        -   Pending approval widget on Legal Counsel Center is not opening properly when Legal Matter Management plugin is not installed.
        -   UI improvements
-   **Version 1.1.1 - November 2023**
    -   New:
        -   Enable legal fulfillers to view similar legal requests and similar legal matters in the Counsel Assist section.
        -   Enable legal fulfillers to directly chat with requesters using Agent Chat functionality.
        -   Enable legal fulfillers to search using AI Search and view results on a page that displays a list of previews for records that match your search query.
        -   The legal matter form now supports Outside Counsels and External Matters' related lists, which enable the legal fulfillers to submit outside counsel engagements for Invention Disclosure and Legal Tracker integration and to view external matter details and track spends. These related lists will be displayed when you have enabled Invention Disclosure or Legal Tracker integration related features.
    -   Fixed:
        -   Some UI issues on compose email and assigning requests.
        -   Added needed RCAs while using other practice applications.
-   **Version 1.0.8 - September 2023**
    -   Fixed:
        -   Response templates in Request and Matter.
        -   Attachment upload issues with Matter artifacts and tasks.
        -   Issues related to UI like scrolling, ordering, field gaps, lookup fields selection, error messages display.
-   **Version 1.0.5 - August 2023**
    -   Legal Counsel Center is the Next Experience Workspace for legal fulfillers replacing the Classic version. The new workspace is more configurable allowing admins to configure the workspace to meet their legal team needs.
    -   ServiceNow Legal Counsel Center is included with Legal Service Delivery and works in concert with Legal Request Management and Legal Matter Management. Legal Counsel Center helps lawyers, paralegals, and internal legal teams keep on top of all legal affairs and internal legal requests within their organization, enabling them to categorize, prioritize, and efficiently address legal requests and issues from a single interface. This version of the cousel center includes our advanced ServiceNow Next Experience configurable workspace for legal fulfillers.


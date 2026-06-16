---
title: License and Permit Playbook release notes
description: Version history for the License and Permit Playbook application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-license-permit-playbook.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Public Sector Industry release notes, ServiceNow Store release notes]
---

# License and Permit Playbook release notes

Version history for the License and Permit Playbook application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.12.5 - June 2026**

    Minor release. Added translations. Accessibility enhancements.

-   **Version 3.12.0 - May 2026**

    New: new playbook activity for gathering optional documents during application intake

-   **Version 3.11.5 - April 2026**
    -   Fixed:
        -   Geographical field values entered by the Service Applicant are now correctly displayed on the Service Applicant Record \(PRB2003648\)
        -   Resolved test failures caused by the removal of the onRecordLicensePermit method from LicensePermitImpl \(PRB1890794\)
        -   At 400% zoom, the Case Task for Requester Approval Activity no longer requires two-directional scrolling to view full content, including the message input field \(PRB1956676\)
        -   Resolved test failures caused by PriceListJSON in script include \(PRB1888583\)
        -   In Japanese environments, the "Move to Process" action button now renders correctly and is no longer replaced by "Mark Complete" \(PRB1981383\)
        -   Hardcoded strings in the License and Permit Playbook are now exposed for translation via Playbook Localization, resolving i18n issues across Public Sector Digital Services \(PRB1968514\)
        -   The Confirm Application Details activity no longer displays duplicate buttons \(PRB1980270\)
        -   Concatenated strings in the License and Permit Playbook have been separated to prevent grammatical issues in translated languages \(PRB1981033\)
-   **Version 2.1.4 - September 2025**

    Fixed: Bug fixes for versions compatible with the Xanadu release

-   **Version 3.0.6 - August 2025**

    Fixed: Resolved minor issues with creating a license and permit and price listing of a license and permit.

-   **Version 3.0.5 - August 2025**
    -   Fixed:
        -   Responsibility Field in 'Add Related Parties' Activity: Fixed to show appropriate options.
        -   Items Received Card Not Displaying: Now visible for the Business Agent.
-   **Version 3.0.4 - May 2025**
    -   Fixed:
        -   Pre-eligibility questions-related issues
        -   Form display issues
        -   Workflow status indicators showing incorrect completion status
    -   Removed: showPayment" function to improve system performance
-   **Version 2.1.2 - January 2025**

    Fixed: Ensure constituent information is auto-populating correctly in "on behalf of" application scenarios.

-   **Version 2.1.0 - November 2024**
    -   New: Playbook experience when initiating applications for licenses/permits on the constituent/business-facing portal
    -   Changed:
        -   Modified the application intake phase to provide a better experience when collecting required application information
        -   Updated the applicant data model to include business contacts
        -   Incorporated the license/permit fee summary card into the item received records on the constituent/business-facing portal
        -   Updated application labels to support accessible rich internet applications \(ARIA\) accessibility requirements.
-   **Version 2.0.2 - June 2024**

    Fixed: Resolved string literals to be translated.

-   **Version 2.0.1 - February 2024**
    -   New:
        -   Generate digital copies of licenses/permits from within the playbook with newly incorporated document template functionality.
        -   If needed, add additional inspection activities from within the playbook without having to manually configure these steps.
        -   Create and submit license/permit applications on behalf of someone else.
        -   Create and submit multi-party license/permit applications.
    -   Changed:
        -   Streamlined the approval workflow by simplifying activities performed by approvers.
        -   Improved the fee card design for better communication around how fees are impacted when license/permit configuration changes are made.
-   **Version 1.0.2 - November 2023**

    The License and Permit Playbook provides governments with a packaged playbook built to simplify and modernize the delivery of licenses and permits &amp;ndash; enabling governments to focus on providing innovative experiences for individuals and businesses, rather than developing and maintaining expensive bespoke or custom solutions.



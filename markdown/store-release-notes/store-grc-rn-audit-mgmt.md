---
title: GRC: Audit Management release notes
description: Version history for the GRC: Audit Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-audit-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Audit Management release notes

Version history for the GRC: Audit Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   Changed: Notifications in the Audit application now redirects users to the workspace experience.
    -   Fixed:
        -   The "Approver" field on the Evidence table now shows GRC business users correctly.
        -   Users can now add Auditable Units to an Audit Engagement.
-   **Version 22.0.1 - March 2026**
    -   Fixed issues:
        -   An engagement can now be moved to Closed Incomplete status even if the planned start date and end date are the same.
        -   Audit word reports can now be generated even when an engagement is marked as confidential.
        -   Resolved security-related defects.
-   **Version 21.1.5 - December 2025 \(Zurich\)**
    -   New: Added Audit Period Start and Audit Period End fields to Engagement records to enable auditing of past or future periods within an ongoing engagement.
    -   Changes: Engagement planned start dates and end dates behavior has been changed to remove rollups on the basis of Audit tasks.
    -   Fixed:
        -   Audit Engagement dates issues due to rollups are now resolved.
        -   Fixed security defects.
-   **Version 21.0.2 - August 2025**
    -   New:
        -   Implemented range queries for improved protection of queries on engagement, control test, audit task.
        -   Continuous monitoring of the EBA configurations is now enabled. The EBA restriction field is updated to reflect the new entity configuration whenever there is a change to the entity or its parent
    -   Fixed:
        -   Engagements are now copied to issues when generated from observations.
        -   Implemented security fixes.
        -   Owner of the cloud file now has access to the file irrespective of whether or not access was provided via cloud file configuration
-   **Version 20.2.0 - July 2025**

    Fixed: Resolved known bugs impacting core functionality and user experience.

-   **Version 20.1.0 - May 2025**

    New: Entity-based access capabilities now supported for Audit. EBA can be used to manage access to Engagement, Control Test, and Test Plans. \(Yokohama Patch 2\)

-   **Version 20.0.2 - February 2025**
    -   Fixed:
        -   Styling changes on audit word templates.
        -   The link on evidence request information message popup navigating user to classic workspace view.
        -   Localisation changes on dashboards
-   **Version 19.1.1 - November 2024**
    -   Changed:
        -   Domain separation is enabled for Audit
        -   Security fixes
-   **Version 19.0.5 - August 2024**
    -   New: Audit reader role for all read operations
    -   Changed:
        -   Audit users should be able to upload documents from local computer to cloud.
        -   Migrated workflows to flow designer
        -   Accessibility improvements for Audit workspace home pages and overview pages.
    -   Fixed: Access control changes in script includes
-   **Version 19.0.0 - August 2024**
    -   Changed:
        -   Ability to upload documents on local computer to cloud.
        -   Accessibility improvements for audit workspace home pages and overview pages.
    -   Fixed:
        -   Localization improvements on audit workspace
        -   Users are not able to add engagements to audit plan from audit workspace
        -   Breadcrumb changes in audit workspace
-   **Version 18.1.5 - June 2024**

    Changed: Audit dashboards are migrated to the Next Experience UI Framework.

-   **Version 18.0.1 - February 2024**
    -   Fixed:
        -   Duplicate entries in audit plan activities.
        -   Engagement Field work planned end date is not populated correctly.
-   **Version 17.0.2 - January 2024**

    Fixed: Access control changes for report template field on engagement table.

-   **Version 17.0.1 - August 2023**
    -   Changed: Access controls for tables extending planned task.
    -   Fixed:
        -   Engagement form shows duplicate fields for planned date
        -   Engagement is not populated on observations created from control test
        -   Duplicate issues are created when observation is finalized
-   **Version 16.0.2 - February 2023**
    -   Changed:
        -   Ability to associate multiple Engagements to the same issue
        -   Ability to scope common controls and reliant entities in Engagements
        -   Support for Localization
    -   Fixed:
        -   Accessibility issues
        -   Engagement Generate Report does not translate multiline strings and HTML fields properly
-   **Version 15.0.3 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.2 - August 2022**
    -   New:
        -   Categorize Audit Engagements, Audit Tasks, Control Tests, etc. based on Functional Domains like IT Compliance and Risk, Privacy, etc.
    -   Fixed:
        -   When an Engagement is Closed Incomplete, related Control Tests are still Open.
        -   Audit Manager should not be allowed to Close an Engagement when related Tasks are Open.
        -   When we create a test template, unable to select the Control Objective field values which have lengthier display names.
        -   Security constraints on Client Callable script includes.
        -   When a Engagement is created from Entity form, newly created Engagement is not coming up in Downstream Engagements of Entity.
-   **Version 14.2.1 - May 2022**

    Changed: Updated Angular version

-   **Version 14.1.1 - March 2022**
    -   New: Security changes
    -   Changed: Security updates
    -   Fixed:
        -   When an issue associated with control test is moved to "Closed Complete" state, a new issue is created.
        -   On upgrading to Quebec, blank entities are added to the engagement.
        -   Unable to close control test if there is an audit task on the same engagement that is in closed complete.
-   **Version 13.0.2 - September 2021**
    -   New: Added support for Workspaces
    -   Fixed:
        -   Control tests are not generated but message says 'Control tests are generated'
        -   Security issues
-   **Version 12.0.2 - June 2021**

    Fixed: Security issues Audit tasks are not created when trying to generate test plans if the controls are retired but it still displays a message saying "Control tests have been generated"

-   **Version 12.0.1 - March 2021**
    -   New: Added support for GRC Workspaces
    -   Fixed: Addressed Engagement Closed state issues, Audit task issues.
-   **Version 11.0.2 - October 2020**
    -   New: Introduced fields to capture engagement start and end dates.
    -   Changed: Modified issue dates rollup logic to engagement.
-   **Version 10.1.0 - June 2020**

    New: Quick start tests for Audit Management have been added.

-   **Version 9.0.0 - November 2019**

    This application was originally released in Kingston and is still compatible with New York. See the section Supporting Links &amp; Docs for release notes and product documentation.



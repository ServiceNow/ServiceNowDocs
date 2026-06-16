---
title: GRC: Business Impact Analysis release notes
description: Version history for the GRC: Business Impact Analysis on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-business-impact-analysis.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Business Impact Analysis release notes

Version history for the GRC: Business Impact Analysis on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.2 - June 2026 \(Australia\)**
    -   New:
        -   Overview pages now display stepper and descriptions for BIA/Plan and Event records. All users can view enhanced overview pages with stepper navigation and contextual descriptions, improving clarity and workflow guidance.
        -   Admins and users can now create, edit, read, delete, and duplicate PA dashboards. Access controls ensure BCM Admins have full dashboard management, while all personas can read default dashboards and create new ones. Users can manage their own dashboards and duplicate any dashboard they can read.
    -   Changed: Overview tab data is now filtered and configurable via UIB properties.\*\* The overview page script has been updated to use configurable table and field properties, enabling more flexible data presentation and filtering.
    -   Fixed:
        -   Dependencies in Impact Dependency Groups now display correctly for BIA records. The issue where certain dependencies appeared empty has been resolved; dependencies are now properly shown when blocked.
        -   The View/Edit buttons in the Impact Assessment confirmation modal now function as expected. Missing client script calls have been added, restoring correct button behavior.
-   **Version 10.0.0 - March 2026**

    Localization and breadcrumb fixes in list view.

-   **Version 9.1.2 - December 2025 \(Zurich\)**
    -   New: Added Finalized RTO field to replace and consolidate previous RTO and Adjusted RTO \(Same change for RPO\)
    -   Changed: Changed charts and list columns where it would have both RTO and Adjusted RTO to only show the Finalized RTO \(Same change for RPO\)
-   **Version 9.0.1 - August 2025**
    -   New:
        -   Generate the Word report using the template using the Report Generation API and UI actions with pop-up to select template
        -   Create Word template, data relationships, content configurations, setup manifest file and design word template for BIA
-   **Version 8.1.2 - June 2025**

    Fixed: PDF generation is not working correctly when Hungarian characters are used.

-   **Version 8.1.1 - May 2025**
    -   Updated:
        -   Added a progress bar for 'Update dependencies' in BIA
        -   Add 'View progress' button in Dependencies screen
        -   Enhanced BIA approval flow with run as configuration setting
    -   Fixed: Element definition filters are not evaluated properly in BIA
-   **Version 8.0.3 - February 2025**
    -   New:
        -   Integrated Business impact analysis with Smart Assessment Engine
        -   BIA can use either Smart Assessment Engine or legacy impact analysis questionnaire for analysis
        -   BIA .pdf updated with new fields from Smart Assessment Engine
        -   Added new field to capture "Maximum tolerable period of disruption"
-   **Version 7.1.2 - November 2024**
    -   Changed: Review sandbox access for client callable scripts
    -   Fixed:
        -   Security table ACL bypass issue
        -   Dependency Group state flips from "Pending" to "not Started"
        -   BIA - bcm manager is owner and planner is unable to edit the BIA if they copy the BIA. RTO can be updated on homepage by BCM manager, add warning for missing mapping between timeframe and recovery tier
-   **Version 7.0.1 - August 2024**
    -   Changed: Added new fields on dependency assessments: related item BIA, related item RPO, related item RTO, related item recovery tier
    -   Fixed:
        -   Disruption choices field displaying wrong selection for choice in dependency assessment.
        -   After a copy of the BIA is created, the RTO value is not calculated correctly from assessments.
        -   The helper text for the impact category is not being displayed correctly if it is too long.
        -   In dependency assessment, values from disruption duration were not getting retained even though the category is set to complete.
-   **Version 6.1.4 - July 2024**

    Fixed: Fixed app compatibility for the glide family releases.

-   **Version 6.1.3 - June 2024**
    -   New:
        -   Added feature to configure BIA dependencies using UI policies
        -   Added feature to configure BIA dependencies using element variables
        -   Added feature to configure BIA dependencies using dictionary updates
        -   Added fix script to fix existing data after metadata change
        -   Update the dependency assessment UI page to support BIA dependency changes
    -   Fixed: Security fix for GlideRecord encoded query.
    -   Removed: Mandatory validation for RRTO.
-   **Version 6.0.3 - February 2024**
    -   New:
        -   Added configuration to set manual or automated updates from CMDB
        -   Added dependency update support from CMDB
        -   Added email notification for updates from CMDB
    -   Fixed:
        -   Fixed BIA assessment tab refresh issue
        -   Fixed missing "Link BIA" UI action
        -   Fixed configuration item for CI in BIA dependency
        -   Fixed view rule for dependency and dependency group
        -   Fixed security gap for BIA flows
        -   Fixed missing PDF UI action in the approved state
-   **Version 5.0.2 - August 2023**
    -   New:
        -   -   Added business impact analysis in the new BCM Next Experience workspace
-   Added pending business impact analysis activities in My Task
-   Added a new homepage tab for business impact analysis
-   Added a new overview page with a stepper component for states
-   Added business impact analysis modules in the List view
-   Added new UI experience for the Assessments tab in BCP
-   Added new UI experience RPO assessment
-   Added new UI experience for RTO assessment
-   Added new UI experience for dependency assessment
    -   Fixed: Accessibility and localization issues
-   **Version 4.1.0 - May 2023**
    -   Fixed:
        -   BIA limitation to add only 20 dependencies. Added a configurable property to update the dependencies limit.
        -   Fixed the lookup reference dropdown field to display the number of dropdown items based on system property.
-   **Version 4.0.0 - February 2023**

    Fixed:

    -   When a BIA is done at Level 1, the dependencies are auto-pulled, and the assets at the third level are listed twice.
    -   Add missing domain separation for BIA approvals.
-   **Version 3.0.3 - December 2022**

    Fixed: Fixed parent POM in order to remove the redundant GLIDE-INF folder and content contained within.

-   **Version 3.0.2 - August 2022**
    -   Changed:
        -   For BCM event scoping changes, updated BIA plan form
        -   For BCM event scoping changes, restricted copy to the user that can write to BIA only
    -   Fixed:
        -   BIA impact categories
        -   Accessibility for charts in BCM workspace
        -   Fixed security gaps for HTML injections in BIA
-   **Version 2.3.2 - March 2022**
    -   New:
        -   Ability to copy Business impact analysis.
        -   Ability to configure grid columns per dependency element and zoom out to a full-screen mode.
        -   A new contributor role is introduced and users with this role will have limited privileges and will be able to participate in BIA assessments.
        -   Enabled multi-language support and included translations.
    -   Changed: 'Add dependencies' action is moved from UI form action to within the grid.
-   **Version 2.2.2 - November 2021**
    -   New:
        -   Ability to generate BIA PDF
        -   Ability to set up multiple levels of approvers and route BIA for approval
        -   Impact assessment and dependency assessment are ordered according to the BIA template
    -   Changed:
        -   Lifecycle UI action behavior is modified to accommodate approval flow
        -   BIA is set as read only in Pending Approval, Approved, and Archived states
-   **Version 2.1.2 - June 2021**

    New: Support for adding dependencies from CMDB

-   **Version 2.0.1 - March 2021**
    -   New: Support for assessing impact to find the recovery point objective
    -   Changed: Setup for impact assessment supports definition of question and its corresponding rating for impact categories used for RPO assessment.
-   **Version 1.0.3 - October 2020**
    -   New:
        -   All new user experience for Business Impact Analysis.
        -   Streamlined integration with ServiceNow CMDB for business processes and asset inventories
        -   Role-based workspace with customizable reports and dashboards

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)


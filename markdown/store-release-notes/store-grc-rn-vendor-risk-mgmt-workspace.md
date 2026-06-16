---
title: GRC: Vendor Risk Management Workspace release notes
description: Version history for the Vendor Risk Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-vendor-risk-mgmt-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Vendor Risk Management Workspace release notes

Version history for the Vendor Risk Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Added SBOM \(Software Bill of Materials\) related lists to company and engagement records.
        -   Added vertical layout configuration for TPRM navigation menu.
        -   Added aria-labels for risk concentration map accessibility.
    -   Changed:
        -   Updated questionnaire template list to show only published templates.
        -   Changed risk activity icon and removed extra spacing in work queue cards.
        -   Removed business user role from vendor detail page widget to improve security.
        -   Updated UCM portal access from risk manager to risk\_admin only.
    -   Fixed:
        -   Resolved approve/reject UI action button visibility after Zurich upgrade \(PRB2012105\).
        -   Corrected return to third party modal due date validation and messaging \(PRB2017639\).
        -   Fixed internal risk score display in assessment overview when SAE enabled \(PRB2007798\).
        -   Resolved engagement location pin visibility on geo map with null values \(PRB2013149\).
        -   Added missing tooltips for buttons across VRM workspace pages \(PRB2010437\).
        -   Fixed UI component rendering at 400% zoom resolution \(PRB2010399\).
        -   Corrected include previous responses editability for internal assessments \(PRB2007197\).
        -   Restored missing templates sidebar item for issues records \(PRB1996880\).
        -   Resolved duplicate audit creation issue \(PRB1992222\).
        -   Fixed return to third party questionnaire action visibility \(PRB1988955\).
        -   Corrected smart assessment component viewport height calculation \(PRB1965536\).
        -   Resolved store certification filename collision error \(PRB1989896\).
        -   Fixed missing New UI action button in Element related list \(PRB2024156\).
-   **Version 22.0.3 - March 2026**
    -   New: Updates have been made to support new issue recommendation skill
    -   Fixed:
        -   Missing configuration for My group's tasks has been added.
        -   An issue where, after upgrading to Zurich, submitting an external questionnaire on behalf of a vendor set the questionnaire status to Returned instead of Received has been resolved.
        -   Workspace alignment issues have been addressed.
-   **Version 21.1.5 - December 2025 \(Zurich\)**
    -   New:
        -   Integration with Document Management System so that accessors and reviewers have the ability to manage all vendor documents in one place along with the ability to reference them across the engagements of that vendor.
        -   Vertical navigation has been introduced across the Vendor Risk Management workspace to improve the experience for Third-party Risk Management application users.
        -   Risk area as related list for internal assessments has been introduced.
    -   Changed:
        -   Upgraded record page template for company records and all other records across the workspace to address missing vertical tabs and improve layout for horizontal scrolling.
        -   Coral theme improvements have been done to improve the borders around widgets in the workspace.
    -   Fixed:
        -   Accessibility issues, including horizontal scrolling and translation issues where strings were not translating as expected, have been addressed.
        -   Issue where the Discuss dialog did not populate the subject from external risk assessment and the discussion was not shown in the activity stream.
-   **Version 21.0.2 - August 2025**
    -   New: The Vendor Risk Management Workspace has been updated to work with Smart Assessment Engine \(SAE\) facilitating, creating, editing, and viewing assessments using SAE.
    -   Changed:
        -   Global TPRM changes
            -   Assessments and Third-party assessments are now renamed as External assessments.
            -   Tiering assessments are now renamed as Internal assessments.
            -   The Tier-level column is now renamed as Risk rating.
            -   The Tiering assessors column is now renamed as Respondents.
            -   The Owner field is now renamed as Assigned to on the internal assessment, external assessment, tiering assessment, and due diligence request forms.
        -   Changes made to the list view in Vendor Management Workspace
            -   The Assessment setup section has been added. From this section, you can create assessment templates, Smart Assessment questionnaire templates, and issue generation rules.
            -   The Questionnaire requests section has been added.
            -   The Tiering assessments and Inherent risk questionnaires \(IRQ\) are combined in the Internal assessments section.
        -   Changes made to internal assessment pages
            -   Tier-level scales are renamed as Scales.
            -   Tiering assessment schedule and Schedules are combined and renamed as Assessment schedule.
        -   Changes made to assessment related lists
            -   Assessment instances is renamed as Questionnaire requests.
            -   Questionnaires is renamed as Questionnaire templates.
            -   Document requests is renamed as Document templates.
            -   Fourth-party questionnaires is renamed as Fourth-party templates.
            -   Repeating assessments is renamed as Assessment scheduling.
-   **Version 20.1.2 - May 2025**
    -   New: Added TPRM Workspace Health Dashboard.
    -   Updated: Changes to improve workspace performance.
    -   Fixed:
        -   Accessibility violations have been addressed.
        -   i18n translation issues have been addressed.
-   **Version 20.0.2 - March 2025**

    New: 'Business Capability' has been added as a Function type that can be selected from a drop-down list on a Function record. The Business Capability records being referenced are from the cmdb\_ci\_business\_capability table.

-   **Version 20.0.1 - February 2025**
    -   New: Added third-party insights dashboard and  TPRM  custom analytics dashboard along with the ability for users to create custom dashboards.
    -   Fixed: Fixed the issue of overview sidebar details not showing up for some specific users in the Vendor Management Workspace.
-   **Version 19.1.2 - November 2024**
    -   New:
        -   Added modules for Digital Operational Resilience Management tables to support DORA.
        -   Added Digital Operational Resilience Management Roles to third-party roles.
-   **Version 19.0.2 - September 2024**

    Fixed: Third-party Risk Management Workspace widgets not loading in overview pages.

-   **Version 19.0.1 - August 2024**
    -   Fixed:
        -   Stepper component on any overview page in the Vendor Management Workspace was not auto-refreshing.
        -   'Total Engagements' widget of the Vendor Management Workspace for the 'Low' section was not permitting drill-down.
        -   When selecting 'Save' on the Vendor Management Workspace assessment form, an unexpected confirmation pop-up appeared after no changes were made to the 'risk rating valid to' field.
    -   Changed: We've made some changes to the workspace's steppers so whenever the underlying record's state is changed, the stepper is also updated to reflect the correct step/state. Workspace stepper correctly reflects state change.
-   **Version 18.1.1 - June 2024**

    Changed: Updated dependency of this app to latest version \(18.1.3\) of GRC: Common Workspace Elements.

-   **Version 18.0.1 - February 2024**
    -   New: View and manage Event-driven Management Rules in the Vendor Risk Management Workspace.
    -   Fixed:
        -   Choices in the dropdown on Lifecycle Management page for request types were not viewable for TPRM users.
        -   Changing the request type on the Lifecycle Management page sometimes resulted in the charts showing no data.
        -   The Work Queue page did not show up when Third-party Risk Due Diligence application was not installed.
        -   Questionnaires were not showing in the Third-party Risk Assessment Risk Overview tab when there were more than 5 questionnaires.
        -   New record button on the Landing Page report drilldowns were not working properly.
        -   Improved screen reader functionality
-   **Version 17.0.4 - November 2023**
    -   Fixed:
        -   Issue loading Risk Concentration Map
        -   Improved translations
-   **Version 17.0.2 - August 2023**
    -   New: Added support for Third-Party Due Diligence application \(if applicable\).
    -   Changed: Updated compliance of workspace for Dark Theming.
    -   Fixed: Various WCAG 2.1.1 compliance issues.
-   **Version 17.0.1 - August 2023**
    -   New
        -   Risk Concentration Map
        -   Due diligence request item added to the employee portal
        -   Due Diligence workflows for:
            -   Onboarding
            -   Renewals
            -   Additional Due Diligence
            -   Offboarding
        -   Automatic trigger of external questionnaires based on answers to IRQs \(inherent risk questionnaires\)
-   **Version 16.0.0 - February 2023**

    Fixed: Adjusted Discuss button functionality to work on VRM Task tables

-   **Version 15.0.7 - November 2022**

    Fixed: Issue where the installation of the Vendor Risk Management application caused approval buttons in the Advanced Risk Management application to not display on the Advanced Risk Assessment record.

-   **Version 15.0.6 - August 2022**
    -   New:
        -   Updated Third Party Scores page in Workspace view of Vendors
        -   Updated overview and landing page reports to incorporate Third Party Score roll ups
    -   Fixed:
        -   Removed the 'Run point scan' property in the workspace
        -   Improved translation support
-   **Version 14.1.2 - March 2022**
    -   New:
        -   Added 4th Party Risk Assessment pages to workspace
        -   Added 4th party metrics reporting on home page and overview pages
    -   Fixed:
        -   Fixed inconsistency in the breadcrumb across workspaces
        -   Increased workspace performance times
        -   Fixed workspace appearance issues in Dark Mode
-   **Version 14.0.0 - February 2022**

    Changed: Updated for San Diego platform compatibility

-   **Version 13.0.1 - September 2021**

    New: Vendor Management Workspace containing updated UI and reporting



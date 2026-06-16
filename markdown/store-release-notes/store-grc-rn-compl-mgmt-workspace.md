---
title: GRC: Compliance Management Workspace release notes
description: Version history for the GRC: Compliance Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-compl-mgmt-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Compliance Management Workspace release notes

Version history for the GRC: Compliance Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Policy authoring now supports a hybrid authentication approach for Google Drive and Sharepoint, using both personal and service accounts:
            -   Actions such as creating, connecting, and uploading documents use personal authentication.
            -   Actions such as enabling or disabling sync, updating links, and finalizing the playbook use the service account.
        -   An alternative DOCX-to-HTML conversion API is now available for Policy authoring, resolving overlapping text issues in translated Knowledge articles caused by the current GroupDocs-based API. Note that output formatting may differ from the current API.
        -   A dashboard landing page is now available on the left panel of the Compliance Workspace.
        -   Control, entity, and user information is now displayed in control attestation \(smart assessment\) lists across the Compliance Workspace.
    -   Fixed issues:
        -   This release resolves the following issues:
            -   Translate button not functioning on the Compliance Workspace.
            -   Workspace View rule not working as expected due to conflicts between the record view and the popup view.
            -   Control status value briefly appearing and then disappearing after the page finishes loading.
            -   Policy text losing spacing and formatting when viewed from the Policy Text tab compared to the Details tab.
            -   Homepage report population job causing out-of-memory issues that require multiple node restarts.
-   **Version 22.0.1 - March 2026**
    -   New:
        -   Workflow introduced on control objectives:
            -   Major and minor updates can be done on a separate record instead of the current active record.
            -   Owners and owning groups added on control objectives.
            -   Dynamic approvals enabled
            -   Auto-publish of control objectives based on the Effective date
            -   Workflows/reports updated to exclude working drafts.
            -   All control objectives will have a record nature as the current version, and active ones will be published by default.
    -   Changed: Minor update done on a control objective will not move a control back to draft.
-   **Version 21.1.3 - December 2025 \(Zurich\)**
    -   New:
        -   Enhanced reports on Citation and Authority document overview pages to consider the associated Citations to Controls
        -   Enhanced reports on Compliance homepage to consider the associated Citations to Controls
        -   Enabled DORA content accelerator installation from Compliance workspace \(available on Yokohama platform onward when Unified Content Management is also installed\)
    -   Fixed:
        -   Google Docs Integration for Policy did not work if file was in the root folder
        -   The "Compare" button on the KB version in the Compliance Workspace is not working as expected.
        -   Breadcrumb issue for new records
        -   Unexpected updates to the state of created controls if the control objective is associated \(via the document field\) with a policy due to fields being copied from content
        -   The user's response was always showing up in the form even when the conditions were not satisfied
        -   The "Combine" declarative action did not work for the list view in Compliance workspace
        -   The list view title is misleading for compliance analyst role users when opening the classic attestation from the Home page
        -   The Edit button was missing for Authority Documents on Compliance Workspace
        -   In the Compliance workspace, for Authority Documents and Citations, under the "most non-compliant document" tab, data was showing for both active and inactive records
        -   The Combine button was missing for Smart Assessments on the GRC Task page in Compliance workspace
        -   Security fix for the issue where users without record creation or field write access were able to create related list records
    -   Changed: The related list under Control objectives now shows associated PaCE policies for integrations with the Policy-as-a-Code-Engine
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Improved user experience:
            -   Card containers with rounded corners and drop shadows are implemented to improve the user experience of widgets on home pages, overview pages and sidebars of Policy and Compliance table records.
            -   The grey background has been removed from home pages to improve the user experience.
    -   Fixed:
        -   Compliance manager/Contributor were unable to view the images under the policy text.
        -   Identical assessments were shown across all control objectives when clicking the pie chart under attestations in Control Objective Overview page.
        -   When attempting to 'Add from existing control' on a reliant entity for a control in the Compliance Workspace, the pop-up modal appeared condensed with incorrect view.
    -   Removed: Removed the Tasks section from the home pages.
-   **Version 20.1.2 - May 2025**
    -   Fixed:
        -   Fixed accessibility issues related to label drop-down and zoom issues on home pages and custom pages
        -   Fixed typography issues for the CORAL theme across the Compliance Management workspace.
    -   Removed: Issue data visualizations from the homepages
-   **Version 20.0.2 - February 2025**

    Changed: Control attestations using smart assessments.

-   **Version 19.1.1 - November 2024**
    -   Changed:
        -   Upload local documents to OneDrive
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimizing zoom capabilities.
    -   Fixed:
        -   User should be able to create an Audit plan from the Compliance workspace
        -   User should be able to add reliant entities to common controls
-   **Version 19.0.1 - August 2024**
    -   New:
        -   When authoring policies, enable users to collaborate on policy text by connecting Google documents to policy.
        -   When authoring policies, enable collaboration on SharePoint.
        -   Support for the Cyber Risk Institute \(CRI\) accelerator. Ability to map CRI assessment questions to control objectives. Perform CRI assessments on entities and create controls based on assessment responses. Evaluate the control compliance status based on the assessment response.
    -   Changed: Accessibility improvements on compliance workspace homepages and overview pages.
    -   Fixed:
        -   Incorrect filters on the Attestations widget on the compliance workspace homepage.
        -   The citations sidebar does not show control objectives associated with risk statements.
        -   Control attestations launched from the compliance workspace are displayed in the classic view instead of the workspace view.
        -   The user is not able to map policies to issues in some scenarios.
-   **Version 18.1.0 - June 2024**

    Fixed: When navigating to different list forms from the Compliance workspace, the URLs must change depending on the list selected.

-   **Version 18.0.1 - February 2024**
    -   New: Policy authoring on Google Drive.
    -   Changed: Policy dynamic approvals.
    -   Fixed:
        -   Users are not able to associate citations, policies, or indicator templates with control objectives from the workspace.
        -   The user name should be displayed in the compliance workspace home pages greeting string.
        -   The skip button is not coming up in the policy redlining playbook.
        -   Indicator form is getting saved even though the next run date is in the past.
-   **Version 17.0.1 - August 2023**
    -   Changed:
        -   Workspace record pages are migrated to risk record page template which extends standard record page template.
        -   Ability to see policy knowledge articles on employee center.
        -   Ability to group control attestations on risk portal.
        -   Policy redlining changes
    -   Fixed:
        -   View Article is not working in compliance workspace for a published policy.
        -   Alignments on issues landing page.
-   **Version 16.0.3 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.2 - February 2023**
    -   New:
        -   Ability to create common controls and associate reliant entities
        -   Ability to associate multiple policies/controls/control objectives with the same issue and vice-versa
    -   Changed:
        -   Next Experience dark theme support
        -   Accessibility support
-   **Version 15.0.3 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.2**
    -   New:
        -   Workspace for IT Compliance Manager to manage Compliance tasks
        -   Categorize Compliance Objects like Policies, Authority Documents, Control Objectives, Citations, Controls etc. based on Functional Domain like IT Compliance and Risk, Privacy etc.
    -   Fixed:
        -   Policy Valid to date should not be in the past
        -   Policy Owner is not able to Retire a policy
        -   Additional Comments section is disabled for Policy Owner/Policy Approval when the Policy is in Awaiting approval state
        -   Localization issues
-   **Version 14.1.1 - March 2022**
    -   New:
        -   Policy authoring and redlining capabilities using O365 integration
        -   Security updates
    -   Changed:
        -   Changes on the Tasks page
        -   Indicator, risk widgets on control objective overview reports
        -   Confirmation message when a control objective is made inactive
    -   Fixed:
        -   The confirmed risk event is not displayed on issue triage
        -   Clicking "Configure workspace" directs to the base Agent Workspace configuration page instead of the compliance workspace configuration
-   **Version 14.0.0 - February 2022**

    Changed: Updated for San Diego platform compatibility.

-   **Version 12.0.2 - March 2021**

    Compliance Workspace is a single-pane view for compliance manager to view the overall compliance posture of the organization, track time-sensitive issues, high risk exceptions, ongoing policy acknowledgements and new regulatory changes. The workspace allows the compliance managers to define and manage compliance library, test effectiveness of the controls as well as continuously monitor the control performance through KCIs.



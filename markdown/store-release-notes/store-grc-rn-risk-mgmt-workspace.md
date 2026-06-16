---
title: GRC: Risk Management Workspace release notes
description: Version history for the Risk Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-risk-mgmt-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Risk Management Workspace release notes

Version history for the Risk Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   The 'Not Applicable' flag in the Risk Assessment section for control effectiveness and residual assessments can now be hidden by configuring the Risk Assessment Methodology.
        -   Smart Assessment Control Attestation is now integrated within the Task page.
        -   Entity setup is now available in Risk Workspace for Operational Risk Managers.
        -   A feedback side panel has been added to Risk Assessment projects to collect and manage feedback within risk assessment projects.
        -   Metric import job and template modules are now available to support data imports.
        -   Notification links now redirect users to the Risk Workspace based on their access permissions.
        -   The "Applies To Record" and "Entity" columns are available in the task list for Smart Assessment-based risk identification. These columns help identify the correct task without opening each record.
-   **Version 22.0.2 - March 2026**
    -   Fixed:
        -   Removed the search icon from reference fields in modal dialogs to align with design standards and prevent opening a modal on top of another modal. Users can continue to search for reference data by typing directly in the field.
        -   Fixed multiple issues in the Risk Workspace Risk Assessment flow where the risk response tasks were not displayed correctly, could not be deleted in non‑English languages, or could be created outside an assessment. These issues could result in incomplete approval routing and visibility gaps.
        -   Fixed an issue where theView All link in the Action Items widget on the Risk Mitigation Overview was not functioning correctly.
        -   Fixed an issue where Risk response task on Risk Overview page was not functioning correctly.
        -   Corrected UI behavior and access control inconsistencies in risk response and mitigation tasks to ensure assignment fields behave consistently as tasks move through theDraft,Work in Progress,Review, andClosed states.
        -   Improved Risk Workspace localization by fixing issues where workspace tabs, actions, and task operations did not work or translate correctly.
        -   Fixed an issue in the Risk Statement workspace view where theRemove action under Child Risk Statements showed a success message but did not remove the selected records.
-   **Version 21.1.1 - December 2025**
    -   New: Introduced an "Active flag" in the GRC Task Page configuration and GRC Choice table; updates to these flags are now reflected in Risk Workspace.
    -   Changed:
        -   Converted existing related lists on the Entity record page into User Interface Builder \(UIB\) pages for a more intuitive experience.
            -   The ‘Downstream Risks’ list is now moved to Risks page with tabs for Directly Related, Suggested risks, and All Risks.
            -   The ‘Entity Type’ list has also been moved to a UIB page.
        -   As part of these changes, customers may experience issues related to custom actions emitting events on the 'Risks' or 'Entity Type' related lists on the Entity record page.To adopt these changes, please refer to KB2593527 for guidance.
    -   Fixed:
        -   Users can now update messages related to the Risk Assessment component without errors.
        -   Carriage returns in factor comments are now properly recognized in Risk Assessments.
        -   Fixed localization and right-to-left \(RTL\) language support issues in Heatmap.
        -   Removing a risk statement from Risk framework record now only removes the relationship; a separate delete action has been introduced to delete the record.
        -   Fixed multiple issues on the Business Operations Risk Manager homepage, including drill-down in the ‘Control–Not Assessed’ widget and updating record lists when clicking Heatmap cells.
    -   Removed: Removed the quick edit option for Risk Assessments to ensure that edits are made only on the dedicated Risk Assessment pages.
-   **Version 21.0.2 - August 2025**
    -   New:
        -   Entity Wise Risk Profile Matrix:
            -   Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.
        -   Project Risk Assessment Grid:
            -   Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.
    -   Changed:
        -   Addressed a bug where assessors were able to delete Risk Response tasks in the Risk Assessment component, even without having the GRC Manager role. The intended behavior is that only the GRC Manager should have deletion rights. However, to accommodate practical usage, the logic has been updated as follows:
            -   Only GRC Managers or assessors who created the Risk Response task within their own assessment are allowed to delete that task.
            -   Assessors who did not create the task \(e.g., tasks copied from previous assessments\) will not be able to delete it.
        -   Task-related widgets have been removed from the Home pages to improve load times. Users can now access all their assigned tasks and group tasks directly on the Task page for better visibility.
        -   Updated the navigation flow for Classic Risk Assessments in Workspace. Previously, clicking on a Classic Risk Assessment would take users directly to the assessment. With this change, users are first taken to the assessment record, where they can then click an action to open the assessment.
    -   Fixed:
        -   Resolved an issue where English-language records in the UI message \(sys\_ui\_message\) table related to the Risk Assessment component could not be edited. Users were able to modify records in other languages, but not in English, which caused challenges in customizing UI messages for the Risk Assessment module.
        -   Corrected translation inconsistencies.
        -   Risk Event tasks are now integrated on the Tasks page within the Risk workspace.
        -   Issue widgets on the Business Operation Risk Manager home page now correctly filter based on entity selection.
        -   Impacted entities on Risk Events can now be deleted properly within the Workspace.
        -   Resolved an issue where comments containing the = character were being truncated in the Risk Identification Rejection workflow.
        -   Fixed a problem where Group Approvers were not visible on the Risk Mitigation task.
        -   Addressed an issue preventing Entity Owners selected as Assessors in Risk Assessment projects from progressing from the Risk Identification state to the Assessment state.
-   **Version 20.1.1 - May 2025**
    -   New:
        -   Add tags on Risk Assessment pages for better categorization and filtering.
        -   Assessors can generate a Risk Assessment summary when submitting an assessment.
        -   Introduced Generative AI to automatically generate risk assessment summaries, helping assessors during submission and providing approvers with a quick view of progress and key insights. This feature is available exclusively with the Now Assist for IRM application.
        -   Implemented Entity-Based Access Control to improve security across key Risk Management and Advanced Risk Management tables.
        -   Enabled support for Coral theme.
    -   Changed:
        -   Renamed GRC Tasks Workspace embedded in Employee Center to GRC Portal.
        -   Deprecated the existing Risk Portal and updated navigation links from Risk Portal modules to direct users to the new GRC Portal.
    -   Fixed:
        -   Improved performance of Risk Workspace home pages by adding composite indexes to the Issue table. Since the Issue table extends the Task table, environments with a large number of Task records may experience longer upgrade times. For example, an increase of approximately 45 minutes for systems with 40 million Task records. The following composite indexes have been added:
            -   Task Type, Active, Due Date
            -   Task Type, Active, Priority
            -   Task Type, Confidential
            -   Task Type, Active, Created By
            -   Refactored Heatmap Workbench layout and fixed scaling issues to ensure smooth reflow and correct content display at zoom levels up to 400%.
        -   Enhanced the user experience in Risk Workspace for those using assistive technologies such as screen readers.
        -   Resolved an issue with drill-down functionality on dashboards containing indicator-based widgets.
        -   Fixed an issue where Risk Response data was missing or duplicated for non-English users on the Risk Assessment pages.
        -   Fixed an issue where the Risk Assessment status did not reflect as Completed when automated factors were used.
-   **Version 20.0.1 - February 2025**
    -   New:
        -   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
        -   Copy risk responses from a previous risk assessment during the reassessment of a risk assessment project.
        -   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
        -   Remove risks from a risk assessment project during the assessment to streamline focus on relevant risks.
        -   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.
    -   Fixed:
        -   Resolved performance issues on the home pages of Operational Risk Manager and IT Risk Manager to improve load times.
        -   Resolved translation issues across multiple pages.
    -   Changed:
        -   Introducing a configurable system for previewing colors in the Risk and Advanced Risk components. This system allows the use of highlighted value component colors instead of hex codes, improving theming and addressing accessibility challenges. The update ensures consistent and accessible risk rating colors across various pages, including Risk Assessment, Heatmap Workbench, Record Overview, Dashboards, and Project Summary page.
        -   Inline dashboards are now set to read-only, resolving customization issues encountered during upgrades.
-   **Version 19.1.1 - November 2024**
    -   New:
        -   Risk Assessment Project:
            -   Empower assessors to perform bulk assessments on multiple risks and controls simultaneously, with an intuitive and seamless user experience.
            -   Enable assessors to set up the assessment project's context, including name, Risk assessment methodology \(RAM\), and other relevant details.
            -   Allow assessors to scope multiple risks for evaluation as part of the assessment project.
            -   Introduce a focused UI that allows assessors to move seamlessly between different stages of risk assessment without needing to switch between multiple screens.
            -   Provide a clear and concise overview of assessment results, including an assessment summary for quick review and effective decision-making.
            -   Ensure accuracy and reliability with error handling and validation frameworks.
            -   Support dynamic approval of the Risk Assessment Project using the approval configurator.
        -   Risk Assessment:
            -   Navigate between different sections of an assessment at any point during the process.
            -   Added a new button in the header to execute automated factors.
    -   Changed:
        -   Risk Assessment:
            -   The "State" field has been replaced with the "Status" field in Workspaces. The "State" will no longer update when navigating between sections.
            -   The navigation panel has been revamped for a refreshed look and improved usability.
            -   Convenient "Back" and "Next" buttons are now always visible at the footer for smoother navigation.
            -   Section-by-section validation during navigation has been removed, implementing a validation framework that checks the entire assessment at once.
            -   Automated factors, which were previously executed on state change, will now be executed when the assessment is created, as there are no longer state changes in Workspaces.
    -   Other: The Risk portal has been deprecated, and a navigation link has been added to access the new Risk portal.
    -   Fixed:
        -   Improved the workspace experience for users with low vision or those relying on assistive technology, such as screen readers, including improved zoom functionality.
        -   Implemented security fixes.
        -   Resolved localization issues.
-   **Version 19.0.2 - August 2024**
    -   Fixed:
        -   Accessibility and localization issues have been resolved.
        -   The loading time of the Business Operational Risk Manager home page has been improved.
        -   The widget on the Business Operational Risk home page now correctly displays the count of issues.
        -   The Risk Workspace home page now excludes issues in Closed or Cancelled state.
-   **Version 18.1.1 - June 2024**
    -   New:
        -   Created a new dashboard page to view the risk-related Next Experience dashboards
        -   Supporting List page URL generation based on filters
    -   Fixed:
        -   Security issues
        -   Routing issues of risk assessment from risk record
        -   Any object assessment modal issues on the record page
-   **Version 18.0.0 - February 2024**
    -   New:
        -   Support auto-save on Risk Assessments
        -   Integration with Parallel review and feedback workflow
        -   Support formula builder in metric definitions
        -   Bulk reassignment and approval in My tasks for risk assessments
    -   Changed:
        -   Create from library option enabled from risk assessment scope playbook, risk assessment component, and risk mitigation task.
        -   Earlier, Risk assessment pages were referred from GRC Workspace. We have created an ARA workspace in GRC: Advanced Risk Application. With this change, the risk assessment content can be referenced from the ARA workspace instead of the GRC Workspace. All customizations that were made in the GRC Workspace aren't carried forward to the ARA Workspace. You must reapply those customizations to the available default pages in the ARA Workspace to see them during the risk assessment. For more information, see KB1585068.
    -   Fixed:
        -   Navigation to risk assessment homepage from the risk assessment record page
        -   Accessibility bugs
        -   Chrome console errors in the risk assessment page
        -   Enhanced security in data brokers
-   **Version 17.0.1 - August 2023**
    -   New:
        -   Revamp experience of the risk assessment scheduler and risk assessment scope using the playbook.
        -   Metric data task page integration in the Risk workspace.
        -   Review and fix the column layout for lists.
        -   AI/ML contextual sidebar on Risk event and Risk record pages.
    -   Fixed:
        -   Padding issue in the Risk event overview page.
        -   Common control was not associating to risk.
        -   Two primary action buttons was appearing on the risk assessment home page.
-   **Version 16.0.2 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.1 February 2023**
    -   New:
        -   Issue architecture-related changes
        -   Common controls-related changes
        -   Risk appetite-related changes on the risk statement records
    -   Fixed:
        -   Dark theme-related bugs
        -   WCAG bug fixes
-   **Version 15.0.2 - December 2022**

    Fixed: Reduced application installation size

-   **Version 15.0.1 - August 2022**
    -   New: Overview pages to show metric related widgets
    -   Fixed:
        -   Business op risk manger is not able to create scope in workspace
        -   Send Assessment button on Object level Assessment popup is not enabled by default
        -   Indicator template message is not being externalized for translation
-   **Version 14.1.1 - March 2022**

    New: Home page for Business Op-Risk manager.

-   **Version 13.0.4 - September 2021**

    The Risk workspace is a single-pane view for the IT Risk Manager and the Operational Risk Manager to view the overall risk posture for your organization, track time-sensitive issues, major losses, and control deficiencies that may increase the risks for your organization.



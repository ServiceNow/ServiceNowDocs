---
title: Digital Product Release release notes
description: Version history for the Digital Product Release application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-digital-product-release.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# Digital Product Release release notes

Version history for the Digital Product Release application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.2 - September 2026**
    -   New:
        -   Configurable dashboards in DPR Workspace: Release admins can add, remove, and set default layouts for widgets on the Release Overview and Release Quality dashboards without developer intervention.
        -   Record-level access control for releases: Product managers can enable restricted access to releases, limiting visibility to defined team members.
        -   Release Home Page personalization: The "My Releases" chart displays only releases where the user is a release owner or part of the release team, updating dynamically for each logged-in user.
        -   Change request page access enforcement: The view release option and release card on Change request pages are hidden from users who are not part of the release team when restricted access is enabled.
        -   Approval definition enhancements: Approval definitions support Release task as an approval source, allowing selection of fields from the Release task table and dot-walking to release fields.
        -   Additional products fields flexibility: Users can create releases without mandating Additional Products Fields, allowing greater flexibility in release configuration.
        -   Planned start and end dates in phase form: Timeline-oriented releases display planned start and end dates in the release phase form as read-only fields.
        -   Docked action buttons in modals: Action buttons at the bottom of modals are docked and always visible, improving navigation and usability.
        -   Single-scroll experience for Add Task modal. The Add Task modal provides a smooth scrolling experience without nested scroll bars.
        -   Link to release from release task form. Users can navigate directly from a release task form to its associated release for improved context.
    -   Changed:
        -   Release actions available across pages: Start Release, Re-target Release, Close Release, Complete Current Phase, and Run Policies buttons are now accessible as secondary actions on all release-related pages, including change, configuration item, release notes, timeline, tasks, policies, and scope.
        -   Release phase optional for Change and CI association: The Release phase field is no longer mandatory when associating Changes or Configuration Items to a release. The field is pre-populated based on system properties and can be changed or left empty. All CIs and Changes for a release are shown by default, with filtering available via the list filter row.
        -   Policy status rollup for multi-product releases: Policy status of newly added product phases in multi-product releases is rolled up to the primary release, ensuring aggregated compliance status reflects the weakest link among all products.
        -   Assigned to field filtering for tasks and key dates: When restricted access is enabled, only users with access to the release are shown as assignable options in Add Task and Key Date modals and side panels.
        -   Release phase list field is editable. Users can edit the Release phase list field directly.
        -   Release template management UI update: The "Manage Release Template" button has been replaced with "Edit Release Template" and the Edit overflow menu has been removed.
    -   Fixed:
        -   Approval workflow flow has been corrected and is no longer in the Draft state.
        -   The Digital Product Release Workspace refreshes correctly and displays newly added products.
        -   Creating a change request with missing required fields no longer generates erroneous errors.
        -   The Next button in DPR works as expected when creating a change request, allowing users to advance after selecting a template.
        -   Release target durations are accurately reflected in the Release Calendar upon record creation.
        -   The timeline component is reliably rendered in the UI.
        -   Policies widget on the dashboards handles long release phase names without chart rendering issues.
-   **Version 2.5.0 - June 2026**
    -   New: Product-level release settings: Product managers can define release behaviors per product, including release calendars, release templates, CI classes, and change models. When creating a release, only the calendar, templates, change models, and CI classes configured in the product-level settings are available, ensuring teams work within approved defaults.
    -   Changed:
        -   Release execution usability enhancements: Release owners can navigate to release tasks and release policies in a single click, with simplified navigation and optimized use of workspace.
        -   Task order defined by release managers is consistently honored in both the Kanban and List views of release tasks.
        -   Release phases appear in the correct sequence when release tasks and release policies are grouped by phase.
        -   Release admins can now configure which work item types imported from Jira and Azure DevOps are created as product enhancements in DPR.
-   **Version 2.4.1 - April 2026**
    -   New:
        -   Add or remove products in multi-product releases: Modify the product scope of an existing multi-product release at any time, eliminating the need to recreate releases when scope changes.
        -   Define task details in release templates: Pre-configure task details such as assignments, descriptions and attachments directly in release templates, reducing manual effort during release creation.
        -   Default form view in DPR Workspace: When Service Operations Workspace \(SOW\) is installed, release records now automatically load the SOW form view in the Digital Product Release Workspace, ensuring a consistent experience.
        -   Risk score for stage-based releases: View a single aggregated risk score to quickly assess the overall health and readiness of a stage-based release, enabling faster go/no-go decisions.
    -   Changed: Auto-close success and info toast messages: Success and informational notification messages now dismiss automatically, reducing screen clutter during release operations.
    -   Fixed:
        -   Fixed the issue where an incorrect start date was displayed in the release timeline when using a non-default date format
        -   Fixed an issue where selecting New to create a change request in a release didn't trigger any action
-   **Version 2.4.0 - March 2026**

    This version is no longer supported. Use Version 2.4.1 - April 2026.

-   **Version 2.3.2 - December 2025**
    -   New:
        -   AI-generated release notes: Automatically create clear, contextual release summaries using AI, using standard artifacts for accuracy.
        -   Email notifications for key release events: Receive ready-to-use email notifications for key release events, improving visibility and reducing manual configuration.
        -   Modular roles: Use granular, role-based permissions for managing release templates and calendars.
        -   Flow actions: Automate release creation and template application through new Flow actions.
        -   Configurable system properties: Set system properties to make release targets mandatory for stage-oriented releases, or allow the creation of releases for past dates.
        -   Attachments in releases: Add supporting documents to releases for better context and collaboration during execution.
        -   Extended APIs: Create releases, run policies, check policy status, and close phases through APIs.
        -   Release cancellation reason:Provide a reason when canceling a release to ensure auditability and compliance.
        -   Links for direct navigation:Quick navigation links to release execution and calendar views, reducing clicks and improving user experience.
    -   Changed: Unified release calendar view: Use the unified release calendar view to review and manage release readiness targets, releases, and related change requests.
-   **Version 2.2.1 - August 2025**
    -   New:
        -   Manage configuration items for each phase of the release
        -   Automate adding configuration items in the release to the Affected CIs of a Change Request
        -   Product Versions can now be used in multiple Releases
        -   Option for release tasks to automatically move into Work in Progress when previous release task is Completed
-   **Version 2.1.0 - May 2025**
    -   New:
        -   Service releases: Create and manage releases at the service level for better control and traceability
        -   Revamped data model: Replaced the 'Software Model' table with a more intuitive and structured 'Software Version' table
        -   Streamlined release creation: Enjoy a simplified, step-by-step flow to create releases faster and with fewer errors
        -   Time-based scheduling improvements: Releases now account for weekends and holidays using schedules, ensuring deployments align with operational calendars
-   **Version 2.0.0 - February 2025**
    -   New:
        -   Create releases for multi-products that have a parent-child relationship for simultaneous execution.
        -   Link incidents, problems, catalog requests and other task types to a release.
        -   Added the Assignment group field on the Product Feature and Product Enhancement forms.
        -   Ability to auto-create releases from Agile 2.0.
    -   Changed:
        -   Updated policies content to support the multi-product releases.
-   **Version 1.3.0 - November 2024**
    -   New:
        -   A new improved experience for creating releases
        -   Introduced Key dates to define release key dates like milestones, deadlines, and important dates
        -   Capability to breakdown product features into product improvements
        -   Improved experience for creating release calendars
        -   Auto-create product versions from GitLab Milestones
-   **Version 1.2.2 - August 2024**
    -   New:
        -   Manage product bundles
            -   Product managers can add and remove additional "child" products within a product to create a hierarchy of bundled products.
        -   Jira Fix Version integration
            -   When connecting Jira projects to a digital products in DPR, product managers can choose to have Fix Versions in Jira create corresponding release versions in Digital Product Release.
            -   When Fix Versions are used to generate release versions, any Jira task that is associated with the Fix Version will be visible within a Release on the Release Scope page.
        -   Release Calendar Improvements
            -   New Release Calendar entity has been created to group release readiness targets together.
            -   Additional schedules \(maintenance windows, blackout schedules, holiday schedules, etc.\) can be added to a Release Calendar and will be shown on the Release calendar page.
        -   Release Management V2 Migration Utilities
            -   Scripts and UI actions to help with the migration of data from Release Management v2 to Digital Product Release
                -   Create DPR release template from RMv2 Release record
                -   Generate digital product from RMv2 Product record
    -   Changed: "Product features" page on the Release has been renamed to "Release scope".
-   **Version 1.1.2 - May 2024**
    -   New:
        -   Release bundle: Group multiple releases into release bundles to track and manage them concurrently from a single place.
        -   Stage-oriented release: Create stage-oriented releases that prioritize completing objectives and features over following a strict schedule
        -   Release Quality dashboard: Get insights into the quality of a release based on the software quality scan summaries and test summaries
-   **Version 1.0.0 - February 2024**

    Digital Product Release is the next evolution of ServiceNow's support for Release Management. Focused on creating a tailored experience for software-based release management practices, Digital Product Release empowers the central release management team to define release policies, templates, and readiness dates that product development teams can leverage to ensure that new versions of their products meet the release teams definition of done.



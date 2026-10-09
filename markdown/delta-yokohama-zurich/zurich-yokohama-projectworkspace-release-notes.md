---
title: Combined Project Workspace release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Project Workspace from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-projectworkspace-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Project Workspace release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Project Workspace from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Project Workspace release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Project Workspace to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Project Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Duplicate a status report in Project Workspace](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&family=yokohama&ft:locale=en-US)**

Reduce effort by duplicating a status report to transfer all project information without manual copying.

-   **[Resource allocation and heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&family=yokohama&ft:locale=en-US)**
    -   Use the allocation heatmap modal to view resource status, remaining capacity, and utilization and enable resource managers to assess task efforts.
    -   Use inline editing to update one or multiple cells in child resource assignments.
    -   Added new fields for resource assignment:
        -   Name
        -   Ready for review
        -   Notes
    -   Extend a resource assignment for a project or project task using the **Extend** row context menu action.

 **Note:** To use the full functionality of Docs v6.6.0 within Project Workspace, upgrade Project Workspace to the v6.1.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

 -   **[Analyze the status report in Project Workspace](https://www.servicenow.com/docs/access?context=view-status-report-in-project-workspace&family=yokohama&ft:locale=en-US)**
    -   You can't edit the status report, but you can change the system property to enable editing.
    -   Import your old status reports to a new status report tool for a consistent and organized reporting system.
-   **[Configuring security for a project in Project Workspace](https://www.servicenow.com/docs/access?context=configuring-security-for-a-project-in-pw&family=yokohama&ft:locale=en-US)**
    -   Apply confidentiality settings to safeguard sensitive projects and make sure that only authorized users can access confidential data and sub-projects.
    -   When a project is marked confidential in one workspace, such as Project Management or Strategic Portfolio Workspace, these settings automatically extend across all associated workspaces, maintaining consistent protection.
    -   To promote security, at least one user must be assigned access to any confidential project.
-   **[Project task checklists](https://www.servicenow.com/docs/access?context=c_project-task-checklists&family=yokohama&ft:locale=en-US)**
    -   Create a checklist for your project tasks and manage a list of activities or steps to be completed for a task.
    -   As an Administrator, you can add or remove checklists as needed.
-   **[View the roll-up financial values for project tasks at parent project level](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&family=yokohama&ft:locale=en-US)**

View and manage the cost plans and expense lines recorded on a project task level on the parent project.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Use Playbooks in Project Workspace](https://www.servicenow.com/docs/access?context=use-playbooks-pw&family=zurich&ft:locale=en-US)**
    -   Playbooks provide structured stages and activities to keep projects on track.
    -   Added two playbooks for Project Workspace: Project Default and Stage-gate Default.
    -   Use one of the two out-of-box playbooks or create your own to match your project process.
-   **[Monitor and update project report status](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&family=zurich&ft:locale=en-US)**
    -   Track the status of project reports using the Status drop down, and change the status from Draft to Published once updates are complete.
    -   Status changes are restricted to the Project Manager role.
-   **[Copy and edit status report enhancements](https://www.servicenow.com/docs/access?context=update-status-report-project-workspace&family=zurich&ft:locale=en-US)**
    -   Simplified workflow for copying and editing status reports. Duplicate a status report directly without opening a form modal.
    -   The duplicated report automatically refreshes with the latest project updates \(for example, overall status, milestones, or metrics\).
    -   Any static or manually added data from the original report is retained in the duplicated version.
    -   When editing is disabled, all fields in the status report are read-only. When editing is enabled, only dynamic fields remain read-only. You can edit the status report in both the scenarios using the Edit Status Report action in the context menu.

 -   **[Resource assignment updates](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&family=zurich&ft:locale=en-US)**
    -   Access and modify resource details directly from the Resource page without having to navigate to Resource Management Workspace.
    -   End resource assignments when a project ends. View the resource assignments and synchronize the resource assignment dates with the project dates.
    -   Move resource assignments to a new start and end date to align with task dependencies or resource availability.
-   **[Status report properties](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&family=zurich&ft:locale=en-US)**
    -   Updates made on the status report form are reflected in the Status Report document when the `sn_pw.status_report_doc_read_only` property is set to `true`.
    -   Updates made on the status report form are not reflected in the document content when the property is set to `false`.
-   **[Project financials](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&family=zurich&ft:locale=en-US)**
    -   View only planned costs of your planning items to track the total cost of your projects.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your projects.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate labor cost for sub-projects based on the resource assignments of your sub-projects.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Project Workspace features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Skill name updates](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=yokohama&ft:locale=en-US)**

Renamed the Project Gen AI Docs skill to the Project doc summarization skill in Project Workspace.

-   **[Resource assignment UI enhancements](https://www.servicenow.com/docs/access?context=resource-assignments-pw&family=yokohama&ft:locale=en-US)**

Added the **Extend** option and the **Extend Assignment** modal to request a resource assignment extension.

    -   Updated the create resource assignment form to include these fields:
        -   The **Name** field to captures a unique or descriptive name for the resource assignment.
        -   The **Ready for review** list to confirm if a resource assignment is ready for the allocation review.
        -   The **Notes** field to add additional context when creating a resource assignment.
    -   Time span fields are changed to weekly and monthly.
    -   Included the following information in the heatmap modal:
        -   The **Utilization** column to display the total effort across approved or pending tasks.
        -   The **Resource status** column to display the approved or pending assignments.
        -   The **Remaining capacity** column to indicate available or exceeded effort limits.

 -   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-spw&family=yokohama&ft:locale=en-US)**
    -   New **Financials** tab in the planning view.
    -   The name of the **ETC** field is changed to **Remaining Estimates**.
    -   The name of the **EAC** field is changed to **Forecast**.
    -   The name of the **Actuals to date** is changed to **Actuals**.

 -   **[Heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&family=yokohama&ft:locale=en-US)**

The resource allocation heatmap displays the resource status, capacity, and utilization, enabling efficient planning and allocation based on availability and workload.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Status report](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&family=zurich&ft:locale=en-US)**
    -   A Status drop down is added in the Project Status Report with two options Draft and Published.
    -   Renamed the **Copy** button to the **Duplicate status report** button.
    -   Added the Playbooks page to define structured stages for projects.
    -   Added the **Create from template** button on homepage.
-   **[RIDAC UI changes](https://www.servicenow.com/docs/access?context=add-risk-project-project-workspace&family=zurich&ft:locale=en-US)**

Filter, Personalize columns, Settings, and Item details icon are moved to panel.


 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Project Workspace UI changes](https://www.servicenow.com/docs/access?context=update-resource-assignment-pw&family=zurich&ft:locale=en-US)**
    -   A Resource page is added to access and manage resource assignments.
    -   **Sync all** button is added to synchronize project dates for all resource assignments.
    -   A new value, Artificial Intelligence, has been added to the Investment Type field in details section of Project form to allow users to choose Artificial Intelligence as an investment type.
-   **[Manage financials](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&family=zurich&ft:locale=en-US)**
    -   Select and view forecasts, compare planned vs. actual costs, and view planned costs or the allocated budget through a new display mode on the Financials record page.
    -   Renamed **Cost** tab as **Costs and benefits** to manage cost plans and benefit plans in one view.
    -   Renamed **Baselines** as **Baseline comparison** to create and compare financial baselines.
    -   Renamed **Time scope** as **Filter time scope** to adjust the time scope to view a focused and customized financial snapshot.
    -   New **Generate labor costs** button to generate labor costs based on the resource assignments.
    -   New **Currency** list option to switch between functional and investment currency.
    -   New **Edit investment currency** option to define investment currency for your projects.
    -   **New monetary benefit plan** option to create new forecast benefit plans.
    -   New **Planned Benefits** widget displays the total forecasted benefits.
    -   New **Total Return** widget displays the total actual benefits form the projects.
    -   New **Record type** column to classify the financial records between benefits and costs.
    -   Renamed **Estimate At Completion** widget to **EAC Cost**.
    -   Renamed **Actual Cost To Date** to **Actuals \(Incl. current fiscal period\)**.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Project Workspace features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Project Workspace features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Project Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Project Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Project Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Project Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Project Workspace, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Project Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Project Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Import your old status reports to a new status report tool and optimize your reporting process.
-   Create a checklist in a project task to track items that must be completed in the task.
-   Inline edit one or more cells in child resource assignments.
-   Explore the heatmap modal to monitor resource status, available capacity, and utilization efforts.

 See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Guide teams through predefined stages and actions for each process using Playbooks.
-   Track, modify, and synchronize all resources assignment for a project from the resource assignment list page, which displays all assignments associated with that specific project.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

 See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)


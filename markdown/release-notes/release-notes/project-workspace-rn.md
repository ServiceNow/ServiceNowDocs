---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Zurich release.

## Project Workspace highlights for the Zurich release

-   Guide teams through predefined stages and actions for each process using Playbooks.
-   Track, modify, and synchronize all resources assignment for a project from the resource assignment list page, which displays all assignments associated with that specific project.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

**Important:** Project Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Use Playbooks in Project Workspace](https://www.servicenow.com/docs/access?context=use-playbooks-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Playbooks provide structured stages and activities to keep projects on track.
    -   Added two playbooks for Project Workspace: Project Default and Stage-gate Default.
    -   Use one of the two out-of-box playbooks or create your own to match your project process.
-   **[Monitor and update project report status](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Track the status of project reports using the Status drop down, and change the status from Draft to Published once updates are complete.
    -   Status changes are restricted to the Project Manager role.
-   **[Copy and edit status report enhancements](https://www.servicenow.com/docs/access?context=update-status-report-project-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Simplified workflow for copying and editing status reports. Duplicate a status report directly without opening a form modal.
    -   The duplicated report automatically refreshes with the latest project updates \(for example, overall status, milestones, or metrics\).
    -   Any static or manually added data from the original report is retained in the duplicated version.
    -   When editing is disabled, all fields in the status report are read-only. When editing is enabled, only dynamic fields remain read-only. You can edit the status report in both the scenarios using the Edit Status Report action in the context menu.
-   **[Resource assignment updates](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Access and modify resource details directly from the Resource page without having to navigate to Resource Management Workspace.
    -   End resource assignments when a project ends. View the resource assignments and synchronize the resource assignment dates with the project dates.
    -   Move resource assignments to a new start and end date to align with task dependencies or resource availability.
-   **[Status report properties](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Updates made on the status report form are reflected in the Status Report document when the `sn_pw.status_report_doc_read_only` property is set to `true`.
    -   Updates made on the status report form are not reflected in the document content when the property is set to `false`.
-   **[Project financials](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View only planned costs of your planning items to track the total cost of your projects.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your projects.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate labor cost for sub-projects based on the resource assignments of your sub-projects.

## UI changes

-   **[Status report](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   A Status drop down is added in the Project Status Report with two options Draft and Published.
    -   Renamed the **Copy** button to the **Duplicate status report** button.
    -   Added the Playbooks page to define structured stages for projects.
    -   Added the **Create from template** button on homepage.
-   **[RIDAC UI changes](https://www.servicenow.com/docs/access?context=add-risk-project-project-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Filter, Personalize columns, Settings, and Item details icon are moved to panel.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Project Workspace UI changes](https://www.servicenow.com/docs/access?context=update-resource-assignment-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   A Resource page is added to access and manage resource assignments.
    -   **Sync all** button is added to synchronize project dates for all resource assignments.
    -   A new value, Artificial Intelligence, has been added to the Investment Type field in details section of Project form to allow users to choose Artificial Intelligence as an investment type.
-   **[Managing financials for your projects](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
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

## Activation information

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Portfolio Management](https://www.servicenow.com/docs/access?context=c_PortfolioManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Use a simplified, team-oriented approach to Project Management and IT development by combining several individual applications.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)


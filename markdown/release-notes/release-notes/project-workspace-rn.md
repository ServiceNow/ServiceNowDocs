---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Yokohama release.

## Project Workspace highlights for the Yokohama release

-   Import your old status reports to a new status report tool and optimize your reporting process.
-   Create a checklist in a project task to track items that must be completed in the task.
-   Inline edit one or more cells in child resource assignments.
-   Explore the heatmap modal to monitor resource status, available capacity, and utilization efforts.

See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Analyze the status report in Project Workspace](https://www.servicenow.com/docs/access?context=view-status-report-in-project-workspace&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   You can't edit the status report, but you can change the system property to enable editing.
    -   Import your old status reports to a new status report tool for a consistent and organized reporting system.
-   **[Duplicate a status report in Project Workspace](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Reduce effort by duplicating a status report to transfer all project information without manual copying.

-   **[Configuring security for a project in Project Workspace](https://www.servicenow.com/docs/access?context=configuring-security-for-a-project-in-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Apply confidentiality settings to safeguard sensitive projects and make sure that only authorized users can access confidential data and sub-projects.
    -   When a project is marked confidential in one workspace, such as Project Management or Strategic Portfolio Workspace, these settings automatically extend across all associated workspaces, maintaining consistent protection.
    -   To promote security, at least one user must be assigned access to any confidential project.
-   **[Project task checklists](https://www.servicenow.com/docs/access?context=c_project-task-checklists&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Create a checklist for your project tasks and manage a list of activities or steps to be completed for a task.
    -   As an Administrator, you can add or remove checklists as needed.
-   **[View the roll-up financial values for project tasks at parent project level](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    View and manage the cost plans and expense lines recorded on a project task level on the parent project.

-   **[Resource allocation and heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Use the allocation heatmap modal to view resource status, remaining capacity, and utilization and enable resource managers to assess task efforts.
    -   Use inline editing to update one or multiple cells in child resource assignments.
    -   Added new fields for resource assignment:
        -   Name
        -   Ready for review
        -   Notes
    -   Extend a resource assignment for a project or project task using the **Extend** row context menu action.

**Note:** To use the full functionality of Docs v6.6.0 within Project Workspace, upgrade Project Workspace to the v6.1.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

## UI changes

-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   New **Financials** tab in the planning view.
    -   The name of the **ETC** field is changed to **Remaining Estimates**.
    -   The name of the **EAC** field is changed to **Forecast**.
    -   The name of the **Actuals to date** is changed to **Actuals**.
-   **[Skill name updates](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Renamed the Project Gen AI Docs skill to the Project doc summarization skill in Project Workspace.

-   **[Resource assignment UI enhancements](https://www.servicenow.com/docs/access?context=resource-assignments-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

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

## Changed in this release

-   **[Heatmap enhancements](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    The resource allocation heatmap displays the resource status, capacity, and utilization, enabling efficient planning and allocation based on availability and workload.


## Activation information

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Portfolio Management](https://www.servicenow.com/docs/access?context=c_PortfolioManagement&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Use a simplified, team-oriented approach to Project Management and IT development by combining several individual applications.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)


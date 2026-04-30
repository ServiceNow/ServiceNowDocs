---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-04"
reading_time_minutes: 4
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Xanadu release.

## Project Workspace highlights for the Xanadu release

-   Migrate your project budget to Next Experience.
-   As a Portfolio Manager, allocate, manage, and approve project budgets.
-   Compare financial baselines to view simple financials and budget.
-   View and track the actuals of each resource assignment with the actuals toggle.

See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Now Assist in Project Workspace](https://www.servicenow.com/docs/access?context=summarize-docs-genai-skill-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Generate a concise summary of selected text on the Docs component using Now Assist.
    -   Summarize, elaborate, and shorten the selected content on the Docs component using the Project Gen AI Docs skill.
    -   Set up automated emails using the Email project summary skill to stay updated on project progress. Schedule the day and frequency for the skill to send the generated emails.
    -   Generate a quick summary on the complete content of the document with Project Gen AI Docs skill and save time on manual content analysis.
-   **[Managing projects with Project Workspace](https://www.servicenow.com/docs/access?context=use-projects-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate the budget of your projects from Classic UI to Next Experience.
    -   Allocate and approve the budget of a project using Financials in Next Experience.
-   **[Resource planning with Project Workspace](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Follow the assigned schedule for allocation when a resource has a schedule.
    -   Allocate users or groups based on the selected effort type when creating an assignment.
    -   Display allocations inline with the selected effort type.
-   **[Project details page enhancements](https://www.servicenow.com/docs/access?context=update-project-details-from-project-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Add stakeholders, extend or confirm a resource plan, and add new resource allocations daily.
    -   View a status report for the programs and save the project as a template with the **Save as New Template** option.
    -   Create an Agile phase or a Test phase from the Agile or Hybrid execution type.
    -   Create or add existing stories to a project, as well as add new epics.
    -   View the project or project task details from the side panel.
    -   Use the **Open task in new tab** icon \(![Open task in new tab icon.](../../product/project-workspace/image/open-task-new-tab-icon.png)\) to open a project in a different tab.
    -   Use the **Full details** link to add work notes and attachments, as well as view related lists of a project or task.
-   **[Financials in Project Workspace](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate existing project budgets from Classic UI to Next Experience using the migrate budget option.
    -   As a Portfolio Manager, allocate and manage the budget of your projects using the Budget vs cost view.
    -   As a Project Manager, view the comparison of budgets to captured costs for your planning items.
    -   Compare financial baselines to view simple financials and budget.
    -   View the cost plans, expense lines, financial baselines of the subprojects using the Financial view of the parent project.
    -   Widgets in the Cost view of the parent projects display the rolled up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with unique sys\_id to generate labor costs.
-   **[Status reporting in Project Workspace](https://www.servicenow.com/docs/access?context=status-reporting-in-pw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create an overview of the current project status, highlighting key metrics such as health, schedule, scope, cost, and resources, offering a clear snapshot of progress.
    -   Create a new report with or without using a template. A status report captures important details such as milestones, risks, issues, decisions, actions, and change requests, ensuring comprehensive tracking.
    -   Use dynamic data tokens, such as Planned End Date, Status Date, and Actual Cost, which automatically pull and update relevant data, making the report accurate and up-to-date.
    -   Leverage the Docs component to fully customize and configure status reports. Edit and update status reports directly within the Docs component, ensuring they remain accurate and up to date.

## UI changes

-   **[Project Workspace UI changes](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   A new **Show actuals** toggle is added in the settings side panel to view actuals in the allocation heatmap.
    -   A new **Open task in new tab** icon \(![Open task in new tab icon.](../../product/project-workspace/image/open-task-new-tab-icon.png)\) is added to open the project details in a different window.
    -   A new **Filter** icon is added to filter projects on the Project Workspace homepage.
    -   A new **Refresh** icon is added to reload projects on the Project Workspace homepage.
    -   The **New Project** button is replaced with the **New** button on the Project Workspace homepage.
    -   A new **Grid view** icon is added to view projects in card format.
    -   A new **List view** icon is added to view the projects in a list format.
    -   The **Save as New template** option is added in the more actions menu to save the project as a template.
    -   The **Copy project** option is renamed to **Duplicate project**.
-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   A new **Budget vs. cost** toggle is added for Project Managers to view the comparison between budgets and captured costs.
    -   A new **Budget allocation** toggle is added for Portfolio Managers to manage a project budget.
    -   A new **Approve budget** button is added in the budget allocation view for Portfolio Managers to approve budget changes.
    -   New grid view to enter and view the project budget information at fiscal period, quarter, yearly; and total breakdowns by Expense Type or Cost Type.
    -   New **Project/Demand** column in the Cost view to show mapping of cost plans to projects and subprojects.

## Deprecations

Starting with Xanadu release, Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Install Project Workspace by requesting it from the ServiceNow Store. Starting with the Xanadu release, installing the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) also installs the Project Workspace application.

## Related ServiceNow applications and features

-   **[Portfolio Management](https://www.servicenow.com/docs/access?context=c_PortfolioManagement&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Use a simplified, team-oriented approach to Project Management and IT development by combining several individual applications.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)


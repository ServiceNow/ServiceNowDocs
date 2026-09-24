---
title: Combined Project Workspace release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Project Workspace from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-projectworkspace-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 22
breadcrumb: [Products combined by family]
---

# Combined Project Workspace release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Project Workspace from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Project Workspace release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Project Workspace to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Project Workspace.

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

</td></tr><tr><td>

Australia

</td><td>

-   **[CWM integration with Project Workspace](https://www.servicenow.com/docs/access?context=cwm-integration-pw&family=australia&ft:locale=en-US)**

See how each project task breaks down and how its status rolls up, directly on the project's planning page, without manually tracking your team's status updates. Turn on the **Show connected tasks** setting to display the CWM tasks and stories that teams are executing as child tasks under each project task.

Spot schedule risks earlier with a date-conflict indicator that flags when a connected item's planned dates fall outside its parent project task. You can review status without CWM access, while your teams continue to track progress in CWM.


 -   **[Now assist for SPM enhancements](https://www.servicenow.com/docs/access?context=now-assist-spm&family=australia&ft:locale=en-US)**

Added support for third-party LLM models: GPT-5.4 mini and Gemini 3.5 Flash

-   **[RIDAC enhancements](https://www.servicenow.com/docs/access?context=manage-ridac-pw&family=australia&ft:locale=en-US)**
    -   The RIDAC menu provides access to AI-Identified Risks, RIDAC by Type \(Risks, Issues, Decisions, Actions, Change Requests tabs\), and All RIDAC.
    -   Access Risks, Issues, Decisions, Actions, and Change Requests \(RIDAC\) through tabs \(presentation list\) in the RIDAC by Type page.

 -   **[Auto-sync resource assignments](https://www.servicenow.com/docs/access?context=realign-resource-assignment-to-task&family=australia&ft:locale=en-US)**

Sync resources automatically with the **sn\_pw.resource\_assignment\_auto\_sync\_enabled** property.

-   **[Project Answers Agent](https://www.servicenow.com/docs/access?context=ask-question-answers-chatbot-pw&family=australia&ft:locale=en-US)**

Use the project answers AI agent to open the Now Assist panel and ask questions about project details. The project answers AI agent supports a broad set of questions across project dimensions and can answer follow-up questions.

-   **[Work notes in project insights](https://www.servicenow.com/docs/access?context=email-project-summary-pw&family=australia&ft:locale=en-US)**

Use task-level work notes as additional context when generating project insights for detailed results. Review insights that reflect both standard task data and work notes content.

-   **[AI rationale enhancements](https://www.servicenow.com/docs/access?context=generate-risks-using-ai-pw&family=australia&ft:locale=en-US)**

View task IDs, resource IDs, and other references in the AI Rationale column of AI Project Risks as hyperlinks instead of plain text. Select a link to navigate directly to the related task, resource,or reference.

-   **[Export RIDAC data](https://www.servicenow.com/docs/access?context=export-ridac-pw&family=australia&ft:locale=en-US)**

Export RIDAC data from Project Workspace in CSV, Microsoft Excel, or XML format using the Export RIDAC option in the more actions menu. Select a file type from the export modal to download the data currently visible in the RIDAC grid. Records not visible in the grid aren't included in the export.

-   **[Project types and project enhancements](https://www.servicenow.com/docs/access?context=project-types-in-pw&family=australia&ft:locale=en-US)**

Configure project types with custom fields and tailored form views across different types of projects.

    -   Use a dynamic category to define custom fields for a specific project type. Custom fields are scoped to that project type and don't appear on records of other types or affect default fields.
    -   Use custom form views to configure a unique form layout for each project type. The form view is dynamically rendered based on the project type assigned to a record.
-   **[Inline comments and email notifications in Docs](https://www.servicenow.com/docs/access?context=collaborative-project-planning-with-docs&family=australia&ft:locale=en-US)**

Streamline collaboration by enabling inline comments in Docs. Select text to add a comment, mention colleagues using @, and include hyperlinks by pasting URLs. You can comment on plain text, hyperlinks, dynamic data, and text inside table cells, and track discussions through threads, all without leaving the page or switching applications.

Email notifications with comment details, document name, workspace name, and document path are sent when a reply is added to your comment or when you're @-mentioned. Each notification includes a button that opens the document and navigates directly to the comment. Edit or delete your comments and choose to show or hide comment highlights. Users with read-only access can add comments and participate in comment threads.


 -   **[Create an Asset Project Request from Project Workspace](https://www.servicenow.com/docs/access?context=create-asset-project-requests-pw&family=australia&ft:locale=en-US)**
    -   Create and track the number of requests with project reference or requests which are created as part of an SPM project.
    -   Provide portfolio and project managers with visibility into the status of associated hardware requests.
    -   Enable project-based tracking of hardware requests, improving traceability across project plans.
    -   Help portfolio or project managers quickly understand which asset requests are tied to the project and track their current status.
-   **[Manage resources directly in Project Workspace using interoperability](https://www.servicenow.com/docs/access?context=assign-approve-unassigned-work-pw&family=australia&ft:locale=en-US)**
    -   View assigned and unassigned work from the embedded resource board.
    -   Assign unassigned work using automatic or manual effort distribution.
    -   Preview real-time effort allocations before assigning work.
    -   Identify resource availability and over-utilization using visual indicators.
    -   Approve, unapprove, or reprioritize assignments by updating the resource status directly from the resource board.
    -   Extend or update assignments, including assignments for unassigned tasks, without leaving Project Workspace.

 -   **[Project plan generation](https://www.servicenow.com/docs/access?context=generate-project-using-ai-pw&family=australia&ft:locale=en-US)**

Use natural language, uploaded files, or both to automatically generate a project plan with tasks, dates, and business cases.


 -   **[Task generation](https://www.servicenow.com/docs/access?context=generate-tasks-using-ai-pw&family=australia&ft:locale=en-US)**

Use natural language, uploaded files, or both to automatically populate an empty project with tasks, hierarchy, and dates. Generate and preview AI-created tasks for any project without tasks, including demand-sourced projects, and make edits before tasks are added.

-   **[Risk generation](https://www.servicenow.com/docs/access?context=generate-risks-using-ai-pw&family=australia&ft:locale=en-US)**

Analyze project data using generative AI and view suggested potential risks in the AI identified risks page. Accept risks to move them to the RIDAC list. Reject risks to remove them from risk list. Regenerate risks to get suggestions based on current project data.

-   **[Assign a resource using AI resource finder](https://www.servicenow.com/docs/access?context=assign-resources-using-resource-finder-pw&family=australia&ft:locale=en-US)**

Identify and assign the best-fit resources to unassigned task assignments using generative AI. The AI analyzes resource data and generates a fit score and rationale for each available resource based on skills and availability. Compare fit scores, AI rationale, and availability for each resource, then confirm the assignment when ready.

-   **[Expanded project insights topics](https://www.servicenow.com/docs/access?context=configure-project-insights-generation-skill&family=australia&ft:locale=en-US)**

Use new AI insight topics within portfolio insights, project insights, and status reports:

    -   Project delays: Identifies delay patterns across your project timeline and reports them in project insights.
    -   Task dependency: Evaluates task relationships to highlight dependency risks and impacts.
    -   Budget fluctuations: Monitors budget changes and highlights significant variances for review.
    -   Scope creep: Detects insights of unplanned growth in a project by comparing the current project state against its first baseline.
-   **[AI status report enhancements](https://www.servicenow.com/docs/access?context=generate-ai-project-status-report&family=australia&ft:locale=en-US)**

Create AI status reports from an existing template using the Generate from template. Add dynamic tokens to your template to display AI-generated field data in the report document.

Track project health visually. Overall status and individual health sections display as color-coded bullet points with highlighted key values. Sections include scope, schedule, and other health areas.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[AI-generated project status reporting](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&family=australia&ft:locale=en-US)**

Generate AI-powered project status reports for quick visibility into project health and executive summaries.

-   **[AI insights for a project](https://www.servicenow.com/docs/access?context=use-projects-pw&family=australia&ft:locale=en-US)**
    -   Use the **AI insights** page to view consolidated information about project tasks, milestones, resources, financials, and RIDACs.
    -   Configure the insights to monitor critical project elements, such as financials and RIDACs, for a project.
    -   Send AI‑generated project insights via email, including financials, RIDACs, milestones, resources, and project tasks.
    -   Track key project indicators, such as budget overruns, cost variance, high‑risk items, issues, decisions, overdue actions, and change requests.
-   **[Additional admin configuration for project insights generation skill](https://www.servicenow.com/docs/access?context=configure-project-insights-generation-skill&family=australia&ft:locale=en-US)**

Configure additional settings as an admin for the project insights generation skill. Choose inputs, display and review the changes.

-   **[Admin role enhancements](https://www.servicenow.com/docs/access?context=r_InstalledWithProjectManagement&family=australia&ft:locale=en-US)**

Project properties can be edited only by users with the pps\_admin role.


</td></tr><tr><td>

Brazil

</td><td>

-   **[List view for centralized navigation](https://www.servicenow.com/docs/access?context=use-projects-pw&family=brazil&ft:locale=en-US)**

Centralized location for accessing all project-related entities such as My projects, All projects, Project templates, and RIDAC categories \(Risks, Issues, Decisions, Actions, Request changes\), streamlining navigation and improving productivity. Create and save custom lists in the My lists tab to organize your work according to your preferences.

-   **[Recalculate planned costs for projects](https://www.servicenow.com/docs/access?context=fin-recalculate-costs-pws&family=brazil&ft:locale=en-US)**

Recalculate the cost plans, benefit plans, and their rolled-up investment-level values directly from the Financials view using the **Recalculate costs** option.

-   **[Create dynamic docs template](https://www.servicenow.com/docs/access?context=create-a-status-report-template-project-workspace&family=brazil&ft:locale=en-US)**

Customize the docs based on your organization and project requirements using the dynamic docs template in Project Workspace.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Project Workspace features.

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

</td></tr><tr><td>

Australia

</td><td>

-   **[RIDAC enhancements](https://www.servicenow.com/docs/access?context=manage-ridac-pw&family=australia&ft:locale=en-US)**

New RIDAC menu is added on the L2 menu. These three pages are added under RIDAC menu:

    -   AI-Identified Risks
    -   RIDAC by Type
    -   All RIDAC

 -   **[Inline comments changes in Docs](https://www.servicenow.com/docs/access?context=collaborative-project-planning-with-docs&family=australia&ft:locale=en-US)**
    -   The Add comments icon appears in the inline toolbar.
    -   Commented text displays a yellow highlight and underline. Selecting commented text darkens the highlight and opens a comment popover showing the full thread, including reply count, user avatars, names, and relative timestamps.
    -   The comment popover provides options to edit or delete comments. Edited comments display an **Edited** indicator.
    -   Users can turn comment highlights on or off using the **Show comment highlights** or **Hide comment highlights** options in the More actions menu of the document.

 -   **[AI-generated status reports](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&family=australia&ft:locale=en-US)**

The **Generate status report** button has been added to generate status reports with AI assistance.

-   **[Configure project insights modal UI enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-pw&family=australia&ft:locale=en-US)**

The **Financials** and **RIDAC** check boxes have been added in the configure project insights modal.

-   **[Project insights generation skill enhancements](https://www.servicenow.com/docs/access?context=configure-project-insights-generation-skill&family=australia&ft:locale=en-US)**

New admin configuration options are available for the project insights generation skill.

-   **[Project insights email template enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-pw&family=australia&ft:locale=en-US)**

The Financials and RIDAC sections have been added in the email template.

-   **[Project Workspace UI enhancements](https://www.servicenow.com/docs/access?context=use-projects-pw&family=australia&ft:locale=en-US)**

An AI Insights page has been added to capture AI‑generated information for each project.

-   **[Skill name updates](https://www.servicenow.com/docs/access?context=ai-skills-project-workspace&family=australia&ft:locale=en-US)**
    -   Renamed the project doc summarization skill to the project doc generation and insights \(Project Workspace\) skill.
    -   Renamed the planning item doc summarization skill to the planning item doc generation and insights \(Strategic Planning\) skill.
    -   Renamed the EAP doc summarization skill to the EAP doc generation and insights \(Enterprise Agile Planning\) skill.
    -   Added the project status generation in Project Workspace.
-   **[Project Workspace UI changes](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=australia&ft:locale=en-US)**
    -   Added a **Project reference** field to request and refresh forms that enables you to associate hardware requests with an SPM project.
    -   Added an Asset Requests related list on the Project form that enables project managers to view, track, and monitor all associated hardware requests directly from a project.
    -   The **Resources** tab in Project Workspace now opens the resource board within the same page instead of launching a new browser tab.

 -   **[AI skills in Project Workspace](https://www.servicenow.com/docs/access?context=ai-skills-project-workspace&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


</td></tr><tr><td>

Brazil

</td><td>

-   **UI options for RIDAC**

RIDAC section is expanded by default to view AI-Identified Risks and RIDAC.

-   **UI options for Financials**
    -   Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.
    -   Added **Recalculate costs** option to recalculate the planned costs and planned benefit when labor rates or budget reference rates change.
-   **UI options for Project Workspace**
    -   Added **Export status report** in the more options menu in the Details page.
    -   Added **Save as new template** and **Project Diagnostics** in the more options menu in the Planning page.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Project Workspace features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Project Workspace features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

-   Starting with the Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Project Workspace supports status report capability.
-   Starting with Australia release, the Project Management Office \(PMO\) dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Execution dashboard supports PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Portfolio Planning Workspace supports Investment Portal capability.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


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

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

Now Assist features are available with activation of the [ServiceNow Otto for Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=now-assist-spm&family=australia&ft:locale=en-US) plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).


**Important:** Project Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

The Project Workspace plugin \(com.snc.project\_workspace\) is available on ServiceNow® Store. Install the plugin to activate the application.


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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Support added for third-party AI models: GPT-5.4 mini and Gemini 3.5 Flash
-   Third-party AI models are the default models for all ServiceNow Otto for SPM skills.
-   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Enable tracking of the hardware requests that are part of a Strategic Portfolio Management \(SPM\) project.
-   View, assign, and approve resources directly from the Resources page in Project Workspace without navigating to the Resource Management Workspace.
-   Deliver clear, executive‑ready project status reports using AI.
-   Use the AI insights page to view task, milestone, resource, financial, and RIDAC \(risks, issues, decisions, actions, and change requests\) insights for a project.
-   Configure project types with custom fields and form views to support configuration independence across different project types within the same SPM instance.
-   Add inline comments and @mention colleagues in Docs and receive email notifications for replies and mentions.

 See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Define, plan, track, and monitor projects from a single interactive workspace with an intuitive UI.
-   Manage project tasks, dependencies, and timelines using an integrated planning console with grid and Gantt views.
-   Allocate and track resources with the resource assignment pane, including allocation heatmaps and effort tracking.
-   Create and compare schedule and financial baselines to monitor project performance against original plans.
-   Collaborate with stakeholders through activity streams, attachments, and status reporting capabilities.

 See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)


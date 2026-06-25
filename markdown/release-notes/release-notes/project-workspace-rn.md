---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Australia release.

## Project Workspace highlights for the Australia release

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Enable tracking of the hardware requests that are part of a Strategic Portfolio Management \(SPM\) project.
-   View, assign, and approve resources directly from the Resources page in Project Workspace without navigating to the Resource Management Workspace.
-   Deliver clear, executive‑ready project status reports using AI.
-   Use the AI insights page to view task, milestone, resource, financial, and RIDAC \(risks, issues, decisions, actions, and change requests\) insights for a project.
-   Configure project types with custom fields and form views to support configuration independence across different project types within the same SPM instance.
-   Add inline comments and @mention colleagues in Docs and receive email notifications for replies and mentions.

See [Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace-landing-page.md) for more information.

**Important:** Project Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   **[Auto-sync resource assignments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/realign-resource-assignment-to-task.md)**

    Sync resources automatically with the **sn\_pw.resource\_assignment\_auto\_sync\_enabled** property.

-   **[Project Answers Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-question-answers-chatbot.md)**

    Use the project answers AI agent to open the Now Assist panel and ask questions about project details. The project answers AI agent supports a broad set of questions across project dimensions and can answer follow-up questions.

-   **[Work notes in project insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/email-project-summary-skill-pw.md)**

    Use task-level work notes as additional context when generating project insights for detailed results. Review insights that reflect both standard task data and work notes content.

-   **[AI rationale enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-risks-using-ai-na-spm.md)**

    View task IDs, resource IDs, and other references in the AI Rationale column of AI Project Risks as hyperlinks instead of plain text. Select a link to navigate directly to the related task, resource,or reference.

-   **[Export RIDAC data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/export-ridac-pw.md)**

    Export RIDAC data from Project Workspace in CSV, Microsoft Excel, or XML format using the Export RIDAC option in the more actions menu. Select a file type from the export modal to download the data currently visible in the RIDAC grid. Records not visible in the grid aren't included in the export.

-   **[Project types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-types-in-pw.md)**

    Configure project types with custom fields and tailored form views across different types of projects.

    -   Use a dynamic category to define custom fields for a specific project type. Custom fields are scoped to that project type and don't appear on records of other types or affect default fields.
    -   Use custom form views to configure a unique form layout for each project type. The form view is dynamically rendered based on the project type assigned to a record.
-   **[Inline comments and email notifications in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-project-planning-with-docs.md)**

    Streamline collaboration by enabling inline comments in Docs. Select text to add a comment, mention colleagues using @, and include hyperlinks by pasting URLs. You can comment on plain text, hyperlinks, dynamic data, and text inside table cells, and track discussions through threads, all without leaving the page or switching applications.

    Email notifications with comment details, document name, workspace name, and document path are sent when a reply is added to your comment or when you're @-mentioned. Each notification includes a button that opens the document and navigates directly to the comment. Edit or delete your comments and choose to show or hide comment highlights. Users with read-only access can add comments and participate in comment threads.

-   **[Project plan generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-projects-using-nowassist.md)**

    Use natural language, uploaded files, or both to automatically generate a project plan with tasks, dates, and business cases.


-   **[Task generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-tasks-using-now-assist.md)**

    Use natural language, uploaded files, or both to automatically populate an empty project with tasks, hierarchy, and dates. Generate and preview AI-created tasks for any project without tasks, including demand-sourced projects, and make edits before tasks are added.

-   **[Risk generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-risks-using-ai-na-spm.md)**

    Analyze project data using generative AI and view suggested potential risks in the AI identified risks page. Accept risks to move them to the RIDAC list. Reject risks to remove them from risk list. Regenerate risks to get suggestions based on current project data.

-   **[Assign a resource using AI resource finder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/assign-resources-using-resource-finder-na.md)**

    Identify and assign the best-fit resources to unassigned task assignments using generative AI, which analyzes resource data and generates a fit score and rationale for each available resource based on skills and availability for the task time period. Compare fit scores, AI rationale, and availability for each resource, then confirm the assignment when ready.

-   **[Expanded project insights topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-project-insights-generation-skill.md)**

    Use new AI insight topics within portfolio insights, project insights, and status reports:

    -   Project delays: Identifies delay patterns across your project timeline and reports them in project insights.
    -   Task dependency: Evaluates task relationships to highlight dependency risks and impacts.
    -   Budget fluctuations: Monitors budget changes and highlights significant variances for review.
    -   Scope creep: Detects insights of unplanned growth in a project by comparing the current project state against its first baseline.
-   **[AI status report enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-ai-status-report-na.md)**

    Create AI status reports from an existing template using the Generate from template. Add dynamic tokens to your template to display AI-generated field data in the report document.

    Track project health visually. Overall status and individual health sections display as color-coded bullet points with highlighted key values. Sections include scope, schedule, and other health areas.


[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[AI-generated project status reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-a-status-report-in-project-workspace.md)**

    Generate AI-powered project status reports for quick visibility into project health and executive summaries.

-   **[AI insights for a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-projects-pw.md)**
    -   Use the **AI insights** page to view consolidated information about project tasks, milestones, resources, financials, and RIDACs.
    -   Configure the insights to monitor critical project elements, such as financials and RIDACs, for a project.
    -   Send AI‑generated project insights via email, including financials, RIDACs, milestones, resources, and project tasks.
    -   Track key project indicators, such as budget overruns, cost variance, high‑risk items, issues, decisions, overdue actions, and change requests.
-   **[Additional admin configuration for project insights generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-project-insights-generation-skill.md)**

    Configure additional settings as an admin for the project insights generation skill. Choose inputs, display and review the changes.

-   **[Admin role enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_InstalledWithProjectManagement.md)**

    Project properties can be edited only by users with the pps\_admin role.

-   **[Create an Asset Project Request from Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-asset-project-requests-pw.md)**
    -   Create and track the number of requests with project reference or requests which are created as part of an SPM project.
    -   Provide portfolio and project managers with visibility into the status of associated hardware requests.
    -   Enable project-based tracking of hardware requests, improving traceability across project plans.
    -   Help portfolio or project managers quickly understand which asset requests are tied to the project and track their current status.
-   **[Manage resources directly in Project Workspace using interoperability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/assign-approve-unassigned-work-pw.md)**
    -   View assigned and unassigned work from the embedded resource board.
    -   Assign unassigned work using automatic or manual effort distribution.
    -   Preview real-time effort allocations before assigning work.
    -   Identify resource availability and over-utilization using visual indicators.
    -   Approve, unapprove, or reprioritize assignments by updating the resource status directly from the resource board.
    -   Extend or update assignments, including assignments for unassigned tasks, without leaving Project Workspace.

## UI changes

-   **[Inline comments changes in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-project-planning-with-docs.md)**
    -   The Add comments icon appears in the inline toolbar.
    -   Commented text displays a yellow highlight and underline. Selecting commented text darkens the highlight and opens a comment popover showing the full thread, including reply count, user avatars, names, and relative timestamps.
    -   The comment popover provides options to edit or delete comments. Edited comments display an **Edited** indicator.
    -   Users can turn comment highlights on or off using the **Show comment highlights** or **Hide comment highlights** options in the More actions menu of the document.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   **[AI-generated status reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-a-status-report-in-project-workspace.md)**

    The **Generate status report** button has been added to generate status reports with AI assistance.

-   **[Configure project insights modal UI enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/email-project-summary-skill-pw.md)**

    The **Financials** and **RIDAC** check boxes have been added in the configure project insights modal.

-   **[Project insights generation skill enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-project-insights-generation-skill.md)**

    New admin configuration options are available for the project insights generation skill.

-   **[Project insights email template enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/email-project-summary-skill-pw.md)**

    The Financials and RIDAC sections have been added in the email template.

-   **[Project Workspace UI enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-projects-pw.md)**

    An AI Insights page has been added to capture AI‑generated information for each project.

-   **[Skill name updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/exploring-now-assist-for-spm.md)**
    -   Renamed the project doc summarization skill to the project doc generation and insights \(Project Workspace\) skill.
    -   Renamed the planning item doc summarization skill to the planning item doc generation and insights \(Strategic Planning\) skill.
    -   Renamed the EAP doc summarization skill to the EAP doc generation and insights \(Enterprise Agile Planning\) skill.
    -   Added the project status generation in Project Workspace.
-   **[Project Workspace UI changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace-landing-page.md)**
    -   Added a **Project reference** field to request and refresh forms that enables you to associate hardware requests with an SPM project.
    -   Added an Asset Requests related list on the Project form that enables project managers to view, track, and monitor all associated hardware requests directly from a project.
    -   The **Resources** tab in Project Workspace now opens the resource board within the same page instead of launching a new browser tab.

## Deprecated features

-   Starting with the Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Project Workspace supports status report capability.
-   Starting with Australia release, the Project Management Office \(PMO\) dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Execution dashboard supports PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, Portfolio Planning Workspace supports Investment Portal capability.

## Activation information

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Now Assist features are available with activation of the [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-spm.md) plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Related ServiceNow applications and features

-   **[Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/c_PortfolioManagement.md)**

    Use a simplified, team-oriented approach to Project Management and IT development by combining several individual applications.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI to help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel conversational interface in the Enterprise Agile Planning workspace to get story recommendations, split or combine stories, and create stories for your epics with the help of generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including feedback summarization, content summarization in Docs, demand creation, and epic to story generation.

-   **[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    The Now Assist Admin console provides you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-business-management-rn-landing.md)


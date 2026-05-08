---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects. Project Workspace was enhanced and updated in the Australia release.

## Project Workspace highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Integrate Hardware Asset Management \(HAM\) requests and refresh with Project Workspace, enabling hardware requests and refreshes to be planned and managed as part of strategic initiatives.
-   Enable tracking of the hardware requests that are part of a Strategic Portfolio Management \(SPM\) project.
-   View, assign, and approve resources directly from Resources page in Project Workspace without navigating to the Resource Management Workspace.
-   Deliver clear, executive‑ready project status reports using AI.
-   Use the AI insights page to view task, milestone, resource, financial, and RIDAC insights for a project.

See Project Workspace for more information.

**Important:** Project Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   **Project plan generation**

    Use natural language, uploaded files \(word, pdf, excel, powerpoint\), or both to automatically generate a project plan with tasks, dates, and a business case.


-   **Task generation**
    -   Use natural language, uploaded files \(word, pdf, excel, power point\), or both to automatically populate an empty project with tasks, hierarchy, and dates.
    -   Generate and preview AI-created tasks for any task less project, including demand-sourced projects, and make edits before the tasks are added.
-   **Risk generation**
    -   Analyze project data and suggests potential risks using generative AI to accept or reject from the AI identified risks page.
    -   Accept risks to move them to the RIDAC list. Reject risks to remove them from risk list. Regenerate risks to get suggestions based on current project data.
-   **Assign a resource using AI resource finder**

    Use AI to identify and assign the best-fit resources to unassigned task assignments.

    -   AI analyzes resource data and generates a fit score and rationale for each available resource, based on skills and availability for the task time period.
    -   Compare fit scores, AI rationale, and availability for each resource, then confirm the assignment when ready.
-   **Expanded project insights topics**

    New AI insight topics are now available across portfolio insights, project insights, and status reports.

    -   Project delays: AI identifies delay patterns across your project timeline and reports them in project insights.
    -   Task dependency: AI evaluates task relationships to highlight dependency risks and impacts.
    -   Budget fluctuations: AI monitors budget changes and highlights significant variances for review.
-   **AI status report enhancements**
    -   Generate status reports from a template: Create AI status reports from an existing template using Generate from template. Add dynamic tokens to your template to display AI-generated field data in the report document.
    -   Track project health visually: Overall status and individual health sections display as color-coded bullet points with highlighted key values. Sections include scope, schedule, and other health areas.

[Australia Patch 1](../quality/australia-patch-1.md)

-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **AI-generated project status reporting**

    Generate AI-powered project status reports for quick visibility into project health and executive summaries.

-   **AI insights for a project**
    -   Use the **AI insights** page to view consolidated information about project tasks, milestones, resources, financials, and RIDACs.
    -   Configure the insights to monitor critical project elements, such as financials and RIDACs, for a project.
    -   Send AI‑generated project insights via email, including financials, RIDACs, milestones, resources, and project tasks.
    -   Track key project indicators, such as budget overruns, cost variance, high‑risk items, issues, decisions, overdue actions, and change requests.
-   **Additional admin configuration for project insights generation skill**

    Configure additional settings as an admin for the project insights generation skill. Choose inputs, display and review the changes.

-   **Admin role enhancements**

    Project properties can be edited only by users with the pps\_admin role.

-   **Create an Asset Project Request from Project Workspace**
    -   Create and track the number of requests with project reference or requests which are created as part of an SPM project.
    -   Provide portfolio and project managers with visibility into the status of associated hardware requests.
    -   Enable project-based tracking of hardware requests, improving traceability across project plans.
    -   Help portfolio or project managers quickly understand which asset requests are tied to the project and track their current status.
-   **Manage resources directly in Project Workspace using interoperability**
    -   View assigned and unassigned work from the embedded resource board.
    -   Assign unassigned work using automatic or manual effort distribution.
    -   Preview real-time effort allocations before assigning work.
    -   Identify resource availability and overutilization using visual indicators.
    -   Approve, unapprove, or reprioritize assignments by updating the resource status directly from the resource board.
    -   Extend or update assignments, including assignments for unassigned tasks, without leaving Project Workspace.

## UI changes

[Australia Patch 1](../quality/australia-patch-1.md)

-   **AI-generated status reports**

    The **Generate status report** button has been added to generate status reports with AI assistance.

-   **Configure project insights modal UI enhancements**

    The **Financials** and **RIDAC** check boxes have been added in the configure project insights modal.

-   **Project insights generation skill enhancements**

    New admin configuration options are available for the project insights generation skill.

-   **Project insights email template enhancements**

    The Financials and RIDAC sections have been added in the email template.

-   **Project Workspace UI enhancements**

    An AI Insights page has been added to capture AI‑generated information for each project.

-   **Skill name updates**
    -   Renamed the Project doc summarization skill to the Project doc generation and insights \(Project Workspace\) skill.
    -   Renamed the Planning item doc summarization skill to the Planning item doc generation and insights \(Strategic Planning\) skill.
    -   Renamed the EAP doc summarization skill to the EAP doc generation and insights \(Enterprise Agile Planning\) skill.
    -   Added the project status generation in Project Workspace.
-   **Project Workspace UI changes**
    -   Added a Project reference field to request and refresh forms that enables you to associate hardware requests with an SPM project.
    -   Added an Asset Requests related list on the Project form that enables project managers to view, track, and monitor all associated hardware requests directly from a project.
    -   The Resources tab in Project Workspace now opens the resource board within the same page instead of launching a new browser tab.

## Deprecated features

-   Starting with the Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Project Workspace supports status report capability.
-   Starting with Australia release, the Project Management Office \(PMO\) dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Execution dashboard supports PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Portfolio Planning Workspace supports Investment Portal capability.

## Activation information

Install Project Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Now Assist features are available with activation of the Now Assist for Strategic Portfolio Management \(SPM\) plugin. For more information, see Install Now Assist plugins.

## Related ServiceNow applications and features

-   **Portfolio Management**

    Use a simplified, team-oriented approach to Project Management and IT development by combining several individual applications.

-   **Now Assist**

    ServiceNow® Now Assist uses generative AI to help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **Now Assist panel**

    Use the Now Assist panel conversational interface in the Enterprise Agile Planning workspace to get story recommendations, split or combine stories, and create stories for your epics with the help of generative AI.

-   **Now Assist skills**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including feedback summarization, content summarization in Docs, demand creation, and epic to story generation.

-   **Overview tab in Now Assist Admin**

    The Now Assist Admin console provides you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)


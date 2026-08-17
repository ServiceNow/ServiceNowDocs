---
title: Generate onboarding ramp-up plan agentic workflow
description: The Generate onboarding ramp-up plan agentic workflow is an AI-powered solution that helps managers at your organization onboard new employees more efficiently. This workflow uses a team of AI agents to generate team specific and personalized plans for every new hire.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/journey-designer/onboarding-ramp-up-plan-agentic-wf.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [AI in Journey designer, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Generate onboarding ramp-up plan agentic workflow

The Generate onboarding ramp-up plan agentic workflow is an AI-powered solution that helps managers at your organization onboard new employees more efficiently. This workflow uses a team of AI agents to generate team specific and personalized plans for every new hire.

The Generate onboarding ramp-up plan agentic workflow facilitates the employee journey that transpires from the preboarding phase to the onboarding phase. As newly hired employees transition from preboarding to onboarding, managers are responsible for producing onboarding plans that ramp up the knowledge and skill of new employees joining their team. Creating onboarding plans, especially personalized, team-specific plans, is a time-consuming process for managers that quickly devolves into an increased burden. This agentic workflow for generating onboarding ramp-up plans significantly reduces the workload for managers by converting a cumbersome process into an automated workflow.

The Generate onboarding ramp-up plan agentic workflow provides the following benefits to help deliver value to your organization:

-   Automates onboarding plan creation by eliminating the need for managers to design individualized plans manually.
-   Generates team-specific and role-specific onboarding plans tailored to new hires.
-   Minimizes the administrative efforts required from managers during onboarding.
-   Ensures that onboarding plans are standardized while still accommodating team differences.
-   Speeds up the process of preparing new hires for their roles.
-   Focuses on structured knowledge and skill acquisition for new hires from the start.

## AI agents

When the Generate onboarding ramp-up plan agentic workflow is triggered, a team of AI agents run autonomously to produce a ramp-up plan tailor-made for the onboarding employee.

This workflow employs AI agents to perform the following functions:

-   Collect data on the employee, their onboarding journey, and the assigned team.
-   Analyze required role-specific skills from the job description and interview notes, and compare them with the employee’s existing skills from their resume.
-   Recommend targeted learning courses to address identified skill gaps.
-   Generate a personalized ramp-up plan for the new hire.
-   Provide an interactive review process, enabling managers to modify the plan as needed.
-   Deliver personalized guidance through an assistant-like interface.

<table id="table_dk5_bf1_bfc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Ramp up plan generation AI agent

</td><td>

This AI agent automates the creation of the personalized onboarding ramp-up plan for new employees. It performs the following functions:-   **Data collection**
    -   Gathers information from the onboarding journey, HR cases, team plans, user and manager profiles, job details, and learning resources.
    -   Extracts employee skills and identifies skill gaps using job descriptions, interview notes, and resumes.
    -   Retrieves relevant learning courses aligned with identified skill gaps and role requirements.
-   **Onboarding plan generation**
    -   Uses the employee’s start date, manager details, and learning recommendations to build a structured onboarding plan.
    -   Organizes the plan into up to four stages:
        -   **Stage 1:** Relevant for Your Role
        -   **Stage 2:** Popular on Your Team
        -   **Stage 3:** Trending Courses
        -   **Stage 4:** Get to Know Your Team
-   **Content creation and task management**
    -   Includes up to five learning courses per stage \(Stages 1–3\).
    -   Skips any stage without available courses.
    -   Stage 4 always appears and contains:
        -   Three core team-related tasks.
        -   Up to six additional 1:1 meeting tasks with teammates.
        -   A maximum of nine tasks in total.
-   **Scheduling and delivery**
    -   Assigns tasks and learning items to both employee and manager.

    -   Calculates and assigns due dates for all courses and tasks to ensure timely completion.


</td></tr><tr><td>

Ramp up plan reviewer AI agent

</td><td>

This AI agent allows managers to review the AI-generated personalized onboarding ramp-up plan and update its details through a conversational interface. It provides practical guidance to support managers in making updates in a user-friendly manner.The following are the AI Agent workflow phases:

-   **Present plan** - Displays the initial ramp-up plan using employee and journey details.
-   **Collect Input** – Accept manager instructions to create, update, or delete tasks and stages, confirming all changes.
-   **Review** – Redisplay the updated plan and check if further changes are needed.
-   **Exit** – End the session.

</td></tr></tbody>
</table>## Plugins required for optimum output

To achieve optimum output of the Generate Onboarding ramp-up plan agent, the following plugins are essential. Installing the recommended plugins helps maximize efficiency and overall output quality.

-   Now Assist for HR Service Delivery \(sn\_hr\_gen\_ai\)
-   Skills Foundation \(sn\_skills\_int\)
-   Learning \(sn\_lep\)
-   Hiring Core \(sn\_ta\_hiring\_core\)
-   Journey Designer \(sn\_jny\)

-   **[Set Onboarding ramp up trigger to use Employee Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/set-trigger-emp-center.md)**  
Set Onboarding ramp-up trigger to use Employee Center portal in the trigger configuration so the onboarding ramp-up plan workflow is accessible through the portal. Without setting the portal, the trigger will not be visible or usable in the Employee Center portal.
-   **[Activate Onboarding ramp-up trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/activate-trigger-rampup.md)**  
Enable the Onboarding ramp-up trigger to ensure that the workflow runs at the right time during the employee onboarding. This automates plan generation, reduces manual setup for managers, and improves consistency in onboarding processes.
-   **[Activate the associated AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/turn-on-nowassist-skills.md)**  
Enable the AI skills to allow the system to analyze interview notes and job descriptions, extract keywords, and identify relevant skills. This improves skill gap analysis and ensures accurate, personalized ramp-up plans for new employees.
-   **[Add Employee Center to the ServiceNow Otto display experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/enable-na-va-ec.md)**  
Enable ServiceNow Otto to appear in Employee Center to converse with AI agents in this agentic workflow.
-   **[Review and edit onboarding ramp-up plans using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/review-edit-ramp-up-plan-na.md)**  
Managers working for organizations using the Generate onboarding ramp-up plan agentic workflow can use ServiceNow Otto to review and edit personalized onboarding plans generated by a team of AI agents. Once the manager approves a plan that they reviewed, the corresponding plan is added to the new employee's onboarding journey.

**Parent Topic:**[AI in Journey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/agentic-wf-jny-dsgnr-na-hrsd.md)


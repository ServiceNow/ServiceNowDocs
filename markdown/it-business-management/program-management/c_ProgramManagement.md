---
title: Program Management
description: A program helps you to logically group related projects or demands under a single entity. The ServiceNow Program Management application helps you to manage related projects and demands in coordinated way which is not possible when projects and demands are managed independently.
locale: en-US
release: australia
product: Program Management
classification: program-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Program Management

A program helps you to logically group related projects or demands under a single entity. The ServiceNow® Program Management application helps you to manage related projects and demands in coordinated way which is not possible when projects and demands are managed independently.

The it\_program\_manager [role](../../project-portfolio-suite-with-financials/reference/roles-installed-with-PPS-finance.md#roles_ProgramMgmt) is essential to be able to manage programs. The Program Management application provides the following capabilities to the program manager:

-   Create a program by adding related projects and demands.
-   Create tasks specific to the program. These tasks are essential for completion of the program but are outside the scope of projects.
-   Define key milestones, anticipated risks, and issues for the program.
-   Monitor the progress and status and of all the projects and demand that are part of the program. Program manager can track the costs, resources, and schedules.

When you create a program, consider:

-   A program can be part of a portfolio or can be a generic standalone program that is not part of any portfolio.
-   A program cannot be part of multiple portfolios.
-   A project or demand cannot be part of multiple programs.
-   You can have projects and demands that can directly be part of a portfolio and not part of a program.

The following diagram illustrates how you can implement programs.

![Program implementation](../image/ProgramManagementConcept.png "Program implementation")

## Basics of Program Management

When you create a program, you can add multiple projects or demands to it. If you have created cost plans for the projects and demands, certain values are rolled up from the cost breakdown of program. At the same time, the risk and issues of the projects and demands are also included with the program. The following diagram illustrates how information in the program is related to the projects and demands that are part of the program.

![Information population in program](../image/program_project_demand_relation.png "Information population in program")

Project workbench provides graphical charts to view and monitor the progress of the program and the projects and demands that are part of it. You can also view the progress of a program, projects, and demands against a timeline with the details of milestones and key milestones.

The project manager dashboard provides a central location to a program manager to generate different graphical reports of programs and the program financials.

## Creating programs: approval and business case workflow

Programs in ServiceNow® follow a different creation pattern than projects:

-   **Why programs don't typically come from demands**
    -   Demand workflow: demand → approval → convert to project
    -   Program workflow: strategic initiative → executive approval → create program directly
    -   Programs are strategic multi-project containers decided at executive/portfolio level, not operational demands. They represent multi-year transformations such as digital transformation and cloud migration, rather than single deliverables.
-   **Recommended program approval workflow**
    1.  Strategic planning phase: Create Initiative planning item in Strategic Planning for the strategic program
    2.  Business case development: Attach business case document to Initiative; define scope, budget \($1M+\), timeline \(2-5 years\)
    3.  Executive approval: Present Initiative with business case to steering committee or executive sponsor for approval
    4.  Program creation: After approval, create Program record in PPM with reference to approved Initiative
    5.  Project breakdown: Create constituent projects under the program \(these can come from demands\)
-   **Alternative: Demand-based program creation \(if needed\)**

    If your organization requires formal demand intake for programs:

    1.  Create Demand with **Category** as Program Request.
    2.  Attach program business case to Demand.
    3.  Route through demand approval workflow.
    4.  After approval, manually create Program \(no automatic conversion like demand→project\).
    5.  Link Program to source Demand via reference field.

Program vs Project decision criteria:

-   Use Program when: Multi-project initiative, $1M+ budget, 2+ year duration, cross-organizational scope
-   Use Project when: Single deliverable

-   **[Create a program to manage projects and demands](../task/t_CreateAProgram.md)**  
Create a program to manage related projects and demands. Define the duration, estimated cost, benefits, and ROI to the organization.
-   **[Program workbench](c_ProgramWorkbench.md)**  
The program workbench is a central location for viewing details of a program and the projects and demands that are part of the program.
-   **[Program Dashboard](c_ProgramManagerDashboard.md)**  
The PMO dashboard provides a central location to a program manager to generate different graphical reports.

**Parent Topic:**[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)


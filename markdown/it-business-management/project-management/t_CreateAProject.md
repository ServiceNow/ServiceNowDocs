---
title: Define a project
description: Define important aspects of your Agile, Waterfall, or Hybrid project such as the duration, estimated cost, and net value to your organization to efficiently track the project's progress.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 36
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Define a project

Define important aspects of your Agile, Waterfall, or Hybrid project such as the duration, estimated cost, and net value to your organization to efficiently track the project's progress.

## Before you begin

Role required: it\_project\_manager

## About this task

You can create a project from the Projects list or from the project planning console. You must have the Agile Development 2.0 plugin to create an Agile or Hybrid project and the Test Management plugin to create a test phase for your project.

**Note:** You can also create a project from the [demand workbench](../../planning-and-policy/task/t_CrtArtftDmdMnu.md).

You can also use the multi-currency feature to create a project in a local currency different from your functional currency. You must enable the PPM Standard Multicurrency plugin \(com.snc.ppm\_multicurrency\) and switch to the Project Currency view for the additional fields in the **Financials** tab of the Project form. For more information, see [Multi-currency in project financials](../../project-portfolio-suite-with-financials/concept/multicurrency-pps.md).

## Procedure

1.  Create a project in any of the following ways.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d220037e105">

Location

</th><th align="left" id="d220037e108">

Steps

</th></tr></thead><tbody><tr><td id="d220037e114">

**From the Projects list**

</td><td>

Navigate to **Project** &gt; **Projects** &gt; **Create New**.

</td></tr><tr><td id="d220037e135">

**From the project workspace**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Click the **New Project** button on the My Projects Space page.
3.  In the Create Project dialog box, enter the **Project name** and **Start date** information.
4.  Select a template to use for the project from the Project template list and click **OK**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project Name

</td><td>

Name of the project. When you create the project from My Projects Space page, the **Project name** field is automatically populated.

</td></tr><tr><td>

Project manager

</td><td>

Project manager assigned to the project.

</td></tr><tr><td>

Status

</td><td>

Current status of the project. This information is retrieved from the **Overall health** field in the most recent project status report of the project.

</td></tr><tr><td>

Number

</td><td>

System-generated number with a configurable prefix.

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of the project that has been completed.

</td></tr><tr><td>

State

</td><td>

Current state of the project. All new projects begin as **Pending**. The state of the project can be set on the Project form or derived from the task state.The default available states are: Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Closed Skipped.

 You can also [create a custom state](customize-project-task-states.md) for each state type by overriding the state dictionary attributes.

 For example, say that for the project tasks you have created a custom state called **Testing** for the **Work in Progress** state type. When you update the project task state to **Testing**, the project state is also updated to **Testing**. However, if you have not created a **Testing** state for the **Work in Progress** state type, the project state is updated to the default **Work in Progress** state.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the project.**Note:** Special characters are not supported in the project description. Also, avoid copying text from text processor as it ma cause issues while displaying project information on the planning console.

</td></tr><tr><td>

Similar projects

</td><td>

Displays projects that have similar values for the **Description** and **Short Description** fields using predictive intelligence and machine-learning algorithms. For more information, see [Predictive Intelligence for Project Management](../concept/predictive-intelligence-for-project.md).

</td></tr><tr><td>

Related Search

</td><td>

Displays search results matching the **Name** field by default. You can use this field to search for matching projects using other terms also.

</td></tr></tbody>
</table><table id="table_gdj_pmz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule

</td><td>

Work schedule to be used for this project. The default schedule is an 8-hour work day \(from 8 a.m. to 12 p.m. and 1 p.m. to 5 p.m.\). A day is considered to be a work day and not a 24-hour day.

</td></tr><tr><td>

Approved start date

</td><td>

The date to start the project. This field retains the demand approved start date if the project is converted from a demand. The project schedule is not applied to this date and the date remains unchanged when you add project tasks to your project. This field is highlighted with red color if the date in this field is set to a date later than the **Planned start date** field.**Note:** The approved start date of the project is also carried forward to any sub-project associated with the project.

</td></tr><tr><td>

Approved end date

</td><td>

The date when this project ends. This field retains the demand approved due date if the project is converted from a demand. The project schedule is not applied to this date and the date remains unchanged when you add project tasks to your project. This field is highlighted with in red if the date in this field is set prior to the date in the **Planned end date** field.**Note:** The approved end date of the project is also carried forward to any sub-project associated with the project.

</td></tr><tr><td>

Planned start date

</td><td>

The start date of the project tasks within the project. This date is rolled up from the project tasks. This date is copied from the **Approved start date**. After planned tasks are added, this value is set to the earliest time that the project schedule allows. For example, if the project task is created at 3 a.m. and the default schedule is in use \(which has an 8 a.m. start date\), then the default task start is 8 a.m. the next day.

 **Note:** The planned start date must be within 10 years of the current date. The [project property](../reference/r_InstalledWithProjectManagement.md#table_Project-Properties-system-properties) **Max date span into future or past from the current date** controls the behavior for project planned start date.

 When you convert a demand to a project, the start date of the demand is carried forward as the **Planned start date** for the project. If the demand start date is a weekend and your project follows a project schedule, the **Planned start date** is adjusted to the first working day of the week.

 When you create the project from My Projects Space page, the **Planned start date** field is automatically populated. You must click the calendar icon and select a date to start the project. Projects do not automatically start on the planned start date.

 **Note:**

-   When you change the planned start date of a project, the associated cost plans and resource plan also change. The [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** controls the behavior for project start date change.
-   This field is not available when creating a project by default. Use the **Approved start date** field to specify the project start date. Configure the form to display this field. However, this field is available for existing projects and projects converted from a demand.


</td></tr><tr><td>

Planned end date

</td><td>

The end date of the project tasks within the project. After you add tasks, the value in the field is calculated from the tasks. For a manual project, any update to the actual start date does not update the planned end date of the project. Enable the project property **Enable alter of planned date with Actual for Manual Project** to update the planned end date from the actual start date and planned duration.

 **Note:** This field is not available when creating a project by default, use the **Approved end date** field to specify the project end date. Configure the form to display this field.

 When you convert a demand to a project, the due date of the demand is carried forward as the **Planned end date** for the project. If the demand due date is a weekend and your project follows a project schedule, the **Planned end date** is adjusted to the first working day of the week.

</td></tr><tr><td>

Planned duration

</td><td>

Expected duration of the tasks within the project. After you add tasks, the value in the field is calculated from the duration of the tasks. The duration also considers the project schedule, accounting for any non-work time in the schedule. **Note:** The [project property](../reference/r_InstalledWithProjectManagement.md#table_Project-Properties-system-properties) **Max duration \(in days\) allowed for a project/project task** controls the behavior for project planned duration.

 For example, if the default schedule is used, with a standard 8-hour work day, a project that starts at 8 a.m. on 1 July and ends at noon on 2 July is calculated as 1 day and 4 hours, not 28 hours.

</td></tr><tr><td>

Planned effort

</td><td>

Estimate of the time that it takes to complete the project. This calculation sums up planned effort values for all tasks and stories \(in the case of Agile and Hybrid projects\) in this project. After you add tasks, this field becomes a read-only, roll-up calculation and overwrites any earlier entry that you made.

</td></tr><tr><td>

Actual start date

</td><td>

Date on which the planned tasks start.

 The time component in the actual start and end dates depends on the value of the **Derive time component from planned dates** field in the **Preferences** tab when you manually populate the actual dates.

 However, when you change the **State** or **Percent complete** of the project, the actual dates are auto-populated with the time component copied from the planned dates. The value of the **Derive time component from planned dates** field has no effect on the time component of actual dates in this case.

</td></tr><tr><td>

Actual end date

</td><td>

Date on which the planned tasks ends.

</td></tr><tr><td>

Actual duration

</td><td>

Duration of the project tasks from project start to project closure. As with the planned duration, the actual duration shows the total project time and takes the project schedule into consideration.

</td></tr><tr><td>

Actual effort

</td><td>

Actual number of hours charged to the resources on this project. If you are using the Time Cards application, it automatically calculates the value for this field. It uses the totals for the time worked from the approved time cards of all the resources who worked on a project and all its tasks.**Note:** The actual effort from the stories for Agile and Hybrid projects is also rolled up to the project's actual effort.

 The field is not editable if the **Update actual effort from time card** field is set to **Yes** on the **Preferences** tab.

</td></tr></tbody>
</table><table id="table_ggk_hkz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portfolio

</td><td>

Primary portfolio to which the project belongs. A project can belong to multiple portfolios. **Note:**

-   If a project, for which the **Portfolio** field is not set is associated to a portfolio using the portfolio form, then the portfolio name is populated in the **Portfolio** field.
-   If a portfolio is deleted, the portfolio name is removed from the **Portfolio** field on the Project form.


</td></tr><tr><td>

Program

</td><td>

Program to which the project belongs.**Note:** If the **Portfolio** field is not set, you can select from the list of all programs in the system. If the **Portfolio** field is set, you cannot select programs that belong to other portfolios.

</td></tr><tr><td>

Investment Class

</td><td>

Type of investment class category assigned to the project:-   **Run**: Investment made to sustain the existing business.
-   **Change**: Investment made to implement a change in business.


</td></tr><tr><td>

Investment Type

</td><td>

Investment type of the project.The default available options are Cost Reduction, End User Experience, Legal and Regulatory, Revenue Generating, Service Sustaining, and Strategic Enabler.

</td></tr><tr><td>

Execution Type

</td><td>

Execution methodology used to run the project: **Waterfall**, **Agile**, and **Hybrid**. The default value is **Waterfall**.

 The **Execution Type** field selection determines the related links and related lists that are available. For example, the **Agile Planning &amp; Tracking** related link appears when you set the Execution Type value to **Agile**. You must have the appropriate plugins such as Agile Development 2.0 and Test Management to view these related links and related lists. Also, you must have the appropriate role to use these related links and related lists.

</td></tr><tr><td>

Demand

</td><td>

Demand from which the project was created. The field is visible only if the project has a demand associated to it.

</td></tr><tr><td>

Phase

</td><td>

Current phase of the project. In addition to the **Phase** field, the different project phases are also shown at the top of each project record. The selected phase is highlighted.

 The default phases are **Initiating**, **Planning**, **Executing**, **Delivering**, and **Closing**.

</td></tr><tr><td>

Department

</td><td>

Department in a business unit to which the project belongs.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit to which the project belongs.

</td></tr><tr><td>

Impacted Business Units

</td><td>

Business unit that is impacted by the project.

</td></tr><tr><td>

Business Capabilities

</td><td>

If the project is to change, enhance, or add one or more business capabilities, those capabilities can be associated with the project. [Business capabilities](https://www.servicenow.com/docs/access?context=business-capability&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US) are defined in the Application Portfolio Management module.

</td></tr><tr><td>

Business Applications

</td><td>

If the project is to change, enhance, or add one or more business applications, those applications can be associated with the project. [Business applications](https://www.servicenow.com/docs/access?context=application-portfolio-management&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US) are defined in the Application Portfolio Management module.You can select any business application in your enterprise regardless of whether it is related to the capability selected in the **Business Capabilities** field.

</td></tr></tbody>
</table>    **Note:** When a demand gets converted into a project, the data on **Business Case** tab gets carried forward from demand to project.

<table id="table_fk5_bkz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strategies

</td><td>

Strategic objectives of the organization that the project fulfills. A project can fulfill multiple strategic objectives.If a **Business Unit** for the project is selected in **Details** tab, then the list displays the business strategies for the selected business unit along with other enterprise strategies.

</td></tr><tr><td>

Goals

</td><td>

Goals associated with the selected strategy. A project can fulfill multiple goals.If a strategy is not selected, then all goals are displayed in the list.

</td></tr><tr><td>

Business case

</td><td>

Business arguments that support the project.

</td></tr><tr><td>

Risk of performing

</td><td>

Risks associated if the project is carried out.

</td></tr><tr><td>

Risk of not performing

</td><td>

Risks associated if the project is not carried out, for example, risk of loss of opportunity.

</td></tr><tr><td>

Enablers

</td><td>

Key enablers for the project.

</td></tr><tr><td>

Barriers

</td><td>

Major barriers to the project.

</td></tr><tr><td>

In scope

</td><td>

Scope of the project. The scope is the set of boundaries that define the extent of a project.

</td></tr><tr><td>

Out of scope

</td><td>

Activities or deliverables that are not in the scope of the project. Anything that is not defined in the scope is out of scope.

</td></tr><tr><td>

Assumptions

</td><td>

Assumptions made for the project. Assumptions help define scope and risks, and fine-tune the estimates for time and cost.

</td></tr></tbody>
</table><table id="table_mvx_rjz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rate Model

</td><td>

Rate model assigned to the project. The [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) is used to derive hourly rates for the associated resource plans and time cards.

 When you create a project from a demand, the rate model is copied from the demand to the project.

 The subprojects in a project derive their resource plan calculations from the rate model associated with the top task.

 If the assigned rate model is removed or replaced or the hourly rates in the rate model are changed, the cost fields on the associated resource plans are not recalculated automatically. You must [update costs of all resource plans in the project](recalculate-resource-costs-of-a-project.md) using the **Recalculate Resource Costs** menu option to reflect new rates from the rate model.

 You can also [update costs of a single resource plan one at a time](../../resource-management/task/recalculate-resource-costs.md).

</td></tr><tr><td>

Total planned cost

</td><td>

Estimated cost of the project. If an operational expenditure, capital expenditure, or both are associated with the project, then the planned cost is the sum of the operational expenditure and capital expenditure, which is in the selected currency for the project.

 For Agile and Hybrid projects, the planned cost for stories is considered when the resource plan is created for Agile assignment group.

 **Note:** To create a resource plan for Agile assignment group, you must assign the pps\_resource role to the group.

</td></tr><tr><td>

Planned capital

</td><td>

Capital expenditure \(Capex\) for the project. If no cost plans are associated with the project, the **Planned capital** field is editable. Select a currency type and enter a value.

</td></tr><tr><td>

Planned operating

</td><td>

Operational expenditure \(Opex\) for the project. If no cost plans are associated with the project, the **Planned operating** field is editable. Select a currency type and enter a value.

</td></tr><tr><td>

Budget cost

</td><td>

Budgeted cost for this project. This field is automatically populated from the project budget breakdowns in the cost plan breakdown table. When project funds are allocated for a fiscal year, the cost plan breakdown stores the budget allocation for each fiscal period. These amounts are rolled up and stored in the budget cost. To manually enter a value, select a currency icon and enter the value.

</td></tr><tr><td>

Actual cost

</td><td>

Actual cost of this project. Select a currency icon and enter a value.

</td></tr><tr><td>

Estimate at completion

</td><td>

Sum of all actuals for past fiscal periods added to the planned cost for future fiscal periods.**Note:** The current month is considered as a future month for EAC calculation purposes.

 For example, if the duration of a project is from January 01 to December 31 and you check the Estimate at Completion in the month of May, it is calculated as: `Sum of actuals from Jan to April + Sum of planned cost from May to December`.

</td></tr><tr><td>

Planned benefit

</td><td>

Planned benefit for the project.This value is rolled up from the benefit breakdown of the project.

 You can also enter the value manually. Select a currency icon and enter a value.

</td></tr><tr><td>

Planned return

</td><td>

The **Planned return** value is derived from the difference between the **Planned benefit** and **Planned cost** values:\(The value in the **Planned benefit** field – the value in the **Planned cost** field.\)

</td></tr><tr><td>

Planned ROI%

</td><td>

The ROI \(return on investment\) percentage result is calculated based on values in the **Planned return** and **Estimated cost** fields.`(Planned return/Estimated cost x 100)`

</td></tr><tr><td>

Discount Rate %

</td><td>

Project discount rate. The discount rate is the interest rate to determine the present value of future cash flows.

</td></tr><tr><td>

Net present value

</td><td>

Present value of future cash based on the given annual interest rate.This value is a measure for comparing money spent today against future expected financial benefits. This information is useful when evaluating the overall investment performance.

 For example, at 12% discount rate, $1.00 today is worth $0.80 in two years. Therefore, expecting to receive $1.00 in two years is the same as receiving $0.80 today.

 Net present value \(NPV\) is calculated from the estimated cost per year, the planned benefit per year, and the discount rate for the project.

</td></tr><tr><td>

Internal rate of return %

</td><td>

Annual interest rate required to achieve an NPV of zero.Internal rate of return \(IRR\) helps to determine which projects can deliver a higher rate of return in terms of revenue.

</td></tr><tr><td>

Estimate to completion

</td><td>

Sum of all planned costs for future fiscal periods.You can define the frequency to calculate EAC and ETC values to match with the expense lines. Navigate to **System Definition** &gt; **Scheduled Jobs**, select the **Calculate Project Completion Estimates** job, and set the frequency using the Run list.

 **Note:** The current month is considered as a future month for ETC calculation purposes.

</td></tr></tbody>
</table><table id="table_m4l_4jz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk Score

</td><td>

Calculated based on the project risk.

</td></tr><tr><td>

Value Score

</td><td>

Calculated based on the ROI% of the project.

</td></tr><tr><td>

Size Score

</td><td>

Calculated based on the value in the **Planned Cost** field.

</td></tr><tr><td>

Score

</td><td>

Calculated based on the individual scores of the attributes **Risk Score**, **Value Score**, and **Size Score**, which in turn are calculated based on the risk, planning ROI%, and estimated cost attributes on a project, respectively. **Note:**

-   You can configure the formula for score calculation.
-   When a demand is converted to a project, the score calculated on the demand is carried forward to the project.


</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Watch list|Users who have subscribed to project notifications.|
    |Work notes list|Users who have chosen to receive email notifications when the work notes on the project are updated.|
    |Activity / Work notes|Information about the milestones, impediments, or changes as the project progresses. Enter the notes in the **Activity** field and click **Work notes**. The text appears in the feed.|

<table id="table_u5s_cjz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow time card reporting on

</td><td>

Level at which the [time cards](https://www.servicenow.com/docs/access?context=t_CreateATimeCard&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for project tasks can be created:-   **Project only**: All time cards for the project are created at the project level only. For example, if a user is assigned to multiple tasks in a project, then the time spent on all tasks is recorded under one time card only for the project.

**Note:** In the [Time Sheet Portal](https://www.servicenow.com/docs/access?context=worker-portal&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), tasks, the project are listed on the **Tasks** tab. For these tasks, the **Add to Time Sheet** and **Add selected to Time Sheet** options are not available. Only the **Quick Add** option is available. On clicking **Quick Add**, a time card is created against the top project, not against the task.

-   **Project tasks only**: Separate time cards are created corresponding to each planned task.

**Note:** In the Time Sheet Portal, the **Add to Time Sheet**, **Quick Add**, and **Add selected to Time Sheet** options are not available for the project.

-   **Project and project tasks**: Time cards can be created at the project level as well as the project task level. The default value is **True**.
-   **No time reporting**: No time cards are created for the project. If the user submits the time card manually, the business rules prevent the user from submitting the time card.

**Note:** In the Time Sheet Portal, the **Add to Time Sheet**, **Quick Add**, and **Add selected to Time Sheet** options are not available for both project and project tasks.

</td></tr><tr><td>

Update actual effort from time card

</td><td>

Determines whether the **Actual effort** field on the **Dates** tab should be updated based on the hours entered in the time cards for the project. If the field is set to **Yes**, then the **Actual effort** field is not editable. If it is set to **No**, then the actual hours from time cards are not rolled up to the project and task. By default, the field is set to **No**.

</td></tr><tr><td>

Calculation

</td><td>

Type of calculation to use for task dependencies: -   **Manual**: Task dates do not reflect any changes made to dependencies.
-   **Automatic**: Task dates are automatically updated to reflect any changes made to dependent or child tasks.


</td></tr><tr><td>

Show on Program Status Report

</td><td>

Option to specify whether the project and its key aspects such as cost, resource, scope, and schedule should be included in the status report of the program to which the project belongs.Default: Selected

</td></tr><tr><td>

Constraint date

</td><td>

A read-only field that displays the project's planned start date. The date in this field is used for calculate the start date of the tasks with **Start ASAP** constraint. Use the **Move Project** related link to change the constraint date. Changing this date also changes the start date for all the tasks with **Start ASAP** constraint. For more information, see [Change the planned start date of a project](change-planned-start-date-of-project.md).

</td></tr><tr><td>

Derive assignee list from resource plan

</td><td>

Option to constrain the resources in the **Assigned to** and **Additional assignee list** fields on the project and project task forms to be derived only from the associated allocated resource plans.

</td></tr><tr><td>

Recalculate score on project change

</td><td>

Determines whether to recalculate and update the project score.-   If the value of the field is set to **Yes**, the project score is recalculated when the projects planned ROI%, estimated cost, or risk is modified.
-   If the value of the field is set to **No**, the project score remains the same even if the project's planned ROI%, estimated cost, or risk is modified. The value of the field can be set to **No** when the user wants to preserve the score value while converting the project to a demand.


</td></tr><tr><td>

Project schedule date format

</td><td>

Determines whether the dates in the planning console should be displayed with the time component. The default is **Date**.

</td></tr><tr><td>

Derive time component from planned dates

</td><td>

Determines whether the time component in the actual start and end dates should be copied from the time component in the planned start and end dates. By default, it is set to **True**.If the **Project schedule date format** field is set to **Date**, this option is selected and inactivated.

 **Note:** When you change the **State** or **Percent complete** value for the project, the actual dates are auto-populated with the time component copied from the planned dates. The value of the **Derive time component from planned dates** field has no effect on the time component of the actual dates in this case. The value of the field affects the time component only when you populate the actual dates manually.

</td></tr></tbody>
</table>    **Note:** This tab appears only when only when you have the Advanced Risk plugin activated and the **Enable Advanced Risk PPM Integration** property under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties** is enabled.

    |Field|Description|
    |-----|-----------|
    |Inherent risk|Score of inherent risk automatically calculated from risk assessment.|
    |Residual risk|Score of residual risk automatically calculated from risk assessment.|
    |Inherent Heatmap|Heatmap of the inherent risks.|
    |Residual Heatmap|Heatmap of the residual risks.|

3.  Click **Submit**.


## What to do next

Use the information provided in the following related links and related lists to capture the important aspects of the project and complete the project record.

<table id="table_bmg_22s_z1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agile Planning &amp; Tracking

</td><td>

Opens the **Backlog** tab of the Agile Board for an Agile project. For more information about backlogs, see [Manage your product backlog](../../sdlc-scrum/task/manage-maintain-backlog.md).This related link appears only when the value for the Execution Type field is set to **Agile** and the Agile Development 2.0 plugin is installed.

</td></tr><tr><td>

Calculate Completion Estimates

</td><td>

Recalculates the values in the **Estimate at Completion** field of the project.

</td></tr><tr><td>

Create Agile Phase

</td><td>

Creates an agile phase for the project. The Agile phase is a child task of the project.This related link appears only when the value for the **Execution Type** field is set to **Agile** and the Agile Development 2.0 plugin is installed.

**Note:** An agile phase includes stories in the Stories related list. You can create an Agile phase from either the Agile or Hybrid execution type. You can also add external dependencies.

</td></tr><tr><td>

Create Test Phase

</td><td>

Creates a test phase for the project. A test phase includes test cases in the Test Cases related list.This related link appears only when the value for the **Execution Type** field is set to **Waterfall** or **Hybrid** and the Test Management plugin is installed.

</td></tr><tr><td>

Planning Console

</td><td>

Opens the [Project Planning console](../concept/c_TheProjectPlanningConsole.md).

</td></tr><tr><td>

Recalculate Strategy and Goal Allocation

</td><td>

Recalculate and update cost field values on the **Strategy** and **Goal Allocation** tabs. Use this link to update the project's total cost and benefits when strategy and goal allocations for the project are changed. For more information, see [Strategic Spend Tracking for PPM](../../itbm-business-outcomes/concept/ppm-strategic-spend-tracking-overview.md).**Note:** This related link is available only if the Strategic Spend Tracking for PPM is installed. You must switch to the Strategic Alignment view to see this related link. If this related link is not available on the form view that you're using, ask your administrator to configure the project form to add this related link.

</td></tr><tr><td>

View RIDAC

</td><td>

View the Risks, Issues, Decisions, Actions, and Request Changes \(RIDAC\) entries for the project. For more information, see [RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md).**Note:** This link only displays converted RIDAC entities. For example, Risks converted to Issues, Decisions, Actions, and Request Changes.

</td></tr><tr><td>

Project Budget

</td><td>

Option to [allocate the budget](allocate-budget-to-project.md) to the project.

</td></tr><tr><td>

Project Workbench

</td><td>

Opens the [Project workbench](../concept/c_ProjectWorkbench.md).

</td></tr><tr><td>

Status Report

</td><td>

Opens the **Status Report** tab on the Planning Console.

</td></tr><tr><td>

Create Baseline

</td><td>

Creates a schedule and financial baseline based on your selection.

</td></tr><tr><td>

Apply Template

</td><td>

Apply one or multiple project templates to the project.

</td></tr><tr><td>

Save as New Template

</td><td>

Saves the current project details such as project tasks and subtasks, attachments, checklists, and other project information as a template. You can create a new project from the templates or apply the template to an existing project. For more information, see [Project templates](../concept/c_ProjectTemplates.md).

</td></tr><tr><td>

Project Diagnostics

</td><td>

Detects data corruption in the current project. You can check for data related to tasks and invalid or cyclic relations in a project. For more information about project diagnostics, see [Use Project Diagnostics to detect corrupt project data](project-diagnostics.md).

</td></tr></tbody>
</table><table id="table_ryw_znz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project Tasks

</td><td>

Tasks in the current project. Only the next-level tasks \(immediate subtasks\) appear in this related list. If any [external dependencies](create-external-dependency-planning-console.md) are created for the project, the corresponding shadow tasks are also listed.

</td></tr><tr><td>

Agile Phase

</td><td>

Lists the agile phases for the project. An agile phase contains project tasks and stories associated with these project tasks.This related list appears only when the value for the **Execution Type** field is set to **Agile** and the Agile Development 2.0 plugin is installed.

</td></tr><tr><td>

Sub-projects

</td><td>

Child project records of the current project.

</td></tr><tr><td>

Stories

</td><td>

List of stories in the current project. Click **New** to create and add new stories to the project.Click **Add Existing** to add stories from the Stories module of the Agile application. For more information, see [Create stories](../../sdlc-scrum/task/t_SDLCPPSCreateStories.md#).

 This related list appears only when the value for the **Execution Type** field is set to **Agile** and the Agile Development 2.0 plugin is installed.

</td></tr><tr><td>

Epics

</td><td>

List of epics in the current project.This related list appears only when the value for the **Execution Type** field is selected as **Agile** and the Agile Development 2.0 plugin is installed.

</td></tr><tr><td>

Requirements

</td><td>

Lists the project requirements with their status. To create a new requirement, click **New**.

To add an existing requirement to the project, click **Edit**.

</td></tr><tr><td>

Resource Plan

</td><td>

Lists the resource plans of the project and project tasks. To [create a resource plan](manage-resources-for-project.md) and manage existing resource plans, click **Manage**.

</td></tr><tr><td>

Cost Plans

</td><td>

Lists the cost plans included in the project.To [create a new cost plan](t_CreateAProjectCostPlan.md), click **New**.

</td></tr><tr><td>

Benefit Plans

</td><td>

Lists the benefit plans included in the project.

 To [create a new benefit plan](create-project-benefit-plan.md), click **New**.

</td></tr><tr><td>

Project Budget

</td><td>

Lists the project budget by fiscal year. Click the amounts in the list to revise them.

</td></tr><tr><td>

Baselines

</td><td>

Collection of all planned dates for all tasks and milestones at the time that you create the baseline.

</td></tr><tr><td>

Status Reports

</td><td>

Lists the status reports for the project.To generate a new status report, click **New**. See, [Create a project status report](t_CreateAProjectStatusReport.md).

</td></tr><tr><td>

Risks

</td><td>

Lists the risks that are part of the project.To create a new risk, click **New**. For more information, see [Add risks for a project](add-risks-for-project.md). Alternatively, you can select risks from an existing risk library by clicking **Create From Library**.

**Note:** The option **Create From Library** appears only when you have the Advanced Risk plugin activated and the **Enable Advanced Risk PPM Integration** property under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties** is enabled.

 **Note:** If the project is a part of another program or portfolio, then any risk added to the project also gets added to the parent program and portfolio.

</td></tr><tr><td>

Issues

</td><td>

Lists the issues included in the programs. To create a new issue, click **New**. For more information, see [Add issues for a project](add-issues-for-project.md).

 Project issues are added with the program and the primary portfolio.

</td></tr><tr><td>

Decisions

</td><td>

Lists the decisions for the current project.To create a new decision, click **New**. For more information, see [Add decisions for a project](add-decisions-for-project.md).

</td></tr><tr><td>

Actions

</td><td>

Lists the action items identified for the project.To create a new action, click **New**. For more information, see [Add actions for a project](add-actions-for-project.md).

</td></tr><tr><td>

Request Changes

</td><td>

Lists the changes that are related to the resource, scope, cost, and schedule for the current project.To create a new project change request, click **New**. For more information, see [Create a request change](create-project-change-request.md).

</td></tr><tr><td>

Stakeholders

</td><td>

Lists the stakeholders for the project.To add a stakeholder to the project, click **Edit**.

**Note:**

-   When you create a project from a demand, the stakeholders are transferred from the demand to the project.
-   If the portfolio associated with the project has stakeholders, the portfolio stakeholders are automatically added to the project.

 To [add a new stakeholder](../../planning-and-policy/task/t_PopulatingTheStakeholderRegistry.md) in the stakeholder registry, click **New**.

</td></tr><tr><td>

Time Cards

</td><td>

Lists the time cards submitted against the project.To create a new time card, click **New**.

</td></tr><tr><td>

Expense Lines

</td><td>

Lists the expense lines of the project. To create a new expense line, click **New**. For more information, see [Create an expense line](t_CreateAExpenseLine.md).

</td></tr><tr><td>

Notifications

</td><td>

Lists the [external dependency](../concept/external-dependencies.md) related notifications raised in the successor project. The [notifications](accept-project-task-notifications.md) are triggered as a result of the changes made in the predecessor project.

</td></tr><tr><td>

Strategy Allocations

</td><td>

Lists the percentage of the project's total cost and benefits allocated toward achievement of strategies associated with the project. For more information, see [Allocate or modify the strategy and goal percentage for a project](../../itbm-business-outcomes/task/associate-goal-strategy-prj.md). **Note:** This related list appears only when [Strategic Spend Tracking for PPM](../../itbm-business-outcomes/concept/ppm-strategic-spend-tracking-overview.md) is installed. This application is available on ServiceNow Store. You must switch to the Strategic Alignment view to see this related list. If this related list is not available on the form view that you're using, ask your administrator to configure the project form to add this related list. For more information, see [Install Strategic Spend Tracking for PPM](../../itbm-business-outcomes/task/install-strategic-spend.md).

</td></tr><tr><td>

Goal Allocations

</td><td>

Lists the percentage of project's total cost and benefits allocated towards achievement of goals associated with the project. For more information, see [Allocate or modify the strategy and goal percentage for a project](../../itbm-business-outcomes/task/associate-goal-strategy-prj.md). **Note:** This related list appears only when [Strategic Spend Tracking for PPM](../../itbm-business-outcomes/concept/ppm-strategic-spend-tracking-overview.md) is installed. This application is available on ServiceNow Store. You must switch to the Strategic Alignment view to see this related list. If this related list is not available on the form view that you're using, ask your administrator to configure the project form to add this related list. For more information, see [Install Strategic Spend Tracking for PPM](../../itbm-business-outcomes/task/install-strategic-spend.md).

</td></tr></tbody>
</table>-   **[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)**  
An overview of the tasks involved in creating a waterfall project.
-   **[Copy a project](t_CopyAProject.md)**  
Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.
-   **[Create baseline of a project](t_CreateAProjectBaseline.md)**  
Create a schedule baseline and financial baseline of a project. A schedule baseline captures planned dates of all tasks and milestones at a particular moment in time. A financial baseline captures benefit and financial metric information \(snapshot of cost plan, benefit plan, and project-level financial metrics\) at a particular moment in time.
-   **[Assign a project schedule](t_UseAProjectSchedule.md)**  
Without an assigned schedule, a project calculates a day as a full 24 work hours. To schedule tasks by a more realistic work day, assign a schedule to the project. If the schedules provided in the base system do not suit your needs, define a new one.
-   **[Create a project cost plan](t_CreateAProjectCostPlan.md)**  
Project cost plans capture the costs of projects. Create a cost plan to specify the unit cost of a cost type for a fiscal period.
-   **[Create a monetary benefit plan for a project](create-project-benefit-plan.md)**  
Project benefit plans capture the potential benefits accrued by the project when the project is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
-   **[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)**  
Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods. Project benefit plans capture the potential non-financial benefits accrued by the project when the project is executed.
-   **[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)**  
Associate monetary and non-monetary benefit plans, so that you can capture the potential benefits \(financial and non-financial\) accrued by the project for the hybrid benefit plans.
-   **[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)**  
Specify the amount of money that projects and portfolios are allowed to have.
-   **[Create an expense line](t_CreateAExpenseLine.md)**  
A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.
-   **[Generate labor costs](gen-cost-pln-prj-wrkspc.md)**  
Generate labor costs based on the planning attributes configured for financials in the planning attributes page for the resource assignments in a project.
-   **[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)**  
Migrate the project budget to Next Experience to manage the financials using Project Workspace.
-   **[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)**  
Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.
-   **[Create a project status report](t_CreateAProjectStatusReport.md)**  
You can periodically create project status report from the related lists of the project form. The project status report created for the most recent status date updates the status of the project in portfolios.
-   **[View project status reports](project-status-report.md)**  
Project status reports provide the most recent, at-a-glance progress of a project displayed in several categories.
-   **[Create a cost type definition](t_CreateAResourceTypeDefinition.md)**  
Create a cost type definition to associate a cost type, operating, or capital, to an account in the General Ledger from the Financial Management application. Create a cost type definition if you are using Project Portfolio Management with Financials.
-   **[Allocate budget to a project](allocate-budget-to-project.md)**  
Set the budget of a project according to the fiscal years.
-   **[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)**  
RIDAC is an acronym for Risk, Issue, Decision, Action, and Request Change records. In Project Workspace, you can create a risk record for your project that you can convert to other records during the project life cycle. You can track issues and avoid copying relevant details in the related records.

**Parent Topic:**[Project Management](../concept/c_ProjectApplicationOverview.md)

**Related topics**  


[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

[Resource Management classic](../../resource-management/concept/c_ResourceManagement.md)


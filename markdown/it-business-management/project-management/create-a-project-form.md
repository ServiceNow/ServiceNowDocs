---
title: Project form
description: Learn about the fields of project form. Use this form to create a project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/create-a-project-form.html
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Form field information for Project Management, Project Management reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project form

Learn about the fields of project form. Use this form to create a project.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project Name

</td><td>

Name of the project.

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

 You can also [create a custom state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/customize-project-task-states.md) for each state type by overriding the state dictionary attributes.

 For example, say that for the project tasks you have created a custom state called **Testing** for the **Work in Progress** state type. When you update the project task state to **Testing**, the project state is also updated to **Testing**. However, if you have not created a **Testing** state for the **Work in Progress** state type, the project state is updated to the default **Work in Progress** state.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the project.**Note:** Special characters are not supported in the project description. Also, avoid copying text from text processor as it ma cause issues while displaying project information on the planning console.

</td></tr><tr><td>

Similar projects

</td><td>

Displays projects that have similar values for the **Description** and **Short Description** fields using predictive intelligence and machine-learning algorithms. For more information, see [Predictive Intelligence for Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/predictive-intelligence-for-project.md).

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

 **Note:** The planned start date must be within 10 years of the current date. The [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **Max date span into future or past from the current date** controls the behavior for project planned start date.

 When you convert a demand to a project, the start date of the demand is carried forward as the **Planned start date** for the project. If the demand start date is a weekend and your project follows a project schedule, the **Planned start date** is adjusted to the first working day of the week.

 When you create the project from My Projects Space page, the **Planned start date** field is automatically populated. You must select the calendar icon and select a date to start the project. Projects do not automatically start on the planned start date.

 **Note:**

-   When you change the planned start date of a project, the associated cost plans and resource plan also change. The [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** controls the behavior for project start date change.
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

Expected duration of the tasks within the project. After you add tasks, the value in the field is calculated from the duration of the tasks. The duration also considers the project schedule, accounting for any non-work time in the schedule. **Note:** The [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **Max duration \(in days\) allowed for a project/project task** controls the behavior for project planned duration.

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

Investment type of the project.-   Cost Reduction
-   End User Experience
-   Legal and Regulatory
-   Revenue Generating
-   Service Sustaining
-   Strategic Enabler
-   Artificial Intelligence

</td></tr><tr><td>

Execution Type

</td><td>

Execution methodology used to run the project: **Waterfall**, **Agile**, and **Hybrid**. The default value is **Waterfall**.

 The **Execution Type** field selection determines the related links and related lists that are available. For example, the **Agile Planning &amp; Tracking** related link appears when you set the Execution Type value to **Agile**. You must have the appropriate plugins such as Agile Development 2.0 and Test Management to view these related links and related lists. Also, you must have the appropriate role to use these related links and related lists.

</td></tr><tr><td>

Demand

</td><td>

Demand from which the project was created. The field is visible only if the project has a demand associated to it.**Note:** When a demand gets converted into a project, the data on **Business Case** tab gets carried forward from demand to project.

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

If the project is to change, enhance, or add one or more business capabilities, those capabilities can be associated with the project. Business capabilities are defined in the Application Portfolio Management module.

</td></tr><tr><td>

Business Applications

</td><td>

If the project is to change, enhance, or add one or more business applications, those applications can be associated with the project. Business capabilities are defined in the Application Portfolio Management module.You can select any business application in your enterprise regardless of whether it is related to the capability selected in the **Business Capabilities** field.

</td></tr></tbody>
</table><table id="table_fk5_bkz_fdc"><thead><tr><th>

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

Rate model assigned to the project. The [rate model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/rate-model/rate-model.md) is used to derive hourly rates for the associated resource plans and time cards.

 When you create a project from a demand, the rate model is copied from the demand to the project.

 The subprojects in a project derive their resource plan calculations from the rate model associated with the top task.

 If the assigned rate model is removed or replaced or the hourly rates in the rate model are changed, the cost fields on the associated resource plans are not recalculated automatically. You must [update costs of all resource plans in the project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/recalculate-resource-costs-of-a-project.md) using the **Recalculate Resource Costs** menu option to reflect new rates from the rate model.

 You can also [update costs of a single resource plan one at a time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/recalculate-resource-costs.md).

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
</table>|Field|Description|
|-----|-----------|
|Watch list|Users who have subscribed to project notifications.|
|Work notes list|Users who have chosen to receive email notifications when the work notes on the project are updated.|
|Activity / Work notes|Information about the milestones, impediments, or changes as the project progresses. Enter the notes in the **Activity** field and select **Work notes**. The text appears in the feed.|

<table id="table_u5s_cjz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow time card reporting on

</td><td>

Level at which the [time cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateATimeCard.md) for project tasks can be created:-   **Project only**: All time cards for the project are created at the project level only. For example, if a user is assigned to multiple tasks in a project, then the time spent on all tasks is recorded under one time card only for the project.

**Note:** In the [Time Sheet Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/worker-portal.md), tasks, the project are listed on the **Tasks** tab. For these tasks, the **Add to Time Sheet** and **Add selected to Time Sheet** options are not available. Only the **Quick Add** option is available. On selecting **Quick Add**, a time card is created against the top project, not against the task.

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

A read-only field that displays the project's planned start date. The date in this field is used for calculate the start date of the tasks with **Start ASAP** constraint. Use the **Move Project** related link to change the constraint date. Changing this date also changes the start date for all the tasks with **Start ASAP** constraint. For more information, see [Change the planned start date of a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/change-planned-start-date-of-project.md).

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
</table>|Field|Description|
|-----|-----------|
|Inherent risk|Score of inherent risk automatically calculated from risk assessment.|
|Residual risk|Score of residual risk automatically calculated from risk assessment.|
|Inherent Heatmap|Heatmap of the inherent risks.|
|Residual Heatmap|Heatmap of the residual risks.|

**Related topics**  


[Starting a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md)


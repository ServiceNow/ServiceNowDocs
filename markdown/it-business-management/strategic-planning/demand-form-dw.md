---
title: Demand form
description: The demand form information is used to create a demand.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Form field information, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Demand form

The demand form information is used to create a demand.

<table id="table_olx_smf_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the demand.

</td></tr><tr><td>

Category

</td><td>

Category of the demand:-   Strategic: For demands for plans, such as projects or stories.
-   Operational: For demands for operational work, such as changes or defects.

</td></tr><tr><td>

Type

</td><td>

The **Category** field selection determines the selections available in the **Type** field.-   The following demand types are available if the demand category is Strategic:
    -   Enhancement
    -   Project
    -   Epic
    -   Story
    -   EAP Epic
    -   EAP Feature
    -   EAP Capability
    -   No Conversion
-   The following demand types are available if the category is Operational:
    -   Change
    -   Defect
    -   No Conversion

If the Agile Development 2.0 application is active, the Story, Epic, Enhancement, and Defect options are available.

If the Strategic Planning application is active, the EAP Epic, EAP Feature, and EAP Capability options are available.

The No Conversion option enables you to use your demand to fund a large project that includes one or more projects, epic, or programs.

The selections in the **Category** and **Type** field also determine the fields that are displayed in the Assessment Data section.

</td></tr><tr><td>

Project

</td><td>

Name of the project created from this demand.This read-only field is visible only when you convert the demand into a project.

</td></tr><tr><td>

Enhancement

</td><td>

Number of the enhancement created from this demand.This read-only field is visible only when you convert the demand into an enhancement.

</td></tr><tr><td>

Epic

</td><td>

Name of the epic created from this demand.This read-only field is visible only when you convert the demand into an epic.

</td></tr><tr><td>

Story

</td><td>

Name of the story created from this demand.This read-only field is visible only when you convert the demand into a story.

</td></tr><tr><td>

Number

</td><td>

Unique, auto-generated identification number for the demand.

</td></tr><tr><td>

Approved start date

</td><td>

The formal date approved by stakeholders for starting the demand. This date is set after prioritization and stakeholder approval and represents the committed and authorized timeline for execution. It’s used for governance and traceability.For example, the approved date to start the database upgrade is 2026-01-10.

This field is carried forward to the **Approved start date** field of the Project form if the demand is converted to a project and remains unchanged, even if the project starts later.This field is highlighted in red if the date is different than the value in the **Start date** field.

**Note:** If this field is empty while creating a demand, the date from the **Start date** field is inserted.

</td></tr><tr><td>

Approved end date

</td><td>

The formal date approved by stakeholders for completing the demand. This date is set after prioritization and stakeholder approval and defines the approved execution window and supports historical tracking. For example, the approved end date to complete the demand is 2026-02-15.

This field is carried forward to the **Approved end date** field of the Project form if the demand is converted to a project and remains unchanged, even if the project ends later.This field is highlighted in red if the date in this field is different than the value in the **Due date** field.

**Note:** If this field is empty while creating a demand, the date from the **Due date** field is inserted.

</td></tr><tr><td>

Start date

</td><td>

The preliminary or estimated date when the work is initially planned to begin. This date helps outline the intended timing for early demand planning and prioritization. You can set this date during initial demand creation or anytime in the planning phase when a rough idea forms. This date can be updated until the demand is officially approved. For example, you’re planning for a database upgrade to start on 2025-11-01.

This date is changed to **Planned start date** when the demand is converted to a project.**Note:**

-   When you change the planned start date of a demand or project, the associated cost plans and resource assignments also change. The **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** property controls the behavior for a demand date change. This property isn’t enabled by default. For more information, see [Properties installed with Project Management](../../project-management/reference/r_InstalledWithProjectManagement.md).
-   The **Start date** column label is changed to **Planned start date**. This change is applicable only for new customers who begin using the Australia version. To ensure continuity, if you’re upgrading to the Australia release from an earlier release, you’ll continue to see the prior labels.

</td></tr><tr><td>

Due date

</td><td>

The preliminary or estimated date when the planned work is expected to be completed. This date provides an expected completion window for planning and stakeholder communication. You can set this date anytime in the planning phase when a rough idea forms and can be updated until the demand is officially approved.For example, you’re planning to complete the database upgrade by 2025-12-31.

**Note:**

-   The **Due date** column label is changed to **Planned end date**. This change is applicable only for new customers who begin using the Australia version. To ensure continuity, if you’re upgrading to the Australia release from an earlier release, you’ll continue to see the prior labels.
-   This date is changed to **Planned end date** when the demand is converted to a project.

</td></tr><tr><td>

Description

</td><td>

Description of the demand.

</td></tr></tbody>
</table><table id="table_y5z_tj3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portfolio

</td><td>

Portfolio indicating the business focus of the demand.

</td></tr><tr><td>

Program

</td><td>

Name of the program to which the demand belongs.

</td></tr><tr><td>

Investment Class

</td><td>

Type of investment class category assigned to the demand:-   Run: Investment made to sustain the existing business.
-   Change: Investment made to implement a change in the business.

</td></tr><tr><td>

Investment Type

</td><td>

Investment type of the demand:-   Cost Reduction
-   End User Experience
-   Legal and Regulatory
-   Revenue Generating
-   Service Sustaining
-   Strategic Enabler
-   Artificial Intelligence

</td></tr><tr><td>

Demand manager

</td><td>

Name of the demand manager.

</td></tr><tr><td>

Collaborators

</td><td>

Users who can edit or contribute to the demand. A demand requester can select any user as a collaborator.

</td></tr><tr><td>

Expense type

</td><td>

The type of the expense, either capex \(capital expense\) or opex \(operational expense\).

</td></tr><tr><td>

Priority

</td><td>

The priority of the demand.

</td></tr><tr><td>

Department

</td><td>

Department in a business unit to which the demand submitter belongs.**Note:** If you don’t select a department, the default value is the name of the department to which the submitter belongs.

</td></tr><tr><td>

Project Manager

</td><td>

Project manager that would be assigned to the project created from this demand. When a project is created, this field becomes read only. This field appears if the **Category** field is set to Strategic and the **Type** field is set to Project. If you delete the project created from this demand, this field becomes editable.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit to which the demand submitter belongs.

</td></tr><tr><td>

Impacted Business Units

</td><td>

Business units affected by the submitted demand. The selected units could experience operational impact, process changes, technology adoption, and so on.For example, if a demand is submitted by the procurement business unit, it can impact the finance, legal, and IT business units.

</td></tr><tr><td>

Idea

</td><td>

Unique identification number of the idea from which the demand was created.

</td></tr><tr><td>

Business Capabilities

</td><td>

Business capabilities associated with the demand that links the demand to organizational goals and value. Business capabilities are defined in the Enterprise Architecture \(formerly Application Portfolio Management\) module.

</td></tr><tr><td>

Impacted Business Applications

</td><td>

If the demand is to change, enhance, or add one or more business applications, the applications associated with the demand. Business applications are defined in the Enterprise Architecture \(formerly Application Portfolio Management\) module. For more information, see [Exploring business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-business-applications.md).You can select any business application in your enterprise regardless of whether it’s related to a capability selected in the **Business Capabilities** field.

</td></tr><tr><td>

Business Applications

</td><td>

If the demand is to change, enhance, or add one or more business applications, the applications associated with the demand. Business applications are defined in the Enterprise Architecture \(formerly Application Portfolio Management\) module. For more information, see [Exploring business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-business-applications.md).You can select any business application in your enterprise regardless of whether it’s related to a capability selected in the **Business Capabilities** field.

</td></tr></tbody>
</table><table id="table_t23_vj3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strategic priority

</td><td>

Strategic objectives of the organization that the demand fulfills. A demand can fulfill multiple strategic objectives.If a business unit has been selected in the **Details** tab, the business strategies for the selected business unit along with other enterprise strategies are available for selection.

</td></tr><tr><td>

Primary goal

</td><td>

The primary goal associated with the strategy selected in the **Strategic priority** field.If a strategy hasn’t been selected, all goals are available for selection.

</td></tr><tr><td>

Business case

</td><td>

Business arguments that support the demand.

</td></tr><tr><td>

Risk of performing

</td><td>

Risks if the demand is approved and implemented.

</td></tr><tr><td>

Risk of not performing

</td><td>

Risks if the demand isn’t approved, for example, risk of loss of opportunity.

</td></tr><tr><td>

Enablers

</td><td>

Key enablers for the demand that would aid the demand to be completed. For example, clearly defined resource and cost plans.

</td></tr><tr><td>

Barriers

</td><td>

Major barriers to the demand that would obstruct the demand's completion. For example, incomplete or unclear demand details.

</td></tr><tr><td>

In scope

</td><td>

Scope of the demand, which is the set of boundaries that define the extent of a demand.

</td></tr><tr><td>

Out of scope

</td><td>

Activities or deliverables not in the scope of the demand. Anything not defined in the scope is out of scope.

</td></tr><tr><td>

Assumptions

</td><td>

Assumptions made for the demand. Assumptions help to define the scope and risks, and fine-tune the estimates for time and cost.

</td></tr></tbody>
</table><table id="table_c4b_wj3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rate Model

</td><td>

Rate model assigned to the demand. This setting is used to derive hourly rates for the associated resource assignments and time cards. For more information, see [Rate Models](../../project-portfolio-suite-with-financials/concept/rate-model.md).**Note:** If the rate model assigned to the demand is changed or removed, the cost fields on the associated resource assignments aren’t recalculated.

</td></tr><tr><td>

Project Currency

</td><td>

Currency used to execute the project once the project is created from this demand.You can select any active currency from the values listed in the Currency \[fx\_currency\] table.

After you create a project in the selected project currency, you can't change the project currency in the Project form if the demand contains a cost plan, a benefit plan, or a project budget. If the demand has no attached plan or budget, you can change the project currency in the Project form.

**Note:** The value of this field defaults to the **Project currency** field of the **Financials** tab in the project currency view of the Project form as well. This field is available only when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) feature is activated and the **Demand Currency** view is enabled.

</td></tr><tr><td>

Capital expense

</td><td>

Capital expenditure \(capex\) for the demand.

</td></tr><tr><td>

Operating expense

</td><td>

Operational expenditure \(opex\) for the demand.

</td></tr><tr><td>

Total planned cost

</td><td>

Result calculated based on the values in the **Capital expense** and **Operating expense** fields.

</td></tr><tr><td>

Financial return

</td><td>

Result calculated based on the values in the **Total costs** and **Financial benefit** fields.

</td></tr><tr><td>

Financial benefit

</td><td>

Estimate of revenue if the demand is approved.This value is rolled up from the benefit breakdown of the demand.

 You can also enter the value manually by selecting a currency icon and entering a value.

</td></tr><tr><td>

ROI %

</td><td>

ROI calculated based on the values in the **Total costs** and **Financial return** fields.The value in this field is updated when a cost plan, benefit plan, or resource assignment is created or updated for the demand in the Qualified or Approved state.

</td></tr><tr><td>

Capital budget

</td><td>

Total capital budget allocated to the demand across all fiscal years. The value is rolled up from the capex budget of the demand.

</td></tr><tr><td>

Operating budget

</td><td>

Total operational budget allocated to the demand across all fiscal years. The value is rolled up from the opex budget of the demand.

</td></tr><tr><td>

Discount Rate %

</td><td>

Demand discount rate, which is the interest rate to determine the present value of future cash flows.

</td></tr><tr><td>

Net present value

</td><td>

Present value of future cash based on the given annual interest rate, a measure for comparing money spent today against future expected financial benefits. This value is useful when evaluating the overall investment performance. For example, at a 12% discount rate, $1.00 today is worth $0.80 in two years. Therefore, receiving $1.00 in two years is the same as receiving $0.80 today.

 Net present value \(NPV\) is calculated from total costs according to year, financial benefit per year, and the discount rate for the demand.

</td></tr><tr><td>

Internal rate of return %

</td><td>

Annual interest rate required to achieve an NPV of zero.Internal rate of return \(IRR\) helps to determine which demands can deliver a higher rate of return in terms of revenue.

</td></tr><tr><td>

Demand Actual Cost

</td><td>

Total cost incurred while working on a demand and demand tasks. Demand actual cost is calculated after the assignee of the demand task creates and submits a time card. When the time card is approved, the resource rate, which is derived from the rate card, labor rate, or system properties, is used to populate this field.

</td></tr><tr><td>

Demand Actual Effort

</td><td>

Time accrued or spent by a resource while working on a demand or a demand task as derived from the submitted and approved time cards. This field isn’t available on the Demand form by default.

</td></tr></tbody>
</table>**Note:** If you’re creating a demand with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and the **Demand Currency** view enabled, then the fields in the **Financials** tab differ from the **Default** view. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency fields in demand-related forms](demand-tables-with-demand-currency-fields.md).

<table id="table_yqw_vj3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Impact

</td><td>

Level of business impact created by the demand.

</td></tr><tr><td>

Risk

</td><td>

Risk value calculated from the demand assessment.

</td></tr><tr><td>

Value

</td><td>

Business value of the demand calculated from the **Impact** and **Financial return** fields.

</td></tr><tr><td>

T-Shirt size

</td><td>

Size of the demand. Before using this value as an indicator of demand size, consider creating and publishing definitions for each option outside the application. That process ensures that the values are interpreted correctly and consistently across the organization or department.

</td></tr><tr><td>

Score

</td><td>

The demand score is calculated based on the **risk**, **value**, and **size** attributes in the base system.The value of the **risk**, **value**, and **size** attributes are derived from the assessment metric category results. For more information, see [assessment categories](../../../administer/assessments/task/t_CreateAnAssessmentCategory.md) and [assessment category results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ViewACategoryResult.md).

-   When the **risk** and **size** values are high, the score of the demand is low.
-   When the **value** setting is high, the score of the demand is high.

</td></tr><tr><td>

Assessment Required

</td><td>

Option for enabling the assessments for the demand. This option is active by default. Only a demand manager can update this value when the demand is in the Draft or Submitted state.

 **Note:** If this option isn’t selected and you reset the demand to the Draft state, the option remains unselected.

</td></tr></tbody>
</table>**Note:** The values in the **Value** and **Score** fields are updated when a cost plan, benefit plan, or resource assignment is created or updated for the demand in the Qualified or Approved state. The values in the fields are updated only until an artifact such as project, enhancement, defect, or change is created from the demand.

|Field|Description|
|-----|-----------|
|Watch list|The groups and users subscribed to the demand who can view the information in the **Additional comments** field.|
|Work notes list|The groups and users subscribed to the demand who can view the information in the **Work notes** field.|
|Work notes|Information about the demand. This information isn’t visible to customers. Work notes are added throughout the demand management life cycle to communicate with other users associated with the demand.|

<table id="table_abw_5j3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Close Demand

</td><td>

Determines when to close the demand automatically if it’s converted to a project.

-   **None**: Keeps the demand in the Open state after it’s converted to a project.
-   **On creation of project**: Closes the demand when the demand is converted to a project.
-   **On closure of project**: Closes the demand when the project created from the demand is closed.

**Note:** The **On creation of project** and **On closure of project** options appear when the value for the **Type** field is set to **Project**. If the **Type** field is set to **Enhancement**, the default setting is **None**.

</td></tr><tr><td>

Project calculation

</td><td>

Determines the calculation to use for task dependencies for the project when the demand is converted to a project. The default value is Automatic.-   Manual: Task dates don’t reflect any changes made to dependencies.
-   Automatic: Task dates are automatically updated to reflect any changes made to dependent or child tasks.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Team|The planning team to which the created EAP entity is assigned. This field becomes read only once the EAP entity is created. This value is an optional value.|
|Converted to|The name of the created EAP entity. This field is read-only.|

|Field|Description|
|-----|-----------|
|Product|Product or system that the demand relates to.|
|Impacted AI systems|Impacted AI systems associated with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.|


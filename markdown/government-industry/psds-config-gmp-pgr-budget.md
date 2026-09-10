---
title: Establish the Grant Program Budget in Grants Management
description: Define the total program budget, including the award allocation and budget categories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-config-gmp-pgr-budget.html
release: zurich
topic_type: task
last_updated: "2026-03-10"
reading_time_minutes: 3
breadcrumb: [Configure the Grant program budget and award allocation, Set up a grant program, Grants Management Program Setup, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Establish the Grant Program Budget in Grants Management

Define the total program budget, including the award allocation and budget categories.

## About this task

Enter award and budget information to communicate the financial scope of the grant program and help the internal team/applicants understand potential funding amounts.

Provide information about the award and budget of the program. Define how the grant program budget is split across different categories. This information is used to manage the program, and is published as part of the solicitation and proposal.

From Grants management version 1.41, this step is organized into three sections: program-level budgeting, category-based allocation, and award configuration.

\[Omitted image "image.psds-gm-program-budget-july-26"\] Alt text: Program budget playbook view showing the three-section layout: Program Budget, Budget Categories, and Award Allocation

## Before you begin

Role required: sn\_gsm\_grnt\_mgmt.program\_manager, sn\_gsm\_grnt\_mgmt.grant\_director

## Procedure

1.  In the **Total program budget** field, enter the total amount that will be used for this program.

    The total program budget cannot exceed the funding program budget. If the entered amount exceeds the funding program budget, an inline error message is displayed.

2.  Define how the grant program budget is split across different categories.

    The **Award** category is fixed and cannot be deleted. All other categories, such as administration, equipment, and indirect costs, are configurable. You can add, remove, or rename non-award categories.

    Enter a percentage allocation for each category. The amount is auto-calculated based on the total program budget. The **Budget allocated** and **Balance left** fields update in real time as you enter percentages.

    **Important:**

    Allocate 100% of the total program budget across all categories. The balance must be zero before you are able to mark the activity as complete.

    For more information on budget categories, see [Budget categories in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gmp-ref-budget-categories.md)

3.  On the Award Allocation form, fill in the fields.

    The **Total award budget allocated** field displays the amount derived from the Award budget category. This value updates automatically when the Award category percentage allocation changes and serves as the budget ceiling for all award type calculations.

<table id="table_jwh_tdz_t3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Total award budget allocated**

</td><td>

Read-only. Displays the amount auto-calculated from the Awards budget category percentage allocation. This value is the budget ceiling for award allocation.

</td></tr><tr><td>

Award type

</td><td>

Select how the award budget is distributed. Options include: -   **Single award** - The full Awards category budget is allocated to a single recipient.
-   **Multiple equal awards** - Enter a fixed number of awards \(minimum 2\). All awards receive equal funding.
-   **Multiple variable awards** - Enter a maximum budget per award as a ceiling value, or a value that is equal to the total award budget allocated.


</td></tr><tr><td>

Target number of awards

</td><td>

Enter the number of awards the total grant award is allocated into. This field is required and must be 2 or greater when **Multiple equal awards** is selected from **Award type**, and is optional when **Multiple variable awards** is selected.

</td></tr><tr><td>

Max budget per award

</td><td>

The maximum amount allocated to each grant award. For **Multiple equal awards**, this value is read-only and is calculated automatically as the total award budget allocated divided by the number of awards. For **Multiple variable awards**, enter a ceiling value that is less than or equal to the total award budget allocated.

</td></tr><tr><td>

Disbursement schedule

</td><td>

Select the frequency of the grant award disbursement. The grant award can be scheduled to disburse weekly, monthly, quarterly, bi-annually, or annually.

</td></tr><tr><td>

Disbursement type

</td><td>

Select **Reimbursement** to specify the manner in which the disbursement is sent to the applicant.

</td></tr></tbody>
</table>4.  Select **Mark Complete**.

    The activity cannot be marked complete until all budget categories are allocated and the balance is zero. If a balance remains, an error message is displayed.


## Result

The total program budget is now allocated across budget categories and the award type is configured. The Budget tab on the Grant Program record displays a read-only summary of the configured budget.

## What to do next

Add milestones for your Grant Program.

**Related topics**  


[psds-config-gmp-pgr-milestones]


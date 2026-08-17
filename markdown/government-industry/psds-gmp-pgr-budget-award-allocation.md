---
title: Configure the Grant program budget and award allocation
description: The program budget and award allocation step structures how Grant Program Managers define, categorize, and allocate the total program budget across budget categories and award types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-gmp-pgr-budget-award-allocation.html
release: australia
topic_type: concept
last_updated: "2026-06-29"
reading_time_minutes: 7
keywords: [program budget, award allocation, grants management, budget categories]
breadcrumb: [Set up a grant program, Grants Management Program Setup, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Configure the Grant program budget and award allocation

The program budget and award allocation step structures how Grant Program Managers define, categorize, and allocate the total program budget across budget categories and award types.

## Program Budget overview

The Program Budget step in the Grants management Program setup playbook defines the total financial scope of a grant program. From Grants management version 1.41, this step is structured into the following three logical sections that separate program-level budgeting, category-based allocation, and award configuration.

1.  **Program budget**: The Grant Program Manager enters the total program budget amount. This value is validated against the associated funding program budget.
2.  **Budget categories**: The Grant Program Manager defines how the total budget is distributed across categories such as awards, equipment, administration, and indirect costs. The total allocation across all categories must equal 100% of the total program budget.

    Non-award budget categories such as equipment, administration, and indirect costs are for internal program tracking purposes. These categories aren't accounted for in the grant program lifecycle beyond the budget allocation step.

3.  **Award allocation**: The Grant Program Manager selects an award type and configures how the award budget, derived from the Awards budget category, is distributed across recipients. Disbursement schedule and disbursement type fields are also configured in this section.

\[Omitted image "psds-gm-program-budget-july-26.png"\] Alt text: Program budget playbook view showing the three-section layout: Program Budget, Budget Categories, and Award Allocation

After the budget activity is completed, the Budget tab on the Grant Program record displays a read-only view.

## Key benefits

The program budget and award allocation workflow provides the following benefits:

-   Separates program-level budget definition from award-level configuration, reducing confusion during program setup.
-   Introduces a Total Award Budget Allocated field that auto-calculates from the Awards budget category, eliminating manual calculation errors.
-   Provides real-time inline validation and auto-calculation of budget amounts as percentages and award counts are entered.
-   Supports three distinct award types to accommodate different grant distribution models.

## Budget categories

Budget categories define how the total program budget is split across different expense types. Each category has a name, a percentage allocation, and an auto-calculated dollar amount.

The **Award** category is a default category that can't be deleted or renamed. It represents the portion of the total program budget that is available for distribution to grant applicants. The Award category is the only category that directly influences the Award Allocation workflow and downstream proposal budget validation. It serves as the bridge between the Budget Categories section and the Award Allocation section. All other budget categories represent internal program expenses that aren't tracked beyond the budget setup step.

When the Grant Program Manager assigns a percentage to the Award category, the system auto-calculates the amount based on the total program budget. This amount populates the read-only Total award budget allocated field in the Award Allocation section.Its dollar amount populates the read-only **Total award budget allocated** field in the Award Allocation section.

## Award types

The Award Allocation section supports the following award types. All award types derive their budget from the Award budget category defined in the Budget Categories section.

-   **Single Award**: The full Awards category budget is allocated to a single recipient. The **Max Budget per Award** field is read-only and auto-populated from the Awards category amount. **Target Number of Awards** is system-set to 1 and isn't editable.
-   **Multiple equal awards**: The Grant Program Manager enters a fixed number of awards \(minimum 2\). The **Max Budget per Award** field is read-only and auto-calculated by dividing the Awards category budget by the number of awards. All awards receive equal funding.
-   **Multiple variable awards**: The Grant Program Manager enters a maximum budget per award as a ceiling value or enters a value equal to the total award amount for maximum flexibility. The target number of awards is optional. If no number is specified, the number of recipients and individual award amounts are determined during the award process. If a number is specified, the budget is distributed among that number of awards.

## Validation chain

The program budget setup enforces validation at three levels. Upstream validation applies constraints inherited from the funding program. Validation within the program budget step itself ensures internal consistency. Downstream validation applies rules to later stages such as proposal budget and funding allocation.

1.  Upstream, funding program check: The Total Program Budget can't exceed the funding program budget. When multiple grant programs exist under the same funding program, the combined budget across all grant programs is validated against the funding program total.
2.  Within the program budget: The Awards budget category amount cascades directly into the Award Allocation section. The **Max Budget per Award** field is derived from and constrained by the Awards category amount. Budget category allocations must total 100% of the Total Program Budget before the activity can be marked complete.
3.  Downstream, proposal budget: The Proposal Budget is validated against the Award type, Max Budget per Award, and Disbursement settings as defined in the Program Budget step.

## Downstream impacts

The **Total award budget allocated** field replaces the **Total program budget** as the reference value in the following areas:

-   Proposal playbook — Proposal budget validation: In the applicant-facing Proposal playbook, the **Add proposal budget** activity validates the **Required budget allocation** field against the **Total award budget allocated** value instead of the Total Program Budget. For single award programs, the applicant's requested budget can't exceed the total award budget allocated amount.
-   Funding allocation — Budget breakdown chart: The **Funding allocation** tab's Budget breakdown section displays the stacked bar graph against the **Total award budget** amount instead of the Total Program Budget.
-   Funding allocation validation: The funding allocation validation checks that allocated proposal budgets don't exceed the **Total award budget allocated** value. The Remaining Budget is calculated against the Total Award Budget.

## Program budget error scenarios

The program budget step displays inline error messages when validation rules aren't met. The following tables describe each error scenario grouped by section.

|Field|Error message|Trigger|
|-----|-------------|-------|
|**Total program budget**|Enter an amount up to the Funding Program budget of \[amount\].|The entered amount exceeds the associated funding program budget.|

|Field|Error message|Trigger|
|-----|-------------|-------|
|**Budget categories** \(banner\)|**Unequal budget** The "Total budget allocated" must equal the "Total program budget" field to continue.|The total allocation across all budget categories is less than the total program budget when you select **Mark Complete**.|
|**Total budget allocated**|Budget allocated exceeds total program budget by \[amount\].|The combined percentage allocation across all budget categories exceeds the total program budget.|
|**Percent allocation**|Percent allocation is required.|A budget category row exists but the percentage field is left empty.|
|**Amount**|Amount is required.|A budget category row exists but the amount field contains the default value None.|
|**Category**|Category is required.|A budget category row is added but the Category drop-down contains the default value None.|

|Field|Error message|Trigger|
|-----|-------------|-------|
|Award Allocation \(banner\)|**Error Alert** The following mandatory fields aren't filled in: Disbursement schedule, Award type, Disbursement type|**Mark Complete** is selected when required Award Allocation fields are empty.|
|**Award type**|Award type is required|The Award type drop-down contains the default value None when **Mark Complete** is selected.|
|**Disbursement schedule**|Disbursement schedule is required|The Disbursement schedule drop-down contains the default value None when **Mark Complete** is selected.|
|**Disbursement type**|Disbursement type is required|The Disbursement type drop-down contains the default value None when **Mark Complete** is selected.|
|**Target number of awards**|The number should be greater than 1|Multiple equal awards is selected and the Target number of awards field is empty or set to 1 or less.|
|**Target number of awards**|Could not parse \[value\] as an integer|A non-integer value such as a decimal number is entered in the Target number of awards field.|
|**Max budget per award**|Must be less than \[total award budget amount\].|The Max budget per award value exceeds the Total award budget allocated amount. This validation applies to the Multiple variable awards type.|

**Related topics**  


[Establish the Grant Program Budget in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-pgr-budget.md)

[Rolling grant approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-rolling-grant-approvals-concept.md)


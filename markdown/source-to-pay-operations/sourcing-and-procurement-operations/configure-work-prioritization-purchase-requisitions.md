---
title: Configure work prioritization for purchase requisitions
description: Configure the Priority defaulting for purchase requisitions decision table to automatically assign priority levels to purchase requisitions based on line item values or other administrator-defined conditions.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 3
keywords: [configure purchase requisition priority, priority defaulting for purchase requisitions, decision table, line total amount, purchase line, financial threshold, procurement administrator, demo rules, business rules, work prioritization, SPO]
breadcrumb: [Configuring work prioritization, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure work prioritization for purchase requisitions

Configure the **Priority defaulting for purchase requisitions** decision table to automatically assign priority levels to purchase requisitions based on line item values or other administrator-defined conditions.

## Before you begin

Before configuring work prioritization for purchase requisitions, confirm the following:

-   The Shopping Hub application \(`sn_shop`\) is installed and active on the instance.
-   The following priority levels exist and are active in the instance's priority choice list: Critical, High, Moderate, Low, and Planning.
-   If demo data is loaded in the instance, review whether the default rules in the decision table reflect your organization's criteria before adding or modifying rules.

Role required: sn\_spend\_psd.psd\_admin or admin

## About this task

The **Priority defaulting for purchase requisitions** decision table contains the rules that determine how priority is assigned to purchase requisitions. Each rule evaluates one or more conditions on the purchase requisition or its line items and returns a priority level when those conditions are met.

The decision table includes example rules that evaluate the total line amount against four financial thresholds. These rules ship as demo data and may not be loaded in your production instance. Review the table before testing to confirm whether rules are present.

Any field on the purchase requisition or purchase line record can be used as a condition input, not just line amount. Administrators can replace or supplement the default rules with conditions based on spend category, supplier, requesting department, or other relevant fields.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Decision Tables**.

2.  In the decision tables list, select **Priority defaulting for purchase requisitions**.

    The decision table opens showing the table header, two input columns \(**Purchase requisition** and **Purchase line**\), and the rules grid. Each row in the grid defines one rule.

3.  If demo rules are present, review each rule and decide whether to keep, modify, or delete it.

    The default demo rules evaluate the **Total line amount** field on the purchase line against four financial thresholds. If these thresholds do not reflect your organization's prioritization criteria, delete or deactivate them before adding your own rules.

4.  Add a rule row to the rules grid.

5.  Configure the rule row by selecting each cell and providing the required values.

    -   To set a condition, select the operator cell and choose an operator, then select the condition value cell and enter a value. For amount fields, enter a numeric value. For category or supplier fields, use the reference field lookup to select the correct records.
    -   To set the result, select the result value cell and choose the priority level to assign when the rule matches.
    For detailed information about working with decision table cells, conditions, and results in Workflow Studio, see [Modify decision table rules in Workflow Studio](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

6.  In the **Rank** column, set the evaluation sequence for each rule.

    To change a rank value, double-click the number to edit it, enter a new value, and press **Enter**. The system evaluates rules in ascending rank order — the rule with the lowest rank number is evaluated first. Place more specific or higher-urgency rules at a lower rank number.

7.  Select **Save** to save the rule.

    Repeat steps 4 through 7 for each additional rule.

    Next, verify that the priority recalculation business rules are active for the purchase requisition and purchase line tables.

8.  Navigate to **System Definition** &gt; **Business Rules** and search for **Recalculate priority on update** filtered by the purchase requisition table and the purchase line table.

    Confirm both rules show as active. These rules are the triggers that call the decision table when records are created or updated.

9.  Test the configuration by creating or updating a purchase requisition with a line item whose value matches one of your configured rules.

    After the background rule runs, verify that the **Priority** field on the purchase requisition reflects the expected value. Also test a requisition whose line values do not match any rule and confirm that its priority remains at **Planning**.

    Priority is assigned asynchronously after the record is saved, so allow a moment before checking the result.


## Result

Purchase requisitions are automatically assigned a priority level when they are created or updated. Procurement specialists can sort and filter their work queue by priority to work the most urgent requisitions first.

**Parent Topic:**[Configuring work prioritization](../concept/configuring-work-prioritization.md)


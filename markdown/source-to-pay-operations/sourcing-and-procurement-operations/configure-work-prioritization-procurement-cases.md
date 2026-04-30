---
title: Configure work prioritization for procurement cases
description: Configure the Priority defaulting for procurement cases decision table to automatically assign priority levels to procurement cases based on conditions you define.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 3
keywords: [configure procurement case priority, priority defaulting for procurement cases, decision table, psd\_admin, procurement case line, modification type, work prioritization, SPO, Procurement Case Management]
breadcrumb: [Configuring work prioritization, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure work prioritization for procurement cases

Configure the **Priority defaulting for procurement cases** decision table to automatically assign priority levels to procurement cases based on conditions you define.

## Before you begin

Before configuring work prioritization for procurement cases, confirm the following:

-   The Procurement Case Management application \(`sn_spend_psd`\) is installed and active on the instance.
-   The Shopping Hub application \(`sn_shop`\) is installed and active — it provides shared priority utilities used by all three record types.
-   The following priority levels exist and are active in the instance's priority choice list: Critical, High, Moderate, Low, and Planning.
-   Your organization has agreed on the business criteria for prioritizing procurement cases before you open the decision table. The table ships with no rules — all conditions must be defined from scratch.

Role required: sn\_spend\_psd.psd\_admin or admin

## About this task

The **Priority defaulting for procurement cases** decision table contains the rules that determine how priority is assigned to procurement cases. Unlike the purchase requisition and sourcing request tables, this table ships with no pre-built rules. Administrators define all conditions from scratch based on the criteria most relevant to their organization.

Any field on the procurement case or case line record can be used as a condition input. For example, case type, modification type, spend category, supplier tier, or contract value. There are no prescribed evaluation dimensions.

This table belongs to the Procurement Case Management application, which is a separate package from the ShoppingHub application that contains the purchase requisition and sourcing request decision tables. If the table does not appear in the decision tables list, confirm that the Procurement Case Management application is installed and that your role includes access to that application scope.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Decision Tables**.

2.  In the decision tables list, select **Priority defaulting for procurement cases**.

    The decision table opens showing the table header, two input columns \(**Procurement case** and **Procurement case line**\), and an empty rules grid.

3.  Add a rule row to the rules grid.

4.  Configure the rule row by selecting each cell and providing the required values.

    -   To set a condition, select the operator cell and choose an operator, then select the condition value cell and enter a value.
    -   To set the result, select the result value cell and choose the priority level to assign when the rule matches.
    For detailed information about working with decision table cells, conditions, and results in Workflow Studio, see [Modify decision table rules in Workflow Studio](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

5.  In the **Rank** column, set the evaluation sequence for each rule.

    To change a rank value, double-click the number to edit it, enter a new value, and press **Enter**. The system evaluates rules in ascending rank order — the rule with the lowest rank number is evaluated first. Place rules for higher-urgency conditions at a lower rank number.

6.  Select **Save** to save the rule.

    Repeat steps 3 through 6 for each additional rule.

    Next, verify that the priority recalculation business rules are active for the procurement case and procurement case line tables.

7.  Navigate to **System Definition** &gt; **Business Rules** and search for **Recalculate priority on update** filtered by the procurement case table and the procurement case line table.

    Confirm both rules show as active.

8.  Test the configuration by creating or updating a procurement case with a case line that matches one of your configured rules.

    After the background rule runs, verify that the **Priority** field on the procurement case reflects the expected value. Also test a case that should not match any rule and confirm that its priority remains at **Planning**.

    Priority is assigned asynchronously after the record is saved, so allow a moment before checking the result.


## Result

Procurement cases are automatically assigned a priority level when they are created or updated. Procurement specialists can sort and filter their work queue by priority to work the most urgent cases first.

**Parent Topic:**[Configuring work prioritization](../concept/configuring-work-prioritization.md)


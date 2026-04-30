---
title: Configure decision tables for License and Permit Playbook
description: Use decisions tables to simplify the pricing configuration of a license or permit request that depends on multiple factors. Decision tables provide a single point where you can create, view, and modify pricing and dependent attributes.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure decision tables for License and Permit Playbook

Use decisions tables to simplify the pricing configuration of a license or permit request that depends on multiple factors. Decision tables provide a single point where you can create, view, and modify pricing and dependent attributes.

## Before you begin

Role required: admin

## About this task

In decision tables, each factor is a decision input. For example, if your agency is setting the price of a fishing permit, these inputs might include the location where the permit is being requested, the type of fish \(one or multiple\) that a fishing permit is being requested for, and the size of the fishing boat. Using a decision table can allow agents to present pricing in a straightforward manner, even when it depends on multiple factors.

## Procedure

1.  Identify which table fields in the License and Permit record will affect the fee associated with the license or permit request.

    For example, each type of fish under the fishing permit record has a different fee associated with it. These are examples of table fields that affect the total fee associated with the permit request.

2.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

3.  Select **New**.

4.  Enter a name for the decision table​ and ensure the table is accessible from **All Application Scopes**.​

5.  Select **Create &amp; Continue**.

6.  Select **Add** to add an input.

7.  Create an input ​with **Case** as the label, **Reference** as the type, and **License &amp; Permit case extension table**as the table.

8.  Select **Add result column** to add the pricing column​.

9.  Set the column label to **Price**, and​ set the result type to **Currency**.

10. Select **Done**.

11. Select **Add condition column**.

12. Set the input to **Case**, and set the Data to evaluate to **Field**.

13. Select the drop-down menu under Field, and select the field that is associated with pricing.

14. Select **Done**.

15. Select **Add New Decision Row**.

16. Select the new table cell that was added under the Field label column and ensure the operator reads “is”.

    If the field type is choice, the input value cannot be “None”. Select the appropriate choice input from the dropdown menu. If the field type is true/false, the input value should be **true**.

17. Select the new table cell that was added under the Price column, and​ enter the price associated with the field value​.

    If the field type is **choice**, repeat steps 15-17 for each option of the choice​.

18. Select the plus icon that appears below Results, and choose **Add Condition Column** to add another pricing field.

    Repeat until all pricing fields are added.

19. Select **Save** to save the decision table, then select **Close**.


## Result

The decision table is now created and can be associated with the License and Permit case type. For more information on how to do this, see [Associate a decision table with a License &amp; Permit case type​​](psds-associate-decision-table-with-lpr.md).


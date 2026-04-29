---
title: Create a pricing configuration decision table for the License and Permit Playbook
description: The License and Permit Playbook uses decision tables to configure pricing.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure decision tables, License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create a pricing configuration decision table for the License and Permit Playbook

The License and Permit Playbook uses decision tables to configure pricing.

## About this task

In the License and Permit Playbook, pricing is established by the following:

1.  Determining the application endorsements on which fees will be based. For more information on adding pricing endorsement fields, see [Add an endorsement field to a pricing configuration decision table in License and Permit Playbook](../concept/psds-lpr-decision-tables-pricing-endorsements.md#).
2.  Creating a decision table to capture the logic used to determine the fees charged.
3.  Associating the newly created decision table to the license/permit cases. For information on how to associate a decision table with a license/permit case, see [Associate a decision table with a License &amp; Permit case type​​](psds-associate-decision-table-with-lpr.md).

Each license/permit case references a specific decision table for pricing, which defines pricing based on the license/permit type and selected endorsements, and is unique to each extended License Permit Case Table.

## Before you begin

Role required: admin

## Procedure

1.  Identify which table fields in the License and Permit record will affect the fee associated with the license or permit request.

    For example, each type of fish under the fishing permit record has a different fee associated with it. These are examples of table fields that affect the total fee associated with the permit request.

2.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

3.  Select **New**.

4.  Enter a name for the decision table​, and ensure the application is set to License and Permit Playbook and that the table is accessible from **All Application Scopes**.​

5.  Enter a description.

6.  Select **Build decision table**.

7.  Select **Add** to add an input.

8.  Create an input ​with **Case** as the label, **Reference** as the type, and **License &amp; Permit case Extended Table** as the reference table.

9.  Select **Add result column** to add the pricing column​.

10. Set the column label to **Price**, and​ set the result type to **Currency**.

11. Select **Done**.

12. Select **Add condition column**.

13. Set the condition column label to **field**, the input to **Case**, and set the Data to evaluate to **Field**.

14. Select the dropdown menu under Field, and select the field that is associated with pricing.

15. Select **Done**.

16. Select **Add New Decision Row**.

17. Select the new table cell that was added under the Field label column and ensure the operator selected is **is**.

    If the field type is choice, the input value cannot be “None”. Select the appropriate choice input from the dropdown menu. If the field type is true/false, the input value should be **true**.

18. Select the new table cell that was added under the Price column, and​ enter the price associated with the field value​.

    If the field type is **choice**, repeat steps 15-17 for each option of the choice​.

19. Select the plus icon that appears below Results, and choose **Add Condition Column** to add another pricing field.

    Repeat until all pricing fields or other endorsement fields are added. For more information on endorsements, see [Pricing endorsements in License and Permit Playbook](../concept/psds-lpr-decision-tables-pricing-endorsements.md#).

20. Select **Save** to save the decision table, then select **Publish**.


## Result

The decision table is now created and can be associated with the License and Permit case type. For more information on how to do this, see [Associate a decision table with a License &amp; Permit case type​​](psds-associate-decision-table-with-lpr.md).

As an admin, you can use a price adjustment definition to add adjustments to field prices based on the conditions of fields that are not price fields, such as residency status of the constituent for the location they are requesting in. For more information on how to add price adjustment definitions, see [Add a price adjustment definition to a decision table​ in License and Permit Playbook](psds-decision-table-price-adjustment.md).


---
title: Total Cost of Ownership \(TCO\) for enterprise assets
description: You can configure your Total Cost of Ownership \(TCO\) to track the total cost of your assets and to enable capital planning.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Total Cost of Ownership \(TCO\) for enterprise assets

You can configure your Total Cost of Ownership \(TCO\) to track the total cost of your assets and to enable capital planning.

During an asset's life span, assets incur costs, which include initial capital costs, costs associated with purchasing new parts, labor costs, and contract costs. TCO for an asset is the sum of all these expenses.

## Benefits of TCO

-   Track and analyze expenses such as procurement, maintenance, repairs, and disposal across the asset hierarchy.
-   Gain better visibility and control over asset-related expenses throughout the life-cycle.
-   Bench mark asset costs against similar assets and asset models to compare performance.

## TCO calculation

TCO is the sum of all the expenses that occurred on the asset during its lifetime. TCO is calculated for the asset by adding the amount for all the expense lines that are created against the asset. The total cost of an asset is updated whenever an expense line is added.

Considerations while calculating TCO:

-   Initial TCO includes the purchase cost coming from the expense line created when an asset record is created.
-   When a new asset record is created, a new expense line is created using the cost field on the asset record.
-   When the cost field is updated, the existing expense line record is also updated.
-   For simple and complex assets, TCO is calculated by aggregating all the expense lines associated with the asset. Whenever a new expense line is added to the asset, the TCO reflects the updated total automatically.
-   For serialized assets, asset TCO is the sum of all expense lines under that asset.
-   For complex assets, the cost incurred on the child is also added to the TCO of the parent asset.
-   If a child asset is swapped, there will be one expense line created that is the operational cost. The capital cost of new child assets is also added to the parent TCO. The **last\_used** field in the swap asset is populated and this field is used to query any expense lines created after that. The **last\_used** field on the swapped out asset is populated as it goes back to the stockroom.
-   The cost of child assets is part of the parent asset cost for a complex asset and thus expense lines for child assets are empty.
-   If a child asset is removed, its expense lines persist and the parent TCO doesn't get affected.
-   In the case of user-assembled assets, parent and child both have expense lines and the child expense line roll ups to the parent and the amount is added to the parent TCO.
-   For multi-hierarchy assets, any expense line created on the child asset is referenced by a many-to-many relationship between all the parents in the hierarchy.
-   Consumables are set to merge and split and so are the expense lines. Any expense lines created by task rate cards are added to the TCO. The calculation applies for simple assets. In case consumables are used as child assets, then their expense lines are rolled up to the parent. TCO won’t be tracked for individual consumables.
-   The value obtained by reselling assets is added as a negative cost to TCO. For leased assets that have a monthly lease payment, create expense lines on the start date of the lease for every month.
-   The **Asset** field on expense lines is populated with the asset reference from the task record.
-   Expense lines created after closing a work order task or an incident will have its **Asset** field populated from the asset reference on the work order task or incident.

## TCO benchmark and threshold

After you specify a TCO benchmark cost, the TCO benchmark threshold is automatically calculated by multiplying the TCO Benchmark by the TCO benchmark threshold percentage. You can manually override the TCO benchmark threshold by changing the percentage in the **asset\_tco\_benchmark\_threshold\_percentage** system property.

You can manually override the TCO benchmark threshold by changing the value on the **TCO benchmark threshold** field in the Financial section of a model form.

If you update the TCO benchmark, the TCO benchmark threshold gets recalculated.

## Rate cards, expense lines, and expense categories

The Enterprise Asset Management application automatically sums the time worked records and calculates the total cost by multiplying the rate cards. Rate cards are created for each task across all workflows. Rate cards capture costs on a per task basis or on the time consumed. The Enterprise Asset Management application supports the following rate cards:

-   task rate cards: Cost captured by tasks.
-   labor rate cards: Cost captured by the time consumed on an hourly basis. Labor rates can be defined at the user level.

**Note:** To use rate cards, you must activate the ServiceNow® Cost Management \(com.snc.cost\_management\) plugin.

By default, the task rate card is used. To change to using the labor rate card, open a task rate record and select the **Use time worked** field.

After a task is closed, an expense line is created based on the task time worked captured. An expense category is then attributed to the expense line. The expense lines amounts are added to the total cost on the asset. The expense lines appear under the Expense line related list under the asset.

## Time capturing for tasks

Each task has a time capturing capability that creates time worked records for you.

You can start, record time, pause, resume, and close your tasks as described below:

1.  Select **Start Work** to begin your work. This moves the status of the task from **Open** to **Work in Progress**. You can then either select **Start Timer** or **Record Time** to capture time.
    -   **Start Timer**: Automatically captures time. After you select this button, the timer is initialized.
    -   **Record Time**: Manually enter the time in hours, minutes, and seconds in the Record Time dialog box and select **Save** to capture the time record.
2.  Select **Pause Work** to pause work. After you pause your work, the timer stops and a task work record automatically gets created in the Time Worked tab. Every time you pause your work, a task work record gets created. Based on the number of times you pause work, multiple task work records get created.
3.  Select **Resume** to resume your work and restart the timer. You can also select **Close Task** to close your task.

When you select **Close task**, the time as well as the task gets closed. To arrive at the total time spent on a task, all task work record entries created for that task are added up and then multiplied with the labor rate to arrive at the total cost for a task.

## TCO reports

There are two types of TCO reports; TCO comparison and TCO vs benchmark. TCO comparison reports are stacked by expense category.

## Normalize TCO

Normalizing TCO refers to averaging the cost over the useful life and the asset life. The normalized calculation is for Projected TCO reports, which are only offline.

## Domain separation

TCO reports support domain separation.

## Upgrade considerations

If you’re upgrading to Australia, after the scheduled job **TCO Upgrade for Enterprise Assets** runs, the following updates are made:

-   The **Asset** field on task records is populated on all the expense lines using the source table mentioned in the **Source ID** field. The source table defines from where the expense line has been created. Whether it’s being created for a task, a configuration item, a contract, or for a purchase asset. When the scheduled job **TCO Upgrade for Enterprise Assets** runs, it searches for all task records and populates asset references from the task record to the corresponding expense line for the task. Similarly, the same scheduled job searches for all configuration items \(CI\) and populates asset references from the CI to the corresponding expense lines.
-   The **Expense category** field, introduced in Australia, is populated based on the source of the expense line. There are several expense categories for tasks. For example, the expense lines created for a purchase asset and for a contract asset have different expense categories. Similarly, there are different expense categories for CIs too.
-   The following three fields in an asset record get populated:
    -   cmn\_asset\_tco: View this field in the Financial section in an asset record.
    -   cmn\_end\_of\_useful\_life: View this field in an asset record by selecting the vertical ellipsis next to **Asset Details** and then select **Show XML**.
    -   cmn\_first\_used: View this field in an asset record by selecting the vertical ellipsis next to **Asset Details** and then select **Show XML**.
-   Any expense lines created on simple assets will be added up to asset\_tco.
-   For pre-assembled and user-assembled assets, any expense lines created on assets will also roll up to the parent TCO.

## TCO configuration

Configuring TCO involves the following procedures:

-   Create task rate cards to capture costs per task type.

    For detailed instructions, see [Create a task rate card in Enterprise Asset Workspace](../task/create-eam-task-rate-card.md).

-   Create labor rate cards to capture costs by the time consumed on an hourly basis.

    For detailed instructions, see [Create a labor rate card in Enterprise Asset Workspace](../task/create-eam-labor-rate-card.md).

-   Create a TCO report to compare the actual or projected TCO of assets and a TCO report source.

    For detailed instructions, see [Create a TCO report in Enterprise Asset Workspace](../task/create-eam-tco-report.md).

-   Create a TCO report source to add sources to a TCO report.

    For detailed instructions, see [Create a TCO report source in Enterprise Asset Workspace](../task/create-tco-report-source-eam.md).

-   Create expense lines for closed tasks.

    For detailed instructions, see [Create expense lines for closed tasks in Enterprise Asset Workspace](../task/create-expenselines-closed-tasks-eam.md).


-   **[Create a TCO report in Enterprise Asset Workspace](../task/create-eam-tco-report.md)**  
Create a TCO report to compare the actual or projected TCO of assets or to compare the actual or projected asset TCO with the benchmark cost of the enterprise model.
-   **[Create a TCO report source in Enterprise Asset Workspace](../task/create-tco-report-source-eam.md)**  
Create a TCO report source to add report sources to a TCO report.
-   **[Create a task rate card in Enterprise Asset Workspace](../task/create-eam-task-rate-card.md)**  
Create a task rate card to capture costs per task type in the Enterprise Asset Workspace.
-   **[Create expense lines for closed tasks in Enterprise Asset Workspace](../task/create-expenselines-closed-tasks-eam.md)**  
Automatically create expense lines for previously closed tasks, that originally had no expense lines, in order to calculate costs for those tasks.
-   **[Create a labor rate card in Enterprise Asset Workspace](../task/create-eam-labor-rate-card.md)**  
Create a labor rate card to capture costs by the time consumed on an hourly basis.

**Parent Topic:**[Create and manage enterprise assets](create-manage-enterprise-assets.md)


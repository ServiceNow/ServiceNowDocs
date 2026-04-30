---
title: Asset Total Cost of Ownership for Hardware Asset Management
description: Assets incur costs throughout their life cycle, including initial capital costs and operational costs. Asset Total Cost of Ownership helps Asset managers to understand, analyze, and track the Total Cost of Ownership \(TCO\) of assets, where the total cost includes initial capital cost and operation cost.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset Total Cost of Ownership for Hardware Asset Management

Assets incur costs throughout their life cycle, including initial capital costs and operational costs. Asset Total Cost of Ownership helps Asset managers to understand, analyze, and track the Total Cost of Ownership \(TCO\) of assets, where the total cost includes initial capital cost and operation cost.

**Important:** You must install Hardware Asset Management 10.0.0 version or later to access the Asset Total Cost of Ownership feature.

## TCO benefits

-   Track and analyze incurred expenses across the asset hierarchy.
-   Benchmark asset costs against assets and asset model to compare performance.
-   Create TCO reports and use predefined reports for better financial planning of your assets.

## TCO calculation

Costs incurred on the assets are created as expense lines. The expense line shows the history of cost incurred for an asset, which includes the total amount on the expense lines, or the initial capital cost and total expense on all the child assets.

TCO is the sum of all the expenses that occurred on the asset during its lifetime.

-   When an asset record is created, the initial cost includes the purchase cost from an expense line that gets created. If you update the cost, the expense line record gets updated.
-   For serialized assets, the capital cost is added one time only and the rest is considered as the operational cost. Any expense line created is added to the total cost.
-   For a child asset,
    -   If any cost is incurred on a child asset, the same cost is added to the TCO of the parent asset.
    -   If a child asset is removed, the expense lines of the child asset persist and the TCO of the parent isn't affected.
    -   If a child asset is swapped, one expense line is created for operational cost.
-   Any expense line created by rate cards is added to the TCO of assets.
-   Incidents affecting hardware assets already include task rate cards.

## Rate cards, expense lines, and expense categories

Rate cards help you track capital, labor, material, and contract costs and the generated expense lines track these costs. For each task, Hardware Asset Management captures the time worked on that task. After a task is closed, Hardware Asset Management creates expense lines based on the time worked on the task. These expense lines amounts are added to the total cost of the asset. An expense category is then attributed to the expense line. The expense lines appear in the **Expense Lines** tab on the Hardware Asset Details form.

The Hardware Asset Management application supports the following rate cards:

-   [Task rate cards](../task/create-ham-task-rate-card.md)
-   [Labor rate cards](../task/create-ham-labor-task.md)

**Note:** The labor rate card is a part of the created expense line and is valid if you’ve included the labor rate card information with the task rate card, which is recording the time worked on the task.

## Capture time for tasks

Each task has a time capturing capability that creates time worked records for that user.

You can start, start a timer, pause, resume, and save your tasks. A new record entry is created in the Time Worked tab in the following scenarios:

-   Select **Start** to begin your work and then select **Save**.
-   Select **Start Timer** to begin recording the time for a task.
-   Select **Pause** to pause the recording.
-   Select **Resume** to resume the recording.

The timer stops only when you close a task. To arrive at the total time spent on a task, all the record entries are added up and then multiplied with the labor rate to arrive at the total cost for a task.

You can select **Record Time** to add time to the tasks manually.

## Work with TCO

TCO enables you to perform the following actions:

-   Create expense lines to track the initial and operational cost of your hardware assets.
-   Track and calculate TCO for the following workflow tasks and the time worked on an individual task in a workflow:

    -   Disposal
    -   Donation
    -   Zero Touch Refresh
    -   Contract renewal

        **Note:** For Contract cost, allocate and distribute amount asset options are used on the contract rate card to distribute the contract cost evenly. You must add assets to the Asset covered for the contract rate card.

    -   Return Merchandise Authorization \(RMA\)
    -   Lease
    -   Loaner
    -   Hardware asset refresh
    -   Asset reclamation
    **Note:**

    Rate cards are included for the Hardware Asset Management workflows. To activate these rate cards, select the **Active** check box on the Task Rate Card form.

-   Track the TCO benchmark of a hardware model. After you specify a TCO benchmark cost, the TCO benchmark threshold is calculated by using the following formula:

    ```
    TCO benchmark cost * TCO benchmark threshold percentage
    ```

    , where the TCO benchmark threshold percentage is set to 75% of the TCO benchmark cost by default. For more information, see [Hardware model details](../reference/hardware-model-fields.md).

-   Create a report and compare TCO for a group of assets. For more information on the TCO dashboard and reports, see [Asset analytics view](asset-analytics-view.md).
-   For real-time or offline TCO reports, normalize the asset TCO over its useful life and compare the normalized TCO for different models and assets.
    -   When the useful life of the asset is equal to or greater than asset life, the Normalized TCO \(TCO per month\) is calculated by using the following formula:

        ```
        (Purchase cost / Useful life) + (Sum of operational cost / Asset life)
        ```

    -   When the useful life of the asset is lower than asset life, Normalized TCO \(TCO per month\) is calculated by using the following formula:

        ```
        (Purchase cost + Sum of operational cost) / Asset life
        ```


**Note:** TCO isn't calculated and tracked for the following assets and consumables:

-   Bundle assets
-   Pallet assets
-   Individual consumables

    If you have used consumables as child assets, their expense lines are added to the parent asset.

-   Excluded assets
-   Assets that are a part of the opted out model categories.


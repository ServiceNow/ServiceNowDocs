---
title: Scoring in Strategic Planning
description: Scoring enables you to prioritize items, such as epics, projects, demands, initiatives, strategic programs, and other planning items, based on a defined quantitative metric.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Explore, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Scoring in Strategic Planning

Scoring enables you to prioritize items, such as epics, projects, demands, initiatives, strategic programs, and other planning items, based on a defined quantitative metric.

Before selecting a scoring framework for your portfolio plan, it's helpful to first learn about the pre-defined frameworks available for you to use. Later you can choose if you want to use one of the pre-defined scoring frameworks, or create a custom scoring framework, based on your preferred scoring parameters.

The following are the three pre-defined scoring frameworks available to use for your portfolio plan:

-   **RICE**

    A framework to prioritize and evaluate items by scoring each criterion. It helps teams assess and compare items based on four key criteria: Reach, Impact, Confidence, and Effort.

    Parameters:

    -   Reach- Indicates the number of people or users who will be affected by the project or feature. It's essential to estimate the potential audience that the item can reach. For example, if a new feature is likely to be used by a small subset of users, it might have a lower reach score compared to a feature that will be utilized by a large portion of the user base.

        To populate this value, answer the question- How many existing/target users within a given period of time?

    -   Impact- Measures the potential impact or benefit that the item will bring to the users or the organization. This criterion focuses on the positive outcomes and value that the project can deliver.

        To populate this value, answer the question- How much will this impact individual users?

    -   Confidence- Confidence gauges the level of certainty that the project will achieve its intended results. This criterion assesses how confident the team is in their estimates of reach and impact. Items with higher confidence are generally based on solid data, user feedback, or previous experiences, making it more likely for them to deliver the expected results.

        To populate this value, answer the question- How confident are you about the impact and reach scores?

    -   Effort- Duration in person months, based on product, design, and development effort. This criterion helps teams understand the relative difficulty of executing. Items with higher effort scores may require more development time, financial investment, or significant changes to existing systems.

        To populate this value, answer the question- How much time will this item require in person months?

    The RICE score is calculated with this formula:

    ```
    RICE Score = (Reach x Impact x Confidence)/Effort
    ```

-   **Value vs Effort**

    A framework to prioritize planning items, based on the effort estimate and the value it brings to the users/customers. The Value vs. Effort method is the quickest way to prioritize your backlog items.

    Parameters:

    -   Value- Significance of items based on the potential revenue, user benefit, business impact, and strategic goals.

        To populate this value, answer the question- How does this contribute to your goal?

    -   Effort- Duration to build the product, including product, design, and development estimates.

        To populate this value, answer the question- How difficult it is to deliver the task?

    The Value vs. Effort score is calculated with this formula:

    ```
    Value vs. Effort Score = Value/Effort
    ```

-   **WSJF**

    A framework to sequence items for maximum benefit, particularly useful where frequent re-prioritization is a driver of economic value. This score is based on the relative cost of delay and relative job duration, business value, time criticality, risk reduction, and job size.

    Parameters:

    -   User Business value- The relative importance to the users/customers and its potential impact on revenue.

        To populate this value, answer the question- How important is this item to your business?

    -   Time Criticality- Identifies how the user business value will decay over time and denotes the urgency to release the item/feature.

        To populate this value, answer the question- How does the item value decay over time?

    -   Risk Reduction- Identifies the items that can reduce technological and business risks and enable new opportunities.

        To populate this value, answer the question- What else does the item do for your business?

    -   Job Size- Relative duration to complete the task.
    -   To populate this value, answer the question- When will you complete the task?
    The WSJF score is calculated with this formula:

    ```
    WSJF Score = (User Business value + Time criticality + Risk reduction)/Job Size
    ```


To get started with Scoring your planning items in Strategic Planning, see [Scoring planning items in Strategic Planning Workspace](using-scoring-frameworks-in-startegic-planning-workspace.md).

**Parent Topic:**[Exploring Portfolio Planning in Strategic Planning Workspace](../../alignment-planner-workspace/concept/alignment-planner-workspace.md)

**Related topics**  


[Custom scoring frameworks in Strategic Planning](custom-scoring-frameworks-in-strategic-planning.md)


---
title: Configuring target source for target automation
description: Configure target sources for target automation so that the goal user can define a target source when setting a target for the goal. Defining a target source for a target updates the actual value of the target automatically.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configuring target source for target automation

Configure target sources for target automation so that the goal user can define a target source when setting a target for the goal. Defining a target source for a target updates the actual value of the target automatically.

Use the following steps as guidelines for configuring target sources.

1.  Create a target source for a target to configure it as a source to update the actual value of the target. For more information, see [Create a target source](../task/create-target-source-for-automating-the-actual-value-of-the-targets-apw.md).

    The context variable is required for target source types Assessment/Survey and PA Indicator. The mandatory context variables are automatically created while creating a target source with the type selected as Assessment/Surveys or PA Indicator. For more information on when the mandatory context variables are created, see [Context variable in target source](context-variable-in-target-source-apw.md).

2.  If required, create context variables for the target source so that the required data is fetched from the context variables to update the actual value of the target. For more information, see [Create context variables for a target source](../task/create-context-variable-for-a-target-source-apw.md).

-   **[Context variable in target source](context-variable-in-target-source-apw.md)**  
The context variable is an additional configuration for the target source that can be used on the Target form to fetch the required data and auto-update the **Actual value** field on the Target form. A context variable is required for target source types Assessment/Survey and PA Indicator.
-   **[Create a target source for automating the Actual value of the targets](../task/create-target-source-for-automating-the-actual-value-of-the-targets-apw.md)**  
Create a target source so that the goal user can configure it for the targets to automate the Actual value of the targets.
-   **[Create a context variable for a target source](../task/create-context-variable-for-a-target-source-apw.md)**  
Create a context variable manually if you want to configure more context variables for a target source.
-   **[Create a context variable for the target source type PA Indicator](../task/create-context-variable-for-a-target-source-type-pa-indicator-apw.md)**  
Create a context variable manually for the target source type PA Indicator if the breakdown is of Choice list type.

**Parent Topic:**[Configuring goals in Strategic Planning](configuring-goal-framework-apw.md)


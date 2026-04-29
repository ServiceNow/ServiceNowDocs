---
title: Configuring target source for target automation using Goal Framework for SPM
description: Configure target sources for target automation so that the goal user can define a target source when setting a target for the goal. Defining a target source for a target updates the actual value of the target automatically.
locale: en-US
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Configuring target source for target automation using Goal Framework for SPM

Configure target sources for target automation so that the goal user can define a target source when setting a target for the goal. Defining a target source for a target updates the actual value of the target automatically.

Use the following steps as guidelines for setting targets and automating the actual value of the targets using Goal Framework for SPM. Some of these steps require the sn\_gf.goal\_user role and some require the sn\_gf.goal\_admin role.

1.  Create a target source for a target to configure it as a source to update the actual value of the target. For more information, see [Create a target source](../task/create-target-source.md).

    The context variable is required for target source types Assessment/Survey and PA Indicator. The mandatory context variables are automatically created while creating a target source with the type selected as Assessment/Surveys or PA Indicator. For more information on when the mandatory context variables are created, see [Context variable in target source](context-variable-in-target-source.md).

2.  If required, create context variables for the target source so that the required data is fetched from the context variables to update the actual value of the target. For more information, see [Create context variables for a target source](../task/create-context-variable-for-a-target-source.md).

-   **[Context variable in target source](context-variable-in-target-source.md)**  
The context variable is an additional configuration for the target source that can be used on the Target form to fetch the required data and auto-update the **Actual value** field on the Target form. A context variable is required for target source types Assessment/Survey and PA Indicator.
-   **[Create a target source for automating the Actual value of the targets](../task/create-target-source.md)**  
Create a target source so that the goal user can configure it for the targets to automate the Actual value of the targets.
-   **[Create context variable for a target source](../task/create-context-variable-for-a-target-source.md)**  
Create a context variable manually if you want to configure more context variables for a target source.
-   **[Create a context variable for the target source type PA Indicator](../task/create-context-variable-for-a-target-source-type-pa-indicator.md)**  
Create a context variable manually for the target source type PA Indicator if the breakdown is of Choice list type.

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](configuring-goal-framework.md)


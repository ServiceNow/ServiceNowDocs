---
title: Context variable in target source
description: The context variable is an additional configuration for the target source that can be used on the Target form to fetch the required data and auto-update the Actual value field on the Target form. A context variable is required for target source types Assessment/Survey and PA Indicator.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring target source for target automation, Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Context variable in target source

The context variable is an additional configuration for the target source that can be used on the Target form to fetch the required data and auto-update the **Actual value** field on the Target form. A context variable is required for target source types Assessment/Survey and PA Indicator.

The context variable is automatically created \(with the **Mandatory** field set to **true** on the context variable form\) for the target source \(of type Assessment/Survey and PA Indicator\) when the Goal Framework for SPM scope is selected before creating a target source. The context variables created automatically are also known as mandatory context variables.

The mandatory context variables are created when you've selected the Goal Framework for SPM scope and you've met one of the following conditions:

-   \(For target source type, Assessment/Survey\) On the Target Source form, the **Type** field is set to **Assessment/Survey** and the **Assessment Metric Types** field is populated with a metric type of **Evaluation method = Assessment**.

    ![Assessment metric type.](../images/goals-assessment-metric-type-apw.png)

-   \(For target source type, PA Indicator\) On the Target Source form, the **Type** field is set to **PA Indicator** and the value populated in the **Breakdown** field isn't of Choice list type.

    To create a context variable for the target source type, PA Indicator, where the Breakdown field is of Choice list type, see [Create a context variable for the target source type PA Indicator](../task/create-context-variable-for-a-target-source-type-pa-indicator-apw.md).


**Note:** Mandatory context variables can't be deleted.

You can also create context variables manually for a target source and use them to configure for fetching the required data and auto-updating the **Actual value** field on the Target form. For more information on how to create a context variable manually, see [Create a context variable for a target source](../task/create-context-variable-for-a-target-source-apw.md).

**Parent Topic:**[Configuring target source for target automation](setting-targets-for-a-goal-and-automating-the-actual-value-using-agf-apw.md)


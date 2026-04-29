---
title: GRC state model configuration
description: Create a Governance, Risk, and Compliance state model to define the steps, transitions, and validations for a custom workflow in CAM. State models control how authorization packages move through workflow life cycles and determine which actions are available at each step.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# GRC state model configuration

Create a Governance, Risk, and Compliance state model to define the steps, transitions, and validations for a custom workflow in CAM. State models control how authorization packages move through workflow life cycles and determine which actions are available at each step.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Select **New** to create a state model record.

3.  On the **GRC state model New record** form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Name|Enter a name for the state model.|
    |Active|Select the **Active** option to enable the state model.|
    |Table name|Select **Authorization Package \[sn\_irm\_cont\_auth\_auth\_pack\]**.|
    |State field|Select **State Model \[state\_model\]**.|
    |State model|Select **Step \[step\]**.|

4.  Select **Submit**.

    You’re directed to the **GRC state models** list page.


## Result

The state model is ready to be configured with workflow states, transitions, and attributes. After completing the configuration, you can map the state model to a workflow configuration and use it for authorization packages.

## What to do next

[Create GRC workflow states](add-workflow-states.md)

[Add existing attributes to a GRC workflow state](configure-state-model-attributes.md)

[Create a new state model attribute](configure-new-state-model-attributes.md)


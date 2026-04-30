---
title: Create GRC model state transition conditions
description: Add Governance, Risk, and Compliance model state transition conditions to a state transition to validate data before enabling authorization packages to move between workflow steps. Transition conditions verify that the required information is complete and accurate before packages proceed.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Configure transition between state models, Create GRC workflow states, GRC state model configuration, CAM workflow configuration, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create GRC model state transition conditions

Add Governance, Risk, and Compliance model state transition conditions to a state transition to validate data before enabling authorization packages to move between workflow steps. Transition conditions verify that the required information is complete and accurate before packages proceed.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Open the state model record that contains your workflow states.

3.  On the **GRC workflow states** related list, select the workflow state.

4.  On the **Model State Transition** related list, select the state transition for which you want to add transition conditions.

5.  On the **GRC model state transition conditions** section, select **New**.

6.  On the **GRC model state transition condition New record** form, fill in the fields.

<table id="table_kgw_fgz_thc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifies the condition in lists and for reference.

</td></tr><tr><td>

Description

</td><td>

Explanation of the condition's purpose.

</td></tr><tr><td>

Error message

</td><td>

Message displayed when the validation fails.

</td></tr><tr><td>

Requires

</td><td>

Specifies the type of validation to perform. The options are:-   Required Fields: Validates that the required fields aren’t empty
-   Task has been through Approval: Checks if the approval process occurred
-   Task is Approved: Validates approval was granted
-   Task is Rejected: Validates task was rejected
-   Transition Condition: Custom condition logic. If you select Transition Condition, select the condition for validation.
-   Transition Script: JavaScript-based validation. Enable **Turn on ECMAScript 2021 \(ES12\) mode** to use JavaScript syntaxes and features for validation.


</td></tr></tbody>
</table>    **Note:** All conditions must pass for the transition to succeed.

    ![Adding state transition conditions.](../image/WF-transition-condition1.png)

7.  Select **Submit** to save the transition condition.


## What to do next

[Add existing attributes to a GRC workflow state](configure-state-model-attributes.md) or [Create a new state model attribute](configure-new-state-model-attributes.md)


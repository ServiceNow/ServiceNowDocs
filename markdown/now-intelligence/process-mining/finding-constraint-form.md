---
title: Finding constraint form
description: Use the Finding constraint form to configure finding constraints for your finding definition. In addition to finding rules, finding constraints further narrow down the scope of your finding definitions using metrics like duration and relation constraints.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Process Mining reference, Process Mining, Platform Analytics]
---

# Finding constraint form

Use the Finding constraint form to configure finding constraints for your finding definition. In addition to finding rules, finding constraints further narrow down the scope of your finding definitions using metrics like duration and relation constraints.

<table id="table_tfh_3jh_4vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the finding constraint

</td></tr><tr><td>

Finding Definition

</td><td>

Finding definition associated with this finding constraint. This field is automatically populated.

</td></tr><tr><td>

Start Condition

</td><td>

Event which triggers a finding constraint. You may select an existing rule, or create a new one using the plus \(+\) button to the right of the field.**Note:** For details on creating a condition, see [Configure advanced conditions](../task/po-advanced-conditions.md).

</td></tr><tr><td>

End Condition

</td><td>

Event that concludes a finding constraint. You may select an existing rule, or create a new one using the plus \(+\) button to the right of the field. **Note:** For details on creating a condition, see [Configure advanced conditions](../task/po-advanced-conditions.md).

</td></tr><tr><td>

Duration min

</td><td>

The minimum duration between when the event defined in the **Start condition** field and event defined in the **End condition** field. The event in the **End condition** field must occur after the amount of time specified in this field.

</td></tr><tr><td>

Relation constraint

</td><td>

Optional constraint conditions to further define when the constraint triggers.-   **-- None --**

No relation constraint

-   **has the same**

Records must have the same value in a specific field. Specify this field in the **Relation constraint field** field.

-   **has different**

Records must have different values in a specific field. Specify this field in the **Relation constraint field** field.

-   **performed by the same user**

Start and end conditions must be triggered by the same user.

-   **performed by different user**

Start and end conditions must be triggered by different users.

-   **is same event**
-   **is different event**

</td></tr><tr><td>

Relation constraint field

</td><td>

Field associated with the relation constraint.

 This field appears when **has the same** or **has different** is selected in the **relation constraint** field.

 **Note:** The available relation constraint field will appear empty if there are no selections in the **Start Condition** or **End Condition** fields.

</td></tr><tr><td>

Duration max

</td><td>

The maximum duration between when the event defined in the **Start condition** field and event defined in the **End condition** field. The event in the **End condition** field must occur before the amount of time specified in this field.

</td></tr><tr><td>

Relation constraint field

</td><td>

**Note:** This field only appears if the **Relation constraint** field is set to **has the same** or **has different**.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)


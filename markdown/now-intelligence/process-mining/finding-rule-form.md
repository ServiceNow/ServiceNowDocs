---
title: Finding rule form
description: Use the Finding Rule form to configure finding rules for your finding definition. Finding rules define what record criteria triggers your finding definitions.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Process Mining reference, Process Mining, Platform Analytics]
---

# Finding rule form

Use the Finding Rule form to configure finding rules for your finding definition. Finding rules define what record criteria triggers your finding definitions.

<table id="table_kjk_ml1_krb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Chain number

</td><td>

Chain to which this finding rule belongs.**Note:** Finding rules can consist of multiple chains.

</td></tr><tr><td>

Finding definition

</td><td>

Finding definition associated with this finding rule. This field is automatically populated.

</td></tr><tr><td>

Sequence

</td><td>

Order in which rules in the same chain execute. Rules with a lower value execute before those with a higher value.

</td></tr><tr><td>

Start condition

</td><td>

Event that triggers a finding rule. You may select an existing rule, or create one using the plus \(+\) button to the right of the field.**Note:** For details on creating a condition, see [Configure advanced conditions](../task/po-advanced-conditions.md).

</td></tr><tr><td>

Relation

</td><td>

Connection between the event defined in the **Start condition** field and event defined in the **End condition** field. -   –- None –-
-   directly followed by
-   eventually followed by
-   not directly followed by
-   not eventually followed by

 **Note:** Order rule sequences appropriately for how you want the rule set to execute relevant to selected relations. If you select an option other than **none**, you’ll want to create a rule, which completes the expression in the desired sequence.

</td></tr><tr><td>

End condition

</td><td>

Event that concludes a finding rule. You may select an existing rule, or create one using the plus \(+\) button to the right of the field. **Note:** For details on creating a condition, see [Configure advanced conditions](../task/po-advanced-conditions.md).

</td></tr><tr><td>

Track duration

</td><td>

Whether the duration between the start and end conditions are tracked.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)


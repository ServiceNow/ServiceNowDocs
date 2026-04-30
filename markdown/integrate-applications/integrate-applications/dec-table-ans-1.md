---
title: Provide answers to the decision table
description: Provide subflows as answers to the conditions mentioned in the decision table. When the specified conditions are met, the associated subflow is triggered.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Provide answers to the decision table

Provide subflows as answers to the conditions mentioned in the decision table. When the specified conditions are met, the associated subflow is triggered.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Open the record for the **Jenkins v2 spoke**.

3.  In the **Decisions** tab, click **New**.

4.  On the form, fill these values:

<table id="table_awj_xgv_z3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Default answer

</td><td>

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Jenkins. See [Jenkins v2 Spoke](../concept/jenkins-spoke-1.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.1.  Click the Lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Jenkins v2 Webhook Answer Subflow [sn_jenkinsv2_spoke_webhook_answer_subflow]`.

</td></tr></tbody>
</table>5.  Click **Submit**.



---
title: Real time protection policies
description: You can configure policies to protect sensitive data in real-time through alerts and blocking actions.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Real time protection, Data privacy, Data Privacy, Platform Privacy]
---

# Real time protection policies

You can configure policies to protect sensitive data in real-time through alerts and blocking actions.

## Before you begin

Role required: data\_privacy\_admin

**Note:** Real-time protection is only enforced for user interactive sessions and not background scripts, integrations or instance data replication.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data privacy** &gt; **Real time protection** &gt; **Real time protection policies**.

    **Note:** Child tables inherit all configurations from parent tables and columns. For example, if a policy is defined on the Task table's description column, then the policy will apply automatically to the Incident table's description column.

2.  Select **Create new policy.**

    **Note:** In order to create real time protection polices, you must first create at least one[alert data pattern](../concept/alert-data-patterns.md).

3.  Fill in the fields on the form:

<table id="table_rpk_b5z_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Enter a descriptive name for this alert policy. This name will help you identify the policy when managing real-time protection rules.

</td></tr><tr><td>

Table

</td><td>

Select the table where alert policies will monitor for sensitive data. Only one table can be selected per policy.

</td></tr><tr><td>

Column

</td><td>

Select the column within the table that will be monitored for sensitive data patterns.

</td></tr><tr><td>

Action

</td><td>

Choose the action to take when sensitive data is detected: -   **Alert and block** notifies you of the infraction and prevents the action.
-   **Alert** notifies without blocking.


</td></tr><tr><td>

Alert data pattern

</td><td>

Select the data pattern that defines what sensitive data to detect. **Note:** You can create [Alert data patterns](../concept/alert-data-patterns.md) if none exist.

</td></tr><tr><td>

Display message

</td><td>

Enter the message users will see when their action is blocked. It should be clear and actionable so they understand why the block occurred.

</td></tr></tbody>
</table>4.  Toggle the **Active** button if you want to activate the policy.

5.  Select **Create**.

    The new real time protection policy is added.


## What to do next

The protection policies you create show in the main view. You can edit or delete them by selecting the appropriate option from their Actions menu. You can also select either of the following buttons under each policy:

|Button|Description|
|------|-----------|
|View logs|View the top 100 activity logs that contain the most sensitive data from the last month. For more information, refer to [User sensitive data logs](user-sensitive-data-logs.md) for more information.|
|View details|View the configuration of the protection policy. You can also toggle the **Active** button to turn the policy on or off.|


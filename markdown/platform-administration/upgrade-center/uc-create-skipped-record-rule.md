---
title: Create a skipped record rule
description: Create skipped record rules based on your set conditions to define your customizations after an upgrade.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Create a skipped record rule

Create skipped record rules based on your set conditions to define your customizations after an upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Administration** &gt; **Skipped Record Rules Editor**.

    A list of available rules shows up.

    **Note:** By default, a few inactive sample rules have been provided. You can set it to active if you want to use the sample rules.

2.  Select **New** to create a new skipped record rule.

    The Upgrade Skipped Record Rules form shows up.

    **Note:** The new rules are active by default. You can make them inactive if you don’t want to use them.

3.  Fill in the fields on the form.

<table id="table_lhx_vd3_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Order

</td><td>

Order in which the rule runs.**Note:** The order number automatically increments from the last rule order created.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule.

</td></tr><tr><td>

Conditions

</td><td>

Conditions as to when the rules are implemented on the skipped records.**Note:** These conditions are only for skipped records that are not being reviewed. If you set the disposition condition to anything other than the skipped records, that condition doesn’t work.

</td></tr><tr><td>

Action

</td><td>

Option to choose one of the four following actions:-   Keep My Modifications \(Always Retain\)
-   Revert and Keep Inactive
-   Assign Skipped Records to User
-   Assign Tags to Skipped Records
**Note:** Based on the selected action, a message shows up with more information.

</td></tr><tr><td>

Comment

</td><td>

Add a comment on the conditions being set.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The new rule appears on the list of available rules.


## What to do next

You can now run the skipped record rules either automatically during an upgrade or can run on demand on the skipped records. See [Execute a skipped record rule](uc-execute-skipped-record-rule.md#) for more information.

**Parent Topic:**[Administering Upgrade Center](../reference/uc-administration.md)

**Related topics**  


[Managing upgrade risk](../concept/uc-manage-upgrade-risk.md)

[Execute a skipped record rule](uc-execute-skipped-record-rule.md#)


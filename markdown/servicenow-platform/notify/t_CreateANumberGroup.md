---
title: Create a number group
description: Group Notify phone numbers and share workflows across grouped numbers.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Numbers and number groups, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a number group

Group Notify phone numbers and share workflows across grouped numbers.

## Before you begin

Role required: notify\_admin

## About this task

Each phone number within Notify has an associated number group. Numbers within a group use the same workflows for handling incoming and outgoing calls and SMS messages.

Numbers associated with a group appear on the **Notify Phone Numbers** related list on the Notify Phone Number Group form.

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Number Groups**.

    ![Use the Notify Number Groups module to group phone numbers into groups](../image/NumberGroups.png)

2.  Click **New**.

3.  Enter a **Name**, and select **Notify: \(Re\)join Conference Call** for the **Incoming call workflow** field.

    ![Notify Phone Number Groups form, which lists the names and workflows of number groups](../image/NumberGroupFields.png)

    **Note:** Ensure not to configure a workflow, which sends an outbound SMS itself, resulting in recursive calling of the workflow.

<table id="table_msm_qtz_py"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the number group.

</td></tr><tr><td>

Incoming call workflow

</td><td>

Workflow to run when there is an incoming phone call for this group.

</td></tr><tr><td>

Incoming SMS workflow

</td><td>

Workflow to run when there is an incoming SMS message for this group.

</td></tr><tr><td>

Outgoing call workflow

</td><td>

Workflow to run when there is an outgoing phone call for this group.

</td></tr><tr><td>

Outgoing SMS workflow

</td><td>

Workflow to run when there is an outgoing SMS message for this group.**Note:** The Out of the Box workflow "Notify: Join Conference Call Via SMS" should not be populated for "Outgoing SMS workflow". Populating a workflow that sends an SMS under Outgoing SMS Workflow will trigger the same workflow thus causing recursive loop.

</td></tr></tbody>
</table>    Incoming call workflows must run on the Notify Call \[notify\_call\] table. Incoming and outgoing SMS workflows must run on the Notify Message \[notify\_message\] or Global \[global\] tables.

    Short codes can only be associated with SMS workflow groups. You cannot add an incoming or outgoing call to a short code group.

4.  Click **Submit**.


## What to do next

[Associate a number to a number group](t_AssignANumberGroup.md)

After creating a number group, associate numbers with that group to use the selected workflows.

**Note:** Each phone number can only be associated with one number group.

You can create multiple number groups and configure with different Twilio numbers. You can then the associate the number groups with the various workflows based on your requirement.

**Parent Topic:**[Numbers and number groups](../concept/c_NumberGroups.md)


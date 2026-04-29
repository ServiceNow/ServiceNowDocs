---
title: Branch a Virtual Agent conversation with a Decision utility
description: Your conversations may need to branch depending on end user input or choices. Use the Decision utility to branch the conversation when certain conditions are met.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Branch a Virtual Agent conversation with a Decision utility

Your conversations may need to branch depending on end user input or choices. Use the Decision utility to branch the conversation when certain conditions are met.

## Before you begin

For more information about the Decision utility, see [Decision utility](../reference/va-decision.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Open a topic and view the **Flow** tab.

3.  Drag the **Decision** utility onto the canvas.

    The **Decision** utility node added to the canvas has a single branch named **Always** by default.

    **Note:** If you insert a **Boolean** user input control, you're prompted to add a **Decision** utility directly after the Boolean node on the canvas. Selecting **Yes** on the Boolean node's Decision utility prompt automatically generates two branches named **True** and **False**. The two branches conditions are automatically set through the condition builder.

4.  Click the plus sign \(**+**\) under the node.

    A second branch named **Always** is added below the Decision utility node.

5.  Click the plus sign \(**+**\) under the node to add additional branches.

6.  Click a branch label, and then specify the branch properties in the form.

<table id="table_yjw_nj3_yrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the branch.

</td></tr><tr><td>

Condition

</td><td>

Expression logic to specify a condition for following this branch in the conversation. The condition must evaluate to true.-   **Condition**: Use the [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) to add or edit conditions.
-   **Script**: Use the script editor to create or edit a script that contains a condition statement.


</td></tr></tbody>
</table>7.  Define the properties for each branch in the Decision utility.

8.  When you're finished with the topic, click **Save** in the topic header bar.


**Parent Topic:**[Creating a Virtual Agent topic](create-virtual-agent-topic.md)


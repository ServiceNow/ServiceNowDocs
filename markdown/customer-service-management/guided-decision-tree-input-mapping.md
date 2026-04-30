---
title: Linking inputs in decision tree nodes
description: Linking of inputs enables decision tree authors to reuse input values \(answers\) from prior nodes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Decision trees in Guided decision, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Linking inputs in decision tree nodes

Linking of inputs enables decision tree authors to reuse input values \(answers\) from prior nodes.

## Linking inputs in question and linking nodes

Most questions are presented to an agent to provide answers. When you link an input to another input, the question is not displayed to the agent. Because the input reuses values from the input it is linked to, the agent does not need to provide any answer.

Similar to other inputs, you can use linked inputs to create path conditions.

![Question related to credit card number in a decision node that reuses the answer from the start node.](../image/question-input-mapping.png "Example of linking inputs in a question node")

For example, if you have already asked the credit card number in the start node, you can reuse that input in the following question node. This question is not presented to the agent again and the value is automatically filled out during run time.

## Linking inputs in guidance nodes

With linking inputs, you can reuse the answers that customer provided to supply input values to the guidance inputs. You can link the task input in the start node to the guidance inputs to pass the information about the record that the agent is working on.

![The reassign case guidance uses the input mapping feature to link the task input in the start node to the guidance input.](../image/guidance-input-mapping.png "Example of linking inputs in a guidance node")

For example, you can connect the start node’s task input to the following guidance. The task input holds a reference of the record the agent is working on in a workspace. You need a case number, which is provided by the task input, for reassigning the case to someone else.

## Special cases for linking inputs

In most cases, you can only link inputs to other prior node’s inputs of the same type. For example, you can link a string input field type to another string input field type.

The Guided Decisions Experience application supports the following special cases.

<table id="table_szj_pfn_zwb"><thead><tr><th>

Input type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String input field type

</td><td>

Accepts any type of field to be linked. For example, string accepts integer, decimal, choice, and others. String is a text field which accepts any characters.

</td></tr><tr><td>

Reference input field type

</td><td>

Accepts only reference type of field.You can link reference input types only if the current question node’s input table matches the prior node’s input table at the same level or at the child level. For example, the Task table can be linked to the Task table or the Task table can be linked to the Case table, which is a child of the Task table.

</td></tr><tr><td>

Choice input field type

</td><td>

Accepts choice type and string type because a choice in a choice list is a string.

</td></tr><tr><td>

Date and Date/Time input field types

</td><td>

Accepts the following types:-   `glide_date_time`
-   `glide_date`
-   `date`
-   `datetime`
-   `due_date`
-   `calendar`

</td></tr></tbody>
</table>**Note:** The Guided Decisions Experience application does not support `glide_var` type fields to map to any inputs.


---
title: Validation errors
description: Several types of errors are displayed for missing or incorrect information in the nodes and paths while saving an element or activating a decision tree.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Validation error notifications in Decision Tree Builder, Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Validation errors

Several types of errors are displayed for missing or incorrect information in the nodes and paths while saving an element or activating a decision tree.

## Question node errors

<table id="table_a21_53c_bxb"><thead><tr><th>

Error message

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

This node needs a unique name

</td><td>

Enter a name in the **Node name** field.

</td></tr><tr><td>

The questions in this node need to be unique

</td><td>

Enter a unique question or instruction in the **Question or instruction** field.

</td></tr><tr><td>

This node needs a question to ask users

</td><td>

Enter a unique question or instruction in the **Question or instruction** field.

</td></tr><tr><td>

The task input needs a reference table to pass data about records

</td><td>

Select a table in the **Reference table** field for the task input to pass data about the record on which this decision tree is run.

</td></tr><tr><td>

Question \{number\} needs a question or instruction

</td><td>

Enter a question or instruction in the **Question or instruction** field.

</td></tr><tr><td>

Question \{number\} needs an answer type

</td><td>

Select an input type for the expected answer in the **Type of answer** field.

</td></tr><tr><td>

Question \{number\} needs answer choices

</td><td>

The Choice answer type requires a choice list. Enter values in the **Label** and **Value** fields to configure a list. You can add as many choices as you want.

</td></tr><tr><td>

Question \{number\} needs an answer-string character limit

</td><td>

Enter a character limit in the **Maximum number of characters** field.

</td></tr><tr><td>

Type of answer in Question \{number\} doesn't exist

</td><td>

The answer type that you entered in the **Type of answer** field isn’t valid. Select the answer type from the list. For more information, see [Answer types for questions](type-of-answer.md).

</td></tr><tr><td>

Question \{number\} needs a choice table and choice fields for the answer\(s\)

</td><td>

The **Pre-defined list from a table** option for the choice answer type requires you to specify the choice table and choice field to reuse choices. Select a table and list field in the **Choice table** and **Choice field** fields respectively.

</td></tr><tr><td>

Choice table in Question \{number\} doesn't exist

</td><td>

Enter a valid table name in the **Choice table** field.

</td></tr><tr><td>

Question \{number\} needs a reference table for the answer\(s\)

</td><td>

The reference input type requires a reference table to be selected. Select a table in the **Reference table** field to add a reference field, which stores a reference to a field on another table, as an answer type.

</td></tr><tr><td>

Reference table in Question \{number\} doesn't exist

</td><td>

Enter a valid table name in the **Reference table** field.

</td></tr><tr><td>

You need to add a path after this node

</td><td>

Question nodes require paths to add the next question or guidance nodes. Select the Add path icon ![Add path icon](../image/icon-add-path.png) on the question node in the canvas to add a new path.

</td></tr><tr><td>

The input you linked in Question \{number\} isn’t valid because of mismatched answer types. You can unlink this input, link a new one, or change this question’s answer type.

</td><td>

After you change a question’s answer type in a prior node, the input mapping from the question in the current node is no longer valid.

 1.  Unlink the input by deleting the link.
2.  Either change this question's answer type to match the changed answer type in the prior node or add a question that matches it.
3.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the inputs.

</td></tr><tr><td>

The input you linked to Question \{number\} no longer exists after recent node changes. Unlink this input to fix this error.

</td><td>

Unlink the input by deleting the link.

</td></tr><tr><td>

The input you linked in Question \{number\} isn't valid because of mismatched reference tables with a prior node. Tables need to match at the same or child level.

</td><td>

You can link reference input types only if the current question node’s input table matches the prior node’s input table at the same level or at the child level. For example, the Task table can be linked to the Task table or the Task table can be linked to the Case table, which is a child of the Task table.

 1.  Unlink the input by deleting the link.
2.  If necessary, select the reference table that matches at the same level or at the child level.
3.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the reference inputs again.

</td></tr></tbody>
</table>## Guidance node errors

<table id="table_iqf_1kc_bxb"><thead><tr><th>

Error message

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

This node needs a unique name

</td><td>

Enter a name in the **Node name** field.

</td></tr><tr><td>

This node needs a guidance

</td><td>

Guidance nodes must be linked to a guidance. Either select an existing guidance or create one.

 -   Select an available guidance from the list in the **Guidance** field.
-   Create a guidance in Core UI by selecting the Create a guidance icon ![Create a guidance icon](../image/icon-add-path.png) in the **Guidance** field. For more information, see [Create a guidance in the Core UI](../task/create-guidances.md).

</td></tr><tr><td>

You need to set inputs for this guidance

</td><td>

Configure the guidance inputs for the guidance that you selected. For more information, see [Provide actions to agents in a decision tree](../task/configure-guidance-in-gdb.md).

</td></tr><tr><td>

\{Guidance input name\} input isn't valid because of mismatched reference tables with a prior node. Tables need to match at the same or child level.

</td><td>

You can link reference input types only if the current guidance node’s input table matches the prior node’s input table at the same level or at the child level. For example, the Task table can be linked to the Task table or the Task table can be linked to the Case table, which is a child of the Task table.

 1.  Unlink the input by deleting the link.
2.  Select the \(![Link input icon](../image/icon-link-input.png)\) icon to link the inputs again or enter a static value.

</td></tr><tr><td>

The input you linked to \{Guidance input name\} no longer exists after recent node changes. Unlink this input to fix this error.

</td><td>

1.  Unlink the input by deleting the link.
2.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the inputs again or enter a static value.

</td></tr><tr><td>

You need to reset the input\(s\) for this guidance because of changes in prior nodes

</td><td>

1.  Unlink the input by deleting the link.
2.  If necessary, select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the new answer type from the prior node or enter a static value.

</td></tr></tbody>
</table>## Linking node errors and warnings

<table id="table_hfb_hxt_tzb"><thead><tr><th>

Error message

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

This node needs a unique name

</td><td>

Enter a name in the **Node name** field.

</td></tr><tr><td>

This node needs a child tree

</td><td>

Linking nodes must be linked to a child tree. Either select an activated decision tree or create one.

 -   Select an activated decision tree from the list in the **Child decision tree** field.
-   Create a decision tree in Core UI by selecting the Create a decision tree icon ![Create a decision tree icon](../image/icon-add-path.png) in the **Child decision tree** field. For more information, see [Create a decision tree in Core UI](../task/configure-decision-trees-gdb.md).

</td></tr><tr><td>

You need to map the inputs of the child decision tree to this decision tree correctly.

</td><td>

Configure the start node inputs of the child decision tree or select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the inputs.

</td></tr><tr><td>

\{Input name\} input isn't valid because of mismatched reference tables with a prior node. Tables need to match at the same or child level.

</td><td>

You can link reference input types only if the current guidance node’s input table matches the prior node’s input table at the same level or at the child level. For example, the Task table can be linked to the Task table or the Task table can be linked to the Case table, which is a child of the Task table.

 1.  Unlink the input by deleting the link.
2.  Select the \(![Link input icon](../image/icon-link-input.png)\) icon to link the inputs again or enter a static value.

</td></tr></tbody>
</table><table id="table_clj_yz5_tzb"><thead><tr><th>

Warning message

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

The child decision tree you linked earlier changed. Double-check the mapped inputs.

</td><td>

1.  Unlink the input by deleting the link.
2.  If necessary, select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the input from the prior node or enter a static value.

</td></tr><tr><td>

Make sure these linked decision trees can still use \{child decision tree\}:

-   \{Name of parent tree 1\}
-   \{Name of parent tree 2\}
-   \{Name of parent tree 3\}

</td><td>

When you update and activate a decision tree, the parent decision trees that use this decision tree as a child tree must also be updated.1.  Select the parent decision tree.
2.  Select the link node that references the child decision tree that has changed.
3.  Unlink the input by deleting the link.
4.  If necessary, select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to link the input from the prior node or enter a static value.

</td></tr></tbody>
</table>## Path errors

<table id="table_cfn_vjc_bxb"><thead><tr><th>

Error message

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

This path needs a name

</td><td>

Enter a name in the **Path name** field.

</td></tr><tr><td>

This path needs a unique path priority

</td><td>

Enter a unique value in the **Path priority** field.

</td></tr><tr><td>

This path needs conditions for showing the next node

</td><td>

Configure one or more conditions by selecting an input from the previous node, an operator, and an input value.

</td></tr><tr><td>

Every condition in this path needs to be complete

</td><td>

Complete a condition in the path by selecting an input from the previous node, an operator, and an input value.

</td></tr><tr><td>

You need to add a node after this path

</td><td>

A path must lead to a node. Select **Add node** to configure the placeholder node as a question node or a guidance node.

</td></tr><tr><td>

The path condition needs new values because of changes in prior nodes

</td><td>

Reconfigure the path condition by selecting the new input from the previous node, an operator, and the new input value.

</td></tr><tr><td>

The path conditions can’t be defined until the prior node has a question and answer

</td><td>

Configure questions and answer types in the path's parent node.

</td></tr></tbody>
</table>
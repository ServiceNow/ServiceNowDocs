---
title: Decision utility
description: Use the Decision utility in a Virtual Agent topic to add two or more branches that represent different paths in a conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assistant Designer utilities, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Decision utility

Use the Decision utility in a Virtual Agent topic to add two or more branches that represent different paths in a conversation.

## Use scripts or variable conditions to set decision branches

Each branch below a Decision utility node has a condition property. You can define the condition using the condition builder or a script that returns a value of true or false. A branch that returns a value of true is followed, while a branch returning a value of false is not. When creating these scripts or conditions, ensure that only one branch in each Decision utility node evaluates to true.

**Note:** If you insert a **Boolean** user input control, you're prompted to add a **Decision** utility directly after the Boolean node on the canvas. Selecting **Yes** on the Boolean node's Decision utility prompt automatically generates two branches named **True** and **False**. The two branches conditions are automatically set through the condition builder.

For more information, see [Branch a Virtual Agent conversation with a Decision utility](../task/add-decision-utility-va-topic.md).

## Example Decision utility node with branches

In this example, a static choice control prompts the user to select from three available colors and the selection is stored in a variable. The Decision utility control is configured with a branch for each possible selection. Each branch uses the condition builder, which returns true when the corresponding color is selected. In the example, the condition builder returns true when the choice is Blue.

![Decision utility with three branches and highlighted corresponding condition defined property for the Blue branch.](../images/DecisionExample.png)

You can also use the Script option for branch conditions. In the following example, the script provides the same functionality as the condition builder.

![Decision utility with three branches and highlighted corresponding scripted property for the Blue branch.](../images/decision-example-script.png)

**Parent Topic:**[Assistant Designer utilities](va-utilities.md)


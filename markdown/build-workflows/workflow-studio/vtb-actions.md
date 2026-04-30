---
title: Visual Task Board \(VTB\) Spoke
description: Provides VTB actions for flow designers to manage the boards, lanes, cards, board members, and assignees.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Spokes, Workflow Studio flow integrations, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Visual Task Board \(VTB\) Spoke

Provides VTB actions for flow designers to manage the boards, lanes, cards, board members, and assignees.

<table id="table_td5_g1s_3z"><thead><tr><th>

Action

</th><th>

Description

</th><th>

Action Inputs

</th><th>

Action Outputs

</th></tr></thead><tbody><tr><td>

Create Freeform VTB Action

</td><td>

Creates a Freeform VTB for any task type. The default lanes are: Todo, Doing, and Done. These lanes can be modified with actions: Add Lane, Rename Lane, Reorder Lane, and Delete Lane

</td><td>

-   Name
-   Board Owner
-   Default view
-   Label visibility
-   Picker visibility
-   Background color

</td><td>

Board record

</td></tr><tr><td>

Create Flexible VTB Action

</td><td>

Creates a Flexible VTB bound to a single Task table. The default lanes are: Todo, Doing, and Done. These lanes can be modified with actions: Add Lane, Rename Lane, Reorder Lane, and Delete Lane

</td><td>

-   Name
-   Task table
-   Filter
-   Board Owner
-   Default view
-   Label visibility
-   Picker visibility
-   Background color

</td><td>

Board record

</td></tr><tr><td>

Create Guided VTB Action

</td><td>

Creates a data-driven VTB bound to a single Task table along with the fields the lanes are derived.

</td><td>

-   Name
-   Task table
-   Land field
-   Filter
-   Board Owner
-   Default view
-   Label visibility
-   Picker visibility
-   Background color

</td><td>

Board record

</td></tr><tr><td>

Add VTB Member Action

</td><td>

Add a user to a VTB. Only members of the VTB can access the board, Any VTB member can add other members.

</td><td>

-   Board record
-   User record

</td><td>

N/A

</td></tr><tr><td>

Remove VTB Member Action

</td><td>

Remove a user from a VTB. Only members of a VTB can access the board. Any VTB member can remove other members.

</td><td>

-   Board record
-   User record

</td><td>

N/A

</td></tr></tbody>
</table><table id="table_hkd_s53_jbb"><thead><tr><th>

Action

</th><th>

Description

</th><th>

Action Steps

</th><th>

State

</th></tr></thead><tbody><tr><td>

Add VTB lane

</td><td>

Add a lane to a Freeform or Flexible VTB. This action does not apply to Guided boards, which are constrained to fixed lanes based on fields configured.

</td><td>

-   Board record
-   Lane name

</td><td>

VTB lane record

</td></tr><tr><td>

Rename VTB Lane

</td><td>

Rename an existing lane on a Freeform or Flexible VTB.

</td><td>

-   Lane record
-   New lane name

</td><td>

N/A

</td></tr><tr><td>

Reorder VTB Lane

</td><td>

Reorder lanes on any VTB.

</td><td>

-   Lane record
-   New lane name

</td><td>

N/A

</td></tr><tr><td>

Delete VTB Lane

</td><td>

Delete an existing lane from a Freeform or Flexible VTB.

</td><td>

Lane record

</td><td>

N/A

</td></tr></tbody>
</table><table id="table_dn3_s53_jbb"><thead><tr><th>

Flow/Action

</th><th>

Description

</th><th>

Action Steps

</th><th>

State

</th></tr></thead><tbody><tr><td>

Create VTB Card

</td><td>

Create a VTB card on a Freeform board for a task.

</td><td>

-   Lane record
-   Task record

</td><td>

Card record

</td></tr><tr><td>

Assign VTB Card

</td><td>

Assign a user to a VTB card.

</td><td>

-   Card record
-   User record

</td><td>

N/A

</td></tr><tr><td>

Move VTB Card

</td><td>

Move a VTB card from one lane to another lane. **Note:** For Flexible boards, use the Update Record action to change the state of the underlying task. For Guided boards, this action changes the field on the task associated with that card.

</td><td>

-   Card record
-   Lane record

</td><td>

N/A

</td></tr><tr><td>

Remove Assignee from VTB Card

</td><td>

Remove an assignee from a card.

</td><td>

Card record

</td><td>

N/A

</td></tr></tbody>
</table>**Parent Topic:**[Spokes](../concept/spokes.md)

**Related topics**  


[c_VisualTaskBoards]


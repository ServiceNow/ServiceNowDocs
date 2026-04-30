---
title: Move a Visual Task Board card to a different lane
description: You can move a card from one lane to another on a Visual Task Board.
locale: en-US
release: yokohama
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with Visual Task Board cards, Using Visual Task Boards, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Move a Visual Task Board card to a different lane

You can move a card from one lane to another on a Visual Task Board.

## Before you begin

Role required: none

## About this task

When you move a card to a different lane on a guided board, the field on which the lanes are based is updated to reflect the new lane value.

## Procedure

1.  Open a Visual Task Board.

2.  Select a card and drag it to a different lane.

    To cancel the move, press the Escape key while you drag the card.

    **Note:**

    All mandatory fields on a record must be filled in to move the associated card to a new lane. For example, assume you have a guided board based on the Incident \[incident\] table, with a lane for each **State**. The **Close code** and **Close notes** fields become mandatory when the **State** changes to **Closed**. If you attempt to move an incident card from the **New** lane to the **Closed** lane, a pop-up view of the form appears and prompts you to fill in the mandatory fields.

    If you get an error message saying **You do not have the permission to modify this record**, create system property `glide.vtb.enable_list_edit_acl` and setting it to **false**.


**Parent Topic:**[Working with Visual Task Board cards](../reference/r_TaskCards.md)


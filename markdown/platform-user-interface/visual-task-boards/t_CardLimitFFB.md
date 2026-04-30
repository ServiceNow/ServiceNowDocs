---
title: Configure the card limit for Visual Task boards
description: Freeform and data driven boards can display up to 1,000 cards by default. You can change the default card limit by adding a system property.
locale: en-US
release: zurich
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with VTB cards, Use, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Configure the card limit for Visual Task boards

Freeform and data driven boards can display up to 1,000 cards by default. You can change the default card limit by adding a system property.

## Before you begin

Role required: admin

## About this task

You can set card limit for both Freeform board and Flexible and Guided board in Data Driven board.

## Procedure

1.  [Add a new system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) with the following field values:

    |Field|Value|
    |-----|-----|
    |Name|glide.vtb.board\_max|
    |Type|integer|

2.  Set the **Value** to the maximum number of cards allowed for each board.

    **Note:** Performance degradation may occur if you set the **Value** to a number greater than 1,000, especially on tablet devices.


**Parent Topic:**[Working with Visual Task Board cards](../reference/r_TaskCards.md)


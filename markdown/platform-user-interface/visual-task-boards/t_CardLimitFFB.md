---
title: Configure the card limit for Visual Task boards
description: Freeform and data driven boards can display up to 1,000 cards by default. You can change the default card limit by adding a system property.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Visual Task Board cards, Using Visual Task Boards, Visual Task Boards, Configure UIs and portals, Configure user experiences]
---

# Configure the card limit for Visual Task boards

Freeform and data driven boards can display up to 1,000 cards by default. You can change the default card limit by adding a system property.

## Before you begin

Role required: admin

## About this task

You can set card limit for both Freeform board and Flexible and Guided board in Data Driven board.

## Procedure

1.  [Add a new system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) with the following field values:

    |Field|Value|
    |-----|-----|
    |Name|glide.vtb.board\_max|
    |Type|integer|

2.  Set the **Value** to the maximum number of cards allowed for each board.

    **Note:** Performance degradation may occur if you set the **Value** to a number greater than 1,000, especially on tablet devices.


**Parent Topic:**[Working with Visual Task Board cards](../reference/r_TaskCards.md)


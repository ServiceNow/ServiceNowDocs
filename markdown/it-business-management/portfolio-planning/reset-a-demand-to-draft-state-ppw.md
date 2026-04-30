---
title: Reset a demand to draft state
description: Move a demand back to the Draft state, if necessary.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Manage demands, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Reset a demand to draft state

Move a demand back to the Draft state, if necessary.

## Before you begin

Role required: it\_demand\_manager

## About this task

A demand can be reset to Draft from the Completed, Approved, Screening, or Submitted states, or until an entity such as a project is created from it. The **Reset to Draft** option is unavailable if the demand is in the Qualified state.

## Procedure

1.  Open a demand from the home page of Next Experience for Demand Management.

    For more information, see [Access demands](access-demands-ppw.md).

2.  Select **Details** from the L-2 \(level 2\) navigation menu.

3.  Select **Reset to Draft**.![Use the Reset to Draft button to reset a demand to the Draft state.](../../spw-demand/images/demands-reset-to-draft.png)

    A confirmation message appears, if there are:

    -   Active assessments pending with stakeholders, or
    -   Resource assignments are created for the demand
4.  Select the check box to replan the allocated resource plans that have no actual hours reported.

5.  Select **OK**.


## Result

-   The demand is moved to the Draft state.
-   All the score values in **Assessment Data** tab are reset to default.
-   All active assessments for the demand are canceled. New assessments are triggered when the demand moves to the Screening state and if the **Assessment Required** field on the demand form is set to true.


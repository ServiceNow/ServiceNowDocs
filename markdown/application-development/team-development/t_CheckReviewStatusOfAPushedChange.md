---
title: Check the review status of a pushed change
description: If the parent instance requires pushed changes to be sent to code review, changes are placed in the Awaiting Code Review stage.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Pushing changes, Working with changes, Team Development, Planning your application, Building applications]
---

# Check the review status of a pushed change

If the parent instance requires pushed changes to be sent to code review, changes are placed in the Awaiting Code Review stage.

## Before you begin

Role required: developer

## About this task

If you configure the parent instance to send [notifications](../concept/c_CodeReviewNotifications.md), it sends the submitting developer a notification when the pushed changes are approved or rejected. Developers can also manually check the status of their pushed changes from the Pushes and Pulls module on the submitting instance.

## Procedure

1.  Log in to the instance that submitted the code for review.

2.  Navigate to **Team Development** &gt; **Pushes and Pulls**.

3.  Filter for the push you want to review.

    -   Pushes in the Complete stage are approved and applied to the parent instance.
    -   Pushes in the Collided stage are rejected because of a collision.
    -   Pushes in the Awaiting Code Review stage are awaiting review.
    -   Pushes in the Code Changes Rejected stage are rejected by a reviewer.
    -   Pushes in the Code Review Request-Canceled stage are canceled by the submitting developer.
4.  Select the **Reviews** related list to see the following information.

    -   Who submitted a review decision?
    -   What the decision was: either approved or rejected.
    -   What comments if any the reviewer provided.

**Parent Topic:**[Pushing changes](../concept/pushing-changes.md)


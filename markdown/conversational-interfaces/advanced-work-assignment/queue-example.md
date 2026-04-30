---
title: Create a queue to route new change requests
description: Create a work item queue in Advanced Work Assignment that routes new change requests through the service channel that handles change requests.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a queue to route new change requests

Create a work item queue in Advanced Work Assignment that routes new change requests through the service channel that handles change requests.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select **New**.

3.  On the form, fill in the fields.

    -   Name: Change Management
    -   Service channel: Change Request
    -   Condition mode: Simple
    -   Work item routing condition: \[State\] \[is\] \[New\]
4.  From the form context menu, select **Save**.


**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)


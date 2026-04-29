---
title: Process task rate cards
description: The business rule Process Task Rate Cards runs when tasks close and checks to see if any task rate cards apply. If they do, an expense line is created according to the rate card.
locale: en-US
release: australia
product: Cost Management
classification: cost-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task and labor rate cards, Cost Management, Strategic Portfolio Management]
---

# Process task rate cards

The business rule Process Task Rate Cards runs when tasks close and checks to see if any task rate cards apply. If they do, an expense line is created according to the rate card.

The process flow of the "Process Task Rate Cards" business rule is:

1.  Task closes.
2.  Business rule runs.
3.  Query active task rate cards in order looking for a matching condition.
4.  Qualifying rate card not using time worked.

    Generate expense line linked to the task using the task rate value.

5.  Qualifying rate card using time worked.
    1.  Get task time worked entries for the task grouped by user \(worker\).
    2.  For each user, check to see if they match conditions in any of the labor rate cards.
        1.  Labor rate card found, generate expense line using the time worked and labor rate.
        2.  Labor rate card not found, generate expense line using the default labor rate from the task rate card.

**Parent Topic:**[Task and labor rate cards](../concept/c_TaskAndLaborRateCards.md)


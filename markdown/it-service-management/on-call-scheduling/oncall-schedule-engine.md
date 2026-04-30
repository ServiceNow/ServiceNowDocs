---
title: On-Call Scheduling new schedule engine
description: Introducing the new On-call schedule engine with enhanced capabilities and user experience.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Explore, On-Call Scheduling, IT Service Management]
---

# On-Call Scheduling new schedule engine

Introducing the new On-call schedule engine with enhanced capabilities and user experience.

The new On-call schedule engine is more efficient with the following enhanced features:

-   It reduces the time taken to move, add, or remove members from a shift.
-   It resolves the gaps arising when members are scheduled for extra-time or partial workdays due to the holiday calendar.
-   It reduces the gaps caused by adding, removing, or replacing members of the shift.
-   It refers the previous rotation to determine the next person to start the new assignment with. To ensure fair assignment, it starts the rotation with a person not yet assigned in the previous rotation.

**Note:**

-   New shift will automatically work with the new schedule engine.
-   For existing shifts, you can go to the shift record page and manually migrate using the **Migrate Now** option.
-   To migrate all the existing shifts in bulk, run **On-Call Upgrade shifts to 2024 schedule engine** schedule job.

**Important:** The shift rotation may change after switching to the new schedule engine. In that case, you can always create a new shift rotation from the current or future date with the new schedule engine which works as expected

**Parent Topic:**[Exploring On-Call Scheduling](exploring-on-call-scheduling.md)


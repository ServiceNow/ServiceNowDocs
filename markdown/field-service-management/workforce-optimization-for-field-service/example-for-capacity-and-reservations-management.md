---
title: Example workflow for assigning tasks to agents based on Capacity and Reservations
description: Explore how dynamic scheduling intelligently distributes tasks, considering the defined capacity reservations, work types, and overflow settings, ensuring optimal utilization of resources in the group.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Example workflow for assigning tasks to agents based on Capacity and Reservations

Explore how dynamic scheduling intelligently distributes tasks, considering the defined capacity reservations, work types, and overflow settings, ensuring optimal utilization of resources in the group.

As an administrator, your goal is to ensure that assignment group works 25% on 'Install' work type, 25% on 'Break fix' work type, and the remaining 50% can be of any type or no type of work. The following example demonstrates how to achieve this through dynamic scheduling.

Prerequisites:

-   Ensure Dynamic Scheduling is enabled.
-   Ensure that your target assignment group, for instance, the 'North Group', has at least one active member.
-   Create an agent schedule record \('agent\_work\_schedule'\) for a user, specifying the 'Day Shift \(8:00-5:00\)' work schedule.

1.  Capacity Definition Setup:
    -   Create a capacity definition record with 'Capacity by' set to 'Tasks', assigning a value of '4' tasks daily.
    -   Set the frequency of this capacity to 'Daily' to align with your scheduling needs.
2.  Capacity Reservation Rules: Create two capacity reservation rules
    -   Rule 1 \('Install Work'\): Conditions set for 'Work type' as 'Install,' allocate 25%, and allow overflow.
    -   Rule 2 \('Break Fix Work'\): Conditions set for 'Work type' as 'Break fix,' allocate 25%, and allow overflow.
3.  Tag Reservations to Definition: Link the created reservation rules to the definition crafted in step 1, forming a structure.
4.  Capacity Assignment:
    -   Within the related lists of the capacity definition, create a new 'Capacity Assignment' record.
    -   Link it to the capacity definition, select the target assignment group \('North Group'\), set the effective start date to the current date and time, and repeat for '5' times to auto-fill the end date.
5.  Create work order of install type:
    -   Create a work order \('wm\_order'\), specifying the location as 'Colorado,' and mark it 'Ready for qualification'.
    -   Open the work order task, ensuring the dispatch group and required assignment group \('North Group'\) are filled.
    -   Set the work type as 'Install' and click 'Qualified'; the task transitions to the Pending Dispatch state.
    -   Repeat the process twice to have 3 'Install' type tasks available for the day.
6.  Create work order of break-fix type:
    -   Create a work order \('wm\_order'\), specifying the location as 'Colorado,' and mark it 'Ready for qualification.'
    -   A new work order task \('wm\_task'\) is generated; open it, ensuring the dispatch group and required assignment group \('North'\) are filled.
    -   Set the work type as 'Break fix' and click 'Qualified'; the task moves to the Pending Dispatch state.
    -   Repeat the process twice to have 3 'Break fix' type tasks available for the day.
7.  Create work order tasks without a specified work type:
    -   Open a work order task, ensure the dispatch group and required assignment group \('North'\) are filled, and leave the work type field blank.
    -   Click 'Qualified'; the task transitions to the Pending Dispatch state.
    -   Repeat this process twice to have 3 tasks without a specified work type available for the day.
8.  Dynamic Scheduling:
    -   Open the four tasks created in the list view and click 'Auto Assign' from the overflow action menu.
    -   A modal window displays possible assignments, allocating tasks based on the predefined 25% capacity for 'Install' type, 25% for 'Break fix' type, and the remaining 50% for any type or no type at all.


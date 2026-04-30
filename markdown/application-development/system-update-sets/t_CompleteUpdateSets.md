---
title: Mark an update set complete
description: When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Update set use, System update sets, Deploying applications, Building applications]
---

# Mark an update set complete

When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.

## About this task

Mark an update set as Complete only when it is ready to migrate. Once an update set is complete, do not change it back to In progress. Instead, create another update set for the rest of the changes, and be sure to commit them together in the order that they were created. Naming conventions may help in this case \(for example, Performance Enhancements and Performance Enhancements 2\).

## Procedure

1.  Open the update set record.

2.  Change the State of the update set from In progress to Complete.

    -   The update set is available for other instances to retrieve.
    -   No additional customizations are tracked in the update set.
    ![update set record](../image/Us20.png "update set reord")



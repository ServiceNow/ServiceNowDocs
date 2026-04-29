---
title: Mark an update set complete
description: When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Mark an update set complete

When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.

## Before you begin

Role required: admin

## About this task

Mark an update set as Complete only when it is ready to transfer. Once an update set is complete, do not change it back to In progress. Instead create another update set for the rest of the changes, and commit them in the order that they were created.

## Procedure

1.  Open the update set record.

2.  Change the State of the update set from In progress to Complete.

    The update set is available for other instances to retrieve and additional customizations aren't tracked in the update set.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)


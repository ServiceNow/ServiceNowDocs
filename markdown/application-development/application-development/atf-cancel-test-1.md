---
title: Cancel running automated test
description: You can cancel a running test from the Run Test progress dialog.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Cancel running automated test

You can cancel a running test from the Run Test progress dialog.

## Before you begin

The system must be running a test.

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  If necessary, [display the Run Test progress dialog](atf-view-progress.md).

2.  Click **Cancel Pending Steps**.

    The system displays a dialog asking you to confirm that you want to cancel this test execution.

3.  In the Confirmation dialog, click **Yes**.


## Result

The system cancels the running test and rolls back any data changes the test made.


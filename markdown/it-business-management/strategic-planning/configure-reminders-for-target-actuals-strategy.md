---
title: Configure reminders for target actuals
description: Configure reminders to notify target owners and contributors to update actuals for their targets by a specified date.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Configure, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Configure reminders for target actuals

Configure reminders to notify target owners and contributors to update actuals for their targets by a specified date.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

The following two system properties must be configured to notify target owners and contributors to update the actuals for their targets:

-   **target\_checkin\_due\_date\_reminder\_feature\_toggle**: Enables the reminder notifications feature for target actuals check-in.
-   **target\_checkin\_due\_date\_reminder\_config**: Defines the number of days before the due date to send the reminder. The following are the default values based on the check-in frequency:

    |Check-in frequency|Default number of days before due date|
    |------------------|--------------------------------------|
    |None|7|
    |Weekly|2|
    |Monthly|5|
    |Quarterly|7|
    |Yearly|10|


## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    A list of all the properties in the System Properties \[sys\_properties\] table appears.

2.  Search for each of the following system properties, enter the required value in the **Value** field, and then select **Update**.

    |System property|Value|
    |---------------|-----|
    |target\_checkin\_due\_date\_reminder\_feature\_toggle|Enter `true` to enable reminder notifications.|
    |target\_checkin\_due\_date\_reminder\_config|Enter the number of days before the due date to send the reminder automatically.|


## Result

Reminder notifications are enabled for target actuals check-in. Target owners and contributors are automatically notified to submit actuals for their targets based on the configured number of days before the due date and the check-in frequency defined for each target.


---
title: Schedule audits
description: Specify the time and day that audits are run.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain Separation Center, Domain separation for service providers, Access Management]
---

# Schedule audits

Specify the time and day that audits are run.

## Before you begin

Role required: admin

## About this task

You [configured one or more audits](configure-domain-separation-audits.md) to run daily, weekly, or monthly. The scheduler specifies what days and times to run those audits. All audits with the same scheduling frequency run sequentially starting at the time you configure.

## Procedure

1.  In the Domain Separation Center, click **Audit Schedules**.

    The Audit Schedule page appears.

2.  Configure the audit schedules.

    1.  Click a schedule name.

    2.  Specify the time of day to run the audit.

        Time units use the 24-hour clock \(that is, 14 equals 2 PM\).

    3.  For weekly schedules, select the day of the week to run the audit, where 1 is Sunday.

    4.  For monthly schedules, select the day of the month to run the audit.

    5.  Repeat the procedure for the other schedules.

3.  Click **Save** to save the configuration changes.

4.  Click **Execute Now** to run all the audits scheduled to run at the frequency shown at the top of the right pane.

    For example, if the pane title is **Domain Audit Schedule - Daily**, **Execute Now** immediately runs all the audits that are scheduled to run daily.


## What to do next

To see the status of a running audit, in the Domain Separation Center, click the number in the **Running Audits** box.


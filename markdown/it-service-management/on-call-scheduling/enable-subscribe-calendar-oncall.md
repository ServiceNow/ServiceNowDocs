---
title: Enable users to subscribe to the On-Call calendar
description: Configure an On-Call calendar subscription URL and send it to the members of a shift. The URL is an iCal link that enables users to subscribe to their on-call calendar from their preferred calendar client.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Enable users to subscribe to the On-Call calendar

Configure an On-Call calendar subscription URL and send it to the members of a shift. The URL is an iCal link that enables users to subscribe to their on-call calendar from their preferred calendar client.

## Before you begin

Role required: admin, rota\_admin, or rota\_manager

## About this task

The Subscription URL supports SSO authentication to view and download on-call calendar.

**Note:** Don’t share the subscription URL for security reasons.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **My Group Schedules**.

2.  Select the shift for which you want to send the on-call calendar subscription URL.

3.  Specify the following details in the **Calendar Subscription** section.

    |Name|Definition|
    |----|----------|
    |Coverage interval|Select if you want to update the subscribed calendar with weekly or daily coverage details.|
    |Get coverage for|Based on your coverage interval selection, select the number of weeks or days for which you want to update the subscribed calendar.|

4.  Select **Update**.

5.  Select **Send Subscriptions** to send the calendar subscription URL to all members of the shift by email.![A preview of the email.](../image/subscriptiom-email-oncall.png)

    Members of the shift will receive an email with the subscription link. Select the **Subscription link** and log in with SSO credentials to download the calendar or generate and copy the subscription URL.![The screen shows the option to download the schedule or to obtain a publicly accessible URL for subscribing to the schedule.](../image/oncall-calendar-subscription-page.png)


**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)


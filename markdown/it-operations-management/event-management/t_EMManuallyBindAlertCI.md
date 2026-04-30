---
title: Trigger alert binding to a CI
description: Trigger a new alert to manually bind an alert to a CI.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Trigger alert binding to a CI

Trigger a new alert to manually bind an alert to a CI.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  If an alert did not automatically bind to a CI, you can manually trigger a new alert and rebind:

    -   Delete the alert and resend the event.
    -   Close the alert, temporarily set the **evt\_mgmt.active\_interval** system property time to `0`, and then resend the alert. After the bind completes, reset the property back to the previous value.

**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)


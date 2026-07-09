---
title: Verify usage insights for Interaction Controls Component \(ICC\) enabled call events
description: After you configure Usage Insights, confirm that call events are captured for the enabled agents and that event payloads appear as expected in the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/verify-usage-insights-for-icc-call-events.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
breadcrumb: [Usage insights for ICC call events, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Verify usage insights for Interaction Controls Component \(ICC\) enabled call events

After you configure **Usage Insights**, confirm that call events are captured for the enabled agents and that event payloads appear as expected in the ServiceNow instance.

## Before you begin

Role required: admin

Complete the configuration steps in [Enable Usage insights for Interaction Controls Component \(ICC\) enabled call events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/enable-usage-insights-for-icc-call-events.md) before you verify the setup. The enabled agents must have logged in and performed call actions for events to appear.

## About this task

After you complete the configuration, **Usage Insights** begins capturing events for the agents you enabled. Use the following steps to confirm that events are captured.

## Procedure

1.  Navigate to **Platform Analytics** &gt; **Usage Insights** and filter by CSM/FSM Configurable Workspace.

2.  Select the **Users** or **Sessions** view.

    The enabled agents' sessions appear after they log in and perform call actions.

3.  Select a session and confirm that ICC triggered **NVC events** appear with complete payloads.


## Result

The enabled agents' call events appear in **Usage Insights** with complete payloads.

**Note:** Users are displayed as \#IDs in **Usage Insights**.

## What to do next

If no events appear after an agent has completed a call action, verify that the **Enable Analytics** toggle is set to **ON** in the agent's preferences and that their **sys\_id** is correctly entered in the **sn\_openframe\_logger\_enabled\_users** property.


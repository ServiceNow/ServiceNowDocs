---
title: Delay incidents
description: Configure delay rules to postpone incident creation for alerts that may resolve automatically or represent transient conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/delay-incidents.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, delay incidents, noise reduction]
breadcrumb: [ITOM Configuration console for Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Delay incidents

Configure delay rules to postpone incident creation for alerts that may resolve automatically or represent transient conditions.

## Before you begin

Verify that you have installed the ITOM AIOps and Now Assist for IT Operations Management \(ITOM\) plugins.

Ensure you're in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

Delay incident rules help reduce unnecessary incident creation by waiting for a specified period before generating incidents from alerts. This is particularly useful for flapping conditions or transient issues that may resolve automatically, preventing ticket creation for self-resolving problems.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Reduce Noise**.

2.  Expand **Reduce Noise**.

3.  Select **Delay incidents**.

    A list of respond alert automations appears.

4.  To create an automation and set a wait time before incident creation, select **Create automation**.

    The Respond to alerts page opens.

5.  Follow the steps in [Create Respond automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/respond-alert-sow-itom.md).

    **Note:** To modify the wait time in an existing automation, open the automation and update the wait time under **Create incident and other response actions**. Ensure you select **Create Incident \(Advanced\)** — the delay configuration form is only available through this option.

6.  To complete the setup, select **Mark as configured**.



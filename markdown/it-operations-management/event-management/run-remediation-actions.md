---
title: Run remediation actions
description: Run remediation actions automatically or trigger them manually from the Express List to speed up alert investigation and resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/run-remediation-actions.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [Configure Event Management using ServiceNow Otto for Setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Run remediation actions

Run remediation actions automatically or trigger them manually from the Express List to speed up alert investigation and resolution.

## Before you begin

Verify you have installed the ITOM AIOps and ServiceNow Otto for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Reduce MTTR**.

2.  Expand **Reduce MTTR**.

3.  Select **Remediation actions**.

    A list of respond alert automations appears where the **Response subflow** field in the Respond alert automation is set to anything other than **Create incident \(advanced\)**.

4.  Select **+Create automation**.

5.  Follow the steps in [Create Respond automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/respond-alert-sow-itom.md).

6.  To complete the setup, select **Mark as configured**.



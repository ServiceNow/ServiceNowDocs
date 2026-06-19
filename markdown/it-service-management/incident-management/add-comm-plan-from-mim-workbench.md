---
title: Add communication plan from the major incident workbench
description: You can create a new communication plan or add a new communication task to an existing communication plan from the workbench. This UI action is helpful when you do not have an existing well-defined communication plan in the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/add-comm-plan-from-mim-workbench.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Major incident workbench, Manage major incidents, Incident Management, IT Service Management]
---

# Add communication plan from the major incident workbench

You can create a new communication plan or add a new communication task to an existing communication plan from the workbench. This UI action is helpful when you do not have an existing well-defined communication plan in the system.

## Before you begin

Role required: major\_incident\_manager

## Procedure

1.  Navigate to [Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/major-incident-workbench.md).

2.  Select the **Communications** tab and then select **Add** that appears in Communication Tasks section to display the Adhoc Communication pop-up window.

3.  On the form, fill in the fields.

<table id="table_nft_qwm_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Communication Plan

</td><td>

List to select a new communication plan or to select an existing plan and add communication tasks to the plan.

</td></tr><tr><td>

Plan Short description

</td><td>

Brief description of what the communication plan is all about.

</td></tr><tr><td>

Task Short description

</td><td>

Brief description of what the communication task is all about.

</td></tr><tr><td>

Channels

</td><td>

Option for selecting email, SMS, Slack, or conference as the communication method channel for the plan.

 **Note:** To use the SMS channel, the Notify plugin \[com.snc.notify\] must be active and configured with a Twilio integration, and a notify number group must be set up. For more information, see [Activate Incident Management - Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/activate-major-incident-management-plugin.md).

</td></tr><tr><td>

Frequency

</td><td>

Frequency at which a specific task needs to be executed. A task can be executed only once or on specific durations.

</td></tr><tr><td>

Due in \(Minutes\)

</td><td>

Time span when the task must be executed after the task initiates. For recurring tasks, it also indicates the time span after which the task must repeat.

</td></tr></tbody>
</table>
**Parent Topic:**[Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/major-incident-workbench.md)


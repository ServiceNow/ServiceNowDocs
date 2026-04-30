---
title: Define how a Zoom chat is closed
description: Define the way a Zoom chat is closed.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Chat-specific configuration for Collaboration services for Zoom, Enhance employee experience by integrating ServiceNow with Zoom, Integrating and using ServiceNow with Zoom, ServiceNow for Zoom, Zoom integrations, Unified Employee Experience, Employee Service Management]
---

# Define how a Zoom chat is closed

Define the way a Zoom chat is closed.

## Before you begin

Role required: admin

## About this task

When a ticket is set to inactive, the system does one final poll for any messages in the Zoom Team Chat. The participants are removed so no further messages about the ticket can be exchanged in the chat. The system then stops polling that chat.

If your custom application doesn’t provide an **Active** option for determining whether the ticket remains active, you must either add that option \(preferred\) or define an alternate condition denoting the ticket as being closed or inactive.

Alternately, to adhere to platform standards, consider adding an active field to your custom application and maintaining the state of that field according to the business logic of your application.

When a parent ServiceNow record is closed, associated Zoom channel is archived, and only an admin user or that chat creator can post new messages on a closed chat or a channel. The users who are removed from a chat can only see the chat messages history.

## Procedure

1.  Navigate to **All** &gt; **Collaboration Services** &gt; **Close Conditions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_srq_2ld_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table to which the requester mapping should be applied.

</td></tr><tr><td>

Inherit

</td><td>

Apply the option to the child tables of the selected table.

</td></tr><tr><td>

Active

</td><td>

Option to activate the close condition.

</td></tr><tr><td>

Order

</td><td>

Order of the configuration.

 You can define multiple chat configurations for a single table. The system executes the query in the descending order.

</td></tr><tr><td>

Close conditions

</td><td>

Defines the condition that determines that the record is closed.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Chat-specific configuration for Collaboration services for Zoom](../concept/additional-configuration-sn-cs-zoom.md)


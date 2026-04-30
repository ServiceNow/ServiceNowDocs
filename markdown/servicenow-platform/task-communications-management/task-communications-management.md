---
title: Task Communications Management process
description: Task Communications Management helps you to streamline the process by creating designated communication plans for effective communication during an event. The communication plan, with its defined tasks, helps you to focus on resolving the current issue instead of deciding when to send a communication, what information to share, and whom to inform.
locale: en-US
release: xanadu
product: Task Communications Management
classification: task-communications-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Task Communications Management process

Task Communications Management helps you to streamline the process by creating designated communication plans for effective communication during an event. The communication plan, with its defined tasks, helps you to focus on resolving the current issue instead of deciding when to send a communication, what information to share, and whom to inform.

![Basic components](../image/tcm-basic-component.png "Task Communications Management basic components")

## How Task Communications Management works

With Task Communications Management, you can predefine a communication plan for an event such as major incident, planned maintenance, and release. Each plan generally involves a series of tasks that define different communication and collaboration activities along with frequency and method of communication. For each task, you must specify the communication channel for contacting the stakeholders. You can also define templates for email and SMS messages.

After defining the task and channel for communication, you can define the contacts or the target audience to be contacted for each task.

After a communication plan is defined, the plan gets associated with the appropriate task table based on the conditions defined. Thereafter, the tasks defined in the plan get executed sequentially and stakeholders are contacted as defined in the plan. The communication plan makes communication and collaboration process smoother and brings a quicker resolution of the issue.

## Task Communications Management flow in major incident management

Assume that you want an incident communication plan generated for a high-priority major incident.

-   As the major incident manager, you can predefine a communication plan and the conditions that drive its attachment. In this case, the conditions are: Priority = High and Major Incident state = Accepted. Consider that the target audience is the technical stakeholders of the incident and the communication plan definition is named Technical Communications.
-   The plan definition can have multiple communication task definitions such as:
    -   Initiate Technical Communications
    -   Technical Status Update
-   Each communication task definition also specifies the channel of communication and the communication frequency \(one time or recurring\).
    -   Initiate Technical Communications uses email as a channel of communication and communication frequency is one time.
    -   Technical Status Update uses email and SMS as channel of communication and the communication frequency is recurring.
-   The target audience for in the communications is defined as communication contact definitions on the plan definition. In this case, consider Service owners of the affected configuration items \(CIs\) related to the incident as technical stakeholders.
-   When an incident meets these conditions, an incident communication plan together with its tasks gets attached to the incident record.
-   As the major incident manager, you can effectively carry out the communication without any delay in the resolution of the major incident.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Task Communications Management](../reference/tcm-landing-page.md)


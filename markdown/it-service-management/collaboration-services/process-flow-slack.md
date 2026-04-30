---
title: Process flow for Slack communication
description: Collaborate with the stakeholders from major incident management workbench using slack for an open and transparent communication.
locale: en-US
release: xanadu
product: Collaboration Services
classification: collaboration-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Collaboration services, IT Service Management]
---

# Process flow for Slack communication

Collaborate with the stakeholders from major incident management workbench using slack for an open and transparent communication.

Define a communication plan to manage the communication process. The plan includes tasks to achieve the plan goal and the stakeholders whom you must contact in the process.

When you create communication tasks for a plan, select slack as a mode of communication. To know how to define a channel for any communication task, refer to [Define a communication channel](https://www.servicenow.com/docs/access?context=create-comm-channel-definition&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Keeping in mind the fact that it not always possible to plan for a communication plan or task in advance, you have the option to create adhoc communication plan and its tasks from an incident. When any task record meets the conditions in the communication plan, the plan gets attached with the task record. If for a major incident, a communication plan gets attached to the incident which has communication channel as slack for any of its tasks, you can send slack notifications from the major incident workbench.

**Note:** The slack communication is a one-way communication from ServiceNow application to slack. The contacts in the slack cannot reply to the person who initiated the slack communication. Also, the users in slack must be employees of the organization. For example, the email address that they share for participating in a slack collaboration must be their email address of that organization.

Slack communication uses the following subflows:

-   TCM Slack – Add Users to Channel
-   TCM Slack – Archive Channel
-   TCM Slack – Create Channel
-   TCM Slack – Send Message
-   TCM Slack – Remove User From Channel

## Slack communication through workbench

-   In the major incident workbench, under the **Communicate** tab, you can find all the communication tasks for the plan.
-   For the task where you have selected slack as a channel, you can click **Compose** to start a slack communication. For information on how to create a communication plan, refer to [Add communication plan from the major incident workbench](../../incident-management/task/add-comm-plan-from-mim-workbench.md)
-   In the dialog box, the **To** field includes the contacts that you have added while creating the communication contact for the plan.
-   The **Message** field includes the message you are intending to convey to the recipients.


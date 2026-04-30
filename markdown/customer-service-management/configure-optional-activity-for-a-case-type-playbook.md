---
title: Configure an optional activity for a playbook
description: Configure optional playbook activities so that agents and fulfillers can insert activities during a playbook run. For example, a customer may want to schedule an optional activity such as making an appointment to visit a location.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-13"
reading_time_minutes: 1
breadcrumb: [Configure Playbooks for Customer Service Management, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure an optional activity for a playbook

Configure optional playbook activities so that agents and fulfillers can insert activities during a playbook run. For example, a customer may want to schedule an optional activity such as making an appointment to visit a location.

## Before you begin

Role required: playbook\_experience.admin

## About this task

Configure optional playbook activities in Process Automation Designer \(PAD\).

Although you can insert global optional activities anywhere in the playbook, you can only insert stage-specific optional activities when a specified stage is active in the playbook. You can also add other global optional activities such as similar records, similar documents, and managed documents.

**Note:** Some optional activities may require additional plugins. For example, for the Approval Request activity, if the approval action needs to be exposed to the customer via the service portal, you must install the plugin portal store app \(com.snc:app-customer-service-portal\) release version 23.2.4. To display the activities for the similar and managed documents in PAD, you must install the document management plugin \(com.snc.platform\_document\_management\).

## Procedure

1.  Navigate to**All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the Playbooks tab at the top of the page.

3.  Select a playbook from the Label column.

4.  See the optional activities under all the stages by turning on the toggle for **Optional activities**.

5.  Select **Add optional activity** at any stage or globally.

6.  Under **Add activity**, select **Playbook for Customer Service Management** &gt; **Approval Request**.

    A new approval request optional activity is created.

7.  Select the **Approval Request** optional activity.

8.  Under **Edit activity properties**, in the **Details** tab, add a **Label**, **Description**, **Activity Definition**, and set **Start Rule** to **Manual**.

    This setting is the Optional Activity indicator.

9.  Save the new activity record.

10. Select **View all properties**.

11. Navigate to **Automation tab** &gt; **parent records** and select the parent record.

12. Go to the **Automation** tab and set the values of the starting state and ending state.

    The values for the starting and ending states are derived from the value field of the sys\_choice table.

    To create a custom state flow, see [Create a state flow](https://www.servicenow.com/docs/access?context=t_CreateAStateFlow&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Ensure that the class of the state flow is “Customer Service Case Flow." You can also configure more declarative actions for the optional activity. For more information, see [Creating new declarative action assignments](https://www.servicenow.com/community/next-experience-articles/creating-new-declarative-action-assignments-in-the-sys/ta-p/2394930).

13. Select **Done**.

14. Select **Activate**.



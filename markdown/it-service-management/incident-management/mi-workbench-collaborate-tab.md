---
title: Major Incident workbench — the Collaborate tab
description: The Collaborate tab helps you to view and manage communication tasks that use conference as their communication channel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/mi-workbench-collaborate-tab.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Major Incident workbench — the Collaborate tab

The **Collaborate** tab helps you to view and manage communication tasks that use conference as their communication channel.

\[Omitted image "collaborate-view.png"\] Alt text: The Collaborate tab

Like the **Summary** tab, you can add a new communication plan by clicking **Add**. You can create communication task for an existing plan by clicking **Add Call**. For more information, see [Add-communication-plan-from-mim-workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/add-comm-plan-from-mim-workbench.md). If you want to add or remove recipients from a particular plan after the plan is saved, select **Manage Participants**.

To initiate a conference call, select **Initiate**. If the communication task is a one-time task, then after the call is ended, the status of the task changes to **Complete**. If task is recurring, the status of the task changes to **Open** and it displays the number of times the conference call is initiated.

**Note:** When you add a user group to the conference call, the group itself is added to the call, and the escalation hierarchy is automatically followed once you start the call. Set the **com.snc.iam.conference\_call\_follow\_on\_call\_escalation** property to true. For more information about the property, see [System properties for On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/on-call-properties.md).

Under each task, the Active participant section displays the active participants and the Inactive participant section displays the inactive participants.

If the call is in progress, the itil user, who has access to the workbench, can join the conference call by clicking **Join Call**. The participants can also add another user to an ongoing conference call by clicking **+ Participants**. The conference leader can end the conference call by clicking **End Call**. The conference leader can mute, unmute, or kick an active participant by hovering over the active participant and clicking \[Omitted image "mute-kick-mim.png"\] Alt text: Mute or remove an active participant.

Under the Work Notes &amp; Activity section, you can send connect message at incident or incident communication plan level. You can also view the activity stream.

To initiate a call directly to the group members, select **Start a call**.

\[Omitted image "start-a-call.png"\] Alt text: Start a call

To start a call, populate the **sn\_major\_inc\_mgmt.notify\_webrtc\_number** property with a valid notify number that has voice capability. For user who is already in an active conference call, **Start a call** is disabled. You can mute or unmute all the participants using the **Mute All** and **Unmute All** options.

To send a Microsoft Teams notification from major incident workbench, see [Send a notification from Major incident management workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/send-mim-notification.md). The procedure applies to both the **Collaborate** and **Communicate** tabs. To  Initiate Microsoft Teams group chat from MIM workbench, see [Initiate Microsoft Teams group chat from MIM workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/initiate-ms-teams-group-chat-mim-workbench.md).

For information on process flow for slack communication, see [Process flow for Slack communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/collaboration-services/process-flow-slack.md).

For information on how to add a collaborative communication task, see [Add a collaborative communication task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/collaboration-services/add-collaborate-task.md).

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Major Incident workbench — Summary tab]()

[Major Incident workbench — the Post Incident Report tab]()

[The Communicate tab in the Major Incident workbench]()


---
title: Collaborate tab in the Major Incident workbench
description: The Collaborate tab displays the communication tasks that use conference calls as their communication channel so you can view and manage them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/mi-workbench-collaborate-tab.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Collaborate tab in the Major Incident workbench

The **Collaborate** tab displays the communication tasks that use conference calls as their communication channel so you can view and manage them.

\[Omitted image "collaborate-view.png"\] Alt text: Collaborate tab showing conference call communication tasks and participants

As on the **Summary** tab, you can add a communication plan by selecting **Add**. You can create a communication task for an existing plan by selecting **Add Call**. For steps to add a communication plan, see [Add-communication-plan-from-mim-workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/add-comm-plan-from-mim-workbench.md). To add or remove recipients from a plan after it's saved, select **Manage Participants**.

To initiate a conference call, select **Initiate**. If the communication task is a one-time task, the status of the task changes to **Complete** after the call ends. If the task is recurring, the status of the task changes to **Open** and it displays the number of times the conference call is initiated.

**Note:** When you add a user group to the conference call, the group itself is added to the call. To follow the group's escalation hierarchy automatically after you start the call, set the **com.snc.iam.conference\_call\_follow\_on\_call\_escalation** property to `true`. For more information about the property, see [System properties for On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/on-call-scheduling/on-call-properties.md).

Under each task, the Active participant section displays the active participants and the Inactive participant section displays the inactive participants.

If the call is in progress, users with the itil role who have access to the workbench can join the conference call by selecting **Join Call**. The participants can also add another user to an ongoing conference call by selecting **+ Participants**. The conference leader can end the conference call by selecting **End Call**. The conference leader can mute, unmute, or remove an active participant by pointing over the participant and selecting the mute and remove icon \[Omitted image "mute-kick-mim.png"\] Alt text:.

In the Work Notes and Activity section, you can send a Connect message at the incident or incident communication plan level. You can also view the activity stream.

To initiate a call directly to the group members, select **Start a call**.

\[Omitted image "start-a-call.png"\] Alt text: Start a call

To start a call, populate the **sn\_major\_inc\_mgmt.notify\_webrtc\_number** property with a valid Notify number that has voice capability. For users who are already in an active conference call, **Start a call** is inactive. You can mute or unmute all the participants using the **Mute All** and **Unmute All** options.

To send a Microsoft Teams notification from the major incident workbench, see [Send a notification from Major incident management workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/send-mim-notification.md). The procedure applies to both the **Collaborate** and **Communicate** tabs. To initiate a Microsoft Teams group chat from the major incident workbench, see [Initiate Microsoft Teams group chat from MIM workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/initiate-ms-teams-group-chat-mim-workbench.md).

For information about the process flow for Slack communication, see [Process flow for Slack communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/collaboration-services/process-flow-slack.md).

For steps to add a collaborative communication task, see [Add a collaborative communication task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/collaboration-services/add-collaborate-task.md).

For the **Collaborate** tab to appear in the major incident workbench, the Notify plugin \(com.snc.notify\) must be active. For troubleshooting information, see [Collaborate tab is not visible in Major Incident Workbench \[KB0754834\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0754834).

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Summary tab in the Major Incident workbench]()

[Post Incident Report tab in the Major Incident workbench]()

[Communicate tab in the Major Incident workbench]()


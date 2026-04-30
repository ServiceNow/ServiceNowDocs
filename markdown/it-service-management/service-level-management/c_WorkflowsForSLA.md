---
title: Workflows for SLA
description: SLA typically uses workflows to send notifications.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Workflows for SLA

SLA typically uses workflows to send notifications.

You can create and edit workflows with the Workflow Editor. The default workflow that is available with the Service level management plugin is **Default SLA Workflow**.

The **Default SLA Workflow** creates the events that send out notifications. For example, it creates an event to send a notification to the user assigned to a task, such as an incident, when the task SLA reaches 50% of its allotted time.

The **SLA Notification and Escalation Workflow** creates the events that send out notifications. When a task reaches 50% of its allotted SLA duration, a notification is sent to the assignee and the user listed in the **Supported by** field on the configuration item. At 75% and 100%, a notification is sent to the assignee and the assignee's manager.

**Note:** This feature is available only in new instances starting with Jakarta or a later release. The Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\) plugin must be activate.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

**Related topics**  


[Workflow editor](https://www.servicenow.com/docs/access?context=workflow-editor&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)


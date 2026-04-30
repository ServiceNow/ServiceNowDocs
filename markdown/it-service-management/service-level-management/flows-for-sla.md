---
title: Flows for SLA
description: Use the flow actions to send SLA notifications when the duration specified in the SLA definition is crossed.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Flows for SLA

Use the flow actions to send SLA notifications when the duration specified in the SLA definition is crossed.

You can create and edit flows using the Flow Designer. The default flow that is available with the Service level management plugin is **Default SLA flow**.

The **Default SLA flow** creates the events that send out notifications. For example, it creates an event to send a notification to the user assigned to a task, such as an incident, when the task SLA reaches 50% of its allotted time.

The **SLA Notification and Escalation flow** creates the events that send out notifications. When a task reaches 50% of its allotted SLA duration, a notification is sent to the assignee and the user listed in the **Supported by** field on the configuration item. At 75% and 100%, a notification is sent to the assignee and the assignee's manager.

**Note:** This feature is available only in new instances starting with Orlando or a later release.

For more information on SLA notifications, refer [SLA notifications](c_SLANotifications.md).

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)


---
title: Initiate a learning task from a lifecycle event
description: When a lifecycle event is triggered, a learning task is created and assigned to the subject person of the case. The task is displayed in the To-dos page in Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/hr-service-delivery/ln-task-pst.html
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Learning Posts, HR Service Delivery, Employee Service Management]
---

# Initiate a learning task from a lifecycle event

When a lifecycle event is triggered, a learning task is created and assigned to the subject person of the case. The task is displayed in the To-dos page in Employee Center.

## Before you begin

Role required: admin

## Procedure

1.  Create a learning task template.

    For more information, see [Create a learning template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/hr-service-delivery/ln-templates.md).

2.  Configure a lifecycle event activity set.

    For more information, see [Configure a lifecycle event activity set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/lifecycle-events/configure-hr-lifecycle-event-activity-set.md).

3.  Configure a lifecycle event activity.

    While creating a lifecycle activity, make sure you select **Activity Type** as **Employee**, **Employee Activity** as **Learning task**, and **HR Template** as any learning template task. For more information, see [Configure a lifecycle event activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/lifecycle-events/configure-hr-lifecycle-event-activity.md).

    When the lifecycle event is triggered, a learning task is created and assigned to the subject person of the case.



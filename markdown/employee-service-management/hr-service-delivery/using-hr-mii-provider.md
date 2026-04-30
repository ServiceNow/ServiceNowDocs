---
title: Using HR Multi Instance Integration for Provider
description: Fulfill a remote HR service request that is placed from a consumer instance to a provider instance.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Using HR Multi Instance Integration for Provider

Fulfill a remote HR service request that is placed from a consumer instance to a provider instance.

## Before you begin

Role required: HR agent

## Procedure

1.  Review the remote HR case that is assigned to you.

    The remote HR case is created from an HR request placed from a consumer instance.

    **Note:** Transferring of cases, suspension of cases, and sharing of knowledge articles is not supported for the remote HR cases that are fulfilled in a provider instance.

2.  To add an HR task for the remote HR case:

    1.  In Related lists, click **Add task**. For more information, see [Adding an HR task to an HR case](../task/t_ViewAnHRTask.md).
    2.  In the **Assigned to** field, specify the consumer user to whom you want to assign the task. A universal task of type URL is assigned to the consumer user.
    **Note:**

    A universal task is created only for consumer user, and not for local users on provider instance. The universal task is created only when the email ID of the consumer user matches in both provider and consumer instances.

3.  To add an approval task for the remote HR case, click **Add an approval** in **Related lists**.

    For more information, see [Add adhoc approvers to a case](../task/add-approvers-cm.md).

    **Note:**

    -   Remote approval's universal tasks are triggered only when the email ID of the approval user matches in both provider and consumer instances.
    -   The Add an approval option appears only when the **Agent can add an approval** option is configured in the HR service against which the remote case is created.
4.  To initiate document signing tasks for the remote HR case:

    1.  In the **Document template** field, select the configured document template.
    2.  In **Assigned to** field, specify the HR agent on provider instance. The assigned HR agent can set a due date, modify the description, and short description of the document task. A universal task of type URL is assigned to the consumer user.
    **Note:**

    -   To initiate document tasks, the Document Templates plugin must be installed on the HR Multi Instance Integration for Provider application.

        For more information on how document tasks are initiated, see [Document tasks generation](../task/task-mapped-participants.md).

    -   In the HR service additional information, Document template must be added in the **Service table** fields.
5.  Request for any additional information from the consumer employee by adding comments or attachments to the case.

    The requested details are synchronized with the provider task in consumer instance. The consumer user can view the updates on their catalog request from Employee Portal.

6.  Close the HR case when the all the tasks associated to it are complete.



---
title: Manage Business Application Lifecycle Management service requests
description: You can approve requests raised by an Enterprise Architecture user either for a new business application or retire an application that the user no longer requires.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage Business Application Lifecycle Management service requests

You can approve requests raised by an Enterprise Architecture user either for a new business application or retire an application that the user no longer requires.

## Before you begin

Role required: sn\_apm.apm\_analyst

The approver \(apm\_analyst\) must also be a part of the Enterprise Architect Group. To add or modify the members in the group, navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Services Approval Group**.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Business Application Lifecycle Management** &gt; **Service Requests**.

    All requests related to the Business Application Lifecycle Management services are stored as tasks in the Business Application Requests table \[business\_app\_request\].

    Note the tasks that are in your queue for your approval.

2.  Select the task number.

3.  Scroll down to the Approvers related items.

4.  Select the state of the approval task.

5.  Select the appropriate state from the list in the **State** field.

6.  Enter a comment if required.

7.  Select **Update**.

    Once you approve or reject a request, a corresponding flow is triggered. Select the **Show flow engine context** related link to view the flow engine context of the request. You can also navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Services Flow Designer** to see the flow in the flow designer.

    -   **If you approve a Register a Business Application request**
        -   The approved business application is created as a record with an identification number in the business applications table \[cmdb\_ci\_business\_app\]. The status of the application is in the **Implementing** state.
        -   An email is sent to the requester notifying the approval of the business application.
    -   **If you approve a Retire a Business Application request**
        -   Based on the value selected in the system property, **sn\_apm.retireBusinessApplicationTaskType**, a project, or demand is created. If the value is set as project, then a project template defined in the system property, **sn\_apm.retireBusinessAppProjectTemplate**, is applied.

            **Note:** If the value is set to project in the system property **sn\_apm.retireBusinessApplicationTaskType**, you require Strategic Portfolio Management \(SPM\) subscription to approve requests to retire business applications and create a project.

            The base system of Enterprise Architecture offers a project template called **Retire Business Application** with eight different pre-defined project template tasks for proper decommissioning of the application.

            After the project is created and a project manager is assigned to the project, the project manager can review, edit, or add tasks as required. For more information on project templates, see [Project templates](https://www.servicenow.com/docs/access?context=c_ProjectTemplates&version=australia&pubname=australia-it-business-management&ft:locale=en-US). To understand the project tasks, see [Project tasks](https://www.servicenow.com/docs/access?context=c_ProjectTasks&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

        -   If the value in the **sn\_apm.retireBusinessApplocationTaskType** system property is set as demand, then a demand is created.

            Unlike a project, Enterprise Architecture doesn’t generate a demand from a template with pre-configured demand tasks. Instead the demand is created with certain values auto-populated in mandatory fields.

            To view the demand that is created to retire an application, navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio Analysis** &gt; **Demands**.

            For field information, see [Demand form to retire an application](../reference/demand-form-retire-application.md).

        -   If you approve a request for which a project or demand is already in place, then another project or demand will not be created for the request.
        -   If the request to retire an application is rejected, then an email notification is sent to the requester. However, the status of the business application isn’t updated irrespective of it being approved or rejected.
        -   You can delete a business application record or mark an application as **Inactive** as an Enterprise Architecture admin or analyst.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)


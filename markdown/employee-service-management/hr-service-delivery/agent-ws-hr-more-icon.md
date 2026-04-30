---
title: Using the More icon in HR Service Delivery Agent Workspace
description: You can use the More icon more icon from HR Service Delivery Agent Workspace to perform many duties related to working an HR case.From HR Service Delivery Agent Workspace, you can create additional cases from either an existing case or from a user's HR profile.Transfer an HR case from one HR service to a different HR service.Escalate an HR case when you are unable to resolve an issue and must amplify the importance of a case.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Using the More icon in HR Service Delivery Agent Workspace

You can use the ![More icon](../reference/images/more-icon.png)more icon from HR Service Delivery Agent Workspace to perform many duties related to working an HR case.

When working a case, select the ![more icon](../reference/images/more-icon.png) more icon in the far, upper right.

![HR Agent Workspace - More icon](../image/agent-ws-hr-more.png)

From here, you can:

-   Associate Interaction: Associate the displayed case with an interaction. For more information, see [Using interactions in HR Service Delivery Agent Workspace](agent-ws-hr-interactions.md#).
-   Compose Email: Send an email from an HR case. The **New Email Draft** tab opens to compose and send the email. The **To** field is automatically updated with the Subject person's email ID. Agent can retain the email or add a new email. For more information, see [Sending an email in HR Agent Workspace](../task/send-an-email-hr-agent-ws.md).
-   Create Additional Case: Create another HR case without leaving the case you are viewing or working on. For more information, see [Creating a case from a case or HR profile](agent-ws-hr-more-icon.md#).
-   Set reminder: Create a reminder to ensure followup by a specific date. For more information, see [Create a reminder in HR Service Delivery Agent Workspace](../task/agent-ws-hr-reminder.md).
-   Transfer Case: Reclassify a case for another HR service. For more information, see [Transfer a case using HR Service Delivery Agent Workspace](agent-ws-hr-more-icon.md#).
-   Add Task: Add an HR task to the case. For more information, see [Create a task for a case using HR Service Delivery Agent Workspace](../task/agent-ws-hr-task.md).
-   Escalate Case: Assign hot or important cases to another tier or agent with more expertise. For more information, see [Escalating a case in HR Service Delivery Agent Workspace](agent-ws-hr-more-icon.md#).
-   Delete: Delete the case you are working on.

## Creating a case from a case or HR profile

From HR Service Delivery Agent Workspace, you can create additional cases from either an existing case or from a user's HR profile.

A convenient and time saving feature of HR Service Delivery Agent Workspace is having everything you need as an HR agent in one place.

You don't have to leave a case you are working on and try to find it later. You can create another HR case from:

-   An HR case you are viewing.
-   From an HR profile that displays on a case you are viewing.

-   **From an open case**

    Use this feature when you want to create a different HR case for the employee that already appears in an existing case.

    ![Create additional case](../image/agent-ws-hr-create-add-case.png)

    Select the ![More icon](../reference/images/more-icon.png) more icon.

    Select **Create Additional Case**. The employee name from the first case pre-populates in the new case.

-   **From an HR profile**

    When viewing an HR case, you can create another case from the Opened for or Subject person's HR profile.

    ![HR Agent Workspace case](../image/agent-ws-hr-profile-icon-case.png)

    Select ![HR profile icon](../reference/images/hr-profile-icon.png) next to the Subject person.

    ![HR Agent Workspace HR profile](../image/agent-ws-hr-profile-case.png)

    Select the ![More icon](../reference/images/more-icon.png) more icon.

    **Note:** The At-a-glance panel displays. See [At a Glance panel](hr-profile-for-hr-agent-workspace.md#).

    Select **New Case**.


## Transfer a case using HR Service Delivery Agent Workspace

Transfer an HR case from one HR service to a different HR service.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### About this task

Many cases are created as a General Inquiry case. After researching the employee's needs, you can transfer an existing case to a different HR service.

For information on configuring HR case transfer or classification properties, see [Transfer an HR case](reclassify-hr-case.md).

You can complete this task in the Classic HR Service Delivery Agent Workspace or the configurable Agent Workspace for HR Case Management.

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Find the case you want to transfer.

    For more information on finding an HR case, see [Using the HR Service Delivery Agent Workspace](use-agent-ws-hr.md).

3.  Select the ![More icon](../reference/images/EllipsisIcon.png) more icon.

4.  Select **Transfer Case**.

5.  From **Transfer type**:

    -   **Transfer with existing case number**: The HR case number does not change, links redirect with new case, and work notes transfer to new case.
    -   **Transfer to a new case number**: The HR case number changes, links do not redirect, and work notes do not transfer. Both HR case numbers appear on the HR case for reference. The original case state changes to **Closed Complete** and cancels.
6.  From **New HR Service**, select the HR service you want to assign to your original case.

7.  Select **OK**.

    The current case and its child tasks close. When you transfer an HR case from one HR service to another, some field values do not transfer to the new case.

    **Note:** Priority transfers from the original case and does not override the HR template for the new HR case.

    The subject person receives a notification email with the closed case and transferred case information. Replies to the email appear in the Comments section of the HR case. If the subject person replies to the email associated with the closed case, the reply appears in the comments for both the closed and transferred cases.

    **Note:** If the sn\_hr\_core.restrict\_guest\_email system property is False, text from an email appears in the Work notes field when the employee is responding from a personal email account. False is the default property.

    See [Email setup](https://www.servicenow.com/docs/access?context=c_EmailConfiguration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


## Escalating a case in HR Service Delivery Agent Workspace

Escalate an HR case when you are unable to resolve an issue and must amplify the importance of a case.

Depending on how you have implemented matching rules determines what group and agent the case is escalated to. For more information, see [Assignment and matching rules in HR](c_UseAssignmentRules-1.md) and [Add or modify escalation rules](../task/t_CreateOrModifyEscalationRules.md).

![HR Agent Workspace More icon](../image/agent-ws-hr-more.png)

<table id="table_r4f_52d_jjb"><thead><tr><th>

Number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![HR Agent Workspace Case form callout 1](../reference/images/1.png)

</td><td>

Select the ![More icon](../reference/images/more-icon.png) more icon.From here, select **Escalate Case**.

</td></tr></tbody>
</table>![HR Agent Workspace case escalation](../reference/images/agent-ws-hr-escalate.png)

<table><thead><tr><th>

Number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![HR Agent Workspace Case form callout 2](../reference/images/2.png)

</td><td>

Enter an explanation on why you are escalating the case.Select **OK**.

 The form refreshes and is now assigned to the next tier assignment group.

</td></tr></tbody>
</table>
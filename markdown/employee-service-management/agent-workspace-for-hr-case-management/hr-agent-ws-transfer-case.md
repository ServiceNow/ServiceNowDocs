---
title: Transfer a case in Agent Workspace for HR Case Management
description: Many cases are created as a General Inquiry case. After researching the employee's needs, you can transfer an existing case to a different HR service.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the More icon in Agent Workspace for HR Case Management, Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Transfer a case in Agent Workspace for HR Case Management

Many cases are created as a General Inquiry case. After researching the employee's needs, you can transfer an existing case to a different HR service.

## Before you begin

Role required: sn\_hr\_core.case\_writer

For information on configuring HR case transfer or classification properties, see [Transfer an HR case](../concept/reclassify-hr-case.md).

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Find the case you want to transfer.

    For more information on finding an HR case, see [Using Agent Workspace for HR Case Management](../concept/agent-ws-hr-case-mgmt-use.md).

3.  Select the ![More icon](../reference/images/EllipsisIcon.png) more icon.

4.  Select **Transfer case**.

5.  Select one of the two options from **Transfer type**.

    -   **Transfer with existing case number**: The HR case number does not change, links are redirected to the new case, and work notes is transferred to the new case.
    -   **Transfer to a new case number**: The HR case number changes, links are not redirected, and work notes is not transferred. Both HR case numbers appear on the HR case for reference. The original case state is changed to **Closed Complete** and is canceled.
6.  Select an appropriate COE.

7.  From **New HR Service**, select the HR service you want to assign to your case.

8.  Click **OK**.

    When you transfer an HR case from one HR service to another, some field values are not transferred to the new case. The current case and its child tasks are closed.

    **Note:** Priority is transferred from the original case and does not override the HR template for the new HR case.

    The subject person receives a notification email with the closed case and transferred case information. Replies to the email appear in the Comments section of the HR case. If the subject person replies to the email associated with the closed case, the reply appears in the comments for both the closed and transferred cases.

    **Note:** If the sn\_hr\_core.restrict\_guest\_email system property is False, text from an email appears in the Work notes field when the employee is responding from a personal email account. False is the default property.

    See [Email setup](https://www.servicenow.com/docs/access?context=c_EmailConfiguration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).



---
title: Universal Request sensitive information security
description: Universal Request security capability provides flexibility to protect information by controlling the view and edit authorization.Mark a universal request as restricted when you identify the request contains sensitive information.You can unrestrict a restricted universal request if you identify that the request does not have any sensitive information.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using Universal Request, Universal Request, Employee Service Management]
---

# Universal Request sensitive information security

Universal Request security capability provides flexibility to protect information by controlling the view and edit authorization.

## Key advantages

-   Requester can mark the request as sensitive at the time of creating the request.
-   Routing agents can mark the request as restricted while creating a request.
-   If the request is not sensitive, a sensitive info routing agent from the current assignment group, or the primary ticket agent can mark the ticket as unrestricted while triaging.
-   When a restricted ticket is created or transferred, only a sensitive info routing agent from the current assignment group, or the primary ticket agent can view the complete details of the ticket.
-   The security controls are also transferred during cross-department transfers, as the assignment group is changed to that of the new department.
-   Use Predictive Intelligence solution to automatically identify and mark the universal request as sensitive.

## Sensitive Info Agent role

The **sn\_uni\_req.sensitiveinfo\_agent** role controls who views and acts on the universal requests that have sensitive information. Only the UR routing agents from the current assignment group with the **sn\_uni\_req.sensitiveinfo\_agent** role, and the primary ticket agent can view the complete details of the ticket.

For example, if an HR case \(primary ticket\) is created for a universal request, then only the HR routing agent with the **sn\_uni\_req.sensitiveinfo\_agent** role, or the HR case agent can view the complete details of the request, such as the short description, description, attachments, and comments.

An agent without the sensitive agent role can access only the primary information of the request. The secured fields \(short description, description\), attachments, and comments in the activity stream are hidden.

## Application Administration enabled scoped application

Universal Request is an Application administration enabled application. If you are configuring your service that is also an application administration enabled application or has it's own security modal, then you must register your application. For more information, see [Register application administration enabled scoped application](../task/ur-service-scoped-administration.md). This ensures that the security is maintained within the universal request.

## Raising a sensitive universal request from the portal

When requesters create a request using the **Request Help** option on the Service Portal, Employee Center, or Mobile app, then they can secure the information provided as sensitive.

To help requesters identify sensitive information, a knowledge article is provided on the **Request Help** page. After determining if the request is sensitive, they can select the **Issue contains sensitive or confidential information** check box. If the check box is selected, the requester can select the department to which the issue might belong, or choose the **I'm not sure \(general submission\)**.

If the Predictive Intelligence for Universal Request \[com.snc.universal\_request.ml\] plugin is installed, then the department is auto-selected, and the requester is notified about the selection. For more information, see [Activate Predictive Intelligence for Universal Request](../task/activate-predictive-intelli-ur.md). The requester can then choose to override the suggestion. On submission, this action creates a universal request marked as **Restricted**.

At times, agents can also create a request from an interaction, a call, or from the Self-Service module. In such cases, the agent can mark the request as **Restricted**.

## Agent experience of UR security

Any agent can view the list of universal requests that are marked as restricted. However, only the service-specific assignment group agent or the agent who have access to sensitive requests can view the detailed information. While triaging, any agent who views the request and identifies that it has sensitive information can mark it as restricted.

If the Predictive Intelligence for Universal Request \[com.snc.universal\_request.ml\] plugin is installed, then UR with sensitive information is automatically identified and marked as restricted and only agents with **sn\_uni\_req.sensitiveinfo\_agent** role can access and work on the request.

However, only the service-specific assignment group agent or the agent with the role to access a sensitive request can mark it as unrestricted. For more information, see [Restrict universal request access](universal-request-security.md#) or [Mark universal request as unrestricted](universal-request-security.md#). You can mark a request as restricted or unrestricted directly on the universal request or from the primary ticket.

## Transferring a restricted request

A restricted request means the parent universal request is marked as restricted. When a primary ticket of the sensitive universal request is transferred to another department, the security controls are also transferred, as the assignment group of the UR changes.

## COE Security

COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Using Universal Request](using-ur.md)

## Restrict universal request access

Mark a universal request as restricted when you identify the request contains sensitive information.

### Before you begin

Role required: employees, routing agents, sn\_uni\_req.sensitiveinfo\_agent or service specific assignment group members

### Procedure

1.  Navigate to the universal request that you want to mark as restricted.

2.  On the form, click the **Restrict** button.

    ![Restrict a universal request with sensitive data](../images/restrict-ur.png)

    The restricted fields are hidden, and the form is only for view purpose.

    **Note:** To mark the request as unrestricted only agents with the access role can modify.


## Mark universal request as unrestricted

You can unrestrict a restricted universal request if you identify that the request does not have any sensitive information.

### Before you begin

Role required: sn\_uni\_req.sensitiveinfo\_agent, Primary ticket agent, or members of assignment group of that UR

### Procedure

1.  Navigate to the universal request that you want to mark as unrestricted or to the primary ticket that you are resolving.

2.  On the form, click the **Unrestrict** button.

    ![Unrestrict the universal request](../images/unrestrict-ur.png)

    The hidden restricted fields are now visible, and any agent can view the content.

    **Note:** To mark the request as unrestricted only agents agent who is part of the primary ticket assignment group or with the access role can modify.



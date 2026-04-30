---
title: Using Universal Request in Agent Workspaces
description: As a Routing Agent, use the Universal Request in Agent Workspaces to view, create, edit and resolve universal requests.The Universal Request is a task that a requester creates from any of the following sources, such as mobile application, service portal, agent workspace, or using a virtual agent chat. As a routing agent, you can create universal requests from the Universal Request application on behalf of the requester to track and resolve issues.Convert an Interaction Record to a Universal Request from the Universal Request Agent Workspace.Change the state of the universal request to Canceled to cancel the request if the issue is resolved already or you no longer require the request.Find similar Universal Requests that are open and closed, Knowledge articles, Catalog items, and Pinned articles using the Agent Assist capability in the Agent Workspace.You can transfer a primary ticket back to Universal Request, service set \(department\), or service either with resolution or without resolution.Mark a universal request as restricted when you identify the request contains sensitive information.You can unrestrict a restricted universal request if you identify that the request does not have any sensitive information.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Universal Request in Agent Workspaces, Universal Request, Employee Service Management]
---

# Using Universal Request in Agent Workspaces

As a Routing Agent, use the Universal Request in Agent Workspaces to view, create, edit and resolve universal requests.

You can start working on Universal Request in the Agent Workspaces from one of these areas:

-   Landing page
-   List queue
-   Global search

For additional information on working within Agent Workspace, see [Using workspace](https://www.servicenow.com/docs/access?context=using-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Universal Request in Agent Workspaces](universal-request-workspace.md)

## Create a universal request in Agent Workspace

The Universal Request is a task that a requester creates from any of the following sources, such as mobile application, service portal, agent workspace, or using a virtual agent chat. As a routing agent, you can create universal requests from the Universal Request application on behalf of the requester to track and resolve issues.

### Before you begin

Role required: sn\_uni\_req.routing\_agent or admin

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Universal Request** &gt; **Open**.

3.  Click **New**.

4.  On the form, fill in the fields.

<table id="table_un2_dyl_n3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The unique number generated for the universal request.

</td></tr><tr><td>

Opened

</td><td>

The date and time when the universal request was created.

</td></tr><tr><td>

Opened by

</td><td>

The agent who created the universal request.

</td></tr><tr><td>

Opened for

</td><td>

The user who requested for this universal request.

</td></tr><tr><td>

Primary task

</td><td>

The task number, for example, an incident or HR case number that is associated with the universal request.

</td></tr><tr><td>

Contact type

</td><td>

The medium from which the universal request was created.

</td></tr><tr><td>

Priority

</td><td>

It identifies how quickly the service desk should address the request.

</td></tr><tr><td>

State

</td><td>

State of the universal request. By default, the state is **New**.

</td></tr><tr><td>

Impact

</td><td>

Impact value indicates a measure of the effect of an incident, problem, or change on business processes.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to the universal request.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the universal request.

</td></tr><tr><td>

Needs resolution review

</td><td>

When checked, and when the department agent closes the primary ticket, the Universal Request does not get closed. Universal Request state remains in **In Progress** and the state reason changes to **Confirm Response**. This notifies the tier 1 agent \(Routing agent\) to either Accept or Reject the resolution provided in the primary ticket before closing the Universal Request for the requester.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the request.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the request.

</td></tr><tr><td class="sub-head" colspan="2">

Notes section

</td></tr><tr><td>

Watch list

</td><td>

Users to receive notifications when work notes are added.

</td></tr><tr><td>

Work notes list

</td><td>

Users to receive notifications when work notes are added.**Note:** The administrator must create an email notification for the work notes list.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

More information about the change.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the universal request or steps taken to resolve it, if applicable. This note is for internal use. The work notes information is not visible to your customer.

</td></tr><tr><td class="sub-head" colspan="2">

Closure Information section

</td></tr><tr><td>

Closed

</td><td>

The date and time when the universal request was closed.

</td></tr><tr><td>

Closed by

</td><td>

The agent that closed the request.

</td></tr><tr><td>

Close notes

</td><td>

How or why the universal request was closed.

</td></tr></tbody>
</table>
## Create a Universal Request from an Interaction Record

Convert an Interaction Record to a Universal Request from the Universal Request Agent Workspace.

### Before you begin

Role required: sn\_uni\_req.routing\_agent or admin

### About this task

Consider the following scenario. An IT service desk agent with a routing agent role receives a phone call on a request and creates a new call record or an Interaction Record with the notes. After reviewing the record, the agent realizes that the request belongs to HR and not IT. In this case, the IT Agent can create a Universal Record from the interaction record and assign it to the HR assignment group.

**Note:** Universal Request is not automatically created when a fulfiller creates a department ticket from an Interaction Record. You have to perform few manual steps to get this. For more information, see [Create universal request automatically for department tickets via other channels](../task/autocreate-ur-from-interactionrecord-WS.md).

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Interactions** &gt; **My Interactions**.

3.  Open the interaction record for which you want to create a Universal Request.

4.  Click the **Create UR** button

    ![Create UR from an Interaction record](../images/create-ur-from-ir-aws.png)

5.  Click **Save**.


## Cancel a universal request in Agent Workspaces

Change the state of the universal request to **Canceled** to cancel the request if the issue is resolved already or you no longer require the request.

### Before you begin

Role required: admin

### About this task

You can cancel a universal request only if there are no active or closed primary tickets attached to it. Also, the state of UR must be either **New** or **In Progress**. When the UR is canceled, email notifications are sent to the stakeholders associated with the request.

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Universal Request** &gt; **Open**.

3.  From the list of open universal requests, select the request you want to cancel.

4.  Select **Canceled** from the **State** field.

    **Note:** If the person in **Opened for** tries to cancel the request, then they must enter the reason for canceling.

5.  Click **Update**.


## Use Agent Assist in Agent Workspace

Find similar Universal Requests that are open and closed, Knowledge articles, Catalog items, and Pinned articles using the Agent Assist capability in the Agent Workspace.

### Before you begin

Role required: sn\_uni\_req.routing\_agent or admin

![Agent Assist in UR](../images/agent-assist-ur.png)

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Universal Request** &gt; **Open**.

3.  Click the universal request from the list or create a request.

4.  In **Agent Assist**, click the settings icon \(![Agent Assist settings](../images/toggle-compose-setting.png)\) and select your resource from the list.

    -   Similar Closed Universal Request: To display all similar Universal Requests that are closed.
    -   Universal Request: To display all similar Universal Requests that are available.
    -   Knowledge and Catalog: To display all related knowledge articles and catalog items.
    -   Knowledge Articles: To display all related knowledge articles.
    -   Catalog Items: To display all related catalog items.
    -   Pinned articles: To display all related pinned articles.

## Transfer primary ticket in Agent Workspaces

You can transfer a primary ticket back to Universal Request, service set \(department\), or service either with resolution or without resolution.

### Before you begin

Role required: No specific role is required. Agents part of the assignment group or assigned-to agents on the primary ticket can perform this task.

![Click to transfer the task](../images/route-to-ur-aws.png)

A routing agent can either resolve and close a primary ticket or transfer it to back to UR or another department for review and closure. When a primary task is transferred back to UR, the ticket is no longer a primary ticket and the primary ticket field of the universal request becomes empty.

When transferring the ticket, the routing agent can choose the department and a specific service within the department or can just choose `I'm not sure` when they are not sure of the department or service to transfer to.

When you transfer a ticket back to universal request, you can transfer it with one of the following reasons:

-   **Transfer with resolution**

    The request is resolved and transferred back to UR, a specific department, or service. Agents can choose this option when another department's help is required to fulfill the request.

-   **Transfer without resolution**

    The request is not resolved or does not belong to the specific department, and is transferred back to UR.


![Choose transfer reason](../images/route-dialog-aws.png)

Configure the **sn\_uni\_req.transfer\_type** property in the **Universal Request properties** page to determine how to handle the primary ticket transfers. For more information, see [Universal Request properties](../reference/ur-properties.md).

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  Open the primary task that you want to route to UR.

3.  Click **Transfer**.

4.  In the **Transfer Ticket** dialog, provide the following details.

    **Note:** Based on your transfer type configuration, the given fields are displayed. For more information, see [Universal Request properties](../reference/ur-properties.md).

    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.
    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for routing the primary ticket that you want to pass to the UR Routing agent.
    -   **Copy additional comments and attachments**: Deselect if you do not want to transfer the ticket with additional comments and attachments. By default, all attachments and comments are transferred.

        **Note:** Work notes are not copied while transferring.

5.  Click **Transfer**.

    The ticket is transferred based on the transfer and transfer type configuration. For more information, see [Transfer configuration](../task/configure-route-state.md).


## Restrict universal request access in Agent Workspace

Mark a universal request as restricted when you identify the request contains sensitive information.

### Before you begin

Role required: routing agents, sn\_uni\_req.sensitiveinfo\_agent or service specific assignment group members

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Universal Request** &gt; **Open**.

3.  Navigate to the universal request that you want to mark as restricted.

4.  On the form, click the **Restrict** button.

    ![Restrict the universal request with sensitive data](../images/restrict-ur-aws.png)

    The restricted fields are hidden, and the form is only for view purpose.

    **Note:** To mark the request as unrestricted only agents with the access role can modify.


## Mark universal request as unrestricted in Agent Workspace

You can unrestrict a restricted universal request if you identify that the request does not have any sensitive information.

### Before you begin

Role required: sn\_uni\_req.sensitiveinfo\_agent or service specific assignment group members

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

2.  From the navigation list, click **Universal Request** &gt; **Open**.

3.  Navigate to the universal request that you want to mark as unrestricted.

4.  On the form, click the **Unrestrict** button.

    ![Unrestrict the universal request](../images/unrestrict-ur-aws.png)

    The hidden restricted fields are now visible, and any agent can view the content.

    **Note:** To mark the request as unrestricted only agents with the access role can modify.



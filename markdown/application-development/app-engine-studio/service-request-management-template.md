---
title: Service Request Management template
description: Build an application in App Engine Studio \(AES\) using the Service Request Management template to create, track, and manage service requests in your organization.The following tables, experiences, automated workflows, and roles are included in the Service Request Management template for App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Available templates, Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Service Request Management template

Build an application in App Engine Studio \(AES\) using the Service Request Management template to create, track, and manage service requests in your organization.

To use the Service Request Management template, install the application from the ServiceNow Store.

![Service Request Management template](../image/template-service-request-mgmt.png)

## Personas in the Service Request Management template

This template contains several important roles that correspond to individuals or groups who may use the app in some way. The following information describes how each persona may interact with the application you build. For more information on the permissions each role contains, see the Security section.

-   **Requester**

    You are a person who has a request.

    Problem: You need a service or a physical item to complete your responsibilities. You want to know that your request is in progress and reassurance that it is making progress. If you have questions or your request has changed, you want the ability to communicate that to those working on the request.

    App objective: Empower employees by guiding them through the process, including what information is required. Make the approval process transparent, and keep them updated on the status and outcome of their request.

-   **Fulfiller**

    You are a person or team who must complete a task in a timely manner.

    Problem: You only want to be assigned a task when it is ready to be fulfilled, meaning after required approvals or dependent tasks \(if relevant\) are closed. You need to ensure that requests are closed in a timely fashion, especially in adherence with SLAs.

    App objective: Direct the fulfiller's attention to the tasks assigned to them and their team. Empower them by providing the information they need such as request information and SLA.

-   **Fulfiller's manager**

    You are the manager of the fulfillment team, and you can fulfill tasks.

    Problem: You need to ensure tasks are being efficiently closed by your team. You want to spot bottlenecks such as popular service requests creating a backlog of tasks, a fulfiller who is under-performing, or late approvals blocking fulfillers from completing their tasks on time.

    App objective: Direct the fullfiller's manager to tasks that need immediate attention so SLAs are met. Clearly show what their team is working on so they can re-prioritize work as needed.

-   **Service owner**

    You are the owner of the services within the app.

    Problem: You need to analyze how services are performing and identify which services need attention. You need information that will help you recommend improvements to the process, if necessary.

    App objective: Provide aggregate information that indicates each service's performance, measured by resolution and response time.

-   **Approver**

    You are the gatekeeper and can respond to or reject requests, saving time for fulfillers.

    Problem: You must review requests before they are assigned to a fulfillment team to ensure the ticket is appropriate.

    App objective: Direct the approver's attention to the requests that require their approval. Empower them by providing the information they need such as request and SLA information.


## Related concepts

For information about how to set up a service for your Service Request Management application, see [Service catalog setup](https://www.servicenow.com/docs/access?context=p_ServiceCatalogs&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Available templates](template-library.md)

## Service Request Management template contents

The following tables, experiences, automated workflows, and roles are included in the Service Request Management template for App Engine Studio \(AES\).

### Tables in the Service Request Management app template

<table id="table_cfc_ctm_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary\[x\_ &lt;company-code&gt;\_&lt;primary&gt;\]

</td><td>

Table that extends the Task table and stores the details of requests raised for the Service Request Management: Primary catalog item. To create a new service and table, extend this Primary table.

</td></tr><tr><td>

Example Request\[x\_ &lt;company-code&gt;\_&lt;example\_request&gt;\]

</td><td>

Example Request table created by extending the Primary table that stores the details submitted from the Travel Request catalog item.

</td></tr><tr><td>

Fulfiller Task\[x\_ &lt;company-code&gt;\_&lt;fulfiller\_task&gt;\]

</td><td>

Stores fulfiller tasks and helps admins keep service requests organized.

</td></tr></tbody>
</table>### Experiences in the Service Request Management app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Travel Request \| Fulfiller view|Form|Form for fulfillers to create a travel request record.|
|Primary \| Fulfiller view|Form|Form for fulfillers to create a service request record.|
|Fulfiller task \| Default view|Form|Form for users to create a fulfiller task.|
|Fulfiller Workspace|Workspace|Workspace for fulfillers to see requests that need their attention, create requests, view request assignments, and see data and analytics related to their requests.|
|Approver Workspace|Workspace|Workspace for approvers to see requests pending their approval, approve or deny requests, and see data and analytics related to their requests.|
|Fulfiller Task \| Fulfiller task view|Form|Form for users to create a fulfiller task.|
|Service Request Management: Primary|Record producer|Contains questions to add information and attach documents relevant to a service request.|
|Travel Request|Record producer|Contains questions to add information and attach documents relevant to a travel request.|
|Primary \| Default view|Form|Form for users to create a service request record.|
|Fulfiller's Manager|Workspace|Workspace for the fulfiller's manager to see requests pending their approval, create requests, approve or deny requests, and see data and analytics related to their and their team's requests.|
|Travel Request \| Default view|Form|Form for users to create a travel request record.|

### Automated workflows in the Service Request Management app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Fulfiller task work notes added|Email|Notifies users in the Assigned to field, Work notes list, and Watch list when work notes are added to a fulfiller task.|
|Fulfillment Process Trigger|Email|Notifies a service owner when a fulfiller task has been created but has no default Fulfiller or Fulfillment Assignment Group.|
|On Insert empty Assigned to|Email|Notifies an assignment group when a request record has been created and has no assignee.|
|On Insert/Change Assigned to|Email|Notifies a user that a request record has been assigned to them.|
|Assignment Process|Flow - record|Creates and updates a new record as it moves through the assignment, approval, and fulfillment processes.|
|Fulfiller Decision|Decision table|Defines the default fulfiller user and fulfiller assignment group for each service.|
|Approval Process|Flow|Moves a record through the approval process.|
|Approver Decision|Decision table|Defines the default approver and approver assignment group for each service.|
|Fulfillment Process|Flow|Moves a record through the fulfillment process.|
|Child worknotes added|Email|Notifies users named in the **Assigned to** field, Work notes list, and Watch list when work notes are added to a travel request task.|
|Primary worknotes added|Email|Notifies users in the **Assigned to** field, Work notes list, and Watch list when work notes are added to a request record on the Primary table.|

### Roles in the Service Request Management app template

<table id="table_htl_zxm_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approver\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.approver\]

</td><td>

Provides access to approver workspace and provides read and write access to the Primary \[x\_ &lt;company-code&gt;\_&lt;primary&gt;\] and Travel Request \[x\_ &lt;company-code&gt;\_&lt;travel\_request&gt;\] tables.

</td></tr><tr><td>

App admin\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.app\_admin\]

</td><td>

Provides complete access to the Service Request Management data and workspaces.

</td></tr><tr><td>

Fulfiller's manager\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.fulfillers\_manager\]

</td><td>

Provides access to fulfiller's Manager workspace and provides read and write access to the Primary \[x\_ &lt;company-code&gt;\_&lt;primary&gt;\], Travel Request \[x\_ &lt;company-code&gt;\_&lt;travel\_request&gt;\], and Fulfiller Task \[x\_ &lt;company-code&gt;\_&lt;fulfiller\_task&gt;\] tables.

</td></tr><tr><td>

Requestor\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.requestor\]

</td><td>

Provides access to submit a request for default record producers from a service portal and provides read and write access to the Primary \[x\_ &lt;company-code&gt;\_&lt;primary&gt;\] and Travel Request \[x\_ &lt;company-code&gt;\_&lt;travel\_request&gt;\] tables.

</td></tr><tr><td>

Fulfiller\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.fulfiller\]

</td><td>

Provides access to the fulfiller workspace and provides read and write access to the Primary \[x\_ &lt;company-code&gt;\_&lt;primary&gt;\], Travel Request \[x\_ &lt;company-code&gt;\_&lt;travel\_request&gt;\], and Fulfiller Task \[x\_ &lt;company-code&gt;\_&lt;fulfiller\_task&gt;\] tables.

</td></tr><tr><td>

admin\[x\_&lt;company-name&gt;\_ &lt;app\_name&gt;.admin\]

</td><td>

The System Administrator role. This role has access to all system features, functions, and data, regardless of security constraints.

</td></tr></tbody>
</table>
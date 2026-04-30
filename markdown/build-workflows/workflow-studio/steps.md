---
title: Workflow Studio steps
description: A step performs a single operation in an action. You can use Workflow Studio to add steps to a custom action.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Workflow Studio steps

A step performs a single operation in an action. You can use Workflow Studio to add steps to a custom action.

A step is a single reusable operation within an action. For example, the **Create Record** step allows action designers to specify the table and field values to use during record creation. Step configuration requires subject matter expertise with application tables, fields, and business logic. Application developers or IT generalists add steps to actions from the Workflow Studio action design environment. Workflow Studio provides a set of ServiceNow core steps to automate ServiceNow AI Platform processes. You can add application-specific steps by activating the associated spoke.

## Search steps

You can use the **Search steps** filter to find a step by name or spoke. As you enter data consisting of at least three characters, Workflow Studio displays a list of steps that match your search criteria.

![The Steps menu displays a text box labelled Search Actions.](../images/search-steps-text-box.png "Search Actions filter")

## ServiceNow data

ServiceNow Data steps are available to all actions regardless of the spokes installed. Use these steps to perform record operations on your data.

![Menu of ServiceNow Data steps by name and description.](../images/servicenow-data-steps-list.png "ServiceNow Data steps")

## Utilities

Utility steps enable you to build payloads, compress data, run scripts, and send notifications.

![Menu of utility steps by name and description](../images/utility-steps-list.png "Utilities steps")

## Integrations

Enable custom actions to integrate with external systems by activating Integration Hub, which adds integration steps to the Workflow Studio interface.

![Menu of integration steps by name and description](../images/integrations-steps-list.png "Integrations steps")

-   **[Ask for Approval step](../reference/ask-approval-action-designer.md)**  
Request approval for a record with an approval field. You can configure a rule set for an approval, rejection, or cancellation. If a due date is added to an approval, the approval is automatically approved, rejected, or canceled if the approvers have not responded by the designated time.
-   **[Create Record step](../reference/create-record-action-designer.md)**  
Creates a record on any table. You can dynamically add and configure fields for the record.
-   **[Create or Update Record step](../reference/create-update-record-step.md)**  
Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.
-   **[Create Task step](../reference/create-task-action-designer.md)**  
Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.
-   **[Delete Multiple Records step](../reference/delete-multiple-records-action-designer.md)**  
Look up and delete multiple existing records as a single operation. This Workflow Studio step removes the need to first look up a list of records and then delete each record in the list.
-   **[Delete Record step](../reference/delete-record-action-designer.md)**  
Deletes a record on any table.
-   **[Get Connection Info step](../reference/get-connection-info-action-designer.md)**  
Provide the connection and credential details from another step, such as a REST step, to other steps in your action.
-   **[Get Latest Response Text From Email step](../reference/get-latest-response-text-from-email-action-designer.md)**  
Provide the most recent reply or forward message in an e-mail chain to other steps in your action.
-   **[JDBC step](../reference/jdbc-step.md)**  
Create a reusable action to send SQL commands to a relational database.
-   **[JSON Builder step](../reference/json-build-step-action-designer.md)**  
Create a JSON payload to use in another step. Enter values or use data pills to produce a dynamic payload. This step supports several data types, including objects and arrays for nested structures.
-   **[Kafka Producer step](../reference/kafka-producer-action-designer.md)**  
Create an action that publishes events to a topic in your Kafka environment.
-   **[Log step](../reference/log-message-action-designer.md)**  
Logs a message in the Workflow Studio log table sys\_flow\_log.
-   **[Look Up Record step](../reference/lookup-record-action-designer.md)**  
Look up a record from any table based on defined conditions.
-   **[Look Up Records step](../reference/lookup-records-action-designer.md)**  
Look up multiple records on any table using defined conditions.
-   **[Notification step](../reference/trigger-notification-action-designer.md)**  
Trigger a notification as a step within an action by selecting a record \(such as an incident, change request, problem, or user record\) to trigger a notification and defining the associated notification.
-   **[Payload Builder step](../reference/payload-build-step-action-designer.md)**  
Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.
-   **[PowerShell step](../reference/powershell-step-action-designer.md)**  
Run PowerShell scripts on remote machines from your ServiceNow instance through a MID Server.
-   **[REST step](../reference/rest-request-action-designer.md)**  
Send an outbound REST web service request to an external system.
-   **[Script step](../reference/javascript-step-action-designer.md)**  
Add custom JavaScript to execute within a reusable action. While most core actions and steps fit common use cases, you can build a Script step to execute behavior not satisfied by the core steps.
-   **[Send Email step](../reference/send-email-action.md)**  
Send an email to specified users or groups as an action in a flow.
-   **[SFTP step](../reference/sftp-step.md)**  
Create a reusable action to manage files and directories on an SFTP server and to move files from one SFTP server to another.
-   **[SSH step](../reference/ssh-step-action-designer.md)**  
The SSH step executes SSH commands on an external \*nix system through a ServiceNow® MID Server. The step also stores scripts and commands for the \*nix systems.
-   **[SOAP step](../reference/soap-step-action-designer.md)**  
Enable action designers to send outbound SOAP web service requests to external systems.
-   **[Update Multiple Records step](../reference/update-multiple-records-action-designer.md)**  
Look up and update multiple records as a single step. Using this step removes the need to separately look up a list of records and then process the list with a Script step. Set field values with a template or add and configure them using data pills.
-   **[Update Record step](../reference/update-record-action-designer.md)**  
Update an existing record in a table. You can dynamically add and configure fields for the record, or use a template to set field values.
-   **[Wait For Condition step](../reference/wait-for-condition-action-designer.md)**  
Pause a flow until record values match a specific set of conditions.
-   **[ZIP step](../reference/zip-step.md)**  
Manage the attachments in a record by performing archive operations such as zip and unzip. You can also view the details of a zipped file.

**Parent Topic:**[Flows, subflows, and actions reference](../reference/flow-designer-reference.md)


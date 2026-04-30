---
title: Workflow Studio actions
description: Actions can be added to any flow, enabling process analysts to automate ServiceNow AI Platform features without having to write code.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Workflow Studio actions

Actions can be added to any flow, enabling process analysts to automate ServiceNow AI Platform features without having to write code.

An action is a reusable operation that enables process analysts to automate ServiceNow AI Platform features without having to write code. For example, the **Create Record** action allows process analysts to generate records in a particular table with particular values when certain conditions occur. ServiceNow core actions like Create Record require some familiarity with ServiceNow AI Platform tables and fields. Action designers can create application-specific actions to pre-set configuration details. For example, creating a Create Incident Task action ensures that the process analyst uses the correct table and field configuration each time the action is used. You can add application-specific actions by activating the associated spoke.

In Workflow Studio, a process analyst adds actions to a flow and defines the configuration options.

## Search actions

You can use the **Search Actions** filter to find an action by name or spoke. As you enter data, Workflow Studio displays a list of actions and spokes that match your search criteria.

![The Action menu displays a text box labelled Search Actions.](../images/search-actions-text-box.png "Search Actions filter")

## Most Recent

You can use the **Most Recent** option to display a list of the actions you recently selected. Each action displays the action name and the spoke to which it belongs underneath the name. You can use the information icon to see more information about the action such as its description, inputs, and outputs.

![The Most Recent option displays a list of recently used actions such as the Look Up record action in the ServiceNow Core spoke.](../images/most-recent-actions-list.png "Most Recent actions")

## Popular

You can use the **Popular** option to display a list of actions that your organization frequently uses. The system runs a scheduled job every seven days to generate the list of popular actions.

## Installed spokes

Workflow Studio displays actions for each installed spoke. You can select a spoke name to see a list of available actions for the spoke. All instances have a ServiceNow Core spoke.

A ServiceNow core action is an action available to any flow regardless of the spokes installed. ServiceNow core actions cannot be viewed or edited from the Workflow Studio flow design environment. For example, the **Ask for Approval** action is a ServiceNow core action that allows process analysts to use ServiceNow AI Platform approvals. Workflow Studio provides a set of ServiceNow core actions to automate ServiceNow AI Platform processes. You can add application-specific actions by activating the associated spoke.

You can find any custom actions you created in the spoke to which they belong. Alternatively, use the Search Actions filter to search for actions by name.

-   **[Add Worknote Link to Context action](../reference/add-worknote-link.md)**  
Add a journal field entry containing a link to the current flow context record. Use the link to view the flow execution details of the current flow. You can add a flow context link to any record that has a journal field.
-   **[Ask for Approval action](../reference/ask-approval-flow-designer.md)**  
Request approval for a record with an approval field. You can configure a rule set for an approval, rejection, or cancellation. If a due date is added to an approval, the approval is automatically approved, rejected, or canceled if the approvers have not responded by the designated time.
-   **[Associate Record to Email action](../reference/associate-to-email-action.md)**  
Associate a record with an Email \[sys\_email\] record so that you can track which record is affected by the email.
-   **[Create Catalog Task action](../reference/create-catalog-task-flow-designer.md)**  
Creates a record in the Catalog Task \[sc\_task\] table associated to a requested item in the Requested Items \[sc\_req\_item\] table. Adds the catalog task record as data to be used in the flow.
-   **[Create Flow Data action](../reference/create-flow-data-flow-designer.md)**  
Collect data from agents interacting with a Workspace playbook. Use this data to create reusable activities for process owners using Playbooks.
-   **[Create Record action](../reference/create-record-flow-designer.md)**  
Creates a record on any table. You can dynamically add and configure fields for the record.
-   **[Create or Update Record action](../reference/create-update-record-designer.md)**  
Create or update a record in a ServiceNow table using a single operation. Update a record that exists, or create a record using the values provided.
-   **[Create Task action](../reference/create-task-flow-designer.md)**  
Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.
-   **[Copy Attachment action](../reference/copy-attachment-flow-designer.md)**  
Copies an attachment from the Attachments \[sys\_attachment\] table to a target record.
-   **[Delete Attachment action](../reference/delete-attachment-flow-designer.md)**  
Removes one or all attachments associated with a record and deletes the attachment record from the Attachments \[sys\_attachment\] table.
-   **[Delete Record action](../reference/delete-record-flow-designer.md)**  
Deletes a record on any table.
-   **[Fire Event action](../reference/fire-event-action.md)**  
Create a system event record in the Event \[sysevent\] table to be processed by a scheduled event handler. Pass event parameters using flow data.
-   **[Get Attachments on Record action](../reference/get-attachments-rec.md)**  
Access the list and count of the attachments associated with the provided source record as data pills in a flow. Use flow logic or scripting to process each attachment in the list of the attachments that the action returns.
-   **[Get Catalog Variables action](../reference/get-cat-variables-flow-designer.md)**  
Select variables from multiple template catalog items and variable sets using the Get Catalog Variables action.
-   **[Get Email Header action](../reference/get-header-action.md)**  
Access an email header value as a data pill in a flow.
-   **[Get Latest Response Text From Email action](../reference/get-latest-response-text-from-email-flow-designer.md)**  
Provide the most recent reply or forward message in an e-mail chain to other actions in your flow.
-   **[Log action](../reference/log-message-flow-designer.md)**  
Logs a message in the Workflow Studio log table sys\_flow\_log.
-   **[Look Up Attachment action](../reference/lookup-attachment-flow-designer.md)**  
Looks up an attachment associated with a record and returns the Attachment Sys ID as a data pill.
-   **[Look up email attachments action](../reference/lookup-email-attachment.md)**  
Look up files that are attached to an email so that you can perform an action on the files.
-   **[Look Up Record action](../reference/lookup-record-flow-designer.md)**  
Look up a record from any table based on defined conditions.
-   **[Look Up Records action](../reference/lookup-records-flow-designer.md)**  
Look up multiple records on any table using defined conditions.
-   **[Move Attachment action](../reference/move-attachment.md)**  
Associates a record from the Attachment \[sys\_attachment\] table with a target record. Removes the attachment from any other associated records.
-   **[Move Email Attachments to Record action](../reference/move-email-attachments-action.md)**  
Move attachments from an email to a record so that the files are available to your users when they view the record.
-   **[Record Producer action](../reference/record-producer-flow-designer.md)**  
 Create a Task record from a Record Producer Catalog Item \[sc\_cat\_item\]. The Task record inherits values from the catalog item's variable values.
-   **[Send Email action](../reference/send-email-flow-designer.md)**  
Send an email to specified users or groups as an action in a flow.
-   **[Send Notification action](../reference/send-notification-action.md)**  
Send an email notification to predefined recipients with predefined content. Select or create a Notification \[sysevent\_email\_action\] record to configure the email notification.
-   **[Send SMS action](../reference/send-sms-action.md)**  
Send an email-based SMS text message to specified users or groups using your instance email server. Recipients must have an SMS device configured to receive the message.
-   **[SLA Percentage Timer action](../reference/sla-percentage-timer-action.md)**  
Identify when a task SLA record reaches a specific percentage value and perform other actions or flow logic that is based on the SLA percentage. For example, send a notification when an SLA percentage timer completes.
-   **[Submit Catalog Item Request action](../reference/submit-catalog-item-request-flow-designer.md)**  
Create a requested item \[sc\_req\_item\] on a Service Catalog Request \[sc\_request\].
-   **[Update Multiple Records action](../reference/update-multiple-records-flow-designer.md)**  
Look up and update multiple records as a single action. Using this action removes the need to separately look up a list of records and then process the list with For Each flow logic. Set field values with a template or add and configure them using data pills.
-   **[Update Record action](../reference/update-record-flow-designer.md)**  
Update an existing record in a table. You can dynamically add and configure fields for the record.
-   **[Wait For Condition action](../reference/wait-for-condition-flow-designer.md)**  
Pause a flow until record values match a specific set of conditions.

**Parent Topic:**[Flows, subflows, and actions reference](../reference/flow-designer-reference.md)


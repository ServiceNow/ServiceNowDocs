---
title: Configuring customer service case types
description: Configure case types to handle different types of customer issues. A case type identifies the processes and the data needed to resolve a specific type of issue.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configuring customer service case types

Configure case types to handle different types of customer issues. A case type identifies the processes and the data needed to resolve a specific type of issue.

## Before you begin

Role required: admin

## About this task

For each case type, you create a table that extends the Case table and configure a number of items, such as business rules and client scripts, that drive customer issues of this type from creation to resolution. When creating cases, agents can select the case type that corresponds to the customer issue.

There are a sequence of tasks that enable you to configure case types for Customer Service Management. To configure Proactive Customer Service Operations, use the Customer Service guided setup. The guided setup takes you through the entire setup and configuration process.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, click **Get Started**

3.  In the Case Types category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Case Types

</td><td>

The first step in creating a case type is to create a table for the case type that extends the Case table \(sn\_customerservice\_case\). **Note:** This table should be created in a scope other than global.

 You can create a table for the case type using one of these methods:

-   Guided Application Creator
-   Platform table creation feature \(navigate to **System Definition** &gt; **Table** and click **New**\)
The extended table for the case type inherits most of the functionality of the Case table.

</td></tr><tr><td>

Set Up View Rules

</td><td>

View rules determine the form views that are available to users. Create view rules that determine the conditions for when the system displays the Case Type table in a specified view.

</td></tr><tr><td>

Set Up States for State Flows

</td><td>

State flows enable you to customize transitions from one state to another in tables derived from the Task \[task\] table, including the Case \[sn\_customerservice\_case\] table and tables extended from Case. You can configure the system to perform work during transitions to specific states. Create choice records for each of the states to be used in state flows for the case type. When creating your desired states, set the **Table** field to the table for the case type and the **Element** field to State.

</td></tr><tr><td>

Set Up UI Policies

</td><td>

UI policies dynamically change the behavior of information on a form, such as setting a field to read-only or making a field mandatory. The case type inherits the following UI policies from the Case table:-   Show or hide major case information section
-   Make Partner Contact Read only If Partner is empty
You can configure additional UI policies for the Case Type form.

</td></tr><tr><td>

Set Up Client Scripts

</td><td>

Client scripts allow the system to run JavaScript on the client when client-based events occur, such as when a form loads or when a field changes value. The case type inherits the following client scripts from the Case table: -   Empty Partner Contact on Partner Change
-   Empty Case Form on Account Change
-   Hide Request Related List
-   Hide SM section and list if no plugin
-   Hide Related Records Section
You can configure additional client scripts for the case type.

</td></tr><tr><td>

Set Up Business Rules

</td><td>

A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried. Use business rules to accomplish tasks like automatically changing values in form fields when certain conditions are met, or to create events for email notifications and script actions. You can set up the desired business rules for the Case Type table.

</td></tr><tr><td>

Set Up Case Type UI Actions

</td><td>

UI actions include the buttons, links, and context menu items that appear on lists and forms. A case type inherits the UI actions from the Case table. You have the following options when setting up UI actions for a case type:

-   Create new UI actions for the case type. If you create a new UI action, select the Case Type table in the **Table** field on the UI Action form.
-   Use any of the inherited case UI actions.
-   Use a combination of the two.
You can also block any inherited case UI actions that you do not want. To block an action, update the **CSUIActionsimpl** script include.

</td></tr><tr><td>

[Enable the **Create Case** UI action for case type selection](config-csm-config-ws-ui-action.md)

</td><td>

This procedure adds the **Create Case** UI action to records in the configured table. Selecting this UI action displays the [case type selector](../concept/csm-case-type-select-modals.md).

 **Note:** For CSM Configurable Workspace, the **Create Case** UI action for case type selection is disabled out of box.

</td></tr><tr><td>

Set Up Case Types

</td><td>

Register a newly created case type by creating a case type definition record. This record is stored in the Case Type table \(sn\_case\_type\) and includes the following information:-   The name of the case type
-   The table created for the case type
-   An optional category
-   An optional subtype
-   A short description
-   A field for setting the case type to active
The Case Type table extends the Application File table \(sys\_metadata\). This table includes a **Domain** column that customers can use to add their own logic. To create a case type definition record, navigate to **Customer Service** &gt; **Manage Case Types** and click **New**.

 After creating and saving the case type definition record, you can configure the following process information for the case type using the related lists on the Case Type form:

-   State flows
-   Special handling notes
-   SLAs
-   Email templates
-   Quick messages
-   Reports
For more information, see [Manage customer service case types](../concept/manage-csm-case-types.md).

**Note:** These related lists only display information for the new case type. They do not include information for the base case.

</td></tr><tr><td>

Set Up Notifications

</td><td>

Notifications keep users informed about different activities and events. You can determine the conditions when a notification appears by creating a record in the Notification table.

</td></tr><tr><td>

Set Up Roles

</td><td>

Create one or more roles to control access to the case type features and capabilities. Then grant these roles access to the desired applications and modules. For agents to work on a case type, configure the case type role to contain the sn\_customerservice\_agent role.

</td></tr><tr><td>

Set Up ACLs

</td><td>

Use Access Control List rules \(ACLs\) to restrict access to data. These rules require users to pass a set of requirements before they can interact with data. For external customers to see a case type, add ACLs that provide read or create access for external users.

</td></tr><tr><td>

Set Up Case Type Selection Conditions

</td><td>

When creating a case of a specific type, an agent clicks **Create Case** and then selects from a list of available case types. The system presents the case types that have been configured for the agent's role. To set up case type selection conditions, use Flow Designer to configure the **Get Case Types** flow and modify the conditions that determine visibility for a case type.

 There are two different implementations of the **Create Case** UI action:

 -   The Customer Service plugin provides a **Create Case** UI action that agents can use as follows:
    -   To create a base case.
    -   To create a case for one specific case type. For example, if your organization always creates the same type of case and you have created only one extension of the Case table, you can modify this UI action to create a case of that specific case type.
-   The Customer Service Case Types plugin also provides a **Create Case** UI action that agents can use to create a case based on a selected case type. After clicking this UI action to create a case, the agent selects the desired case type from a list of multiple available case types.
 **Note:** It is recommended that you configure one of the **Create Case** UI actions but not both to avoid confusion.

</td></tr><tr><td>

Set Up Record Producers

</td><td>

A record producer is a specific type of catalog item that enables users to create task-based records, such as case records, from the service catalog. Create a record producer that exposes the new case type on the Customer Service Portal.

</td></tr><tr><td>

Set Up Case Digest for Case Types

</td><td>

The case digest feature enables agents to proactively communicate with customers and internal stakeholders about cases. While a case is in progress, agents can send periodic case summaries that describe actions taken, next steps, and other case-related information. When the work on a case has been completed, agents can create a post case review that includes information such as the root cause, mitigation plan, and preventive actions.**Note:** Using case types with the case digest feature requires the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) and the Case Digests plugin \(com.sn\_csm\_case\_digest\).

 Cases that are created from a selected case type can use Case Action Summaries and Post Case Reviews. To create the mapping that identifies the case type fields that are copied to Post Case Review and Case Action Summary records:

-   Create a configuration for the desired case type. Navigate to **Case Digests** &gt; **Configuration** and click **New**.
-   Create new records in the CSM Table Map table \(csm\_table\_map\) to map the **Send Case Action Summary** and **Create Post Case Review** UI actions.
 The Case Digests related list on the Case Type form shows the case action summaries and post case review configurations for a case type.

</td></tr><tr><td>

Set Up Contextual Search for Case Types

</td><td>

Navigate to **Contextual Search** &gt; **Table Configuration** and create a table configuration record to add contextual search to the case type. In this record, configure the **Table** field as the case type and the **Search Context** field as Case Knowledge Base Search.

</td></tr><tr><td>

Set Up Agent Workspace for Case Types

</td><td>

To configure Agent Workspace differently for each case type, follow the Agent Workspace Guided Setup. You can configure the following features specific to each case type:-   Workspace lists
-   Notifications
-   Highlighted values
-   Ribbon settings
-   Form headers
-   Action assignments


</td></tr><tr><td>

Set Up Portal View for Case Types

</td><td>

Configure the fields that a customer can see when they view a case on the Customer or Consumer Service Portals. Create a new record to configure the fields for each case type.For more information about the Ticket Configuration form, see [Configure the standard ticket page](https://www.servicenow.com/docs/access?context=configure-st-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>4.  To perform a task, click **Configure**.

    This button opens the page in your instance where the configuration is completed.


**Related topics**  


[Enable the case type single select property](enable-case-type-single-select-prop.md)

[Create a configuration for case type single-select](create-case-type-single-selection.md)


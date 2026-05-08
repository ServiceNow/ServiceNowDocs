---
title: SAP Concur Spoke
description: The SAP Concur spoke is built by Bristlecone, Inc. Manage expenses, payments, purchases, users, travel, and so on in the SAP Concur account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP Concur Spoke

The SAP Concur spoke is built by Bristlecone, Inc. Manage expenses, payments, purchases, users, travel, and so on in the SAP Concur account from your ServiceNow instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for SAP Concur API versions v3.0 and v4.0, but may be compatible with later versions.

## Spoke version

SAP Concur spoke v2.3.2 is the latest version.

## Spoke requirements

-   SAP Concur API user with these roles:

    -   Travel Wizard User
    -   Expense User
    -   Expense Approver
    -   Authorised Support Contact
    -   Invoice User
    ![SAP Concur API user roles](../image/sap-concur-user-roles.png)

-   SAP Concur API user with these Expense API and Invoice User permissions.

    ![Expense API permissions](../image/sap-concur-expense-prms.png)

    ![Invoice API permissions](../image/sap-concur-invoice-prms.png)

-   Contact SAP Concur Implementation team to obtain values of Client ID, Client Secret, Company ID, and Company Request Token, and define the scope of the client application.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Remote Tables \(com.glide.script.vtable\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SAP Concur spoke provides a sample flow, Get All Modified Expense Reports to demonstrate retrieving the expense reports modified within 24 hours of the provided Expense Report Last Modified Date. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The SAP Concur spoke provides a sample subflow, Get Expense Report Workflow Step ID to demonstrate retrieving the Workflow Step ID of an expense report on the basis of whether the given expense report is submitted or not. The output Workflow Step ID is required to run the Execute Workflow Action for Expense Report action. To customize the sample subflow, copy it to the required application scope.

## Spoke actions

The SAP Concur spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_szt_jcd_h4b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expense Configuration Management

</td><td>

Get Expense Group Configurations

</td><td>

Retrieves all the expense group configuration for the specified user.

</td></tr><tr><td rowspan="6">

Expense Entry Management

</td><td>

Create Expense Entry

</td><td>

Creates a new expense entry for the specified user.

</td></tr><tr><td>

Delete Expense Entry

</td><td>

Deletes the specified expense entry.

</td></tr><tr><td>

Get Expense Entry Details

</td><td>

Retrieves details of the specified expense entry.

</td></tr><tr><td>

Look up Expense Entries

</td><td>

Retrieves all expense entries owned by the user.

</td></tr><tr><td>

Look up Expense Itemizations Stream

</td><td>

Retrieves all expense itemizations owned by the user.

</td></tr><tr><td>

Update Expense Entry

</td><td>

Updates details of the specified expense entry.

</td></tr><tr><td rowspan="8">

Expense Report Management

</td><td>

Create Expense Report

</td><td>

Creates an expense report with the supplied data.

</td></tr><tr><td>

Execute Workflow Action for Expense Report

</td><td>

Executes a workflow action for an expense report using it's workflow step ID.**Note:** One of the action inputs is Workflow Step ID. Use the default subflow, Get Expense Report Workflow Step ID, to obtain the required Workflow Step ID value.

</td></tr><tr><td>

Get Expense Report Details

</td><td>

Retrieves details of the specified expense report.

</td></tr><tr><td>

Look up Comments

</td><td>

Retrieves the comments from the specified report header and from the specific expense within an expense report.

</td></tr><tr><td>

Look up Expense Reports

</td><td>

Retrieves all expense reports owned by the user, based on the search criteria.

</td></tr><tr><td>

Look up Expense Reports After Last Modified Date

</td><td>

Retrieves the reports modified within 24 hours after the specified Report Last Modified Date.

</td></tr><tr><td>

Submit Expense Report

</td><td>

Submits an expense report for the specified report.

</td></tr><tr><td>

Update Expense Report

</td><td>

Updates details of the expense report for the specified report.

</td></tr><tr><td>

Itinerary Management

</td><td>

Look up Itinerary by Trip ID

</td><td>

Retrieves information about the required trip.

</td></tr><tr><td rowspan="3">

Payment Request Management

</td><td>

Create Payment Request

</td><td>

Creates a payment request with all relevant details, including line items and associated allocations.

</td></tr><tr><td>

Get Payment Request Details

</td><td>

Retrieves details such as Payment Request Header, Payment Request Line Item and Payment Request Allocation, for the specified payment request.

</td></tr><tr><td>

Update Payment Request

</td><td>

Updates details of the specified payment request such as line items and associated allocations.

</td></tr><tr><td rowspan="3">

Purchase Order Management

</td><td>

Create Purchase Order

</td><td>

Creates a purchase order in SAP Concur.

</td></tr><tr><td>

Get Purchase Order Details

</td><td>

Retrieves information about the specified purchase order.

</td></tr><tr><td>

Update Purchase Order

</td><td>

Updates details of the specified purchase order.

</td></tr><tr><td rowspan="3">

Receipt Management

</td><td>

Get Expense Entry Receipt Image URL

</td><td>

Retrieves expense entry receipt image URL of the specified expense entry.

</td></tr><tr><td>

Get Expense Report Receipt Image URL

</td><td>

Retrieves expense report receipt image URL of the specified expense report.

</td></tr><tr><td>

Post Expense Report Receipt Image

</td><td>

Creates a receipt image for the specified expense report.

</td></tr><tr><td rowspan="3">

User Management

</td><td>

Get User Details

</td><td>

Retrieves details of the specified user.**Note:** Details of only the expense users are retrieved using this action.

</td></tr><tr><td>

Look up Users

</td><td>

Retrieves details of the required user, based on the provided search criteria.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves details of all users in a given company. The filter operation can also be used to retrieve the required user’s identity information.

</td></tr><tr><td>

Webhook Management

</td><td>

Create Webhook Subscription

</td><td>

Creates subscriptions in SAP Concur for the selected topic with provided endpoint.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|SAP Concur payment request management AI agent|Manages and retrieves payment request details.|
|SAP Concur expense report management AI agent|Manages and submits expense reports, retrieves detailed information, and manages comments|
|SAP Concur purchase order management AI agent|Manages purchase order operations and retrieves the required purchase order details.|
|SAP Concur expense entry management AI agent|Manages and retrieves expense entry details.|
|SAP Concur receipt management AI agent|Manages receipts by enabling users to perform tasks such as uploading receipt images to expense reports, retrieving URLs for expense entry receipt images, and obtaining URLs for expense report receipt images.|
|SAP Concur itinerary management AI agent|Manages itineraries and expenses, and retrieves the required itinerary information.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see Modify an agentic workflow.

Available sample agentic workflow includes:

<table id="table_chb_l90v_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Get Purchase Order and Payment Request Details

</td><td>

Retrieves purchase order information and the corresponding payment request details for review and processing.

</td><td>

-   SAP Concur payment request management AI agent
-   SAP Concur purchase order management AI agent

</td><td>

No**Note:** To activate the workflow, see Activate an agentic workflow template.

</td></tr><tr><td>

Upload Expense Receipt Image and Submit Expense Report

</td><td>

Retrieves recently updated expense reports, uploads a receipt image to an expense report, and submits the expense report for approval.

</td><td>

-   SAP Concur receipt management AI agent
-   SAP Concur expense report management AI agent

</td><td>

No**Note:** To activate the workflow, see Activate an agentic workflow template.

</td></tr></tbody>
</table>## Spoke module

The SAP Concur spoke adds the SAP Concur Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|SAP Concur Expense Entries|View details of the expense entries. After you [Set up the SAP Concur spoke](../task/setup-sapconcur-spk.md) and map the users in the SAP Concur User Mappings module, the system retrieves details of the expense entries and populates in this module.|
|SAP Concur Expense Report Details|View the expense report details. Configure the default flow Get All Modified Expense Reports as per your requirement to retrieve and populate data.|
|SAP Concur Expense Report Last Modified Date|View the latest timestamp or last modified date on which the flow was executed or reports were filtered. Configure the default flow Get All Modified Expense Reports as per your requirement to retrieve and populate data.|
|SAP Concur Expense Reports|View the expense reports. After you set up the [Set up the SAP Concur spoke](../task/setup-sapconcur-spk.md) and map the users, the system retrieves details of the expense reports and populates in this module.|
|SAP Concur User Mappings|Map ServiceNow users to their corresponding User IDs in SAP Concur.|

## Spoke user roles

The SAP Concur spoke provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
|sn\_sap\_concur\_spok.SAP Concur Spoke Admin|Users with this role can perform all operations.|
|sn\_sap\_concur\_spok.SAP Concur Expense Entries User|Users with this role can only view the data available in the SAP Concur Expense Entries module.|
|sn\_sap\_concur\_spok.SAP Concur Expense Reports User|Users with this role can only view the data available in the SAP Concur Expense Reports module.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the SAP Concur spoke](../task/setup-sapconcur-spk.md).


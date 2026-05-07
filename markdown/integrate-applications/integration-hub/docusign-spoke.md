---
title: Docusign eSignature Spoke
description: Automate the process of sending a document to an individual or list of recipients for digital signature using Docusign eSignature. For example, automate employee onboarding and offboarding, or send non-disclosure agreements, legal agreements, and statements of work. Use ServiceNow data in document templates and enable users to upload documents for signature as needed.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Docusign eSignature Spoke

Automate the process of sending a document to an individual or list of recipients for digital signature using Docusign eSignature. For example, automate employee onboarding and offboarding, or send non-disclosure agreements, legal agreements, and statements of work. Use ServiceNow data in document templates and enable users to upload documents for signature as needed.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Docusign eSignature spoke v4.3.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Compatible versions

This spoke was built for Docusign eSignature API version v2 or v2.1, but may be compatible with later versions.

## Key features

Docusign eSignature spoke enables a flow designer to:

-   Automate the process of sending a document from a ServiceNow attachment or Docusign eSignature template to an individual or recipient list for digital signature.
-   Discover and synchronize Docusign eSignature accounts and templates in ServiceNow.
    -   Retrieve a list of accounts and associated templates from Docusign eSignature and then insert or update them as records in the Accounts \[sn\_docusign\_spoke\_accounts\] and Templates \[sn\_docusign\_spoke\_docusign\_templates\] tables using the Get Accounts subflow.
    -   Retrieve templates associated with a specified Docusign eSignature account and then insert or update them as records in the Templates \[sn\_docusign\_spoke\_docusign\_templates\] table using the Get Templates Per Account subflow.
-   Copy and customize sample flows for sending templates and on-demand document requests.
-   Pause a flow until a document is signed. A scripted REST API webhook waits for the recipient to sign the document.
-   Use values from a signed document in a flow.
-   Attach a completed Docusign eSignature document to a ServiceNow record for auditing purposes.
-   Manage envelopes and users.

## Spoke requirements

-   Docusign eSignature account
-   Docusign eSignature administrator credentials
-   Docusign eSignature application configured to integrate with ServiceNow
-   Docusign eSignature application details such as client ID, integrator key, secret keys, and RSA keypairs
-   ServiceNow IntegrationHub subscription

    **Note:** Ensure that you have activated the Flow Designer support for the Service Catalog \(com.glideapp.servicecatalog.flow\_designer\) plugin.


See the [Docusign Developer Center](https://developers.docusign.com/) documentation for instructions on creating and configuring custom applications.

## Spoke flows

The Docusign eSignature spoke provides sample flows to demonstrate automating Docusign tasks. Use Docusign eSignature spoke actions to automate any tasks desired by your organization. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Send a Document for Digital Signature|Sends a document to Docusign for a digital signature when a Service Catalog request is created by the **Send a Document for Digital Signature** item. Before using this flow, activate the **Send a Document for Digital Signature** catalog item.|
|Send employment offer to candidate using Docusign template|Sends a Docusign envelope to a user using a template. For example, use this flow to send a job offer to a candidate. Before using this flow, activate the **Demonstrate Template - Send Job Offer to Candidate** catalog item.|

The Docusign eSignature spoke adds catalog items for use with the Docusign eSignature spoke sample flows. Before triggering a Docusign eSignature spoke sample flow, activate these catalog items.

|Catalog item|Description|
|------------|-----------|
|Send a Document for Digital Signature|Sends a document for digital signature in Docusign.|
|Demonstrate Template - Send Job Offer to Candidate|Sends a job offer using a Docusign template.|

## Spoke subflows

The Docusign eSignature spoke provides sample subflows to demonstrate automating Docusign tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Category|Subflow|Description|
|--------|-------|-----------|
|Envelope Management|Attach Docusign Envelope To ServiceNow Record|Attaches all the documents in an envelope to a ServiceNow record.|
|Get &amp; Set Docusign Field Data|Processes a list of catalog item variables and updates a draft envelope with each variable value.|
|User Management|Create User|Creates a user including the permission profile and group memberships.|
|Update User|Updates a user including the permission profile and group memberships.|
|Templates Management|Get Templates Per Account|Retrieves templates from a Docusign account and stores them in the Templates table.|
|Default|Docusign Webhook Sample Subflow|Retrieves the recipient details for the specified envelope.|
|Account Management|Get Accounts|Retrieves Docusign Accounts and Templates related to every account and store them in Accounts and Templates table respectively.|

## Spoke actions

The Docusign eSignature spoke provides actions to automate Docusign tasks when events occur in ServiceNow. Available actions include:

<table id="table_o4g_pc3_lfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Account Management

</td><td>

Look up Account Signature Providers

</td><td>

Retrieves a list of signature providers that the specified account can use.

</td></tr><tr><td>

Look up Accounts by Alias

</td><td>

Retrieves accounts associated with the spoke Connection and Credential alias record.

</td></tr><tr><td>

Look up Role ID

</td><td>

Retrieves the roles ID for the specified role name.

</td></tr><tr><td rowspan="12">

Bulk Envelopes Management

</td><td>

Create Bulk Send List

</td><td>

Creates a bulk send list.

</td></tr><tr><td>

Create Bulk Send Request

</td><td>

Creates a bulk send request based on an existing bulk send list using an envelope or template.

</td></tr><tr><td>

Create Bulk Send Test Request

</td><td>

Creates a bulk send test request for testing compatibility with the existing envelope or template.

</td></tr><tr><td>

Delete Bulk Send List

</td><td>

Deletes the specified bulk send list.

</td></tr><tr><td>

Look up Bulk Send Batch Envelopes Stream

</td><td>

Retrieves the envelopes from the specified bulk send batch.

</td></tr><tr><td>

Look up Bulk Send Batch Status

</td><td>

Retrieves the general status of the specified bulk send batch such as number of successes, number pending, number of errors and so on.

</td></tr><tr><td>

Look up Bulk Send Batches Stream

</td><td>

Retrieves the information of the bulk send batches.

</td></tr><tr><td>

Look up Bulk Send List

</td><td>

Retrieves the specified bulk send list.

</td></tr><tr><td>

Look up Bulk Send Lists

</td><td>

Retrieves a list of the bulk send lists.

</td></tr><tr><td>

Update Bulk Send Batch Action

</td><td>

Performs a bulk action \(resend, correct or void\) on the specified bulk send batch.

</td></tr><tr><td>

Update Bulk Send Batch Status

</td><td>

Updates the name of the specified bulk send batch.

</td></tr><tr><td>

Update Bulk Send List

</td><td>

Updates the specified bulk send list.

</td></tr><tr><td rowspan="2">

Document Signature

</td><td>

Look up Embedded Signing URL

</td><td>

Creates a signing URL that is embedded into an application. User can sign the document without leaving the application.**Note:** Signing URL is active for 300 seconds and can be sent to one recipient at a time.

</td></tr><tr><td>

Look up Embedded Signing URL Inline

</td><td>

Retrieves a URL which enables you to embed the recipient view of the on Docusign.

</td></tr><tr><td rowspan="6">

Document Management

</td><td>

Add Document to Envelope

</td><td>

Adds documents to envelope.

</td></tr><tr><td>

Attach Combined Document to ServiceNow Record

</td><td>

Attaches Docusign documents to a ServiceNow record.

</td></tr><tr><td>

Attach Docusign Document to ServiceNow Record

</td><td>

Retrieves a signed Docusign document and attaches it to a ServiceNow record.

</td></tr><tr><td>

Look up Document ID by Name

</td><td>

Retrieves the document ID from an envelope using the specified document name.

</td></tr><tr><td>

Look up Documents in an Envelope

</td><td>

Returns a list of documents with an ID and name in the given Docusign envelope.

</td></tr><tr><td>

Replace Document in an Envelope

</td><td>

Replaces documents to envelope.

</td></tr><tr><td rowspan="23">

Envelope Management

</td><td>

Add Recipient to Envelope

</td><td>

Adds the specified recipient to the specified envelope.**Note:**

-   Recipient ID used in this action is associated with the envelope and is different from the Recipient ID used in the Get All Template Fields action.
-   Administrator enters a numeric value for this Recipient ID.

</td></tr><tr><td>

Add Recipients to Envelope

</td><td>

Adds the specified recipients to the specified envelope.

</td></tr><tr><td>

Attach Docusign Certificate To ServiceNow Record

</td><td>

Attaches a Docusign certificate to a ServiceNow record.

</td></tr><tr><td>

Cancel Envelope

</td><td>

Cancels an in-process envelope.

</td></tr><tr><td>

Create Draft Envelope from Template

</td><td>

Creates a draft envelope from an existing Docusign template.

</td></tr><tr><td>

Create Envelope from Composite Template

</td><td>

Creates an envelope from an existing composite template.

</td></tr><tr><td>

Look up Field ID

</td><td>

Retrieves the ID of the specified field from the specified draft envelope.

</td></tr><tr><td>

Look up Field Value

</td><td>

Retrieves the value of the specified field from the specified envelope.

</td></tr><tr><td>

Look up Fields

</td><td>

Retrieves the list of fields associated to a document in a draft envelope.

</td></tr><tr><td>

Look up Recipient ID by Role Name

</td><td>

Retrieves the recipient ID of the specified role name from the specified envelope.

</td></tr><tr><td>

Look up Recipients in an Envelope

</td><td>

Returns a list of recipients with a Recipient ID and Role Name in the given Docusign envelope.

</td></tr><tr><td>

Remove Recipient from Envelope

</td><td>

Deletes a recipient from a Docusign envelope.

</td></tr><tr><td>

Send Adhoc Signature Request to User

</td><td>

Sends a Docusign document associated with the specified ServiceNow record to the specified recipient for signature.

</td></tr><tr><td>

Send Adhoc Signature Request To Users - Inline

</td><td>

Sends one or more uploaded documents from a ServiceNow record to multiple recipients.

</td></tr><tr><td>

Send Envelope

</td><td>

Sends an envelope to the specified recipients.**Note:** All recipient details must be provided before sending an envelope.

</td></tr><tr><td>

Resend Envelop

</td><td>

Send a reminder to recipients who are currently the pending signers.

</td></tr><tr><td>

Lock Envelop

</td><td>

Locks the specified envelope and sets the time until the lock expires to prevent other users or recipients from changing the envelope.

</td></tr><tr><td>

Unlock Envelope

</td><td>

Unlocks the specified locked envelope.

</td></tr><tr><td>

Set Field Value

</td><td>

Sets the value of the specified field in the specified draft envelope.

</td></tr><tr><td>

Set Field Values

</td><td>

Assigns the values of multiple fields associated to a document in a draft envelope.

</td></tr><tr><td>

Wait for Signature from Docusign

</td><td>

Pauses a flow until the specified document has been signed or rejected. Returns the status of the document to the flow for further processing.

</td></tr><tr><td>

Remove Recipient from Envelope

</td><td>

Deletes a recipient from an envelope. Prior to using this action, Create Draft Envelope from Template action should be used to generate a draft Envelope.

</td></tr><tr><td>

Upsert Recipients for Envelope

</td><td>

Updates or adds recipients to the envelope. If a recipient with the specified recipient ID already exists, their information will be updated; otherwise, a new recipient will be created with the provided details. Prior to using this action, Create Draft Envelope from Template action will be used to generate a draft Envelope.

</td></tr><tr><td rowspan="3">

Group Management

</td><td>

Add User To Group

</td><td>

Adds user from a group.

</td></tr><tr><td>

Look up Group ID

</td><td>

Retrieves a group ID for the specified role name.

</td></tr><tr><td>

Remove User From Group

</td><td>

Removes the specified user from a group.

</td></tr><tr><td rowspan="3">

Template Management

</td><td>

Look up Templates Per Account

</td><td>

Retrieves the templates associated with the specified Docusign account.

</td></tr><tr><td>

Look up Template Fields

</td><td>

Retrieves all fields in a template that is defined for a recipient.**Note:**

-   Recipient ID used in this action is associated with the template and is different from the Recipient ID used in the Add Recipient to Envelope action.
-   Value of the Recipient ID is a unique system-generated number.

</td></tr><tr><td>

Look up Template Recipients

</td><td>

Retrieves all recipients defined for a template.

</td></tr><tr><td rowspan="4">

User Management

</td><td>

Create User

</td><td>

Creates a Docusign user with the specified user details.

</td></tr><tr><td>

Look up User Detail

</td><td>

Retrieves details for a user.

</td></tr><tr><td>

Update User

</td><td>

Updates the specified user.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the specified Docusign user.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Docusign eSignature account management AI agent|Manages account management \(that is, looks up accounts by alias, retrieves role IDs and identifies account signature providers\) in Docusign.|
|Docusign eSignature envelope management AI agent|Manages envelope management \(that is, sendS signature requests, manages envelope statuses, and attaches DocuSign data to ServiceNow records\) in Docusign.|
|Docusign eSignature templates management AI agent|Manages template management \(that is, retrieves recipient details, accesses template fields, and fetches template names per account\) in Docusign.|
|Docusign eSignature bulk envelopes management AI agent|Manages bulk envelope management tasks \(that is, updates and looks up bulk send batch statuses, manages bulk send lists, create bulk send requests\) in Docusign.|
|Docusign eSignature user management AI agent|Manages user management \(that is, creates, updates, deletes, and retrieves user details\) in Docusign.|
|Docusign eSignature group management AI agent|Manages group management \(that is, looks up group IDs, adds users to groups, and removes users from groups\) in Docusign.|
|Docusign eSignature document management AI agent|Manages document management tasks \(that is, attaches documents, manages envelopes, and retrieves document details\) in Docusign.|
|Docusign eSignature document signature AI agent|Manages document signature tasks \(that is, looks up embedded signing URL, and looks up embedded signing URL inline\) in Docusign.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke module

The Docusign eSignature spoke adds a Docusign module to your ServiceNow instance. The Docusign eSignature spoke synchronizes and stores templates and envelopes in ServiceNow. The Docusign eSignature spoke includes these tables and records.

|Table/Record|Description|
|------------|-----------|
|Connection Aliases|The Docusign connection alias.|
|Scheduled Job|The Get Accounts &amp; Templates scheduled job that synchronizes templates and envelopes with your Docusign account.|
|Accounts|Docusign accounts synchronized with your ServiceNow instance. To synchronize accounts, see [Synchronize Docusign with ServiceNow](../task/sync-docusign-servicenow.md). The Get Accounts subflow retrieves a list of accounts and associated templates from Docusign and then inserts or updates them as records in the Accounts \[sn\_docusign\_spoke\_accounts\] and Templates \[sn\_docusign\_spoke\_docusign\_templates\] tables.|
|Templates|Docusign templates from synchronized Docusign accounts. The Get Templates Per Account subflow retrieves templates associated with a specified Docusign account and then inserts or updates them as records in the Templates \[sn\_docusign\_spoke\_docusign\_templates\] table.|
|Envelopes|Docusign envelopes from synchronized Docusign accounts. Records in the Envelopes table are updated only when webhook is configured for the Docusign account.|
|DocuSign Webhook Answer Subflows|List of webhook answer subflows.|

The Docusign eSignature spoke tables include these fields.

<table id="table_gbz_nyc_ygb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Accounts \[sn\_docusign\_spoke\_accounts\]

</td><td>

-   Account ID
-   Account Name
-   Description
-   Email
-   Alias
-   Display Name

</td></tr><tr><td>

Templates \[sn\_docusign\_spoke\_docusign\_templates\]

</td><td>

-   Account
-   Template ID
-   Name
-   Description
-   Last Modified
-   Display Name

</td></tr><tr><td>

Envelopes \[sn\_docusign\_spoke\_envelopes\]

</td><td>

-   Account
-   ID
-   Status
-   Signed Date
-   Declined Reason
-   Display name
-   Embedded Signing
-   Signed Date Time Zone
-   Template

</td></tr></tbody>
</table>## Spoke triggers

ServiceNow supports specific events on Docusign that create triggers. You must first configure a flow with a supported trigger definition. When an event, for example, a push request, occurs on the Docusign, it sends the payload via a webhook to the ServiceNow instance. After that, the flow that you configured is triggered at the ServiceNow instance to automate a workflow. The supported events are:

|Category|Trigger|Definition|
|--------|-------|----------|
|Envelope Management|Envelope Completed|Trigger is initiated when an envelope has been completed by all the recipients. Configure the flow to execute only when the specified trigger conditions are met.|
|Envelope Declined|Trigger is initiated when an envelope has been declined by one of the recipients. Configure the flow to execute only when the specified trigger conditions are met.|
|Envelope Deleted|Trigger is initiated when a sent envelope is deleted. Configure the flow to execute only when the specified trigger conditions are met.|
|Envelope Delivered|Trigger is initiated when all recipients have opened the envelope through the Docusign signing website. Configure the flow to execute only when the specified trigger conditions are met.|
|Envelope Sent|Trigger is initiated when an envelope is sent to recipient. Configure the flow to execute only when the specified trigger conditions are met.|
|Envelope Voided|Trigger is initiated when an envelope has been voided by the sender or has expired. Configure the flow to execute only when the specified trigger conditions are met.|
|Recipient Management|Recipient Completed|Trigger is initiated when the recipient has completed their actions for the envelope. Configure the flow to execute only when the specified trigger conditions are met.|
|Recipient Declined|Trigger is initiated when the recipient declines to sign the document\(s\) in the envelope. Configure the flow to execute only when the specified trigger conditions are met.|
|Recipient Delivered|Trigger is initiated when the recipient has viewed the document\(s\) in an envelope through the Docusign signing web site. Configure the flow to execute only when the specified trigger conditions are met.|
|Recipient Sent|Trigger is initiated when an email notification is sent to the recipient signifying that it is their turn to sign an envelope. Configure the flow to execute only when the specified trigger conditions are met.|

For information about setting up the triggers for the Docusign eSignature spoke, see [Set up triggers for the Docusign eSignature spoke](../task/setup-ext-triggers-docusign.md#). For more information about inbound integration, see [Conditional and event-driven inbound integration](../../integrationhub/concept/conditional-and-event-driven-inbound-integration.md).

## Docusign account requirements

The Docusign eSignature spoke requires configuring your Docusign account to generate an OAuth 2.0 JWT Bearer Grant token.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Docusign Connection &amp; Credential Alias record to authorize actions.

**Important:**

-   You can choose to set up the Docusign spoke using [authorization code grant](../task/setup-docusign-authorization-code.md#) or [JWT grant](../task/setup-docusign-jwt.md#).

    -   Use Authorization Code Grant if your integration uses a browser or client to make requests to a web server.
    -   Use JWT Grant if each user of your integration will use a single system account to log in.
    For more information about when to chose either of the setup methods, see [Choose OAuth Type](https://developers.docusign.com/platform/auth/choose/) in [Docusign Developer documentation](https://developers.docusign.com/).

-   Your company may have a Docusign account for each department that uses Docusign. To use multiple accounts with this spoke, create a child alias for each account. Also, ensure that you override the base alias with the child alias in your flows. At runtime, the system identifies the child alias associated with the account and sends the correct connection and credential information in the request.

    -   For more information about child alias and overriding the base alias, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    -   For information about setting up multiple accounts, see [Create child aliases for additional Docusign accounts](../task/create-aliases-docusign.md).
    If your company only has one account, you can use the default **Docusign** alias provided with the spoke and proceed to setting up the Docusign spoke using [authorization code grant](../task/setup-docusign-authorization-code.md#) or [JWT grant](../task/setup-docusign-jwt.md#).


## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Docusign alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


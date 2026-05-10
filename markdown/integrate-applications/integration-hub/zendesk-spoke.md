---
title: Zendesk Spoke
description: The Zendesk spoke provides actions to view and analyze meaningful usage data for Zendesk software subscriptions. Analyze usage for your Zendesk account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Zendesk Spoke

The Zendesk spoke provides actions to view and analyze meaningful usage data for Zendesk software subscriptions. Analyze usage for your Zendesk account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Zendesk spoke v1.8.0 is the latest version.

## Supported versions

This spoke was built for Zendesk version 11015, but may be compatible with later versions.

## Spoke requirements

Zendesk admin account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Zendesk spoke provides the Upsert Zendesk Tickets flow to check if a new ticket has been created in the Zendesk Ticket table or if an existing ticket has been updated, and accordingly synchronizes it in Zendesk. To customize a sample flow, copy it to a new application scope.

## Spoke subflows

The Zendesk spoke provides sample subflows to demonstrate automating tasks. To customize the sample subflow, copy it to a new application scope. Available subflows include:

|Subflow|Description|
|-------|-----------|
|Create Zendesk Webhook|Creates a webhook in Zendesk whene a request is received from the Webhook Registries \[sn\_zendesk\_spoke\_webhook\_registries\] table.|
|Process Zendesk Webhook|Inserts and updates records in the Zendesk Tickets table based on the changes happening in Zendesk.|
|Update Zendesk Webhook|Updates the webhook tokens and synchronizes them both in ServiceNow and Zendesk.|

## Spoke actions

The Zendesk spoke provides actions to automate Zendesk tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_dky_jyk_2qb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Activity Management

</td><td>

Look up Activities Stream

</td><td>

Retrieves details of the ticket activities. Ticket activities include assigning a ticket to the agent, increasing the priority of a ticket assigned to the agent, or adding a comment to a ticket assigned to the agent.

</td></tr><tr><td>

Look up Activity by ID

</td><td>

Retrieves details of the specified ticket activity. Activities include assigning a ticket to the agent, increasing the priority of a ticket assigned to the agent, or adding a comment to a ticket assigned to the agent.

</td></tr><tr><td rowspan="2">

Attachment Management

</td><td>

Look up Attachment by ID

</td><td>

Retrieves attachment details by value of the Attachment ID.

</td></tr><tr><td>

Upload Attachment

</td><td>

Uploads a file you want to attach.

</td></tr><tr><td rowspan="2">

Group Management

</td><td>

Look up Group by ID

</td><td>

Retrieves information about the specified group.

</td></tr><tr><td>

Look up Groups Stream

</td><td>

Retrieves the list of all groups within an account.

</td></tr><tr><td rowspan="2">

Organization Management

</td><td>

Look up Organization by ID

</td><td>

Retrieves information about the specified organization.

</td></tr><tr><td>

Look up Organizations Stream

</td><td>

Retrieves the list of all organizations.

</td></tr><tr><td rowspan="8">

Request Management

</td><td>

Create Request

</td><td>

Creates a request by setting one or more properties.

</td></tr><tr><td>

Look up Comment by ID

</td><td>

Retrieves the comment added to the request corresponding to the Request ID and the Comment ID.

</td></tr><tr><td>

Look up Comments by Request ID Stream

</td><td>

Retrieves the comments added to the request related to the Request ID that you sent through the input.

</td></tr><tr><td>

Look up Request by ID

</td><td>

Retrieves the request details by value of the Request ID.

</td></tr><tr><td>

Look up Requests by Organization ID Stream

</td><td>

Retrieves all the requests in an account corresponding to the Requester ID.

</td></tr><tr><td>

Look up Requests by Requester ID Stream

</td><td>

Retrieves all the requests in an account corresponding to the Requester ID.

</td></tr><tr><td>

Look up Requests Stream

</td><td>

Retrieves all the requests in an account based on the state of the request.

</td></tr><tr><td>

Update Request by ID

</td><td>

Updates the request with a comment or collaborators \(cc's\).

</td></tr><tr><td rowspan="2">

Role Management

</td><td>

Look up Custom Role by ID

</td><td>

Retrieves information about the specified custom role.

</td></tr><tr><td>

Look up Custom Roles

</td><td>

Retrieves the list of all custom roles within an enterprise account.

</td></tr><tr><td rowspan="2">

Search

</td><td>

Search Entities by Parameter Stream

</td><td>

Retrieves all tickets, requests, and users in an account related to the query.

</td></tr><tr><td>

Search Requests by Keyword Stream

</td><td>

Retrieves all requests in an account related to the search string.

</td></tr><tr><td rowspan="5">

Suspended Tickets Management

</td><td>

Delete Multiple Suspended Tickets by IDs

</td><td>

Deletes multiple suspended tickets. A list of suspended ticket IDs should be provided.

</td></tr><tr><td>

Delete Suspended Ticket by ID

</td><td>

Deletes a specific suspended ticket.

</td></tr><tr><td>

Look up Suspended Ticket by ID

</td><td>

Searches for a specific suspended ticket by its ID.

</td></tr><tr><td>

Look up Suspended Tickets Stream

</td><td>

Retrieves the details of suspended tickets.

</td></tr><tr><td>

Recover Suspended Ticket by ID

</td><td>

Recovers the details of the specified suspended ticket.

</td></tr><tr><td rowspan="6">

Ticket Audit

</td><td>

Look up Audit by ID

</td><td>

Retrieves the audit details of a ticket specific to an audit.

</td></tr><tr><td>

Look up Audit Log by ID

</td><td>

Retrieves the audit log details of a ticket specific to an audit.

</td></tr><tr><td>

Look up Audit Logs Stream

</td><td>

Retrieves the audit log displaying the various changes in a Zendesk account since the account creation.

</td></tr><tr><td>

Look up Audits Stream

</td><td>

Retrieves the list of audits for all the tickets.

</td></tr><tr><td>

Look up Ticket Audits Stream

</td><td>

Retrieves the audits for the specified ticket.

</td></tr><tr><td>

Update Audit as Private

</td><td>

Updates a comment from public to private for a ticket specific to an audit.

</td></tr><tr><td>

Ticket Comment Management

</td><td>

Look up Comments by Ticket ID Stream

</td><td>

Retrieves the comments added to the specified ticket.

</td></tr><tr><td rowspan="10">

Ticket Management

</td><td>

Create Multiple Tickets

</td><td>

Creates multiple tickets with the provided details, at a time.

</td></tr><tr><td>

Create Ticket

</td><td>

Creates a ticket in the Zendesk instance.

</td></tr><tr><td>

Create Ticket Async

</td><td>

Creates a ticket in the Zendesk instance. Ticket creation can sometimes take a while because of the complex business rules. Asynchronous creation enables you to get the response back quickly and queues a background job to do the actual work.

</td></tr><tr><td>

Look up Job Status by ID

</td><td>

Retrieves the status record created when a user starts a job.

</td></tr><tr><td>

Look up Multiple Tickets Stream

</td><td>

Retrieves details of multiple tickets.

</td></tr><tr><td>

Look up Ticket by ID

</td><td>

Retrieves details of the specified ticket.

</td></tr><tr><td>

Look up Tickets Stream

</td><td>

Retrieves the ticket properties.

</td></tr><tr><td>

Recover Multiple Suspended Tickets by IDs

</td><td>

Recovers the specified suspended tickets.

</td></tr><tr><td>

Update Multiple Tickets

</td><td>

Updates details of multiple tickets.

</td></tr><tr><td>

Update Ticket

</td><td>

Updates the specified properties of a ticket.

</td></tr><tr><td rowspan="4">

Ticket Metric Management

</td><td>

Look up Metric by ID

</td><td>

Retrieves a specific metric, or the required metrics of a ticket.

</td></tr><tr><td>

Look up Metrics by Ticket ID

</td><td>

Retrieves the metric details of the specified ticket.

</td></tr><tr><td>

Look up Ticket Metric Events Stream

</td><td>

Retrieves the ticket metric events that occurred on or after the start time.

</td></tr><tr><td>

Look up Tickets Metric Stream

</td><td>

Retrieves a list of tickets, along with their metrics.

</td></tr><tr><td rowspan="7">

User Management

</td><td id="delete-user">

Delete User

</td><td>

Deletes the specified user and associated records from an account. Deleted users cannot be recovered. To comply with General Data Protection Regulation \(GDPR\), you must use the additional [Permanently Delete User](zendesk-spoke.md#permanently-delete-user) action to permanently delete the user after deleting the user.

</td></tr><tr><td>

Create User

</td><td>

Creates a user with the specified details.

</td></tr><tr><td>

Look up Deleted Users Stream

</td><td>

Retrieves the list of all deleted users, including permanently deleted users, within an account.

</td></tr><tr><td>

Look up User by ID

</td><td>

Retrieves the specified user’s details.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves the list of all users within an account.

</td></tr><tr><td id="permanently-delete-user">

Permanently Delete User

</td><td>

Permanently deletes the specified user from an account.Before you can permanently delete the user, you must first delete the user using the [Delete User](zendesk-spoke.md#delete-user) action.

</td></tr><tr><td>

Update User

</td><td>

Modifies details about the specified user.

</td></tr><tr><td rowspan="7">

Webhook Management

</td><td>

Create Webhook

</td><td>

Creates a webhook with the provided details.

</td></tr><tr><td>

Delete Webhook

</td><td>

Deletes the specified webhook.

</td></tr><tr><td>

Look up Webhook Details by ID

</td><td>

Retrieves details of the specified webhook.

</td></tr><tr><td>

Look up Webhook Signing Secret by ID

</td><td>

Retrieves signing secret of the required webhook.

</td></tr><tr><td>

Look up Webhooks Stream

</td><td>

Retrieves details of all the available webhooks.

</td></tr><tr><td>

Reset Webhook Signing Secret by ID

</td><td>

Resets the signing secret of the specified webhook.

</td></tr><tr><td>

Update Webhook

</td><td>

Updates details of the specified webhook.

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Integration Hub imports

The Zendesk spoke adds the Import Zendesk Users Integration Hub imports to your ServiceNow instance. The Integration Hub imports help you import the users' data from Zendesk account to your ServiceNow instance in an automated way. For more information about Integration Hub imports, see[Integration Hub - Import](../../integrationhub/concept/integrationhub-imports.md).

## Spoke modules

The Zendesk spoke adds the Zendesk Spoke application to your ServiceNow instance. The Zendesk Spoke application includes these modules:

|Module|Description|
|------|-----------|
|Users|Stores the details of the Zendesk users. These details are imported using the Import Zendesk Users Integration Hub imports.|
|Remote table|
|Request|Retrieves and displayes the details of the requests raised by the specified requestor. For this, you must provide the value of **Requester ID**.|
|Webhook|
|Webhook Registries|Stores the webhook registries. The webhook registries register a Zendesk webhook in ServiceNow to notify ServiceNow when certain events occur in Zendesk.|
|Routing Policies|Stores the details of the webhook.|
|Tickets|Stores detailf of the tickets created or updated in Zendesk.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

For information about setting up the spoke, see [Set up the Zendesk spoke](../task/setup-zendesk.md#).


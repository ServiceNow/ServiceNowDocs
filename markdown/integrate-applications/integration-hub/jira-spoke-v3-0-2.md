---
title: Jira Spoke
description: Manage issues, users, stories, groups, projects, sprints, and webhooks, and look up audit logs in Jira. Retrieve Jira data to use in a flow. Use bi-directional webhooks and subscribe to Jira with a ServiceNow callback URL. Install Now Assist for Integration Hub and start using the available AI agents to perform tasks in your ServiceNow instance. Set up triggers for the required events to enable webhooks to connect with your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Jira Spoke

Manage issues, users, stories, groups, projects, sprints, and webhooks, and look up audit logs in Jira. Retrieve Jira data to use in a flow. Use bi-directional webhooks and subscribe to Jira with a ServiceNow callback URL. Install Now Assist for Integration Hub and start using the available AI agents to perform tasks in your ServiceNow instance. Set up triggers for the required events to enable webhooks to connect with your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Jira spoke v6.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Step - Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Integrations - External Authentication Framework \(com.glide.external.app\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for API version v2, but may be compatible with later versions.

**Note:**

-   If your Jira instance supports another API version, specify the API version in **API Version** in the respective connection record under the Attributes related list. By default, the **API Version** is `2`.
-   Jira Service Desk isn’t supported by the Jira spoke. ServiceNow offers [Jira Service Management Spoke](jira-serv-mngmt.md) to integrate with Jira Service Management that is the new version of Jira Service Desk.

## Jira Webhooks module

Bi-directional webhooks can be set up to be notified about the required events. Routing policy defines conditions that must be met to notify the ServiceNow instance. These conditions are based on the events in Jira that you want to be notified about. When the conditions are met, the routing policy triggers the associated subflow, which in turn automates the Jira tasks.

The bi-directional webhooks require separate setup and can be used independently without using the spoke actions. By default, the Jira Webhooks application is available in the Jira and has the following modules:

-   Jira Webhook Registries
-   Jira WebHook Routing Policies

Use the Jira Webhook Registries module to assign a token and provide the API path. You must generate a Callback URL here and provide the URL in Jira. A default routing policy is provided in the Jira WebHook Routing Policies module. The default routing policy supports these fields:

<table id="table_routing_policy"><thead><tr><th>

Category

</th><th>

Field

</th></tr></thead><tbody><tr><td>

Issue

</td><td>

-   Jira instance URL
-   Webhook Event
-   Issue Description
-   Created
-   Updated
-   Issue Resolution
-   Previous Issue Resolution
-   Issue Summary
-   Issue Type
-   Previous Issue Type
-   Issue Priority
-   Previous Issue Priority
-   Issue Status
-   Previous Issue Status
-   Issue Status Category
-   Previous Issue Status Category
-   Project

</td></tr><tr><td>

Comment

</td><td>

-   Jira Instance URL
-   Webhook Event
-   Comment
-   Created
-   Updated
-   Issue Summary
-   Issue Type
-   Issue Priority
-   Issue Status
-   Issue Status Category
-   Project

</td></tr><tr><td>

Worklog

</td><td>

-   Jira Instance URL
-   Webhook Event
-   Worklog Time Spent
-   Created
-   Updated

</td></tr><tr><td>

Attachment

</td><td>

-   Jira Instance URL
-   Webhook Event
-   Created
-   Attachment File Name
-   Attachment Size
-   Attachment Mime Type

</td></tr><tr><td>

Project

</td><td>

-   Jira Instance URL
-   Webhook Event
-   Project

</td></tr><tr><td>

Version

</td><td>

-   Jira Instance URL
-   Webhook Event
-   Version
-   Version Description
-   Merged To Version
-   Merged To Version Description

</td></tr></tbody>
</table>To use other conditions in the routing policy, create a routing policy in the Jira WebHook Routing Policies module and specify conditions as per your requirement. See [Set up a bi-directional webhook for the Jira spoke](../task/setup-jira302-webhooks.md#) for information regarding setting up and configuring the webhooks.

**Tip:** To set up and use webhooks, you should configure webhook registries, decision tables, and create subflows. For a low-code alternative with less configurations, you can use [Spoke triggers](jira-spoke-v3-0-2.md#section_cpg_rpm_ccc).

## Spoke subflow

The Jira spoke provides a sample subflow to handle various Jira webhook events. The available sample subflow is Process Jira Webhooks. The Process Jira Webhooks subflow supports these fields:

<table id="table_ydf_st1_1jb"><thead><tr><th>

Category

</th><th>

Field

</th></tr></thead><tbody><tr><td>

Issue

</td><td>

-   User
-   Issue
-   Attachments
-   Issue Change Log
-   Project

</td></tr><tr><td>

Comment

</td><td>

-   Issue
-   Project
-   Comment

</td></tr><tr><td>

Worklog

</td><td>

Worklog

</td></tr><tr><td>

Attachments

</td><td>

Attachment

</td></tr><tr><td>

Project

</td><td>

Project

</td></tr><tr><td>

Version

</td><td>

Version

</td></tr><tr><td colspan="2">

Webhook Event

</td></tr><tr><td colspan="2">

Timestamp

</td></tr><tr><td colspan="2">

Payload**Note:** This is the entire Jira payload.

</td></tr></tbody>
</table>To customize the default subflow, you must a create a copy of the sample subflow, parse the payload, and customize the subflow as per your requirement. Payload is one of the inputs to the subflow.

While customizing subflows, you must ensure that the subflows are configured to avoid infinite loops.

**Note:**

-   You must configure webhooks to use the spoke subflow. See [Set up a bi-directional webhook for the Jira spoke](../task/setup-jira302-webhooks.md#) for information regarding setting up and configuring the webhook.
-   The sample subflow runs as a user by default. The subflow can be configured to run as system.

## Spoke triggers

Use triggers in the Jira spoke to subscribe to the required events. The endpoint enables webhooks to connect with your ServiceNow instance. You can configure the flows to execute only when the specified trigger conditions are met. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Board Management|Board Deleted|Trigger is initiated when a board is deleted.|
|Board Updated|Trigger is initiated when a board is updated.|
|Board Created|Trigger is initiated when a board is created.|
|Comment Management|Comment Deleted|Trigger is initiated when a comment is deleted.|
|Comment Updated|Trigger is initiated when a comment is updated.|
|Comment Created|Trigger is initiated when a comment is created.|
|Issue Managament|Issue Updated|Trigger is initiated when an issue is updated. The events like issue assigned, issue resolved, issue closed, issue reopened, issue moved, and other events that are related to updating an issue come under this webhook event.|
|Issue Assigned|Trigger is initiated when an issue gets assigned.|
|Issue Deleted|Trigger is initiated when a issue is deleted.|
|Issue Created|Trigger is initiated when a issue is created.|
|Sprint Management|Sprint Updated|Trigger is initiated when a sprint is updated.|
|Sprint Deleted|Trigger is initiated when a sprint is deleted.|
|Sprint Created|Trigger is initiated when a sprint is created.|
|Sprint Closed|Trigger is initiated when a sprint is closed.|
|Sprint Started|Trigger is initiated when a sprint is started.|

For information about setting up the triggers for the Jira spoke, see [Set up triggers for the Jira spoke](../task/jira-ext-trigger.md#). For more information about inbound integration, see [Conditional and event-driven inbound integration](../../integrationhub/concept/conditional-and-event-driven-inbound-integration.md).

## Spoke actions

Use actions in the Jira spoke in Workflow Studio to automate Jira tasks when an event occurs in the ServiceNow AI Platform. Available actions include:

**Note:**

-   Some of the spoke actions from this release onwards don't have the **Connection Alias** input.

    The existing flows in your instance that use actions of the previous versions, continue to work. However, those earlier actions are renamed by adding the `deprecated` suffix and you can't use them from this version onwards.

-   Error evaluation capabilities are provided in some of the spoke actions.

<table id="table_ntl_nhn_ngc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Audit Management

</td><td>

Look up Audit Logs Stream

</td><td>

Retrieves login activity for the Jira user subscriptions.**Note:** This action is supported on Jira Server 9 and earlier versions, and Jira Cloud.

</td></tr><tr><td>

Look up Audit Logs Stream \(Server 10+\)

</td><td>

Retrieves audit log records from the Jira instance within a specified date range.**Note:** This action is supported on Jira Server 10 and later versions.

</td></tr><tr><td rowspan="6">

Group Management

</td><td>

Add User to Group

</td><td>

Adds given user to a group in Jira.

</td></tr><tr><td>

Create Group

</td><td>

Creates a group in Jira.

</td></tr><tr><td>

Look up Groups Stream

</td><td>

Retrieves all groups in the Jira account, including the default groups.**Note:** This action can be used with Jira Cloud subscription only.

</td></tr><tr><td>

Look up Users by Group Name Stream

</td><td>

Retrieves details of all members in a Jira group.

</td></tr><tr><td>

Remove Group

</td><td>

Removes the given group from Jira.

</td></tr><tr><td>

Remove User from Group

</td><td>

Removes the given user from a group in Jira.

</td></tr><tr><td rowspan="17">

Issue Management

</td><td>

Add Comment

</td><td>

Adds a comment to the specified issue in Jira.

</td></tr><tr><td>

Add Watcher

</td><td>

Adds the specified user as a watcher for the specified issue.

</td></tr><tr><td>

Assign Issue

</td><td>

Assigns the issue in Jira to the user.

</td></tr><tr><td>

Copy Attachment

</td><td>

Copies the required attachment associated with the ServiceNow record to the required issue in Jira.

</td></tr><tr><td>

Create Issue

</td><td>

Creates an issue in Jira. Depending on how your organization is using Jira, an issue could represent a software bug, a project task, a help desk ticket, or more. An issue in Jira represents a task in the ServiceNow AI Platform.

</td></tr><tr><td>

Delete Attachment

</td><td>

Deletes the required attachment in Jira.

</td></tr><tr><td>

Delete Issue

</td><td>

Deletes an issue in Jira.

</td></tr><tr><td>

Delete Watcher

</td><td>

Deletes the user as a watcher for the specified issue.

</td></tr><tr><td>

Do Transition

</td><td>

Transitions an issue in Jira from one state to another.

</td></tr><tr><td>

Look up Issue Type Statuses by Project

</td><td>

Retrieves details of the statuses in a project.

</td></tr><tr><td>

Look up Issue

</td><td>

Retrieves the details for an issue.

</td></tr><tr><td>

Look up Issue Priorities

</td><td>

Retrieves the list of issue priorities and details for individual issue priorities.

</td></tr><tr><td>

Look up Issues Stream

</td><td>

Retrieves a list of issues matching a JQL query string.

</td></tr><tr><td>

Look up Sprint Issues Stream

</td><td>

Retrieves the details of all issues for the given sprint.

</td></tr><tr><td>

Look up Transitions

</td><td>

Retrieves information about all Transitions for a given Issue ID.

</td></tr><tr><td>

Look up Watchers

</td><td>

Retrieves the list of watchers for the specified issue.

</td></tr><tr><td>

Update Issue

</td><td>

Updates a set number of fields of an issue in Jira with values passed as input.

</td></tr><tr><td rowspan="3">

Metadata Retrieval

</td><td>

Get Creatable Fields \(Metadata\)

</td><td>

Retrieves the list of all fields in a required Jira project.

</td></tr><tr><td>

Get Editable Fields \(Metadata\)

</td><td>

Retrieves the list of all editable fields in a required Jira issue.

</td></tr><tr><td>

Get Issue Types \(Metadata\)

</td><td>

Retrieves the list of all issue types in a required Jira project.

</td></tr><tr><td rowspan="5">

Project Management

</td><td>

Create Project

</td><td>

Creates a project in Jira.

</td></tr><tr><td>

Look up Project

</td><td>

Retrieves details of the specified project by its ID or key.

</td></tr><tr><td>

Look up Projects

</td><td>

Retrieves details of all projects.**Note:** This action only works for the Jira server.

</td></tr><tr><td>

Look up Projects Stream

</td><td>

Retrieves details of all projects.**Note:** This action only works for the Jira Cloud.

</td></tr><tr><td>

Look up Users Assignable to Projects

</td><td>

Retrieves a list of users that can be assigned to issues in one or more projects.

</td></tr><tr><td rowspan="5">

Sprint Management

</td><td>

Create Sprint

</td><td>

Creates a sprint in Jira.

</td></tr><tr><td>

Delete Sprint

</td><td>

Deletes a sprint in Jira.

</td></tr><tr><td>

Look up Sprint

</td><td>

Retrieves the details of the required sprint as a complex object.

</td></tr><tr><td>

Look up Sprints by Board

</td><td>

Retrieves the details of all sprints in the required board.

</td></tr><tr><td>

Update Sprint

</td><td>

Updates the details of a sprint in Jira.

</td></tr><tr><td rowspan="3">

Story Management

</td><td>

Create Story

</td><td>

Creates a story in the Jira Cloud instance. This is comparable to story in the ServiceNow Agile Development plugin.

</td></tr><tr><td>

Look up Stories Stream

</td><td>

Retrieves details of all stories.

</td></tr><tr><td>

Update Story

</td><td>

Updates a set number of fields of a story in Jira Cloud with the provided input values.

</td></tr><tr><td rowspan="6">

User Management

</td><td>

Create User

</td><td>

Creates a user in Jira.

</td></tr><tr><td>

Look up Authenticated User

</td><td>

Retrieves details of the authenticated user account.

</td></tr><tr><td>

Look up Group Memberships for User

</td><td>

Retrieves details of all groups of a Jira user.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves details of all Jira user subscriptions.**Note:** This action can be used with a Jira Cloud subscription only.

</td></tr><tr><td>

Look up Users Stream by Name

</td><td>

Retrieves a list of users that match the search string.**Note:** This action can be used with a Jira server subscription only.

</td></tr><tr><td>

Remove User

</td><td>

Removes a user from Jira.

</td></tr><tr><td rowspan="6">

Utility Actions

</td><td>

Copy Issue Attachment to Record

</td><td>

Copies Attachment from Jira to any record in ServiceNow instance. When you use this action in a subflow, make sure that the Content URL data pill is specified in the Attachment URL field.

</td></tr><tr><td>

Look up Fields

</td><td>

Retrieves the internal name and other details of the required field label in Jira.

</td></tr><tr><td>

Look up Issue from Comment

</td><td>

Retrieves the details of the issue by parsing the payload for the specified comment. You can use this action in the Process Jira Webhook subflow for Jira on-prem server when only comment related information is specified without any details about the Jira issue. For example, when only comment information is specified, this action parses the payload and extracts the issue details.

</td></tr><tr><td>

Look up Latest Attachment on Issue

</td><td>

Retrieves the latest attachment for the specified issue from Jira. You can use this action in a flow or subflow for validation. For example, a subflow adds an additional attachment only when the latest attachment of an issue in Jira isn’t as the same specified attachment.

</td></tr><tr><td>

Look up Latest Comment on Issue

</td><td>

Retrieves the latest comment for the specified issue from Jira. You can use this action in a flow or subflow for validation. For example, a subflow adds an additional comment only when the latest comment of an issue in Jira isn’t as the same specified comment.

</td></tr><tr><td>

Look up Server

</td><td>

Retrieves general information about the current Jira instance.

</td></tr><tr><td rowspan="4">

Webhook Management

</td><td>

Look up Webhooks

</td><td>

Retrieves details of all registered webhooks from the Jira instance.

</td></tr><tr><td>

Subscribe Webhook

</td><td>

Registers a webhook in the Jira instance.

</td></tr><tr><td>

Unsubscribe Webhook

</td><td>

Deletes the registered webhook in Jira instance.

</td></tr><tr><td>

Update Webhook

</td><td>

Updates webhook with the given ID in Jira.**Note:** This action isn’t supported when OAuth 2.0 authentication is used.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Jira story management AI agent|Retrieves information about stories in a stream, creates new stories, and updates existing stories.|
|Jira utility management AI agent|Provides utility actions that can copy issue attachment to record, retrieve the latest attachment and comments on a Jira issue, and retrieve field details using labels. Ensures accurate data retrieval.|
|Jira user management AI agent|Creates and removes the required user. Retrieves information about users, group memberships, and authenticated user accounts.|
|Jira audit management AI agent|Manages audit logs and provides actionable insights by automating repetitive tasks.|
|Jira sprint management AI agent|Deletes sprints, updates sprint details, and retrieves specific sprint information.|
|Jira project management AI agent|Retrieves project details, creates new projects, retrieves project streams, and identifies users assignable to projects.|
|Jira group management AI agent|Manages groups by performing actions such as, creating and deleting groups, adding and removing users, retrieving details about groups, retrieving data and updates, and retrieving group members.|
|Jira issue management AI agent|Manages issues by performing actions such as, deleting issues, managing transitions, handling watchers, and working with attachments. Also, manages transitions, comments, attachments, and watchers.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Jira account requirements

The Jira requires generating an API token for Jira using your Jira account.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Jira alias record. To use these actions, you must create a connection record and a credential record and associate them with the Jira alias record.

These actions use REST calls, which can run on an instance. Use the connection record associated with the Jira alias to configure the endpoint against which the actions run.


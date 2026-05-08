---
title: GitHub Spoke
description: Manage distributed version control and source code in GitHub from your ServiceNow instance. Create flows in ServiceNow to manage collaborative features such as tracking bugs, feature requests, tasks and so on, for projects in GitHub. View and analyze meaningful usage data for GitHub Enterprise Cloud and GitHub Enterprise Server software subscriptions so that you can reclaim stale licenses.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# GitHub Spoke

Manage distributed version control and source code in GitHub from your ServiceNow instance. Create flows in ServiceNow to manage collaborative features such as tracking bugs, feature requests, tasks and so on, for projects in GitHub. View and analyze meaningful usage data for GitHub Enterprise Cloud and GitHub Enterprise Server software subscriptions so that you can reclaim stale licenses.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

GitHub spoke v3.5.2 is the latest version.

## Supported versions

This spoke was built for GitHub API version v3, but may be compatible with later versions.

## Spoke requirements

-   GitHub account
-   User with admin credentials
-   Token to authenticate the ServiceNow instance

See the [GitHub documentation](https://help.github.com/en) for instructions on creating a GitHub account and generating a token.

## GitHub Webhooks module

Bi-directional webhooks can be set up to be notified about the required events. Routing policy defines conditions that must be met to notify the ServiceNow app. These conditions are based on the events in GitHub for which you want to be notified about. When the conditions are met, the routing policy triggers the associated subflow, which in turn automates the GitHub tasks.

The bi-directional webhooks require separate setup and can be used independently without using the spoke actions. By default, the GitHub Webhooks application is available in the GitHub spoke and has the following modules:

-   GitHub Webhook Registries
-   GitHub WebHook Routing Policies

Use the GitHub Webhook Registries module to assign a token and provide the API path. You must generate a Callback URL here and provide this URL in GitHub. A default routing policy is provided in the GitHub WebHook Routing Policies module. The default routing policy supports these GitHub fields:

|Supported GitHub fields|
|-----------------------|
|Action|Project Card Creator|Ref|
|Base Ref|Project Card Note|Ref Type|
|Commit Comment Body|Project Card Previous Note|Release Assets|
|Commit Comment Created At|Project Card Updated At|Release Author|
|Commit Comment Path|Project Column Created At|Release Body|
|Commit Comment Updated At|Project Column Name|Release Created At|
|Commit Comment User|Project Column Previous Name|Release Draft|
|Force Push|Project Column Updated At|Release Name|
|GitHub Instance URL|Project Created At|Release Published At|
|Issue Assigned To|Project Name|Release Tag Name|
|Issue Assignees|Project Previous Body|Release Target Commits|
|Issue Body|Project Previous Name|Repository Archived|
|Issue Closed At|Project State|Repository Created At|
|Issue Comment|Project Updated At|Repository Description|
|Issue Comment Count|Pull Request Assigned To|Repository inactive|
|Issue Comment Created At|Pull Request Assignees|Repository Full Name|
|Issue Comment Updated At|Pull Request Body|Repository Has Issues|
|Issue Created At|Pull Request Closed At|Repository Has Projects|
|Issue Labeled To|Pull Request Comment Count|Repository Import Status|
|Issue Labels|Pull Request Created At|Repository License|
|Issue Locked|Pull Request Draft|Repository Open Issues Count|
|Issue Milestone|Pull Request Labeled To|Repository Owner|
|Issue Previous Body|Pull Request Labels|Repository Private|
|Issue Previous Comment|Pull Request Locked|Repository Pushed At|
|Issue Previous Milestone|Pull Request Mergeable|Repository Starred At|
|Issue Previous Title|Pull Request Merged|Repository Updated At|
|Issue Previously Assigned To|Pull Request Merged At|Repository Vulnerability Alert Affected Range|
|Issue Previously Labeled To|Pull Request Milestone|Repository Vulnerability Alert External Identifier|
|Issue State|Pull Request Previous Body|Repository Vulnerability Alert Fixed In|
|Issue Title|Pull Request Previous Title|Repository Vulnerability Alert Package Name|
|Issue Updated At|Pull Request Previously Assigned To|Security Advisory Description|
|Issue User|Pull Request Previously Labeled To|Security Advisory ID|
|Milestone Closed At|Pull Request Rebaseable|Security Advisory Published At|
|Milestone Created At|Pull Request Review Body|Security Advisory Severity|
|Milestone Creator|Pull Request Review Comment|Security Advisory Summary|
|Milestone Description|Pull Request Review Comment Count|Security Advisory Updated At|
|Milestone Due On|Pull Request Review Comment Created At|Security Advisory Withdrawn At|
|Milestone State|Pull Request Review Comment File Path|Sender login|
|Milestone Title|Pull Request Review Comment Previous Comment|Status Commit Message|
|Milestone Updated At|Pull Request Review Comment Updated At|Status Context|
|Organization Description|Pull Request Review Previous Body|Status Created At|
|Organization Login|Pull Request Review State|Status Description|
|Pre-Release|Pull Request State|Status Name|
|Project Body|Pull Request Title|Status State|
|Project Card Archived|Pull Request Updated At|Status Updated At|
|Project Card Created At|Pull Request User|Webhook Event|

To use other conditions in the routing policy, create a routing policy in the GitHub WebHook Routing Policies module and specify conditions according to your requirement. See [Set up bi-directional webhook for the GitHub spoke](../task/setup-biwebhoook-github.md#) for information regarding setting up and configuring the webhooks.

## Spoke triggers

ServiceNow supports specific events on GitHub that create triggers. You must first configure a flow with a supported trigger definition. When an event, for example, a push request, occurs on the GitHub, it sends the payload via a webhook to the ServiceNow instance. After that, the flow that you configured is triggered at the ServiceNow instance to automate a workflow. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Branch Management|Branch Created|Flow is triggered when you create a branch on GitHub.|
|Repository Management|Pull Request Opened|Flow is triggered when you initiate a new pull request on GitHub.|
|Pull Request Edited|Flow is triggered when you update a pull request on GitHub.|
|Pull Request Closed|Flow is triggered when you close a pull request on GitHub.|
|Pull Request Assigned|Flow is triggered when you assign a pull request to a user on GitHub.|
|Pull Request Reopened|Flow is triggered when you reopen a pull request on GitHub.|
|Repository Fork|Flow is triggered when you fork a repository on GitHub.|
|Repository Push|Flow is triggered when you push to a repository on GitHub.|
|Release Management|Release Created|Flow is triggered when the details of a release are created on GitHub.|
|Release Edited|Flow is triggered when the details of a release are updated on GitHub.|
|Release Deleted|Flow is triggered when a release is removed on GitHub.|
|Release Released|Flow is triggered when a release is released on GitHub.|

For information about setting up the triggers for the GitHub spoke, see [Activate the trigger definition on ServiceNow instance](../task/set-up-triggers-github-spoke.md#). For more information about inbound integration, see [Conditional and event-driven inbound integration](../../integrationhub/concept/conditional-and-event-driven-inbound-integration.md).

## Spoke subflows

The GitHub spoke provides a sample subflow to handle various GitHub webhook events. Available sample subflows are:

<table id="table_jcm_pvg_jkb"><thead><tr><th>

Subflow

</th><th>

Description

</th><th>

Supported GitHub Event

</th></tr></thead><tbody><tr><td>

Process GitHub Branch and Tag Webhook Events

</td><td>

Handles branch and tag webhook events.

</td><td>

Branch and Tag

</td></tr><tr><td>

Process GitHub Commit Webhook Events

</td><td>

Handles commit webhook events.

</td><td>

Commit

</td></tr><tr><td>

Process GitHub Issue Webhook Events

</td><td>

Handles issue webhook events.

</td><td>

Issue

</td></tr><tr><td>

Process GitHub Milestone Webhook Events

</td><td>

Handles milestone webhook events.

</td><td>

Milestone

</td></tr><tr><td>

Process GitHub Project Webhook Events

</td><td>

Handles project webhook events.

</td><td>

Project

</td></tr><tr><td>

Process GitHub Pull Request Webhook Events

</td><td>

Handles pull request webhook events.

</td><td>

Pull Request

</td></tr><tr><td>

Process GitHub Push Webhook Events

</td><td>

Handles push request webhook events.

</td><td>

Push Request

</td></tr><tr><td>

Process GitHub Release Webhook Events

</td><td>

Handles release webhook events.

</td><td>

Release

</td></tr><tr><td>

Process GitHub Repository Webhook Events

</td><td>

Handles repository webhook events.

</td><td>

Repository

</td></tr><tr><td>

Process GitHub Security Webhook Events

</td><td>

Handles security webhook events.

</td><td>

Security

</td></tr><tr><td>

Process GitHub Webhook Events

</td><td>

Handles all GitHub webhook events.

</td><td>

**Note:** This subflow handles all GitHub events. You can customize this subflow to handle other GitHub webhook events that are not supported by default.

</td></tr></tbody>
</table>To create subflows to handle other GitHub webhook events or handle the supported GitHub webhook events differently, customize the Process GitHub Webhook Events subflow. For this, you must a create a copy of the subflow, parse the payload, and customize the subflow according to your requirement. Payload is one of the inputs to the subflow.

While customizing subflows, you must confirm that the subflows are configured to avoid infinite loops.

**Note:**

-   You must configure webhooks to use the spoke subflow. See [Set up bi-directional webhook for the GitHub spoke](../task/setup-biwebhoook-github.md#) for information regarding setting up and configuring the webhook.
-   The sample subflows run as a user by default. It can be configured to run as a system.
-   GitHub spoke supports application/json payload. Configure the GitHub webhook accordingly. See the [GitHub Developer](https://developer.github.com/) documentation for instructions on creating and configuring a webhook.

## Spoke actions

The GitHub spoke provides actions manage branches, issues, repositories, and source code when events occur in ServiceNow. Available actions include:

<table id="table_ds1_vy2_3kb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

Branch Management

</td><td>

Create Branch

</td><td>

Creates a branch in GitHub based on a specific commit SHA.

</td></tr><tr><td>

Delete Branch

</td><td>

Deletes a branch from the GitHub repository.

</td></tr><tr><td>

Look up Branch

</td><td>

Retrieves the details of a branch in the GitHub repository.

</td></tr><tr><td>

Look up Branch Protection

</td><td>

Retrieves the restriction details of the required branch.

</td></tr><tr><td>

Look up Branches

</td><td>

Retrieves the list of all branches in a repository.

</td></tr><tr><td>

Remove Branch Protection

</td><td>

Removes protection on the required branch.

</td></tr><tr><td>

Update Branch Protection

</td><td>

Updates protection on the required branch.

</td></tr><tr><td rowspan="9">

Issue Management

</td><td>

Create Comment on Issue

</td><td>

Creates comment on a required issue.

</td></tr><tr><td>

Create Issue

</td><td>

Creates issue for the required repository.

</td></tr><tr><td>

Delete Comment on Issue

</td><td>

Deletes comment on a required issue.

</td></tr><tr><td>

Lock Issue

</td><td>

Locks the required issue. This limits the conversation to collaborators only.

</td></tr><tr><td>

Look Up Comments on Issue Stream

</td><td>

Retrieves the list of comments on an issue.

</td></tr><tr><td>

Look Up Issues Stream

</td><td>

Retrieves the list of issues for a repository.

</td></tr><tr><td>

Unlock Issue

</td><td>

Unlocks the required issue. This opens conversation to all users.

</td></tr><tr><td>

Update Comment on Issue

</td><td>

Updates a comment on an issue.

</td></tr><tr><td>

Update Issue

</td><td>

Updates the details of the required issue.

</td></tr><tr><td rowspan="5">

Metadata Retrieval

</td><td>

Look up Fields by Action

</td><td>

Retrieves the list of fields for an action filter in the GitHub Fields table.

</td></tr><tr><td>

Look up Branches Metadata

</td><td>

Retrieves metadata of the branches.

</td></tr><tr><td>

Look up Issues Metadata

</td><td>

Retrieves metadata of the issues.

</td></tr><tr><td>

Look up Milestones Metadata

</td><td>

Retrieves metadata of the milestones.

</td></tr><tr><td>

Look up Pull Requests Metadata

</td><td>

Retrieves metadata of the pull requests.

</td></tr><tr><td rowspan="10">

Organization Management

</td><td>

Look up Organization Plan

</td><td>

Retrieves the plan name of an organization.

</td></tr><tr><td>

Look up Organization Members Stream

</td><td>

Retrieves the list of all members within an organization.

</td></tr><tr><td>

Look up Organization Repositories Stream

</td><td>

Retrieves the list of all repositories within an organization.

</td></tr><tr><td>

Remove Organization Member

</td><td>

Removes a user from an organization.

</td></tr><tr><td>

Look up Organization Events Stream

</td><td>

Retrieves the list of events in an organization based on the provided look back date.

</td></tr><tr><td>

Look up Organization Outside Collaborators Stream

</td><td>

Retrieves the list of all Outside Collaborators within an organization.

</td></tr><tr><td>

Remove Organization Outside Collaborator

</td><td>

Removes an outside collaborator from an organization.

</td></tr><tr><td>

Look up Organization Pending Outside Collaborators Stream

</td><td>

Retrieves a list of pending collaborators within a repository.

</td></tr><tr><td>

Look up Organization Invitations Stream

</td><td>

Retrieves a list of invitations within an organization.

</td></tr><tr><td>

Look up Organization Audit Log Stream

</td><td>

Retrieves a list of organization audit log events for a specified look-back date.

</td></tr><tr><td rowspan="21">

Repository Management

</td><td>

Add Collaborator

</td><td>

Adds collaborator to the required repository.

</td></tr><tr><td>

Delete Repository

</td><td>

Deletes a repository from GitHub.

</td></tr><tr><td>

Create Comment on Pull Request

</td><td>

Create review comments on a pull request.

</td></tr><tr><td>

Create Milestone

</td><td>

Creates milestone for the required repository.

</td></tr><tr><td>

Create Pull Request

</td><td>

Creates a pull request for a repository.

</td></tr><tr><td>

Create Reply on Pull Request Review Comment

</td><td>

Creates reply to a review comment for a pull request.

</td></tr><tr><td>

Create Repository

</td><td>

Creates a repository in GitHub.

</td></tr><tr><td>

Delete Comment on Pull Request

</td><td>

Deletes review comment on a pull request.

</td></tr><tr><td>

Delete Milestone

</td><td>

Deletes milestone from the required repository.

</td></tr><tr><td>

Look up Comments on Pull Request Stream

</td><td>

Retrieves the list of all review comments on a pull request.

</td></tr><tr><td>

Look up Milestones Stream

</td><td>

Retrieves the list of all milestones in a repository.

</td></tr><tr><td>

Look up Repository Events Stream

</td><td>

Retrieves the list of events across a repository.

</td></tr><tr><td>

Look Up Pull Requests Stream

</td><td>

Retrieves the details of pull requests for a repository.

</td></tr><tr><td>

Look Up Repositories Stream

</td><td>

Retrieves the details of repositories based on a specific user or organization.

</td></tr><tr><td>

Look up Repository Details

</td><td>

Retrieves the details of the specified repository.

</td></tr><tr><td>

Merge Pull Request

</td><td>

Merges the pull request to a repository.

</td></tr><tr><td>

Remove Collaborator

</td><td>

Removes collaborator from a repository.

</td></tr><tr><td>

Update Comment on Pull Request

</td><td>

Updates review comments provided for a pull request.

</td></tr><tr><td>

Update Milestone

</td><td>

Updates the details of a milestone in a repository.

</td></tr><tr><td>

Update Pull Request

</td><td>

Updates the details of a pull request in a repository.

</td></tr><tr><td>

Update Repository

</td><td>

Updates the details of a repository in GitHub.

</td></tr><tr><td rowspan="6">

Source Code Management

</td><td>

Create Comment on Commit

</td><td>

Creates a comment for the required commit using its SHA.

</td></tr><tr><td>

Create or update a file

</td><td>

Creates a file or updates an existing file in a repository.

</td></tr><tr><td>

Look up Comments by Commit ID Stream

</td><td>

Retrieves comments provided for a single commit.

</td></tr><tr><td>

Look up Commit Information By ID

</td><td>

Retrieves the contents of the required commit reference.

</td></tr><tr><td>

Look up File Content

</td><td>

Retrieves the contents of a file in a repository.**Note:** This action supports files with file size up to 1 MB.

</td></tr><tr><td>

Look up Commits on a Repository

</td><td>

Retrieves the details of all commits made on a repository.

</td></tr><tr><td rowspan="4">

User Management

</td><td>

Look up All Users for Enterprise Server

</td><td>

Retrieves the list of all GitHub Enterprise Server users.

</td></tr><tr><td>

Look up Organizations for the Authenticated User Stream

</td><td>

Retrieves the list of organizations that the logged-in user is a member of.

</td></tr><tr><td>

Suspend User

</td><td>

Suspends a GitHub user account.

</td></tr><tr><td>

Look up Authenticated User

</td><td>

Retrieves information about the authenticated user.

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
|GitHub branch management AI agent|Manages and maintains the GitHub branches. Also, retrieves information about the GitHub branches.|
|GitHub issue management AI agent|Manages and automates GitHub-related tasks in Integration Hub.|
|GitHub repository management AI agent|Manages the GitHub repositories by handling the repository operations, pull requests, comments on pull request and milestones.|
|GitHub source code management AI agent|Manages source code and handles the repository files, commits, and comments.|
|GitHub Code Automation AI Agent|Manages code changes and GitHub operations from your ServiceNow instance. This agent interprets your requests, asks clarifying questions, and analyzes context to deliver well-integrated code updates. It also performs GitHub tasks such as creating branches, committing changes, and opening pull requests.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke modules

The GitHub spoke adds these modules to your ServiceNow instance.

|Module|Description|
|------|-----------|
|GitHub Owner|Displays the GitHub owner records that you had created.|
|GitHub Repositories|Displays the details of the GitHub repositories associated with the GitHub owners.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the GitHub spoke](../task/set-up-github-spoke.md).


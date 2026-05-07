---
title: GitLab Spoke
description: Manage the DevOps lifecycle in GitLab from your ServiceNow instance. Create flows in ServiceNow to manage branches, groups, issues, merge requests, projects, and source code in GitLab.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# GitLab Spoke

Manage the DevOps lifecycle in GitLab from your ServiceNow instance. Create flows in ServiceNow to manage branches, groups, issues, merge requests, projects, and source code in GitLab.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

GitLab spoke v2.4.1 is the latest version.

## Compatible versions

This spoke was built for GitLab API version v4, but may be compatible with later versions.

## Spoke requirements

-   GitLab account
-   An application in GitLab configured to integrate with ServiceNow
-   **Application ID** and **Secret** of the GitLab application

See the [https://docs.gitlab.com/ee/integration/oauth\_provider.html](https://docs.gitlab.com/ee/integration/oauth_provider.html) documentation for instructions on creating and configuring applications.

## Spoke actions

The GitLab spoke provides actions to automate GitLab tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Branch Management|Compare Branches Tags or Commits|Compares branches, tags, or commits.|
|Create Branch|Creates a branch in the required project.|
|Delete Branch|Deletes the required branch from a project.|
|Delete Merged Branches|Deletes the required merged branch from a project.|
|Look up Branch|Retrieves the details of the required branch.|
|Look up Branches Stream|Retrieves a list of branches and the branch details in a project.|
|Protect Branch|Protects a branch in a project with access levels.|
|Unprotect Branch|Unprotects a branch in a project with access levels.|
|Group Management|Add User To A Group|Adds user to a GitLab group.|
|Remove User From A Group|Removes user from a GitLab group.|
|Issue Management|Create Issue|Creates an issue in the required project.|
|Create Issue Note|Creates an issue note for the required issue.|
|Delete Issue Note|Deletes an issue note for the required issue.|
|Look up Issue Notes Stream|Retrieves all issue notes in an issue.|
|Look up Issues Stream|Retrieves a list of issues and issue details.|
|Update Issue|Updates details of the required issue.|
|Update Issue Note|Updates an issue note in a project.|
|Merge Request Management|Accept Merge Request|Approves a merge request in GitLab.|
|Create Merge Request|Creates a merge request in GitLab.|
|Create Merge Request Note|Creates a note for the required merge request.|
|Delete Merge Request Note|Deletes a note for the required merge request.|
|Look up all Merge Requests Stream|Retrieves the list of merge requests in a project.|
|Look up Merge Request Notes|Retrieves the list of merge request notes in a project.|
|Update Merge Request|Updates details of the required merge request.|
|Update Merge Request Note|Updates details of the required merge request note.|
|Package Management|Delete Package File|Deletes a package file from the project package registry.|
|Delete Project Package|Deletes a package from the project package registry.|
|Delete Registry Repository|Removes a registry repository from a project.|
|Delete Registry Repository Tags|Removes registry repository tags in a batch from a project.|
|Look up Details of a Registry|Retrieves details of a registry repository for a specified project.|
|Look up Package Files Stream|Retrieves list of package files of a single package.|
|Look up Packages within Group Stream|Retrieves a list of project packages and package details at the group level.|
|Look up Packages within Project Stream|Retrieves a list of project packages and package details.|
|Look up Project Package|Retrieves the details of the specified package for a specified project.|
|Look up Registry Repositories|Retrieves a list of registry repositories for a specified project.|
|Pipeline Management|Look up Project Pipeline by ID|Retrieves the details of a specified pipeline for a specified project.|
|Look up Project Pipeline Jobs Stream|Retrieves the list of jobs in a project pipeline.|
|Look up Project Pipeline Test Report|Retrieves the test report of the specified pipeline for the specified project.|
|Look up Project Pipelines Stream|Retrieves the list of pipelines in a project.|
|Project Hook Management|Create Project Hook|Creates a hook to a project.|
|Delete Project Hook|Removes a hook from a project.|
|Look up Project Hook|Retrieves details of a specified hook in a project.|
|Look up Project Hooks|Retrieves details of all the hooks in a project.|
|Update Project Hook|Updates details of a hook for a specified project.|
|Project Management|Add User To A Project|Adds user to a project in GitLab.|
|Archive Project|Archives a project in GitLab.|
|Create Milestone|Creates milestone in a GitLab project.|
|Create Project|Creates a project in GitLab.|
|Delete Milestone|Deletes milestone in a GitLab project.|
|Delete Project|Deletes a project in GitLab.|
|Look up Milestones Stream|Retrieves the details of the milestones GitLab.|
|Look up Project|Retrieves details of the specified project.|
|Look up Project Jobs Stream|Retrieves the project jobs details.|
|Look up Projects Stream|Retrieves the details of the projects.|
|Remove User from a Project|Removes user from a project in GitLab.|
|Share Project With Group|Shares a project with a group in GitLab.|
|Unarchive Project|Unarchives a project in GitLab.|
|Unshare Project With Group|Unshares a project with a group in GitLab.|
|Update Milestone|Updates details of a milestone in a project.|
|Update Project|Updates details of a project.|
|Source Code Management|Get Commit|Retrieves a details of a commit in GitLab.|
|Add New File To Repository|Adds a file to a repository in GitLab.|
|Token Management|Look up Personal Access Tokens|Retrieves a list of personal access tokens.|
|Revoke Personal Access Token|Revokes a personal access token.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|GitLab pipeline management AI agent|Manages pipeline tasks \(that is, looks up project pipelines by ID, retrieves pipeline test reports, streams project pipeline jobs and streams project pipeline data\) in GitLab.|
|GitLab branch management AI agent|Manages branch management \(that is, compare branches, tags, or commits, creates and deletes branches, manages branch protection, and looks up branch details or streams\) in GitLab.|
|GitLab merge request management AI agent|Manages merge requests \(creates, updates, accepts, and deletes merge request notes, and retrieves information about merge request notes\) in GitLab.|
|GitLab package management AI agent|Manages package management \(that is, deletes project packages, manages registry repositories, and performs detailed lookups for packages and files\) in GitLab.|
|GitLab token management AI agent|Manages token management \(that is, looks up and revokes personal access tokens\) in GitLab.|
|GitLab issue management AI agent|Manages issue management tasks \(that is, creates, updates, and manages issues and the related notes\) in GitLab.|
|GitLab project management AI agent|Manages project management tasks \(that is, creates, updates, and deletes projects and milestones, manages user and group access, and retrieves project and milestone streams\) in GitLab.|
|GitLab source code management AI agent|Manages source code tasks \(that is, looks up commit difference, adds new file to repository, and looks up commit by project ID\) in GitLab.|
|GitLab group management AI agent|Manages user-group tasks \(that is, adds and removes users from groups\) in GitLab.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke flows

The GitLab spoke provides sample flows to demonstrate automating the GitLab tasks. To customize a sample flow, copy it to a new application scope.

|Flow|Description|
|----|-----------|
|Archive projects older than 6 months|Archives the projects which are inactive for the last six months.|

## Spoke subflows

The GitLab spoke provides sample flows to demonstrate automating the GitLab tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflows|Description|
|--------|-----------|
|Process GitLab Deployment Webhook Events​|Processes deployment webhooks in GitLab.|
|Process GitLab Job Webhook Events​|Processes job webhook events in GitLab.|
|Process GitLab Merge Request Webhook Events|Processes merge request webhook events in GitLab.|
|Process GitLab Pipeline Webhook Events​|Processes pipeline webhook events in GitLab.|
|Process GitLab Push Webhook Events​|Processes push webhook events in GitLab.|

## Spoke webhooks

Bi-directional webhooks can be setup to be notified about the required events. Routing policy defines conditions that must be met to notify the ServiceNow app. These conditions are based on the events in GitLab for which you wish to be notified about. When the conditions are met, routing policy triggers the associated subflow, which in turn automates the GitLab tasks.

The bi-directional webhooks requires separate setup and can be used independently without using the spoke actions. By default, the GitLab Webhooks application is available in the GitLab spoke and has the following modules:

|Webhook|Description|
|-------|-----------|
|GitLab Webhook Registries|Displays the list of available webhook registries.|
|GitLab Webhook Routing Policies|Displays the list of available webhook routing policies.|

## Spoke module

The GitLab spoke provides Gitlab Token Management application that includes the Gitlab Token Managements module. You should record here to authenticate requests from your ServiceNow instance.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the GitLab spoke](../task/setup-gitlab-spoke.md#).


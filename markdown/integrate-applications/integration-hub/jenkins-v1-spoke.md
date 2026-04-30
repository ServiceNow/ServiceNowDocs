---
title: Jenkins Spoke
description: Manage builds, users, settings, and jobs on the Jenkins server. Retrieve Jenkins data to use in a flow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 6
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Jenkins Spoke

Manage builds, users, settings, and jobs on the Jenkins server. Retrieve Jenkins data to use in a flow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

All versions between 1.651.1 and 2.150.3.

## Spoke version

Jenkins spoke v2.3.0 is the latest version.

## Spoke actions

The Jenkins spoke provides actions to automate the Jenkins tasks when events occur in the ServiceNow instance. Available actions include:

<table id="table_ds2_wwk_4fb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Build Management

</td><td>

Delete Build

</td><td>

Deletes a build from a Jenkins server job.

</td></tr><tr><td>

Get All Builds

</td><td>

Retrieves all the builds for a given Jenkins server job. Returns the URL, build number, and class of each build.

</td></tr><tr><td>

Get Build History

</td><td>

Retrieves a range of build history for a given job from the Jenkins server.

</td></tr><tr><td>

Get Build Information

</td><td>

Retrieves the build timestamp, build status, and complete build information of a given job from the Jenkins server.

</td></tr><tr><td>

Get Build Number

</td><td>

Retrieves the build number for a Jenkins server job based on a pre-defined build filter, such as the last successful build.

</td></tr><tr><td>

Perform a Build

</td><td>

Executes a job on the Jenkins server.

</td></tr><tr><td rowspan="7">

Configuration Management

</td><td>

Create Jenkins Credentials

</td><td>

Creates the Jenkins server credentials.

</td></tr><tr><td>

Create Node

</td><td>

Creates a node that you can launch with the Java Web Start software. A node is a machine that is part of the Jenkins environment and capable of executing jobs.

</td></tr><tr><td>

Delete Node

</td><td>

Deletes a node from the Jenkins server.

</td></tr><tr><td>

Get CSRF Token

</td><td>

Retrieves a CSRF token if your Jenkins server has the "Prevent Cross Site Request Forgery exploits" option enabled.

 **Note:** If your Jenkins server has CSRF protection enabled, use this action to retrieve a token for use by the rest of the flow. The action outputs the token as a data pill for use in other actions in the flow.

</td></tr><tr><td>

Get Version

</td><td>

Retrieves the Jenkins server version.

</td></tr><tr><td>

Restart Jenkins

</td><td>

Restarts the Jenkins server.

</td></tr><tr><td>

Test Connection

</td><td>

Tests the connection to the Jenkins server.

</td></tr><tr><td rowspan="11">

Job Management

</td><td>

Copy Job

</td><td>

Creates a job by copying an existing Jenkins server job.

</td></tr><tr><td>

Create Folder

</td><td>

Creates a Jenkins server folder to organize the jobs.

</td></tr><tr><td>

Create Job

</td><td>

Creates a Jenkins server job from an XML file.

</td></tr><tr><td>

Delete Folder

</td><td>

Deletes an existing Jenkins server folder.

</td></tr><tr><td>

Delete Job

</td><td>

Deletes a Jenkins server job.

</td></tr><tr><td>

Get All Jobs From Folder

</td><td>

Retrieves all the jobs from a given Jenkins server folder. Returns the class and name of each job up to the specified number of levels.

</td></tr><tr><td>

Get Build timestamp

</td><td>

Retrieves the build timestamp of a specified Jenkins server job.

</td></tr><tr><td>

Get Console Output

</td><td>

Retrieves the build console output of a Jenkins server job.

</td></tr><tr><td>

Get Job Configuration

</td><td>

Retrieves the XML configuration for a Jenkins server job.

</td></tr><tr><td>

Reload Job

</td><td>

Reloads a Jenkins server job.

</td></tr><tr><td>

Rename Job

</td><td>

Renames a Jenkins server job.

</td></tr><tr><td rowspan="2">

User Management

</td><td>

Create User

</td><td>

Creates a Jenkins server user.

</td></tr><tr><td>

Delete User

</td><td>

Deletes an existing Jenkins server user.

</td></tr><tr><td rowspan="5">

View Management

</td><td>

Add Job To View

</td><td>

Adds a job to the Jenkins server view. Views are containers to organize jobs. As a Jenkins instance grows, you can create views for appropriate groups and categories. For example, you may want to create a Build view, which only displays the build-specific jobs.

</td></tr><tr><td>

Create View

</td><td>

Creates a Jenkins server view.

</td></tr><tr><td>

Delete View

</td><td>

Deletes a Jenkins server view.

</td></tr><tr><td>

Get All Jobs From View

</td><td>

Retrieves all jobs from a Jenkins server view. Returns the class and the name of the top-level jobs.

</td></tr><tr><td>

Remove Job From View

</td><td>

Removes a job from a Jenkins server view.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

<table id="table_ugm_jds_k2c"><thead><tr><th>

AI Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Jenkins View Management AI Agents

</td><td>

Manages job records and retrieves details of all jobs from a Jenkins server view.

</td></tr><tr><td>

Jenkins Job Management AI Agents

</td><td>

Manages jobs and retrieves details of all the jobs from a given Jenkins server folder.

</td></tr><tr><td>

Jenkins Configuration Management AI Agents

</td><td>

Manages a node from the Jenkins server.Retrieves a CSRF token if your Jenkins server has the "Prevent Cross Site Request Forgery exploits" option enabled.

</td></tr><tr><td>

Jenkins User Management AI Agents

</td><td>

Manages the Jenkins server user recor.ds

</td></tr><tr><td>

Jenkins Build Management AI Agents

</td><td>

Manages a build from a Jenkins server job and retrieves the required build details.

</td></tr></tbody>
</table>Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Support for CRSF tokens

If your Jenkins server has the "Prevent Cross Site Request Forgery exploits" option enabled, certain actions require a unique token. Use the Get CSRF Token action to retrieve a token for use by the rest of the flow. The action outputs the token as a data pill for use in other actions in the flow.

## Connection and credential requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Jenkins Connection &amp; Credential Alias record to authorize actions. To use the spoke connection alias, create an associated Connection record and an associated Credential record.

For information about setting up the spoke, see [Set up Jenkins spoke](../task/set-up-jenkins-v1.md#).

## MID Server requirements

These actions use the REST calls, which must run on a MID Server. Use the connection record associated with the Jenkins alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


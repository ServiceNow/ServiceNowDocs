---
title: Jenkins v2 Spoke
description: Manage builds, users, settings, and jobs on the Jenkins server. Retrieve Jenkins data to use in a flow.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Jenkins v2 Spoke

Manage builds, users, settings, and jobs on the Jenkins server. Retrieve Jenkins data to use in a flow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Jenkins v2 spoke v1.2.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke requirements

The Jenkins v2 spoke v2 requires generating an API token. See [Security Hardening: New API token system in Jenkins 2.129+](https://jenkins.io/blog/2018/07/02/new-api-token-system/) for more information about the API tokens.

## Supported versions

All versions between 2.176.2 to 2.222.1.

## Spoke modules

You can configure the Jenkins v2 spoke v2 to receive updates from Jenkins at your ServiceNow instance. In the routing policies, conditions that must be met to receive updates at your ServiceNow instance are defined. When the conditions are met, routing policy triggers the associated subflow, which in turn automates the Jenkins tasks. This requires separate setup and can be used independently without using the spoke actions. See [Set up a webhook for the Jenkins spoke](../task/receive-jenkins-upd.md#) for information regarding setting up and configuring the webhooks. To use other conditions in the routing policy or customize the default subflows, see [Customize a webhook](../task/receive-jenkins-upd.md#).

Routing policies and subflows support these fields:

-   Keywords
-   Build Number
-   Job Name
-   Job Path
-   Show Related Fields

By default, the Jenkins v2 application is available in the Jenkins v2 spoke and has these modules:

|Module|Description|
|------|-----------|
|Webhook Answer Subflows|Details of the webhook authorization key to authorise requests from Jenkins.|
|Webhook Client Detail|Details about the subflows in Jenkins v2 spoke.|

The Jenkins v2 spoke v2 includes these tables:

-   Jenkins v2 Webhook Answer Subflow \[sn\_jenkinsv2\_spoke\_webhook\_answer\_subflow\]
-   Jenkins Webhook Client Details \[sn\_jenkinsv2\_spoke\_webhook\_client\_details\]

## Spoke subflows

The Jenkins v2 spoke provides sample subflows to demonstrate automating Jenkins tasks. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Build Jenkins Job|Receives updates from Jenkins at the ServiceNow instance.|
|Jenkins Webhook Answer Subflow: Process build information|Builds Jenkins job and retrieves the information. To customize this subflow, create a copy of the subflow and change it as per your requirement.|
|Build Jenkins Job with Parameters|Builds Jenkins job with the specified parameters and retrieves the information.|

## Spoke actions

The Jenkins v2 spoke provides actions to automate Jenkins tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Build Management|Delete Build|Deletes a build from a Jenkins server job.|
|Get Build ID|Retrieves the Build ID of an executed job from the Jenkins server.|
|Get Build Timestamp|Retrieves build timestamp of a given job from the Jenkins server.|
|Get Console Output|Retrieves build console output for a given job from Jenkins Server.|
|List Builds|Retrieves all the builds for a given job from the Jenkins server.|
|Perform Build with Parameters|Executes a job with parameters on the Jenkins server.|
|Get Build History|Retrieves a range of build history for a given job from Jenkins Server.|
|Get Build Information|Retrieves the build timestamp, build status, and complete build information of a given job from the Jenkins server.|
|Get Build Number|Retrieves the build number for a Jenkins server job based on a pre-defined build filter, such as last successful build.|
|Perform Build|Executes a job on the Jenkins server.|
|Look up Builds by Date Range|Retrieves all the builds between date range for a given job from the Jenkins server.|
|Look up Commits by Build|Retrieves the commits of a particular build for a given job from the Jenkins server.|
|Look up Stage Nodes by Build|Retrieves information about the Sonar actions, restartable stages, and nodes of all stages of a particular build for a given pipeline job from the Jenkins server.|
|Look up Stages by Build|Retrieves the build status, start time, end time, duration, and stages of a particular build for a given pipeline job from the Jenkins server.|
|Look up Test Report by Build|Retrieves information about the test summaries, total number of executed tests, passed tests, failed tests, skipped tests, and time taken to execute JUnit tests in a particular build for a given job from the Jenkins server.|
|Configuration Management|Create Node|Creates a node that you can launch with Java Web Start software. A node is a machine that is part of the Jenkins environment and capable of executing jobs.|
|Delete Node|Deletes a node from the Jenkins server.|
|Get Version|Retrieves the Jenkins server version.|
|Restart Jenkins|Restarts the Jenkins server.|
|Test Connection|Tests the connection to the Jenkins server.|
|Job Management|Copy Job|Creates a job by copying an existing Jenkins server job.|
|Create Folder|Creates a Jenkins server folder to organize jobs.|
|Create Job|Creates a Jenkins server job from an XML file.|
|Delete Folder|Deletes an existing Jenkins server folder.|
|Delete Job|Deletes a Jenkins server job.|
|List Jobs By Folder|Retrieves all the jobs for a given folder from the Jenkins server.|
|Get Job Configuration|Retrieves the XML configuration for a Jenkins server job.|
|Reload Job|Reloads a Jenkins server job.|
|Rename Job|Renames a Jenkins server job.|
|User Management|Create User|Creates a Jenkins server user.|
|Delete User|Deletes an existing Jenkins server user.|
|View Management|Add Job To View|Adds a job to the Jenkins server view. Views are containers to organize jobs. As a Jenkins instance grows, you can create views for appropriate groups and categories. For example, you may want to create a Build view, which only displays build-specific jobs.|
|Create View|Creates a Jenkins server view.|
|Delete View|Deletes a Jenkins server view.|
|List Jobs By View|Retrieves all jobs from a view on the Jenkins server.|
|Remove Job From View|Removes a job from a Jenkins server view.|

## Spoke triggers

Use triggers in the Jenkins spoke to subscribe to the required events. The endpoint enables webhooks to connect with your ServiceNow instance. You can configure the flows to execute only when the specified trigger conditions are met. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Build Management|Build Aborted|Trigger initiates when a Jenkins build is aborted.|
|Build Failed|Trigger initiates when a Jenkins build fails.|
|Build Success|Trigger initiates when a Jenkins build is successful.|
|Build Unstable|Trigger initiates when a Jenkins build is unstable.|
|Job Management|Pipeline Failed|Trigger initiates when a Jenkins pipeline fails.|

## Connection and credential requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Jenkins v2 Connection &amp; Credential Alias record to authorize actions. To use the spoke connection alias, create an associated Connection record and an associated Credential record. For information about setting up the spoke, see [Set up the Jenkins spoke](../task/set-up-jenkins.md#).

## MID Server requirements

These actions use REST calls, which must run on a MID Server. Use the connection record associated with the Jenkins alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


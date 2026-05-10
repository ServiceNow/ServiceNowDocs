---
title: Microsoft Azure DevOps Pipelines Spoke
description: The Microsoft Azure DevOps Pipelines spoke enables you to automate your work on pipelines on Azure DevOps. Create a flow with the actions that automate your work on Azure DevOps. For example, create a flow that automates the retrieval of the details of logs for a pipeline. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure DevOps Pipelines Spoke

The Microsoft Azure DevOps Pipelines spoke enables you to automate your work on pipelines on Azure DevOps. Create a flow with the actions that automate your work on Azure DevOps. For example, create a flow that automates the retrieval of the details of logs for a pipeline.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Azure DevOps Pipelines REST API version 7.0 and Azure DevOps Server 2022 but may be compatible with the later versions.

## Spoke version

Microsoft Azure DevOps Pipelines spoke v1.0.0 is the latest version.

## Spoke requirements

-   Spoke dependencies are installed
-   Personal access token is generated on Azure DevOps
-   Microsoft Azure DevOps Pipelines alias is set up on your ServiceNow instance
-   Microsoft Azure DevOps Pipelines spoke plugin is installed on your ServiceNow instance

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   com.glide.hub.action\_type.datastream​
-   com.glide.hub.integration.runtime​
-   com.glide.cobject​
-   com.glide.hub.action\_step.rest​

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke actions

The Microsoft Azure DevOps spoke provides actions to automate Azure DevOps Pipelines' tasks when events occur in your ServiceNow instance. Available actions include:

**Note:** To execute the actions, you must first set up an outbound integration by configuring the Microsoft Azure DevOps Pipelines spoke connection and credential record.

|Category|Action|Description|
|--------|------|-----------|
|Pipeline Management|Look up Pipelines Stream​|Retrieves the details of all pipelines such as ID and name for an Azure DevOps project.|
|Look up Pipeline|Retrieves the details of a pipeline such as the ID and name of the pipeline.|
|Run Management|Run Pipeline​|Runs a pipeline based on the details you specify.|
|Look up Run​|Retrieves details of a run such as name and ID for a pipeline.|
|Look up Runs|Retrieves the list of the top 10000 runs such as name and ID for a pipeline.|
|Log Management|Look up Logs|Retrieves the details of all logs such as URL and signed content for a corresponding pipeline run.|
|Look up Log|Retrieves the details of a log object such as ID and URL for a corresponding pipeline run.|
|Artifact Management|Look up Artifact​|Retrieves an artifact object from a pipeline run.|
|Utility Actions|Attach File to ServiceNow Record​|Attaches the log or artifact file to a ServiceNow record.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).


---
title: Google Cloud Storage Spoke
description: Manage storage and retrieval of data in Google Cloud from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Cloud Storage Spoke

Manage storage and retrieval of data in Google Cloud from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud Storage spoke v1.1.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Google Cloud Storage account requirements

The Google Cloud Storage spoke requires a custom app that you create in Google Cloud Platform.s

## Supported versions

This spoke was built for API version v1, but may be compatible with later versions.

## Spoke subflows

The Google Cloud Storage spoke provides sample subflows to demonstrate automating Google Cloud Storage tasks. To customize the sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Move An Object|Moves an object from the source bucket to destination bucket.|
|Rename An Object|Renames the specified object.|

## Spoke actions

The Google Cloud Storage spoke provides actions to automate Google Cloud Storage when events occur in ServiceNow. For the spoke actions to be performed, you must ensure that your project or organization in Google Cloud Platform has the mentioned permissions. Available spoke actions include:

<table id="table_byd_1tb_4lb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th>

Permissions Required

</th></tr></thead><tbody><tr><td rowspan="3">

Bucket Access Control Management

</td><td>

Create/Update Bucket Access Control

</td><td>

Creates or updates a bucket access control.

</td><td>

-   storage.buckets.get
-   storage.buckets.getIamPolicy
-   storage.buckets.setIamPolicy
-   storage.buckets.update

</td></tr><tr><td>

Delete Bucket Access Control

</td><td>

Deletes the specified bucket access control.

</td><td>

-   storage.buckets.get
-   storage.buckets.getIamPolicy
-   storage.buckets.setIamPolicy
-   storage.buckets.update

</td></tr><tr><td>

List All Bucket Access Controls

</td><td>

Retrieves the list of all bucket access controls.

</td><td>

-   storage.buckets.get
-   storage.buckets.getIamPolicy

</td></tr><tr><td rowspan="8">

Bucket Management

</td><td>

Create Bucket

</td><td>

Creates a bucket in Google Cloud Storage.

</td><td>

storage.buckets.create

</td></tr><tr><td>

Delete A Bucket

</td><td>

Deletes the specified bucket in Google Cloud Storage.

</td><td>

storage.buckets.delete

</td></tr><tr><td>

Get Bucket Details

</td><td>

Retrieves details of the specified bucket in Google Cloud Storage.

</td><td>

-   storage.buckets.get
-   storage.buckets.getIamPolicy

</td></tr><tr><td>

Get Bucket Labels

</td><td>

Retrieves labels of the specified bucket in Google Cloud Storage.

</td><td>

-   storage.buckets.get
-   storage.buckets.getIamPolicy

</td></tr><tr><td>

Get IAM Policy

</td><td>

Retrieves IAM policy of the specified bucket in Google Cloud Storage.

</td><td>

storage.buckets.getIamPolicy

</td></tr><tr><td>

List All Buckets

</td><td>

Retrieves details of all buckets in Google Cloud Storage.

</td><td>

-   storage.buckets.list
-   storage.buckets.getIamPolicy

</td></tr><tr><td>

Update Bucket Details

</td><td>

Updates details of the specified bucket in Google Cloud Storage.

</td><td>

-   storage.buckets.update
-   storage.buckets.setIamPolicy

</td></tr><tr><td>

Update Bucket IAM Policy

</td><td>

Updates IAM policy of the specified bucket in Google Cloud Storage.

</td><td>

storage.buckets.setIamPolicy

</td></tr><tr><td rowspan="3">

Object Access Control Management

</td><td>

Create/Update Object Access Control

</td><td>

Creates or updates a object access control.

</td><td>

-   storage.objects.get
-   storage.objects.getIamPolicy
-   storage.objects.setIamPolicy
-   storage.objects.update

</td></tr><tr><td>

Delete Object Access Control

</td><td>

Deletes the specified object access control.

</td><td>

-   storage.objects.get
-   storage.objects.getIamPolicy
-   storage.objects.setIamPolicy
-   storage.objects.update

</td></tr><tr><td>

List All Object Access Controls

</td><td>

Retrieves the list of all object access controls.

</td><td>

-   storage.objects.get
-   storage.objects.getIamPolicy

</td></tr><tr><td rowspan="9">

Object Management

</td><td>

Copy Object

</td><td>

Copies an object from one bucket to another bucket.

</td><td>

-   storage.objects.create \(for the destination bucket\)
-   storage.objects.delete \(for the destination bucket\)
-   storage.objects.get \(for the source bucket\)

</td></tr><tr><td>

Delete An Object

</td><td>

Deletes an object in a bucket.

</td><td>

storage.objects.delete

</td></tr><tr><td>

Download Object To ServiceNow

</td><td>

Downloads the specified object to ServiceNow.

</td><td>

-   storage.objects.get
-   storage.objects.getIamPolicy

</td></tr><tr><td>

Get Object Details

</td><td>

Retrieves the details of the specified object.

</td><td>

-   storage.objects.get
-   storage.objects.getIamPolicy

</td></tr><tr><td>

List All Objects

</td><td>

Retrieves list of all objects in the specified bucket.

</td><td>

-   storage.objects.list
-   storage.objects.getIamPolicy

</td></tr><tr><td>

Rewrite An Object

</td><td>

Rewrites an object from the source bucket to destination bucket.

</td><td>

-   storage.objects.create \(for the destination bucket\)
-   storage.objects.delete \(for the destination bucket\)
-   storage.objects.get \(for the source bucket\)

</td></tr><tr><td>

Update Object Details In A Bucket

</td><td>

Updates details of the specified object in a bucket.

</td><td>

-   storage.objects.update
-   storage.objects.setIamPolicy

</td></tr><tr><td>

Update Object Storage Class

</td><td>

Updates storage class of the specified object.

</td><td>

-   storage.objects.update
-   storage.objects.setIamPolicy

</td></tr><tr><td>

Upload An Object

</td><td>

Uploads an object to the specified bucket.

</td><td>

-   storage.objects.create
-   storage.objects.delete

</td></tr></tbody>
</table>For more information about the required permissions, see [IAM permissions reference](https://cloud.google.com/iam/docs/permissions-reference).

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Google Cloud Storage object management AI agent|Manages object management tasks \(that is, object management, storage class updates, and object transfers\) in Google Cloud Storage.|
|Google Cloud Storage object access control management AI agent|Manages object access control management tasks \(that is, object access controls, deletes, lists, and creates or updates access control settings\) in Google Cloud Storage.|
|Google Cloud Storage bucket management AI agent|Manages bucket management \(that is, creates, updates, and deletes buckets, retrieves bucket details, manages IAM policies, lists all available buckets\) in Google Cloud Storage.|
|Google Cloud Storage bucket access AI agent|Manages bucket access \(that is, bucket access controls, create or update bucket access controls, and delete bucket access controls\) in Google Cloud Storage.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Cloud Storage spoke](../task/setup-gstorage.md#).


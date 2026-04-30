---
title: Amazon Elastic Container Service Spoke
description: Manage clusters, instances, services and so on, in Amazon Elastic Container Service account from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Amazon Elastic Container Service Spoke

Manage clusters, instances, services and so on, in Amazon Elastic Container Service account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon Elastic Container Service spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for Amazon Elastic Container Service API version 2014-11-13, but may be compatible with later versions.

## Spoke requirements

-   User with full access to Amazon Elastic Container Service.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Amazon Elastic Container Service spoke provides actions to automate Amazon Elastic Container Service tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Cluster Management|Create Cluster|Creates an Amazon ECS cluster.|
|Delete Cluster|Deletes the specified cluster.|
|Look up Cluster|Retrieves the specified cluster.|
|Look up Clusters|Retrieves the list of existing clusters.|
|Update Cluster Settings|Updates settings of the specified cluster.|
|Instance Management|Deregister Container Instance|Deregisters an Amazon ECS container instance from the specified cluster.|
|Look up Container Instances|Lists Amazon Elastic Container Service container instances.|
|Register Container Instance|Registers an EC2 instance into the specified cluster.|
|Service Management|Create Service|Runs and maintains the desired number of tasks from the specified task definition.|
|Delete Service|Deletes a specified service within a cluster.|
|Look up Service|Retrieves the specified service running in your cluster.|
|Look up Services|Retrieves the services that are running in a specified cluster.|
|Update Service|Updates the parameters of a service.|
|Task Definition Management|Deregister Task Definition|Deletes the specified task set within a service.|
|Look up Task Definition|Deregisters the specified task definition by family and revision.|
|Look up Task Definitions|Deregisters the specified tasks definition by family and revision.|
|Register Task Definition|Creates a task set in the specified cluster and service.|
|Task Management|Create Task Set|Creates a task set in the specified cluster and service.|
|Delete Task Set|Deletes the specified task set within a service.|
|Look up Task Set|Lists the task sets in the specified cluster and service.|
|Run Task|Starts a task using the specified task definition.|
|Start Task|Starts a task from the specified task definition on the specified container instance or instances.|
|Stop Task|Stops the specified running task.|
|Update Task Set|Modifies the specifies task set.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon Elastic Container Service spoke](../tasks/setup-amzn-elastic-contnr.md#).


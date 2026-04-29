---
title: AWS OpsWorks Spoke
description: Manage elastic load balancers, instances, relational database services, and others in AWS OpsWorks account from the ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS OpsWorks Spoke

Manage elastic load balancers, instances, relational database services, and others in AWS OpsWorks account from the ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for AWS OpsWorks API version 2013-02-18, but may be compatible with later versions.

## Spoke requirements

-   User with full access to AWS OpsWorks
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke version

AWS OpsWorks spoke v1.0.2 is the latest version.

## Spoke actions

The AWS OpsWorks spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Elastic Load Balancer Management|Attach Elastic Load Balancer|Attaches an Elastic Load Balancer to a specified layer.|
|Detach Elastic Load Balancer|Detaches a specified Elastic Load Balancing instance from its layer.|
|Look up Elastic Load Balancers|Retrieves information about Elastic Load Balancers of the specified stack ID.|
|Instance Management|Create Instance|Creates an instance in the specified stack.|
|Delete Instance|Deletes the specified instance.|
|Look up Instances|Retrieves the list of instances for the specified stack ID.|
|Start Instance|Starts the specified instance.|
|Start Stack Instances|Starts instances of the specified stack.|
|Stop Instance|Stops the specified instance.|
|Stop Stack Instances|Stops instances of the specified stack.|
|Relational Database Service Management|Deregister RDS DB Instance|Deregisters an Amazon RDS instance.|
|Look up RDS DB Instances|Retrieves the list of Amazon RDS instances.|
|Register RDS DB Instance|Registers an Amazon RDS instance with a stack.|
|Stack Management|Delete App|Deletes a specified app.|
|Delete Layer|Deletes the specified layer.|
|Get Stack Summary|Retrieves information of the specified stack ID.|
|Get User Profile|Retrieves information about the user profile.|
|Look up Apps|Retrieves information about the apps in the specified stack ID.|
|Look up Deployments|Retrieves information about the deployments in the specified stack ID.|
|Look up Layers|Retrieves list of the layers in the specified stack ID.|
|Look up Permissions|Retrieves information about the permissions for the specified stack ID or IAM user.|
|Look up Stacks|Retrieves list of information of the specified stack ID.|
|Tag Management|Add Tags|Adds tags for the specified resource.|
|Delete Tags|Deletes tags of the specified resource.|
|Look up Tags|Retrieves list of tags for the specified resource.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS OpsWorks spoke](../task/setup-aws-opsworks.md#).


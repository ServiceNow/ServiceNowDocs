---
title: AWS CloudFormation Spoke
description: Model and provision AWS resources in your cloud environment using AWS CloudFormation from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS CloudFormation Spoke

Model and provision AWS resources in your cloud environment using AWS CloudFormation from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for AWS CloudFormation API version 2010-05-15, but may be compatible with later versions.

## Spoke version

AWS CloudFormation spoke v1.1.4 is the latest version.

## Spoke requirements

-   User with full access to AWS CloudFormation.
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

## Spoke actions

The AWS CloudFormation spoke provides actions to automate AWS CloudFormation tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Change Set Management|Create Change Set|Creates a list of changes that will be applied to a stack so that you can review the changes before executing them.|
|Delete Change Set|Deletes the specified change set.|
|Execute Change Set|Updates the stack using the input information that was provided when the specified change set was created.|
|Get Change Set|Returns the details of the specified change set.|
|Look up Change Sets|Returns basic information of each active change set for a stack.|
|Stack Management|Cancel Update Stack|Cancels an update on the specified stack.|
|Continue Update Rollback|For the specified stack that is in the UPDATE\_ROLLBACK\_FAILED state, continues rolling the state back to the UPDATE\_ROLLBACK\_COMPLETE state.|
|Create Stack|Creates a stack as specified in the template.|
|Delete Stack|Deletes the specified stack.|
|Get Stack Policy|Returns the stack policy for a specified stack.|
|Get Template|Returns the template body for a specified stack.|
|Look up Stack Events|Returns all stack related events for a specified stack in reverse chronological order.|
|Look up Stack Set Operation Stream|Returns the summary of information for the operations performed on a stack set.|
|Look up Stack Set Operation Result Stream|Returns the summary of information for the results of a stack set operation.|
|Look up Stack Resources|Returns details of all resources of the specified stack.|
|Look up Stacks|Returns the details for the specified stack.|
|Set Stack Policy|Sets policy for the specified stack.|
|Update Stack|Updates the specified stack.|
|Validate Template|Validates a specified template. AWS CloudFormation initially verifies if the template is a valid JSON. If it is not a valid JSON, AWS CloudFormation verifies if the template is a valid YAML. If both these checks fail, AWS CloudFormation returns a template validation error.|
|Stack Set Management|Create Stack Instance|Creates stack instances for the specified accounts, within the specified regions.|
|Create Stack Set|Creates Stack set in the specified region.|
|Delete Stack Instance|Deletes stack instances for the specified accounts, in the specified regions.|
|Delete Stack Set|Deletes the specified Stack set.|
|Get Stack Set|Returns the details of the specified stack set.|
|Look up Stack Instances|Returns information about stack instances that are associated with the specified stack set.|
|Look up Stack Sets|Returns summary information about all the stack sets or the stack sets with the specified Status.|
|Update Stack Set|Updates the specified stack set and associated stack instances in the specified accounts and Regions.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS CloudFormation spoke](../task/setup-awscloud-form.md#).


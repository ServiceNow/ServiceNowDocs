---
title: Amazon EC2 Spoke
description: Integrate ServiceNow instance with Amazon Elastic Compute Cloud \(EC2\). Manage Amazon instances, Amazon Machine Images \(AMIs\), Key Pairs, and Tags from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Amazon EC2 Spoke

Integrate ServiceNow instance with Amazon Elastic Compute Cloud \(EC2\). Manage Amazon instances, Amazon Machine Images \(AMIs\), Key Pairs, and Tags from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon EC2 spoke v1.4.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported version

This spoke was built for API version 2016-11-15, but may be compatible with later versions.

## Spoke requirements

-   User with full access to Amazon EC2.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

## Spoke flows and subflows

This spoke has no flows and subflows.

## Available sample conversational subflows

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Conversational subflow|Description|
|----------------------|-----------|
|Look up Images - Sample|Returns information on the specified images.|
|Run instances - Sample|Executes the specified instances.|

## Spoke actions

The Amazon EC2 spoke provides actions to automate Amazon EC2 tasks when events occurs in ServiceNow. Available actions include:

<table id="table_g4c_rw3_glb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="5">

Amazon Machine Image Management

</td><td>

Copy Image

</td><td>

Copies an Amazon Machine Image \(AMI\) from the specified source region to the current region.

</td></tr><tr><td>

Create Image

</td><td>

Creates an Amazon EBS supported AMI from an Amazon EBS supported instance that is either running or stopped.

</td></tr><tr><td>

Deregister Image

</td><td>

Deregisters the specified AMI.

</td></tr><tr><td>

List Image Attribute

</td><td>

Retrieves the specified AMI attribute.

</td></tr><tr><td>

List Images

</td><td>

Retrieves the specified AMIs.

</td></tr><tr><td rowspan="13">

Instance Management

</td><td>

Get Instance Attribute

</td><td>

Retrieves the specified attribute of the specified instance.

</td></tr><tr><td>

Get Instances Status

</td><td>

Retrieves the status of the specified instance.

</td></tr><tr><td>

Get Password Data

</td><td>

Retrieves the encrypted administrator password for an active Windows instance.

</td></tr><tr><td>

List Instance Types

</td><td>

Retrieves the list of all instance types in an AWS region.

</td></tr><tr><td>

List Instances

</td><td>

Retrieves a list of all instances.

</td></tr><tr><td>

Monitor Instances

</td><td>

Enables monitoring for all active instances.

</td></tr><tr><td>

Reboot Instances

</td><td>

Reboots the specified instances.

</td></tr><tr><td>

Run Instances

</td><td>

Launches the specified number of instances using an AMI.

</td></tr><tr><td>

Start Instances

</td><td>

Starts the specified instances.

</td></tr><tr><td>

Stops Instances

</td><td>

Stops the specified instances.

</td></tr><tr><td>

Terminate Instances

</td><td>

Shutdowns or terminates the specified instances.

</td></tr><tr><td>

Unmonitor Instances

</td><td>

Disables monitoring for the specified running instances.

</td></tr><tr><td>

Update Instance Attribute

</td><td>

Updates the specified attribute for the specified instance. **Note:** You can specify only one attribute at a time. Before you update an attribute, ensure that the instance is stopped.

</td></tr><tr><td rowspan="3">

Key Pair Management

</td><td>

Create Key Pair

</td><td>

Creates a 2048-bit SSH-2 RSA key pair.

</td></tr><tr><td>

Delete Key Pair

</td><td>

Deletes the specified key pair.

</td></tr><tr><td>

List Key Pair

</td><td>

Retrieves the specified key pair or a list of all key pairs.

</td></tr><tr><td rowspan="2">

Region and Availability Zone Management

</td><td>

Get Availability Zones

</td><td>

Retrieves the list of availability zones in the specified AWS region.

</td></tr><tr><td>

List Regions

</td><td>

Retrieves the list of all AWS regions.

</td></tr><tr><td rowspan="3">

Tag Management

</td><td>

Create Tags

</td><td>

Adds or overwrites the specified set of tags from the specified set of resources.

</td></tr><tr><td>

Delete Tags

</td><td>

Deletes the specified set of tags from the specified set of resources.

</td></tr><tr><td>

List Tags

</td><td>

Retrieves the list of tags for the specified region.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon EC2 spoke](../task/setup-amazon-ec2.md#).


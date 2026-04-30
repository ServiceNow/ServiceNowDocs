---
title: Amazon VPC Spoke
description: Provision a logically isolated section of the AWS cloud using Amazon VPC and launch the required AWS resources in a virtual network, from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon VPC Spoke

Provision a logically isolated section of the AWS cloud using Amazon VPC and launch the required AWS resources in a virtual network, from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon VPC spoke v1.0.3 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported version

This spoke was built for API version 2016-11-15, but may be compatible with later versions.

**Note:** If you use different API version, ensure that you change the API version in all spoke actions.

## Spoke requirements

-   User with full access to Amazon VPC.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke subflows

The Amazon VPC spoke provides sample subflows to demonstrate automating Amazon VPC tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Delete Subnet|Deletes the specified subnet. Before you delete the subnet, you must terminate all the running instances in the subnet.|
|Delete VPC|Deletes the specified VPC. Before you delete the VPC, you must terminate all the associated instances.|

## Spoke actions

The Amazon VPC spoke provides actions to automate Amazon VPC tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Network &amp; Security Group Management|Add Egress Rules To A Security Group|Adds the specified egress rules to a security group.|
|Add Ingress Rules To A Security Group|Adds the specified ingress rules to a security group.|
|Create Security Group|Creates a security group.|
|Delete Egress Rules From Security Group|Removes the specified egress rules from security group. Values must match the existing rule's values exactly.|
|Delete Ingress Rules From Security Group|Adds the specified ingress rules to a security group.|
|Delete Security Group|Deletes a security group.|
|List Security Groups|Lists the specified security groups or all of your security groups.|
|Lookup Security Group|Retrieves the specified security group.|
|Virtual Private Cloud Management|Create Subnet|Creates a subnet in an existing VPC.|
|Create VPC|Creates a VPC with the specified IPv4 CIDR block and can optionally request an IPv6 CIDR block for the VPC.|
|Delete NAT Gateway|Deletes the specified NAT gateway. Deleting a NAT gateway disassociates its Elastic IP address, but does not release it.|
|Delete Route Table|Deletes the specified route table. You must disassociate the route table from any subnets before you can delete it.|
|Delete Subnet|Deletes the specified subnet. You must terminate all running instances in the subnet before you can delete the subnet.|
|Delete VPC|Deletes the specified VPC. You must detach or delete all gateways and resources that are associated with the VPC before you can delete it or use Delete VPC subflow.|
|Delete VPC Peering Connection|Deletes a VPC peering connection. Either the owner of the requester VPC or the owner of the accepter VPC can delete the VPC peering connection if it's in the active state.|
|Detach Internet Gateway|Detaches an internet gateway from a VPC, disabling connectivity between the internet and the VPC.|
|Detach Route Table|Disassociates a subnet from a route table.|
|List Internet Gateways|Retrieves the details of the required internet gateways.|
|List NAT Gateways|Retrieves the details of the required NAT gateways.|
|List Route Tables|Retrieves the details of the required route tables.|
|List Subnets|Retrieves the details of the required subnets in an existing VPC.|
|List VPC Peering Connections|Retrieves the details of the required VPC peering connections.|
|Virtual Private Network Management|Detach VPN Gateway|Detaches a virtual private gateway from a VPC.|
|List VPN Gateways|Retrieves the details of the required virtual private gateways.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon VPC spoke](../../integrationhub-store-spokes/task/setup-vpc.md#).


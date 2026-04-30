---
title: AWS Elastic Load Balancing Spoke
description: Manage load balancers, tags, and target groups in AWS account from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# AWS Elastic Load Balancing Spoke

Manage load balancers, tags, and target groups in AWS account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AWS Elastic Load Balancing spoke v1.0.1 is the latest version.

## Supported versions

This spoke was built for AWS Elastic Load Balancing API version 2012-06-01.

## Spoke requirements

-   User with full access to AWS Elastic Load Balancing.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - XML Parser \(com.glide.hub.action\_step.xmlparser\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The AWS Elastic Load Balancing spoke provides actions to automate AWS Elastic Load Balancing tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Elastic Load Balancer Management|Create Load Balancer|Creates an application load balancer or network load balancer.|
|Create Load Balancer Listener|Creates a listener for the specified application load balancer or network load balancer.|
|Delete Load Balancer|Deletes the specified application load balancer or network load balancer.|
|Delete Load Balancer Listener|Deletes the specified listener.|
|Get Account Limits|Lists the Elastic Load Balancing resource limits for the AWS account.|
|Get Load Balancer Attributes|Lists the attributes for the specified application load balancer or network load balancer.|
|Look up Listeners|Retrieves list of the specified listeners for the specified application load balancer or network load balancer.|
|Look up Load Balancers|Retrieves list of the specified load balancers or all the load balancers.|
|Look up SSL Policies|Lists all policies used for SSL negotiation.|
|Update Load Balancer Attributes|Updates the specified attributes of the specified application load balancer or network load balancer.|
|Tag Management|Add Tags|Adds the specified tags to the specified Elastic Load Balancing resource.|
|Delete Tags|Removes the specified tags from the specified Elastic Load Balancing resource.|
|Look up Tags|Retrieves list of the tags for the specified resources.|
|Target Group Management|Create Target Group|Creates a target group.|
|Deregister Target|Deregisters the specified targets from the specified target group.|
|Get Target Group Attributes|Lists the attributes for the specified target group.|
|Get Target Health|Lists the health of the targets.|
|Look up Target Groups|Retrieves details of the specified target groups or all of your target groups.|
|Register Target|Registers the specified targets with the specified target group.|
|Update Target Group|Updates the health checks used for evaluating the health state of the targets in the specified target group.|
|Update Target Group Attribute|Updates the specified attributes of the specified target group.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS Elastic Load Balancing spoke](../../integrationhub/tasks/setup-load-balancing.md#).


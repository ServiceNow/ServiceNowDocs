---
title: AWS Lambda Spoke
description: Manage alias and function in AWS Lambda from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS Lambda Spoke

Manage alias and function in AWS Lambda from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AWS Lambda spoke v1.1.3 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   [AWS IAM Spoke](aws-iam-spoke-1.md) \(sn\_aws\_iam\_spoke\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported version

This spoke was built for API version 2010-05-08, but may be compatible with later versions.

**Note:** If you use different API version, ensure that you change the API version in all spoke actions.

## Spoke requirements

-   User with full access to Lambda.

    **Note:** The AWSLambdaFullAccess IAM policy must be assigned to the user. See [Identity-based IAM policies for AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/access-control-identity-based.html) for more information about the IAM policy.

-   Access Key ID and Secret Access Key of the user as obtained in the IAM Console. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke actions

The AWS Lambda spoke provides actions to automate AWS Lambda tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Alias Management|Create Function Alias|Creates an alias for the specified function.|
|Delete Function Alias|Deletes the specified alias of the function.|
|Get Function Alias Details|Retrieves the details of the specified function alias.|
|List Function Aliases|Retrieves the list of all aliases for the specified function.|
|Update Function Alias|Updates settings of the specified alias.|
|Function Management|Add Permission|Grants an AWS service or another account permission to use the specified AWS Lambda function.|
|Create Function|Creates a function in AWS Lambda.|
|Delete Function|Deletes the specified AWS Lambda function or function version.|
|Get Function Details|Retrieves details of the specified AWS Lambda function or function version.|
|Invoke Function|Invokes the specified AWS Lambda function.|
|List Functions|Retrieves list of all AWS Lambda functions in a region|
|Update Function Code|Updates code of the specified AWS Lambda function.|
|Update Function Configuration|Updates configuration of the specified AWS Lambda function.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS Lambda spoke](../task/setup-aws-lambda.md#).


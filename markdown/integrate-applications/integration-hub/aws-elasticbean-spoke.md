---
title: AWS Elastic Beanstalk Spoke
description: AWS Elastic Beanstalk enables you to quickly deploy and manage applications in the Amazon AWS Cloud. Elastic Beanstalk reduces management complexity without restricting choice or control. When you upload your application, Elastic Beanstalk automatically handles capacity provisioning, load balancing, scaling, and application health monitoring.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS Elastic Beanstalk Spoke

AWS Elastic Beanstalk enables you to quickly deploy and manage applications in the Amazon AWS Cloud. Elastic Beanstalk reduces management complexity without restricting choice or control. When you upload your application, Elastic Beanstalk automatically handles capacity provisioning, load balancing, scaling, and application health monitoring.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AWS Elastic Beanstalk spoke v1.0.3 is the latest version.

## Supported versions

AWS Elastic Beanstalk API version 2010-12-01.

## Spoke subflows

There are no subflows provided with the AWS Elastic Beanstalk spoke.

## Spoke actions

The AWS Elastic Beanstalk spoke provides actions to perform Elastic Beanstalk tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Look Up Account Attributes|Retrieves attributes related to AWS Elastic Beanstalk that is associated with the calling AWS account.|
|Application Management|Check DNS Availability|Checks if the specified CNAME is available.|
|Create application|Creates an application that has one configuration template name default and no application versions.|
|Create Application Version|Creates an application version for the specified application.|
|Create Configuration Template|Creates an AWS Elastic Beanstalk configuration template, associated with a specific Elastic Beanstalk application.|
|Delete Application|Deletes the specified application along with all associated versions and configurations.|
|Delete Application Version|Deletes the specified version from the specified application.|
|Delete Configuration Template|Deletes the specified application along with all associated versions and configurations.|
|Look Up Application Versions|Retrieves the descriptions of existing applications.|
|Look up Applications|Retrieves the descriptions of existing applications.|
|Update Application|Updates the specified application to have the specified properties.|
|Update Application Version|Updates the specified application version to have the specified properties.|
|Update Configuration Template|Updates the specified configuration template to have the specified properties or configuration option values.|
|Environment Management|Create Environment|Launches an AWS Elastic Beanstalk environment for the specified application.|
|Create Storage Location|Creates a bucket in Amazon S3 to store application versions, logs, and other files used by Elastic Beanstalk environments.|
|Get Environment Health|Lists the overall health information of the specified environment.|
|Look up Available Solution Stacks|Lists the available solution stack names.|
|Look up Environment Resources|Lists AWS resources for the specified environment.|
|Look up Environments|Retrieves the information about the existing environments.|
|Look Up Instances Health|Retrieves the descriptions of existing applications.|
|Restart App Server|Restarts the application container server running on each Amazon EC2 instance in the environment.|
|Swap Environment CNAMEs|Swaps the CNAMEs of two environments.|
|Terminate Environment|Terminates the specified environment.|
|Update Environment|Updates the specified environment.|

## AWS Elastic Beanstalk account requirements

The AWS Elastic Beanstalk spoke requires a credential that you create in the Amazon Web Services Management Console.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Create a credential record for the AWS Elastic Beanstalk spoke](../task/setup-elasticbean-spk.md#).


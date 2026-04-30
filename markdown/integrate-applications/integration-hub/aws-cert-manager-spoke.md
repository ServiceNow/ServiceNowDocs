---
title: AWS Certificate Manager Spoke
description: Manage certificates in AWS Certificate Manager account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS Certificate Manager Spoke

Manage certificates in AWS Certificate Manager account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AWS Certificate Manager spoke v1.0.1 is the latest version.

## Supported versions

This spoke was built for AWS Certificate Manager API version 2015-12-08, but may be compatible with later versions.

## Spoke requirements

-   User with full access to AWS Certificate Manager.
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

The AWS Certificate Manager spoke provides actions to automate AWS Certificate Manager tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Certificate Management|Delete Certificate|Deletes a certificate and its associated private key.|
|Get Certificate|Retrieves an Amazon-issued certificate and its certificate chain.|
|Get Certificate Details|Retrieves detailed metadata about the specified ACM certificate.|
|Import Certificate|Imports a certificate to AWS Certificate Manager \(ACM\) to use with services that are integrated with ACM.|
|Look up Certificates|Retrieves a list of certificate ARNs and domain names.|
|Request Certificate|Requests an ACM certificate for use with other AWS services.|
|Resend Validation Email|Resends the email that requests domain ownership validation.|
|Update Certificate Option|Updates details of the specified certificate.|
|Tag Management|Add Tags To Certificate|Associates a set of tags with the required certificate.|
|Look up Tags For Certificate|Retrieves all tags that are associated with the specified certificate.|
|Remove Tags From Certificate|Removes the association of tags from certificate.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS Certificate Manager spoke](../task/setup-aws-cert-manager.md#).


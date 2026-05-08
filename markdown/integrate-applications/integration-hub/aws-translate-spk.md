---
title: AWS Translate Spoke
description: Integrate your ServiceNow instance with AWS Translate to detect languages in the text and translate text to the required language.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AWS Translate Spoke

Integrate your ServiceNow instance with AWS Translate to detect languages in the text and translate text to the required language.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported version

This spoke was built for AWS Translate API version 2017-07-01 and AWS Comprehend version 2017-11-27, but may be compatible with later versions.

**Note:**

-   If you use different API version, ensure that you change the API version in all spoke actions.
-   The current version of the AWS Translate spoke is not compatible with dynamic translation.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke requirements

-   User with full access to AWS Translate.
-   Access Key ID and Secret Access Key of the user. Record these values for later use. For more information, see [Create an access key](../task/aws-translate-setup.md#).

For more information about creating user and providing the required access, see [AWS Identity and Access Management Documentation](https://docs.aws.amazon.com/iam/index.html) site.

## Spoke flow

The AWS Translate spoke provides a sample flow, Translate Short Description when Incident is Created to demonstrate translating the short description to Spanish when an incident is created. You can customize the sample flow as per your requirement by creating a copy of it in the required scope.

## Spoke actions

The AWS Translate spoke provides actions to automate translating tasks when events occur in ServiceNow. Available actions include:

<table id="table_upl_dtm_fvb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Language Management

</td><td>

Detect Dominant Language

</td><td>

Detects the language of text using AWS Comprehend service.**Note:** Provide the text for which you want to detect the dominant language in the action input **Text**. The output is a JSON string that contains an array of the detected languages. One of the elements in the array is **Score**. This is a decimal number and its value is between `0` and `1`.

![Using Score in subsequent actions.](../image/aws-translate-score.png)

When the action is executed, the Languages Detected action output may not display any runtime value. However, the output data pill still holds the response data and can be used in the subsequent actions in the flow or subflow.

![Score value in the output response body.](../image/aws-translate-datapill.png)

</td></tr><tr><td>

Translate Management

</td><td>

Translate Text

</td><td>

Translates text from the source language to the target language using AWS Translate service.**Note:**

-   For **Source Language** and **Target Language**, input values can’t be selected until a valid input value is provided for **Region**.
-   If you select **Auto** from the **Source Language** list, the AWS Translate API uses the AWS Comprehend service to automatically detect the language. In this case, you must provide the region that supports Amazon Comprehend. Else, the request returns an error indicating the auto-detect is not supported.

</td></tr></tbody>
</table>**Note:** The actions have **Region** as an input. To retrieve the list of available regions, use the List Regions action from the [Amazon EC2 Spoke](amazon-ec2-spoke-1.md).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS Translate spoke](../task/aws-translate-setup.md#).


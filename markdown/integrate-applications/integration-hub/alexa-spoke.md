---
title: Amazon Alexa Spoke
description: Manage intents, skills, vendors, and slots in your Amazon Alexa account from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Amazon Alexa Spoke

Manage intents, skills, vendors, and slots in your Amazon Alexa account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Amazon Alexa API version v1, but may be compatible with later versions.

## Spoke version

Amazon Alexa v1.2.0 is the latest version.

## Spoke requirements

Admin access to [Amazon Developer Portal](https://developer.amazon.com/) and AWS Lambda.

## Important security considerations

Be aware of these considerations to securely use Amazon Alexa:

-   Amazon stores voice recordings of the Amazon Alexa smart assistant customers forever unless the Amazon Alexa account is configured to delete the recordings. For more information about deleting the voice recordings, see [Delete Alexa Voice Recordings Automatically](https://www.amazon.com/gp/help/customer/display.html?nodeId=G68KUKTXN92WY3C3).
-   To stop recording conversations, turn the microphone off on the Alexa enabled devices.
-   To ensure safety and protect privacy when using Alexa devices, take measures such as, choosing a strong password and using a pin for voice purchases.
-   Install or activate only the legitimate skills.
-   Ensure proper credential management in AWS Lambda when invoking the ServiceNow Rest API.
-   Ensure that your AWS Lambda function is accessible to only the required skills by adding the Alexa Skills Kit trigger to the required AWS Lambda function. Using these triggers, you can allow only the required skills to access your AWS Lambda function. For more information, see [Configure the trigger for a Lambda function](https://developer.amazon.com/en-US/docs/alexa/custom-skills/host-a-custom-skill-as-an-aws-lambda-function.html#configuring-the-alexa-skills-kit-trigger).

    **Note:** Use the AWS Lambda function as an endpoint of your skill. If your are using custom web service, validate the skills. For more information, see [Host a Custom Skill as a Web Service](https://developer.amazon.com/en-US/docs/alexa/custom-skills/host-a-custom-skill-as-a-web-service.html).

-   You can securely store your sensitive data in the AWS Lambda function using environment variables. For more information, see Using [AWS Lambda environment variables](https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Amazon Alexa spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Intent Management|Create Intent|Creates an intent for the specified skill and locale.|
|Delete Intent|Deletes the specified intent from the specified skill.|
|Look up Intents|Lists available intents for the specified skill and locale.|
|Update Intent|Updates an intent for the specified skill and locale.|
|Interaction Model Management|Get Interaction Model|Gets the interaction model schema for the specified skill.|
|Look up Interaction Model Versions|Lists the available versions of the interaction model for the specified skill.|
|Update Interaction Model|Updates the interaction model for the specified skill and locale.|
|Skill Management|Create Skill|Submits a skill creation request for the specified Vendor ID.|
|Delete Skill|Deletes the specified skill.|
|Get Skill|Gets the details for the specified skill.|
|Get Skill Status|Gets the status for the specified skill.|
|Look up Skills|Lists the skills for the specified Vendor ID.|
|Update Skill|Submits a request to update a skill for the specified Vendor ID.|
|Slot Type Management|Create Slot Type|Creates a slot type for the specified skill in the specified locale.|
|Look up Slot Types|Lists available slot types for the specified skill and locale.|
|Update Slot Type|Updates the specified slot type for the specified skill and locale.|
|Vendor Management|Look up Vendors|Lists details of all the available vendors.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon Alexa spoke](../task/ssetup-alexa.md#).


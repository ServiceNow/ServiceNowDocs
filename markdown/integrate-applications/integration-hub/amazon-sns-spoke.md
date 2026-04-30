---
title: Amazon SNS Spoke
description: Integrate ServiceNow with Amazon SNS. Manage topics and subscriptions, and delegate roles in Amazon SNS from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Amazon SNS Spoke

Integrate ServiceNow with Amazon SNS. Manage topics and subscriptions, and delegate roles in Amazon SNS from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon SNS spoke spoke v1.1.0 is the latest version.

## Supported version

This spoke was built for API version 2010-03-31, but may be compatible with later versions.

## Spoke requirements

-   User with full access to Amazon SNS.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For information about creating and accessing keys, see the [AWS Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-security-credentials.html) documentation.

## Spoke subflows

The Amazon SNS spoke provides a sample subflow to demonstrate automating Amazon SNS tasks. To customize the sample subflow, copy it to a new application scope. Available sample subflow is, Amazon SNS Subscription. The subflow receives three types of messages; Notification, Subscription Confirmation, and Unsubscribe Confirmation. This subflow is triggered when you configure your ServiceNow instance to receive events from Amazon SNS. For more information about the required configurations, see [Receive events at your ServiceNow instance from Amazon SNS](../task/notification-sns.md#).

**Note:** Spoke subflow can be used independently to subscribe for notifications from Amazon SNS. For more information about the configurations, see [Receive events at your ServiceNow instance from Amazon SNS](../task/notification-sns.md#).

## Spoke actions

The Amazon SNS spoke provides actions to automate Amazon SNS tasks when events occur in ServiceNow. Available actions include:

<table id="table_gvv_pl5_pkb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Permission Management

</td><td>

Add Permission

</td><td>

Adds a statement to a topic's access control policy and grants access for the specified AWS accounts for the specified actions.

</td></tr><tr><td>

Remove Permission

</td><td>

Removes a statement from a topic's access control policy and revokes access for the specified AWS accounts for the specified actions.

</td></tr><tr><td rowspan="7">

Subscription Management

</td><td>

Confirm Subscription

</td><td>

Verifies intent of endpoint owner to receive messages by validating the token sent to the endpoint through an earlier Subscribe action.

</td></tr><tr><td>

Create Subscription

</td><td>

Creates a subscription on a topic.

</td></tr><tr><td>

Delete Subscription

</td><td>

Deletes a subscription on a topic.

</td></tr><tr><td>

Get Subscription Attributes

</td><td>

Retrieves all properties of a subscription.

</td></tr><tr><td>

List Subscriptions

</td><td>

Retrieves a list of all subscriptions to a specific region.**Note:** In your flow, use the Get Subscription Attributes action before this action to populate the required records.

</td></tr><tr><td>

List Subscriptions By Topic

</td><td>

Retrieves a list of the subscriptions to a specific topic.**Note:** In your flow, use the Get Subscription Attributes action before this action to populate the required records.

</td></tr><tr><td>

Set Subscription Attributes

</td><td>

Enables a subscription owner to set an attribute of the subscription to a new value.

</td></tr><tr><td rowspan="8">

Topics Management

</td><td>

Create Topic

</td><td>

Creates a topic for which notifications can be published.

</td></tr><tr><td>

Delete Topic

</td><td>

Deletes a topic and all its subscriptions.

</td></tr><tr><td>

Get Topic Attributes

</td><td>

Retrieves all properties of a topic. Topic properties retrieved may differ based on the authorization of the user.

</td></tr><tr><td>

List Topics

</td><td>

Retrieves a list of the requester's topics.**Note:** In your flow, use the Get Topic Attributes action before this action to populate the required records.

</td></tr><tr><td>

Publish Batch Messages to Topic

</td><td>

Sends batch messages to an Amazon SNS topic.

</td></tr><tr><td>

Publish Message to Topic

</td><td>

Sends a message to an Amazon SNS topic.

</td></tr><tr><td>

Set Topic Delivery Policy

</td><td>

Enables a topic owner to set a delivery policy of the topic to a new value.

</td></tr><tr><td>

Set Topic Display Name

</td><td>

Enables a topic owner to set a display name of the topic to a new value.

</td></tr></tbody>
</table>**Note:** Spoke actions can be used independently without subscribing to notifications from Amazon SNS.

## Spoke module

The Amazon SNS spoke adds an AWS Configurations module to your ServiceNow instance. If you want receive events at your ServiceNow instance from Amazon SNS, you must specify the subflow internal name here. For more information about the required configurations, see [Receive events at your ServiceNow instance from Amazon SNS](../task/notification-sns.md#).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon SNS spoke](../task/setup-amazon-sns.md#).


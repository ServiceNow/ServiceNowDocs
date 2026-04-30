---
title: Amazon SQS Spoke
description: Amazon SQS spoke automates various actions on the Amazon SQS based on a trigger in your ServiceNow instance. Set up a flow in the Workflow Studio using the actions and automate tasks on Amazon SQS. For example, you can set up a flow that automates sending messages to a queue.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Amazon SQS Spoke

Amazon SQS spoke automates various actions on the Amazon SQS based on a trigger in your ServiceNow instance. Set up a flow in the Workflow Studio using the actions and automate tasks on Amazon SQS. For example, you can set up a flow that automates sending messages to a queue.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon SQS spoke v1.0.1

is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke actions

The Amazon SQS provides actions to automate tasks on the simple queue services when events occur in your ServiceNow instance. Available actions include:

<table id="table_rtm_khs_1yb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

Message Management

</td><td>

Change Visibility for Message

</td><td>

Changes the visibility of a message from a queue. You specify inputs such as the queue URL and the visibility timeout and the action returns the status of the execution.

</td></tr><tr><td>

Change Visibility for Messages

</td><td>

Changes the visibility of up to 10 messages from a queue. You provide inputs such as the queue URL and the request that comprises the messages' list and the action returns the list of messages and the status of the action.

</td></tr><tr><td>

Delete Message

</td><td>

Deletes a message from a queue. You provide the queue URL and the receipt handle and the action returns the status of the execution.

</td></tr><tr><td>

Delete Messages

</td><td>

Deletes up to 10 messages from a queue. You provide the queue URL and the receipt handle and the action returns the status of the execution.

</td></tr><tr><td>

Receive Message

</td><td>

Retrieves up to 10 messages from a queue. You provide the queue URL and the number of messages as inputs and the action returns the list of messages and the status of the execution.

</td></tr><tr><td>

Send Message

</td><td>

Delivers a message to a queue. You provide inputs such as the queue URL and the message and the action returns outputs such as sequence number and message ID.

</td></tr><tr><td>

Send Messages

</td><td>

Sends up to 10 messages to a queue. You provide inputs such as the queue URL and the message and the action returns outputs such as sequence number and message ID. **Note:** You can send messages with size up to 256 KB.

</td></tr><tr><td rowspan="2">

Permission Management

</td><td>

Add Permission

</td><td>

Adds a permission to a queue for a principal. You provide inputs such as the queue URL and the permission label and the action returns the status of the execution.

</td></tr><tr><td>

Remove Permission

</td><td>

Revokes permissions in the queue policy that matches a label. You provide inputs such as the queue URL and the permission label and the action returns the status of the execution.

</td></tr><tr><td rowspan="7">

Queue Management

</td><td>

Create FIFO Queue

</td><td>

Creates a FIFO queue. You can provide inputs such as region and queue name and the action returns the new queue URL and the status of the execution.

</td></tr><tr><td>

Create Standard Queue

</td><td>

Creates a standard queue. You can specify inputs such as region and the queue name and the action returns the queue name and the status of the execution.

</td></tr><tr><td>

Delete Queue

</td><td>

Deletes a queue. You can provide the queue URL and the action returns the estatus of the execution.

</td></tr><tr><td>

Look up Queue Attributes

</td><td>

Retrieves the attributes of a queue. You can specify the queue URL and the action returns the queue attributes.

</td></tr><tr><td>

Look up Queue URL

</td><td>

Retrieves the URL of the specified queue. You can specify inputs such as the region and queue name and the action returns the queue URL.

</td></tr><tr><td>

Look up Queues Stream

</td><td>

Retrieves a list of queues in a region. You provide inputs such as region and page size and the action returns the details.

</td></tr><tr><td>

Purge Queue

</td><td>

Deletes the messages in a queue. You specify the queue URL and the action returns the execution status code.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

To learn to set up the spoke, see [Set up Amazon SQS spoke](../task/set-up-amazon-sqs-spoke.md).


---
title: Acknowledge foundation data sync offering request
description: Acknowledge a foundation data sync \(FDS\) offering request and send a sample payload to help your consumer understand the type of data they’ll receive.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring outbound FDS as providers, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Acknowledge foundation data sync offering request

Acknowledge a foundation data sync \(FDS\) offering request and send a sample payload to help your consumer understand the type of data they’ll receive.

## Before you begin

Role required: admin

## About this task

After a consumer requests an FDS offering, the system generates an FDS request and corresponding FDS subscriptions in your Service Exchange instance.

If **Auto acknowledge FDS Requests** option isn't selected, you must manually acknowledge the consumer's FDS request to inform them that you’re working on the request. Then, send a sample payload to help them understand the type of data they’ll receive.

Also, when a consumer requests an FDS offering, you receive an email notification about the new request, including any required actions.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Open Records** &gt; **FDS Request**.

2.  Open the provider offering request by selecting the record number in the Number column.

3.  Select the **Acknowledge** button.

    The request state changes from Received to Work In Progress.

4.  Send a sample payload for each subscription.

    Each sample payload contains up to five records of sample data.

    1.  From the Foundation Data Provider Subscription related list, open the subscription by selecting the record number in the Number column.

    2.  Select the **Send Sample** button.

        The sample payload sent to your customer is listed under the **Sample Payload** column in the Subscription Items related list.


## Result

A sample payload for each subscription is sent to the consumer as sample data. Consumers can review the sample to verify the data structure and content before accepting the full data synchronization.

## What to do next

[Publish a foundation data subscription](service-bridge-v2-publish-fds-subscription.md).


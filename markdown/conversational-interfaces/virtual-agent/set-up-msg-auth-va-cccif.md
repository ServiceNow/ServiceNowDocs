---
title: Set up message authentication for your custom chat configuration
description: Create a Hash Message Verification record and Message Auth record to set up message authentication for your custom chat integration. This is configured in the Hash Message Verifications \[hash\_message\_verification\] table.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Virtual Agent conversational custom chat integration configuration, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up message authentication for your custom chat configuration

Create a Hash Message Verification record and Message Auth record to set up message authentication for your custom chat integration. This is configured in the Hash Message Verifications \[hash\_message\_verification\] table.

## Before you begin

[Configure a provider for your custom chat integration](create-provider-va-cccif.md).

Role required: admin

## About this task

You can create a Hash Message Verification record and Message Auth record to set up message authentication.

## Procedure

1.  Navigate to **All**, and then enter `hash_message_verification.list` in the filter.

2.  On the Hash Message Verifications page, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the authentication token, such as TwilioSMSTestAppAuthToken.|
    |Description|Description of the authentication token, such as "Twilio SMS Testing application Auth Token."|
    |Secret|Authentication token \(random string\).|

4.  Click **Submit**.

5.  Navigate to **All**, and then enter `message_auth.list` in the filter.

6.  On the Message Auths page, click **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the message authentication, such as VA Twilio SMS Test App Message Authentication.|
    |Provider|Provider, such as Twilio.|
    |Group name|Name of the group or team of the provider channel.|
    |Service Portal|Option to redirect users to a service portal for authentication during account linking.|
    |Inbound message verification|Hash message token that was created.|
    |Outbound message creation|Hash message token that was created.|
    |Outbound service token|Token passed to the sender subflow that is used to invoke REST endpoint for the chat client. Use the outbound token to send a message using the REST API.|

8.  Click **Submit**.


## What to do next

[Create a channel identifier for your custom chat integration](create-channel-id-va-cccif.md)


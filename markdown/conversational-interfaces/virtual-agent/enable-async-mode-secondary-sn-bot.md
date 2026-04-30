---
title: Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance
description: Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance to use ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use ServiceNow Virtual Agent as a secondary bot in synchronous or asynchronous mode, Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance

Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance to use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect.

## Before you begin

Role required: admin

## Procedure

1.  On the secondary bot instance, navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select the VA Bot to Bot record.

3.  In the Endpoint field, specify the outbound endpoint URL of the primary ServiceNow® instance to which the Virtual Agent responses are posted. `http://<primary instance>/api/sn_va_bot_ic/bot_interconnect/va_api_response`

4.  In the Authentication tab, set the Authentication type field to either Basic or OAuth 2.0.

    For more information on configuring a basic authentication profile and OAuth 2.0 profile, see Configure a REST message with basic auth and Configure a REST message with OAuth respectively.

5.  Click **Update**.

6.  In the HTTP Methods section, select the postMessage method and specify the endpoint URL. `http://<primary instance>/api/sn_va_bot_ic/bot_interconnect/va_api_response`

7.  Click **Update**.


**Parent Topic:**[Use ServiceNow Virtual Agent as a secondary bot in synchronous or asynchronous mode](../concept/use-servicenow-virtual-agent-as-a-secondary-bot-in-synchronous-or-asynchronous-mode_0.md)


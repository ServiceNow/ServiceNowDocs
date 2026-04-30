---
title: Provider configuration in Voice
description: For both inbound and outbound calls, a provider configuration contains settings about the involved components and message transformers for a specific third-party phone system provider. Any request from that phone system provider is handled within ServiceNow based on these settings.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scripting for operation handlers, Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Provider configuration in Voice

For both inbound and outbound calls, a provider configuration contains settings about the involved components and message transformers for a specific third-party phone system provider. Any request from that phone system provider is handled within ServiceNow based on these settings.

To view the available provider configurations, navigate to **ServiceNow Voice - Core** &gt; **Provider Configurations**.

Any request from a third-party phone system is passed into a ServiceNow instance through the CTI Operation endpoint of the CTI API. For information about this API, see [CTI API](https://www.servicenow.com/docs/access?context=cti-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US). Based on the provider and the component specified in the endpoint, the corresponding message transformers are invoked to perform the following:

-   Transform the request from the third-party phone system before passing the request to an operation handler.
-   Transform the response from the operation handler before passing it on to the third-party phone system.

## Provider component

For each component or node available in the third-party phone system, a provider configuration contains a provider component. It contains a mapping between the component and a message transformer.

To view the available provider components, navigate to **ServiceNow Voice - Core** &gt; **Provider Components**.

## Message transformer

A message transformer defines how a request and response can be transformed between a third-party phone system and the ServiceNow instance.

-   The **Input Transformer** field has a script that defines how a request from a third-party phone system should be transformed within the ServiceNow instance before passing the request to an operation handler.
-   The **Output Transformer** field has a script that defines how the response from the operation handler should be transformed before passing it on to the third-party phone system.

To view the available message transformers, navigate to **ServiceNow Voice - Core** &gt; **Provider Message Transformers**.

## Provider configuration for the integration of Voice with Amazon Connect

For the ServiceNow Voice integration with the ServiceNow Voice with Amazon Connect application, the **AWS Connect Default Handler** provider component is available by default.

**Note:** The ServiceNow Voice with Amazon Connect integration with ServiceNow application \[sn\_cti\_amzn\_cct\] must be installed from the ServiceNow® Store. For information on installing this application, see [Install ServiceNow Voice applications](../task/install-ccc-apps.md).

For each node that can be used an integration point between Amazon services and the ServiceNow instance, the following provider components and the corresponding message transformers are available.

|Node|Provider component|Message transformer|
|----|------------------|-------------------|
|Get Customer Input|sn\_aws\_connect\_lex\_intent\_processor\_component|AWS - Lex - Intent - Message Transformer \(SN Proxy\)|
|Invoke AWS Lambda Function|sn\_aws\_connect\_lambda\_proxy\_component|AWS - Connect - Lambda - Message Transformer|

When a customer dials using a phone number, a call is placed through the Amazon Connect 's phone system. Using one of its components, Amazon Connect provides the request to the ServiceNow instance through the CTI Operation endpoint of the CTI API. For information about this API, see [CTI API](https://www.servicenow.com/docs/access?context=cti-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US). Based on the provider and the component specified here, the corresponding message transformers are invoked to perform the following:

-   Transform the request from Amazon Connect before passing the request to an operation handler.
-   Transform the response from the operation handler before passing it on to Amazon Connect.

**Parent Topic:**[Scripting for operation handlers](cloud-call-center-api.md)


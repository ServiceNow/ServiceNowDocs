---
title: Integrate ServiceNow voice assistant with Genesys Cloud service \(SIP\)
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Genesys Cloud service using the Session Initiation Protocol \(SIP\) communication channel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/integrate-voice-service-with-genesys-sip.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
keywords: [Genesys, Genesys Cloud, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, SIP]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Genesys Cloud service \(SIP\)

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Genesys Cloud service using the Session Initiation Protocol \(SIP\) communication channel.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/create-an-ai-voice-service.md) for more information.

Role required: sn\_aia.admin

## About this task

Connect your Genesys Cloud contact center to a ServiceNow voice assistant using the Session Initiation Protocol \(SIP\) communication channel. After the integration is configured, Genesys Cloud routes calls to the ServiceNow SIP endpoint, where the AI voice agent handles the interaction. When call handling is complete, the integration supports transferring the caller to a live agent queue using the SIP REFER transfer method.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to Genesys Cloud service and select **Edit**.

3.  Select **Communication channels** from the guided setup navigation.

4.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

5.  Select the **Telephony provider** tab.

6.  From the **Select communication channels** dropdown, select **Session Initiation Protocol \(SIP\)**.

7.  From the **CCaaS provider** dropdown, select **Genesys**.

    Enter the **Transfer number/address** and note the following generated values. You will need these to configure the SIP trunk in your Genesys Cloud account.

    |Field|Description|
    |-----|-----------|
    |Transfer number/address|SIP URI to transfer the call to your Genesys Cloud service. Use the format `user@domain`, where the user part is up to 16 characters and the domain part is up to 256 characters. URI parameters are not supported.|
    |Transfer method|Read-only. Set to **REFER** for Genesys Cloud service.|
    |ServiceNow SIP Trunk information|Read-only. The ServiceNow SIP fully qualified domain name \(FQDN\) for your region, used to route calls from Genesys Cloud service to the voice assistant. For SIP trunk configuration details including IP addresses and FQDNs per region, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612).|
    |x-snc-param|Read-only. Generated token to send to your Genesys Cloud account to authenticate requests to the voice assistant.|

    \[Omitted image "voice-agents-genesys-sip-integration.png"\] Alt text: Genesys SIP integration configuration showing the Transfer number/address, Transfer method, ServiceNow SIP Trunk information, and x-snc-param fields.

8.  In your Genesys Cloud account, configure the SIP trunk using the ServiceNow SIP FQDN and authentication token.

    Use the **ServiceNow SIP Trunk information** and the **x-snc-param** token generated in the previous step. For SIP trunk configuration details, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612).


## Result

Genesys Cloud service is connected to your ServiceNow voice assistant. Incoming calls routed through Genesys Cloud service are handled by the AI voice agent, which responds with a greeting and processes the caller's requests.

## What to do next

For live agent transfer configuration and advanced SIP trunk settings, refer to your Genesys Cloud documentation or contact Genesys support.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/integrating-voice-service-with-ccaas-providers.md)


---
title: Integrate ServiceNow voice assistant with Five9
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Five9 voice service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/integrate-voice-service-with-five9.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [Five9, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, SIP]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Five9

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Five9 voice service.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/create-an-ai-voice-service.md) for more information.

Role required: sn\_aia.admin

## About this task

Connect your Five9 contact center to a ServiceNow voice assistant using the Session Initiation Protocol \(SIP\) communication channel. After the integration is configured, Five9 routes calls to the ServiceNow SIP endpoint, where the AI voice agent handles the interaction. When call handling is complete, the integration supports transferring the caller to a live agent queue.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to Five9 and select **Edit**.

3.  Select **Communication channels** from the guided setup navigation.

4.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

5.  Select the **Telephony provider** tab.

6.  From the **Select communication channels** dropdown, select **Session Initiation Protocol \(SIP\)**.

7.  From the **CCaaS provider** dropdown, select **Five9**.

    The following read-only fields are generated. Use these values to configure the SIP trunk in your Five9 account.

    |Field|Description|
    |-----|-----------|
    |Transfer method|Read-only. Set to **BYE** for Five9.|
    |ServiceNow SIP Trunk information|Read-only. The ServiceNow SIP fully qualified domain name \(FQDN\) for your region, used to route calls from Five9 to the voice assistant. For SIP trunk configuration details including IP addresses and FQDNs per region, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612).|
    |x-snc-param|Read-only. Generated token to send to your Five9 account to authenticate requests to the voice assistant.|

    \[Omitted image "voice-agents-five9-integration.png"\] Alt text: Five9 integration configuration showing the Transfer method, ServiceNow SIP Trunk information, and x-snc-param fields.

8.  In your Five9 IVR, add the **x-snc-param** as a SIP custom header using the Set Variable Module.

    In the Set Variable Module, use the following function to pass the **x-snc-param** value generated in the previous step:

    ```
    PUT(ToIVA, "x-snc-param", "*x-snc-param value*")
    ```


## Result

Five9 is connected to your ServiceNow voice assistant. Incoming calls routed through Five9 are handled by the AI voice agent, which responds with a greeting and processes the caller's requests.

## What to do next

For live agent transfer configuration and advanced SIP trunk settings, refer to the [Five9 BYO SIP Trunk Integration Guide](https://documentation.five9.com/bundle/byo-sip-trunk-integration-guide/resource/byo-sip-trunk-integration-guide.pdf) or contact Five9 support.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/integrating-voice-service-with-ccaas-providers.md)


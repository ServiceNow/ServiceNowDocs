---
title: Integrate ServiceNow voice assistant with a custom SIP provider
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with a custom Session Initiation Protocol \(SIP\) provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/integrate-voice-service-with-custom-sip.html
release: australia
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 3
keywords: [custom SIP, SIP, voice assistant, voice integration, telephony provider, AI voice agent, SIP trunk]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, AI Agent Studio \(legacy\), Enable AI experiences]
---

# Integrate ServiceNow voice assistant with a custom SIP provider

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with a custom Session Initiation Protocol \(SIP\) provider.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md) for more information.
-   Access to your SIP-capable telephony system with permissions to configure SIP trunks.

Role required: sn\_aia.admin

## About this task

Connect any SIP-capable telephony system to a ServiceNow voice assistant using the Custom provider option. Use this integration when your organization routes calls through its own SIP infrastructure rather than a named CCaaS provider. Inbound calls arrive over the provided SIP trunk and are handled by the AI voice agent. When call handling is complete, the integration supports transferring the caller back to your telephony system or terminating the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to your SIP provider and select **Edit**.

3.  Select the **Settings** tab.

4.  Select **Communication channels** from the guided setup navigation.

5.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

6.  Select the **Telephony provider** tab.

7.  From the **Communication channel** dropdown, select **Session Initiation Protocol \(SIP\)**.

8.  From the **CCaaS provider** dropdown, select **Custom**.

9.  Configure the transfer settings.

    |Field|Description|
    |-----|-----------|
    |Transfer method|Select **REFER** or **BYE** depending on the transfer protocol supported by your telephony system. Select **REFER** to transfer the caller to a live agent queue using SIP REFER. Select **BYE** to terminate the SIP session when call handling is complete, which allows your telephony system to take over the call independently.|
    |Transfer number/address|The SIP URI to transfer the call to your telephony system. Use the format `user@domain`. This field is visible only when **Transfer method** is set to **REFER**.|

10. Select a **Context transport format** to specify how the voice assistant passes conversation context when transferring or terminating a call.

    |Option|Description|
    |------|-----------|
    |X-snc-context \(default\)|Passes conversation context using the ServiceNow proprietary SIP header. Maintains conversation state and session metadata across call transfers, handoffs, and interactions.|
    |User-to-User \(UUI\)|Passes conversation context using the standard SIP User-to-User header, enabling transfers without losing conversation state. Use this option when your telephony system supports the SIP UUI header.|
    |None|No session or interaction data is shared between systems.|

    \[Omitted image "ai-voice-assistant-custom-sip-configuration.png"\] Alt text: Custom SIP provider configuration showing SIP communication channel, custom provider, REFER transfer method, transfer number/address, and X-snc-context selected for context transport.

11. Select **Save and continue**.

    The **ServiceNow SIP Trunk information** section displays a read-only **x-snc-param** value. Copy this token to use it when configuring your SIP trunk to authenticate requests to the voice assistant.

12. Configure your SIP-capable telephony system to route calls to the **ServiceNow SIP FQDN** for your region.

    For SIP trunk configuration details including IP addresses and FQDNs per region, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612).

13. Pass the **x-snc-param** value as a SIP header on outbound calls to the voice assistant.


## Result

Your custom SIP provider is connected to the ServiceNow voice assistant. Incoming calls routed through your SIP trunk are handled by the AI voice agent. When call handling is complete, the voice assistant transfers or terminates the call according to the configured transfer method.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md)


---
title: Integrate ServiceNow voice assistant with NICE CXone
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with NICE CXone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/integrate-voice-service-with-nice.html
release: australia
topic_type: task
last_updated: "2026-07-03"
reading_time_minutes: 3
keywords: [NICE CXone, NICE, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, SIP]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with NICE CXone

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with NICE CXone.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md) for more information.
-   Access to your CXone account with permissions to configure SIP trunks.
-   NICE API credentials, including the API endpoint, token endpoint, username, password, client ID, and client secret. Contact your CXone account admin to retrieve this information.

Role required: sn\_aia.admin

## About this task

Connect your CXone contact center to a ServiceNow voice assistant using the Session Initiation Protocol \(SIP\) communication channel. After the integration is configured, CXone routes calls to the ServiceNow SIP endpoint, where the AI voice agent handles the interaction. When call handling is complete, the integration supports transferring the caller to a live agent queue using the SIP REFER transfer method.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to CXone and select **Edit**.

3.  Select **Communication channels** from the guided setup navigation.

4.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

5.  Select the **Telephony provider** tab.

6.  From the **Select communication channels** dropdown, select **Session Initiation Protocol \(SIP\)**.

7.  From the **CCaaS provider** dropdown, select **NICE**.

    Enter the values in the **NICE API credentials** section. After saving, copy the generated **x-snc-param** value and paste it in your CXone account to link the assistant.

    |Field|Description|
    |-----|-----------|
    |API endpoint|The CXone API base URL. Must be a valid NICE domain, such as `https://cxone.niceincontact.com` or `https://cxone-gov.niceincontact.com`.|
    |Token endpoint|The CXone OAuth token URL used to generate authentication tokens. Must be a valid NICE domain.|
    |Username|The username for your CXone account.|
    |Password|The password for your CXone account.|
    |Client ID|The OAuth client ID from your CXone account.|
    |Client Secret|The OAuth client secret from your CXone account.|

    After saving the credentials, copy the generated **x-snc-param** value from the page. This is a token that authenticates requests from CXone to the voice assistant. Paste it in your CXone account when configuring the SIP trunk.

    \[Omitted image "voice-agents-nice-integration.png"\] Alt text: The Communication channels guided setup with NICE selected as the CCaaS provider, showing the NICE API Credentials section with the API endpoint, token endpoint, username, and password fields.

8.  In your CXone account, configure the SIP trunk using the **ServiceNow SIP FQDN** and pass the **x-snc-param** value as a SIP header on outbound calls to the voice assistant.

    For SIP trunk configuration details including IP addresses and FQDNs per region, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612). For CXone-side SIP trunk configuration steps, see the [CXone developer documentation](https://developer.niceincontact.com/Documentation/GettingStarted).


## Result

CXone is connected to your ServiceNow voice assistant. Incoming calls routed through CXone are handled by the AI voice agent, which responds with a greeting and processes the caller's requests. When call handling is complete, the voice assistant transfers the caller back to CXone using the REFER method.

## What to do next

Configure the **Onsignal** event action flow in your CXone account. When a voice agent call ends or transfers to a live agent, ServiceNow automatically notifies CXone by sending a signal to the `/interactions/{contactId}/signal` API endpoint, which triggers the Onsignal event action flow. For configuration details, see the [CXone developer documentation](https://developer.niceincontact.com/Documentation/GettingStarted).

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md)


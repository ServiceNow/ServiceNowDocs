---
title: Integrate ServiceNow voice assistant with Nice CXone
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Nice CXone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/integrate-voice-service-with-nice.html
release: zurich
topic_type: task
last_updated: "2026-07-03"
reading_time_minutes: 3
keywords: [NICE CXone, NICE, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, SIP]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, AI Agent Studio, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Nice CXone

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Nice CXone.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-an-ai-voice-service.md) for more information.
-   Access to your CXone account with permissions to configure SIP trunks.
-   Nice API credentials, including the API endpoint, token endpoint, access key ID, access key secret, client ID, and client secret. Work with your Nice account team to obtain the access key ID and secret. See the [CXone developer documentation](https://developer.niceincontact.com/Documentation/GettingStarted) for more information.

Role required: sn\_aia.admin

## About this task

Connect your CXone contact center to a ServiceNow voice assistant using the Session Initiation Protocol \(SIP\) communication channel. After the integration is configured, CXone routes calls to the ServiceNow SIP endpoint, where the AI voice agent handles the interaction. When call handling is complete, the integration supports transferring the caller to a live agent queue using the SIP REFER transfer method.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to CXone and select **Edit**.

3.  Select the **Settings** tab.

4.  Select **Communication channels** from the guided setup navigation.

5.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

6.  Select the **Telephony provider** tab.

7.  From the **Communication channel** dropdown, select **Session Initiation Protocol \(SIP\)**.

8.  From the **CCaaS provider** dropdown, select **Nice**.

    Enter the values in the **Nice API credentials** section.

    |Field|Description|
    |-----|-----------|
    |API endpoint|The CXone API base URL. Must be a valid Nice domain, such as `https://cxone.niceincontact.com` or `https://cxone-gov.niceincontact.com`.|
    |Token endpoint|The CXone OAuth token URL used to generate authentication tokens. Must be a valid Nice domain.|
    |Username|The access key ID from your CXone account. Work with your Nice account team to obtain this credential.|
    |Password|The access key secret from your CXone account. This value is only displayed once when generated. Copy it before navigating away.|
    |Client ID|The OAuth client ID from your CXone account.|
    |Client Secret|The OAuth client secret from your CXone account.|

    After saving the credentials, copy the generated **x-snc-param** value from the page. This is a token that authenticates requests from CXone to the voice assistant. Paste it in your CXone account when configuring the SIP trunk.

9.  Enable context data persistence for the voice service.

    1.  Navigate to `sys_now_assist_deployment_config_attributes.list` and check whether a `persist_context_data` attribute exists for your voice service.

    2.  If the attribute exists, open it and set **Value** to `true`.

        \[Omitted image "voice-agents-persist-context-data.png"\] Alt text: The persist\_context\_data configuration attribute record for the voice service with its value set to true.

    3.  If the attribute does not exist, navigate to `sys_now_assist_deployment_config.list`, open your voice assistant's deployment configuration record, and copy its `sys_id`.

        To copy the `sys_id`, right-click the record header bar and select **Copy sys\_id**.

    4.  Navigate to `sys_now_assist_deployment_config_attributes.list`, click **New**, set **Deployment Configuration** to the `sys_id` you copied, **Name** to `persist_context_data`, and **Value** to `true`, then click **Submit**.

10. In your CXone account, configure the SIP trunk using the **ServiceNow SIP FQDN** and pass the **x-snc-param** value copied in the previous step as a SIP header on outbound calls to the voice assistant.

    For SIP trunk configuration details including IP addresses and FQDNs per region, see [KB3023612](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3023612). For CXone-side SIP trunk configuration steps, see the [CXone developer documentation](https://developer.niceincontact.com/Documentation/GettingStarted).


## Result

CXone is connected to your ServiceNow voice assistant. Incoming calls routed through CXone are handled by the AI voice agent, which responds with a greeting and processes the caller's requests. When call handling is complete, the voice assistant transfers the caller back to CXone using the REFER method.

## What to do next

Configure the **Onsignal** event action flow in your CXone account. When a voice agent call ends or transfers to a live agent, ServiceNow automatically notifies CXone by sending a signal to the `/interactions/{contactId}/signal` API endpoint, which triggers the Onsignal event action flow. For configuration details, see the [CXone developer documentation](https://developer.niceincontact.com/Documentation/GettingStarted).

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md)


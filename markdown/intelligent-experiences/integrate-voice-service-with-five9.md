---
title: Integrate ServiceNow voice assistant with Five9
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Five9 voice service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/integrate-voice-service-with-five9.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [Five9, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, SIP]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, AI Agent Studio, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Five9

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Five9 voice service.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md) for more information.

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

8.  Enable context data persistence for the voice service.

    1.  Navigate to `sys_now_assist_deployment_config_attributes.list` and check whether a `persist_context_data` attribute exists for your voice service.

    2.  If the attribute exists, open it and set **Value** to `true`.

        \[Omitted image "voice-agents-persist-context-data.png"\] Alt text: The persist\_context\_data configuration attribute record for the voice service with its value set to true.

    3.  If the attribute does not exist, navigate to `sys_now_assist_deployment_config.list`, open your voice assistant's deployment configuration record, and copy its `sys_id`.

        To copy the `sys_id`, right-click the record header bar and select **Copy sys\_id**.

    4.  Navigate to `sys_now_assist_deployment_config_attributes.list`, click **New**, set **Deployment Configuration** to the `sys_id` you copied, **Name** to `persist_context_data`, and **Value** to `true`, then click **Submit**.

9.  In your Five9 IVR, add the **x-snc-param** as a SIP custom header using the Set Variable Module.

    In the Set Variable Module, use the following function to pass the **x-snc-param** value generated in the previous step:

    ```
    PUT(ToIVA, "x-snc-param", "*x-snc-param value*")
    ```


## Result

Five9 is connected to your ServiceNow voice assistant. Incoming calls routed through Five9 are handled by the AI voice agent, which responds with a greeting and processes the caller's requests.

## What to do next

For live agent transfer configuration and advanced SIP trunk settings, refer to the [Five9 BYO SIP Trunk Integration Guide](https://documentation.five9.com/bundle/byo-sip-trunk-integration-guide/resource/byo-sip-trunk-integration-guide.pdf) or contact Five9 support.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md)


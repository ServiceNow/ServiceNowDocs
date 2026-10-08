---
title: Set up an AI proxy
description: Configure an AI proxy server to monitor AI commands traveling from your Agent Client Collector \(ACC\) agent to the AI Control Tower \(AICT\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/ai-proxy-setup.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [AI Proxy, AI Control Tower, Agent Client Collector, IT Operations Management]
---

# Set up an AI proxy

Configure an AI proxy server to monitor AI commands traveling from your Agent Client Collector \(ACC\) agent to the AI Control Tower \(AICT\).

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key. For details, see [Configure an agent registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/agent-registration-key-configuration.md).

You must configure ACC with an ICS \(mid-less\) architecture to enable using an AI proxy. For details on configuring ACC without a MID Server, see [Configuring MID-less Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-configuring-without-mid.md).

Role required: agent\_client\_collector\_admin

## Procedure

1.  Retrieve the publicly accessible gateway URL, based on your location.

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
2.  Run the relevant command, depending on the OS you're using.

    -   On a Windows server:

        ```
        msiexec /i <msi_file_path> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<itom_gateway_url>" REGISTRATION_KEY="<agent_registration_key>" INSTANCE_URL="https://<instance_url> AI_PROXY_ENABLED="true" LOCALUSERNAME="LocalSystem" 
        ```

    -   On a Linux or macOS server:

        ```
        sudo CONNECT_WITHOUT_MID="true" ACC_CNC=<itom gateway url> REGISTRATION_KEY=<agent registration key> INSTANCE_URL=<instance url> AI_PROXY_ENABLED="true" LOCALUSERNAME="LocalSystem" bash -c "$(curl -L https://<instance url>/api/sn_acc_shadow_ai/agents/install_agent)"
        ```

    For details on the parameter values in the command, see [Agent Client Collector MID-less installation command parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-ics-command-params.md).


## Result

The AI proxy monitors AI traffic coming from your AI tools. Traffic is either allowed to pass through to the AI Control Tower, or is blocked, depending on your configured AICT policies.

## What to do next

Configure AICT policies to determine which AI resources are blocked, and for whom. For details, see .


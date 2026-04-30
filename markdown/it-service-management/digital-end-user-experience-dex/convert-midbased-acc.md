---
title: Convert MID-based ACC to MID-less
description: Convert MID-based Agent Client Collector \(ACC\) to MID-less ACC by adjusting the configuration in acc.yml, decoupling from a specific MID to enhance flexibility and adaptability.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Getting started, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Convert MID-based ACC to MID-less

Convert MID-based Agent Client Collector \(ACC\) to MID-less ACC by adjusting the configuration in acc.yml, decoupling from a specific MID to enhance flexibility and adaptability.

## Before you begin

Verify that the ACC registration key was set up and the ACC was installed. For more information, see the following:

-   [Create an ACC registration key](setup-acc.md).
-   [Install ACC for DEX on Windows](install-acc-for-dex-windows.md) or [Install ACC for DEX on macOS](install-acc-for-dex-macos.md).

Role required: agent\_admin and agent\_client\_collector\_admin

For more information, see [Agent Client Collector user roles](https://www.servicenow.com/docs/access?context=acc-users&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Procedure

1.  Stop ACC based on your operating system:

    -   For Windows, access Services as administrator and stop the Agent Client Collector Service.
    -   For macOS, execute the command: `sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist;`.
2.  Open the `acc.yml` file.

3.  Edit the instance URL.

4.  Edit the **backend-url** parameter to point to `<ITOM Cloud Services Gateway>`.

    Use one of the following gateways based on the instance location:

    -   `AMER: itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   `EMEA: itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   `APAC: itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
    For more information on how the Agent uses the ITOM Cloud Services Gateway, see [DEX Architecture](../concept/dex-architecture.md).

5.  Configure the following parameters:

    -   connect-without-mid: true
    -   instance-url: &lt;full\_instance\_url&gt;

        For example: https://dex.servicenow.com.

    -   insecure-skip-tls-verify: false
    -   registration-key: &lt;registration key value&gt;

        For more information, see [Create an ACC registration key](setup-acc.md).

6.  Comment out the API key parameter:

    `api-key: "encrypted....”`

7.  Save the file.

8.  Delete files based on your operating system:

    -   On Windows, navigate to `/agent-client-collector/config/cert/cnc` and remove the following files: `cnc_chain.crt` and `priv_key.pem.go`.
    -   On macOS, access `/Library/Application Support/servicenow/agent-client-collector/cert/cnc` and delete the files: `cnc_chain.crt` and `priv_key.pem`.
9.  Delete `assets.db`, `queue.db`, and all subdirectories in the cache folder based on your operating system:

    -   On Windows: `/agent-client-collector/cache`.
    -   On macOS:
        -   For Agent 3.4.1 or above: `/Library/Application Support/servicenow/agent-client-collector/cache`.
        -   For Agent 3.4.0 or below: `/Library/Caches/servicenow/agent-client-collector`.
    **Important:** Keep `agent_now_id` in the cache folder.

10. Initiate the ACC service based on your operating system.

    -   On Windows, open Services as administrator, then start the Agent Client Collector Service.
    -   On macOS, use the command: `sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist`.


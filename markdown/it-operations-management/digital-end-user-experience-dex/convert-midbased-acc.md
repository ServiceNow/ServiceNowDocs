---
title: Convert MID-based ACC to MID-less
description: Convert MID-based Agent Client Collector \(ACC\) to MID-less ACC by adjusting the configuration in the acc.yml file so that ACC doesn't depend on a specific MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/convert-midbased-acc.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 2
breadcrumb: [DEX advanced configuration, Configure, Digital End-User Experience, IT Operations Management]
---

# Convert MID-based ACC to MID-less

Convert MID-based Agent Client Collector \(ACC\) to MID-less ACC by adjusting the configuration in the acc.yml file so that ACC doesn't depend on a specific MID Server.

## Before you begin

Verify that the ACC registration key was set up and the ACC was installed. For more information, see the following:

-   [Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-acc-reg-key.md).
-   [Install ACC for DEX on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/install-acc-for-dex-windows.md) or [Install ACC for DEX on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/install-acc-for-dex-macos.md).

Role required: agent\_admin and agent\_client\_collector\_admin

For more information, see [Agent Client Collector user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-users.md).

## Procedure

1.  Stop ACC based on your operating system:

    -   For Windows, access Services as administrator and stop the Agent Client Collector service.
    -   For macOS, execute the command: `sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist;`.
2.  Open the `acc.yml` file.

3.  Edit the instance URL.

4.  Edit the **backend-url** parameter to point to `<ITOM Cloud Services Gateway>`.

    Use one of the following gateways based on the instance location:

    -   `AMER: itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   `EMEA: itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   `APAC: itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
    For more information about how the agent uses the ITOM Cloud Services Gateway, see [DEX architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-architecture.md).

5.  Configure the following parameters:

    -   **connect-without-mid**: `true`
    -   **instance-url**: &lt;full\_instance\_url&gt;

        For example, `https://<instance-name>.service-now.com`.

    -   **insecure-skip-tls-verify**: `false`
    -   **registration-key**: &lt;registration key value&gt;

        For more information, see [Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-acc-reg-key.md).

6.  Comment out the API key parameter:

    `api-key: "encrypted....”`

7.  Save the file.

8.  Delete files based on your operating system:

    -   On Windows, navigate to `/agent-client-collector/config/cert/cnc` and remove the following files: `cnc_chain.crt` and `priv_key.pem.go`.
    -   On macOS, access `/Library/Application Support/servicenow/agent-client-collector/cert/cnc` and delete the files: `cnc_chain.crt` and `priv_key.pem`.
9.  Delete `assets.db`, `queue.db`, and all subdirectories in the cache folder based on your operating system:

    -   On Windows: `/agent-client-collector/cache`.
    -   On macOS:
        -   For Agent 3.4.1 or later: `/Library/Application Support/servicenow/agent-client-collector/cache`.
        -   For Agent 3.4.0 or earlier: `/Library/Caches/servicenow/agent-client-collector`.
    **Important:** Keep `agent_now_id` in the cache folder.

10. Start the ACC service based on your operating system.

    -   On Windows, open Services as administrator, then start the Agent Client Collector service.
    -   On macOS, use the command: `sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist`.

**Parent Topic:**[DEX advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-advanced-configuration.md)


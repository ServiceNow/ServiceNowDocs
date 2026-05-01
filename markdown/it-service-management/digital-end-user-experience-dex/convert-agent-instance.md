---
title: Switch ACC from one instance to another
description: Switch Agent Client Collector \(ACC\) to a different instance.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Switch ACC from one instance to another

Switch Agent Client Collector \(ACC\) to a different instance.

## Before you begin

Confirm you have installed the Agent Client Collector \(ACC\) and set up the ACC registration key. For information on how to set up and install, see:

-   [Create an ACC registration key](setup-acc.md).
-   [Install Agent Client Collector on a Windows machine manually](https://www.servicenow.com/docs/access?context=acc-install-windows&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) or [Manually install Agent Client Collector on macOS](https://www.servicenow.com/docs/access?context=acc-install-macOS-manual&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

Role required: agent\_admin and agent\_client\_collector\_admin

For more information on roles, see [Agent Client Collector user roles](https://www.servicenow.com/docs/access?context=acc-users&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## About this task

If ACC is already connected to one instance, you can switch the agent to another instance by changing the configuration in `acc.yml`.

## Procedure

1.  Stop ACC with the steps appropriate for your operating system.

    -   For Windows, access Services as Administrator and stop the Agent Client Collector service.
    -   For macOS, execute the command: `sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist;`
2.  Open the `acc.yml` file.

    -   Windows: `C:\ProgramData\ServiceNow\agent-client-collector\config`
    -   macOS: `/Library/Application\ Support/servicenow/agent-client-collector/`
3.  Edit the **backend-url** parameter to point to `<ITOM Cloud Services Gateway>`.

    Use any of the following gateways based on the instance location:

    -   `AMER: itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   `EMEA: itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   `APAC: itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
    For more information on how the Agent uses the ITOM Cloud Services Gateway, see [DEX Architecture](../concept/dex-architecture.md).

4.  Update the following parameters:

    -   connect-without-mid: true
    -   instance-url: &lt;full\_instance\_url&gt;, example: https://dex.servicenow.com
    -   registration-key: &lt;registration key value&gt;

        For more information on how to create a registration key, see [Create an ACC registration key](setup-acc.md).

5.  Save the file.

6.  Delete files based on your operating system.

    -   On Windows, navigate to `/agent-client-collector/config/cert/cnc` and remove the following files: `cnc_chain.crt` and `priv_key.pem.go`.
    -   On macOS, access `/Library/Application Support/servicenow/agent-client-collector/cert/cnc` and delete the files: `cnc_chain.crt` and `priv_key.pem`.
7.  Delete the following folders based on your operating system.

    -   On Windows, delete the folder: `/agent-client-collector/cache`.
    -   On macOS:
        -   For Agent 3.4.1 or above, delete the folder: `/Library/Application Support/servicenow/agent-client-collector/cache`.
        -   For Agent 3.4.0 or below, delete the folder: `/Library/Caches/servicenow/agent-client-collector`.
8.  If you have connected this ACC to another instance before, do the following:

    1.  Copy your device serial number.

    2.  In the Agent Client Collectors table \(sn\_agent\_cmdb\_ci\_agent\), search using your device serial number.

        **Note:** Add the **Agent ID** column to the list view if it isn’t available.

    3.  If you find a record, copy the record Agent ID.

    4.  In the Agent Registrations table \(sn\_agent\_agent\_registration\), search using the record Agent ID.

    5.  Delete any records resulting from the search.

9.  Initiate the ACC service by following the steps specific to your operating system.

    -   On Windows, open Services as Administrator, then start Agent Client Collector.
    -   On macOS, use the command: `sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist`.


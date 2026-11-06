---
title: Switch ACC from one instance to another
description: Switch Agent Client Collector \(ACC\) to a different instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/convert-agent-instance.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 3
breadcrumb: [DEX advanced configuration, Configure, Digital End-User Experience, IT Operations Management]
---

# Switch ACC from one instance to another

Switch Agent Client Collector \(ACC\) to a different instance.

## Before you begin

The Agent Client Collector \(ACC\) must be installed and the ACC registration key must be set up. For information about how to set up and install ACC, see the following topics:

-   [Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-acc-reg-key.md).
-   [Install the Agent Client Collector on a Windows machine manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-install-windows.md) or [Manually install Agent Client Collector on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-install-macOS-manual.md).

Role required: agent\_admin and agent\_client\_collector\_admin

For more information about roles, see [Agent Client Collector user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-users.md).

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
    For more information about how the agent uses the ITOM Cloud Services Gateway, see [DEX architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-architecture.md).

4.  Update the following parameters:

    -   **connect-without-mid**: `true`
    -   **instance-url**: &lt;full\_instance\_url&gt;, for example, `https://<instance-name>.service-now.com`
    -   **registration-key**: &lt;registration key value&gt;

        For more information about how to create a registration key, see [Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-acc-reg-key.md).

5.  Save the file.

6.  Delete files based on your operating system.

    -   On Windows, navigate to `/agent-client-collector/config/cert/cnc` and remove the following files: `cnc_chain.crt` and `priv_key.pem.go`.
    -   On macOS, access `/Library/Application Support/servicenow/agent-client-collector/cert/cnc` and delete the files: `cnc_chain.crt` and `priv_key.pem`.
7.  Delete the following folders based on your operating system.

    -   On Windows, delete the folder: `/agent-client-collector/cache`.
    -   On macOS:
        -   For Agent 3.4.1 or later, delete the folder: `/Library/Application Support/servicenow/agent-client-collector/cache`.
        -   For Agent 3.4.0 or earlier, delete the folder: `/Library/Caches/servicenow/agent-client-collector`.
8.  If you have connected this ACC to another instance before, do the following:

    1.  Copy your device serial number.

    2.  In the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table, search using your device serial number.

        **Note:** Add the **Agent ID** column to the list view if it isn’t available.

    3.  If you find a record, copy the record Agent ID.

    4.  In the Agent Registrations \[sn\_agent\_agent\_registration\] table, search using the record Agent ID.

    5.  Delete any records resulting from the search.

9.  Start the ACC service by following the steps specific to your operating system.

    -   On Windows, open Services as Administrator, then start Agent Client Collector.
    -   On macOS, use the command: `sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist`.

**Parent Topic:**[DEX advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-advanced-configuration.md)


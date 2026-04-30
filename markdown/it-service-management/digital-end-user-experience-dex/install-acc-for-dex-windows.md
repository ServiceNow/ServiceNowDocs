---
title: Install ACC for DEX on Windows
description: Install Agent Client Collector \(ACC\) to work with Digital End-User Experience \(DEX\) to monitor and collect data, provide insights into system performance, identify issues, and enable proactive maintenance.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Getting started, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Install ACC for DEX on Windows

Install Agent Client Collector \(ACC\) to work with Digital End-User Experience \(DEX\) to monitor and collect data, provide insights into system performance, identify issues, and enable proactive maintenance.

## Before you begin

Install the ITOM Cloud Services plugin.

Create an agent registration key.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Retrieve the publicly accessible gateway URL, based on your location.

    -   AMER \(Americas\): `itomcnc-prod-gateway.amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway.emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway.apac.sncapps.service-now.com:443`
2.  On the Windows server where the agent is installed, enter the following command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>"
    ```

    The following table shows the parameter values in the command.

<table id="table_usf_fpf_wfc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable MID-less Agent Client Collector installation. If you don't specify a value, the regular MID Server websocket installation is invoked.

</td></tr><tr><td>

ACC\_CNC

</td><td>

Specify a public gateway endpoint for Agent Client Collector.

</td></tr><tr><td>

REGISTRATION\_KEY

</td><td>

Active and valid registration key for the agent to communicate with.

</td></tr><tr><td>

INSTANCE\_URL

</td><td>

ServiceNow instance that the agent is registered with.

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

Optional string. To disable the allow list, set **ACC\_ALLOW\_LIST=0**. By default, the allow list is enabled.**Note:** Disabling the allow list compromises your system's security and is intended as a temporary measure while you’re updating the allow list. After completing the update, enable the allow list by setting **ACC\_ALLOW\_LIST=1**.

</td></tr><tr><td>

ACC\_VALIDATE\_SIG

</td><td>

Optional string. To disable verification of the installer certification validation, set **ACC\_VALIDATE\_SIG=0** that you can add to disable the verification of the installer certification validation. By default, validation is enabled.**Note:** Disable the certification validation only when using non-standard signature validation tools.

</td></tr></tbody>
</table>3.  Start the Agent Client Collector service using the default ServiceNow user role created during this installation.

    The default ServiceNow user role has the following privileges:

    -   Performance Monitor: Viewing all performance counters in the system.
    -   Log on as a service: Starting network services and services that run continuously, even when no one is logged in to the console.
    -   Debug program: Monitoring the installed applications and collecting in-depth metrics and remedial actions, such as restart and stop.
4.  To collect DEX metrics, restart the ACC service using one of the following methods:

    -   Add **Remote Desktop user** to ServiceNow user.
    -   [Run as a local system account user](run-acc-local-sys-account.md).
    -   [Run as a managed group user](run-acc-as-managed-group-user.md).
5.  Restart the Agent Client Collector service.



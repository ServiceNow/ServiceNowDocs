---
title: Install MID-less Agent Client Collector using a single-line command in a Windows environment
description: Install MID-less Agent Client Collector on a Windows machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Installing MID-less Agent Client Collector, Configuring MID-less Agent Client Collector, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Install MID-less Agent Client Collector using a single-line command in a Windows environment

Install MID-less Agent Client Collector on a Windows machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key. For details, see [Configure an agent registration key](agent-registration-key-configuration.md).
-   Role required: agent\_client\_collector\_admin

## About this task

For details on sending data through the cloud in a MID-less deployment, see [DEX Architecture](https://www.servicenow.com/docs/access?context=dex-architecture&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

## Procedure

1.  Retrieve the publicly accessible gateway URL, based on your location.

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
2.  On the Windows server where the agent is installed, enter the following command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>"
    ```

    For details on the parameter values in the command, see [Agent Client Collector MID-less installation command parameters](../reference/acc-ics-command-params.md).


**Parent Topic:**[Installing MID-less Agent Client Collector](../concept/acc-itom-cloud-services.md)


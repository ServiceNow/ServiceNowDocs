---
title: Installing MID-less Agent Client Collector
description: Installing MID-less Agent Client Collector enables you to send data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring MID-less Agent Client Collector, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Installing MID-less Agent Client Collector

Installing MID-less Agent Client Collector enables you to send data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

Before using MID-less Agent Client Collector, do the following:

1.  Ensure that your ServiceNow instance has migrated from an F5 load balancer to Application Delivery Controller, version 2 \(ADCv2\) and has mTLS support.
    1.  Enter the following command in your terminal: `curl -v https://<instance>.service-now.com/stats.do 2>&1 | grep "< Server"`.
        -   If the system returns **snow\_adc**, the instance is on ADCv2/ADCv3.
        -   If the system doesn't return **snow\_adc**, the instance isn’t on ADCv2/ADCv3. To migrate the instance to ADCv2/ADCv3, contact Customer Support.
    2.  Navigate to `<instance_url>/adcv2/supports_tls`

        If the URL returns a value of **true**, mTLS is supported.

2.  Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) scoped app plugin.

    If you’re using Agent Client Collector for Visibility - Content, install the Agent Client Collector for Visibility - Content \(sn\_acc\_vis\_content\) plugin.

3.  Configure an agent registration key on the instance. For details, see [Configure an agent registration key](../task/agent-registration-key-configuration.md).

-   **[Install MID-less Agent Client Collector using a single-line command in a Windows environment](../task/acc-install-ics-windows.md)**  
Install MID-less Agent Client Collector on a Windows machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
-   **[Install MID-less Agent Client Collector manually in a Linux environment](../task/acc-install-ics-linux-manual.md)**  
Install MID-less Agent Client Collector manually on a Linux machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
-   **[Install MID-less Agent Client Collector using a single-line command in a Linux environment](../task/acc-install-ics-linux.md)**  
Install MID-less Agent Client Collector on a Linux machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
-   **[Install MID-less Agent Client Collector manually in a macOS environment](../task/acc-install-ics-macos-manual.md)**  
Install MID-less Agent Client Collector manually on a macOS machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
-   **[Install MID-less Agent Client Collector using a single-line command in a macOS environment](../task/acc-install-ics-macos.md)**  
Install MID-less Agent Client Collector on a macOS machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

**Parent Topic:**[Configuring MID-less Agent Client Collector](acc-configuring-without-mid.md)


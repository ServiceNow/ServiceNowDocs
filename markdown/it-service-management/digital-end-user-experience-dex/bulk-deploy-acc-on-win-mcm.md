---
title: Bulk deploy Agent Client Collector on Windows using Microsoft Configuration Manager
description: Use Microsoft Configuration Manager to install Agent Client Collector \(ACC\) on multiple Windows devices at once when your organization manages endpoints with Configuration Manager rather than Microsoft Intune.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/bulk-deploy-acc-on-win-mcm.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [bulk deploy acc configuration manager, microsoft configuration manager acc, mcm agent deployment, deploy acc multiple windows devices, sccm acc deployment]
breadcrumb: [Deploying DEX to employees, Configure, Digital End-User Experience, IT Service Management]
---

# Bulk deploy Agent Client Collector on Windows using Microsoft Configuration Manager

Use Microsoft Configuration Manager to install Agent Client Collector \(ACC\) on multiple Windows devices at once when your organization manages endpoints with Configuration Manager rather than Microsoft Intune.

## Before you begin

-   Create an agent registration key and retrieve its value to use in the procedure. For more information, see [Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-acc-reg-key.md).
-   Install ACC on a single candidate device and verify it, so that you have a working `acc.yml` file and a validated installation command. For more information, see [Install ACC for DEX on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-windows.md).
-   Uninstall the agent from your candidate test devices. For more information, see [Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md).

Role required: agent\_client\_collector\_admin

Contact your Configuration Manager application administrator for enterprise-wide deployments.

## About this task

The following procedure describes how to mass-deploy ACC using Microsoft Configuration Manager. Your organization might have a different method to accomplish this task.

## Procedure

1.  On the ServiceNow instance, prepare the installation content.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

    2.  Download the MSI installer.

    3.  Copy the command from the **Single-line installer commands** section, under **Commands without MID**.

    4.  Create an installable package from your updated `acc.yml` file.

        Confirm the following values in `acc.yml` before you package it:

        -   **backend-url**: the gateway endpoint for your region.
        -   **connect-without-mid**: set to `true`.
        -   **instance-url**: the URL of your instance.
        -   **registration-key**: an active registration key.
        The `acc.yml` file is located at `C:\ProgramData\ServiceNow\agent-client-collector\config`.

2.  In the Microsoft Configuration Manager console, create the application.

    1.  Navigate to **Software Library** &gt; **Application Management** &gt; **Applications**.

    2.  Select **Create Application**.

    3.  Select **Manually specify the application information**.

    4.  Enter the application name, publisher, and version for the ACC agent.

        Enter ServiceNow for the publisher.

    5.  Upload the installation package and enter the installation command line that you copied earlier.

    6.  Configure the detection method so that Configuration Manager can verify a successful installation.

    7.  Specify the user experience settings, including the installation behavior and device restart options.

3.  Add a deployment type and distribute the content.

    1.  On the **Deployment Types** tab, select the deployment type for the application.

    2.  Select **Add Deployment Type** and associate it with the ACC agent installation package.

    3.  Specify the content location and distribution settings for the deployment package.

    4.  Select **Next** and specify any conditions that are necessary for deployment in the **Requirements** section.

4.  Deploy the application.

    1.  Access the **Deployments** section of the Configuration Manager console.

    2.  Select **Create Deployment** and select the ACC agent application.

    3.  Specify the deployment target, such as a collection of Windows devices.

    4.  Configure the deployment settings, including the scheduling and alert options.

5.  Verify the deployment across your devices.

    For details, see [Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md).


**Related topics**  


[Install Agent Client Collector on Windows using Microsoft Intune](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/bulk-deploy-acc-on-win.md)

[Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md)

[Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md)


---
title: Install Agent Client Collector on Windows using Microsoft Intune
description: Use Microsoft Intune to install Agent Client Collector \(ACC\) on multiple Windows devices at once, promoting consistent deployment across your organization.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-08-25"
reading_time_minutes: 2
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Install Agent Client Collector on Windows using Microsoft Intune

Use Microsoft Intune to install Agent Client Collector \(ACC\) on multiple Windows devices at once, promoting consistent deployment across your organization.

## Before you begin

-   Create an agent registration key. For more information, see [Create an ACC registration key](../../product/digital-end-user-experience/task/setup-acc.md).

Role required: agent\_client\_collector\_admin

## About this task

The following procedure describes how to mass-deploy ACC using Microsoft Intune. Your organization might have a different method to accomplish this task.

## Procedure

1.  On the ServiceNow instance, download the installation package:

    1.  Navigate to **Self-Service** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Client Downloads**.

    2.  Download the MSI installer by selecting the Download icon \(![](../../product/digital-end-user-experience/image/icon-download-blue.png)\) under the Windows Downloads section.

    3.  Copy the command from the Single-line installer commands section of **Agent Client Downloads**.

2.  In Microsoft Intune, navigate to **Apps** &gt; **Windows**.

3.  Select **+ Create**.

4.  From the **Select app type** drop-down menu, select **Line-of-business app**, then click **Select**.

    **Note:** Depending on your setup, you might have to select **Win 32 app**.

5.  Click **Select app package file**, browse to the folder where you stored the ACC installation package file, and select **OK**.

6.  Complete the **Add app** form:

<table id="table_brt_shm_pgc"><thead><tr><th>

Tab

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

**App information**

</td><td>

Complete the required fields as shown in the following procedure.1.  Name your application.
2.  Provide an easily recognizable description.
3.  Enter ServiceNow for **Publisher**.
4.  Paste the command that you copied earlier into **Command-line arguments** and remove content before `/quiet`.
5.  In the command string `/quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="*ACC\_CNC*" REGISTRATION_KEY="*REGISTRATION KEY*" INSTANCE_URL="*INSTANCE URL*" LOCALUSERNAME="*local user name*"`, confirm or enter the variable parameters as follows:
    -   ACC\_CNC: one of the following gateway URLs, based on your location:
        -   AMER \(Americas\): `itomcnc-prod-gateway.amer.sncapps.service-now.com:443`
        -   EMEA \(Europe\): `itomcnc-prod-gateway.emea.sncapps.service-now.com:443`
        -   APAC \(Asia Pacific\): `itomcnc-prod-gateway.apac.sncapps.service-now.com:443`
    -   REGISTRATION KEY: ACC registration key
    -   INSTANCE\_URL: URL that contains your ServiceNow instance name
    -   LOCALUSERNAME: `SYSTEM`


</td></tr><tr><td>

**Scope tags**

</td><td>

Define the scope tags to control role-based access to the objects you create, then select **Next**.This setting is optional.

</td></tr><tr><td>

**Assignments**

</td><td>

Define the groups, users, and devices to which you want to deploy the ACC, then click **Select**.

</td></tr></tbody>
</table>7.  Select **Next**.

8.  Review the settings, then select **Create**.

    You can view the ACC application in the application list. Once the users check-in and are synchronized with Microsoft Intune, the silent installation process begins.

9.  Do one of the following to monitor the deployment status:

    -   In Microsoft Intune, select your newly created application.
    -   Review the log file on the endpoint devices: `C:\ProgramData\ServiceNow\agent-client-collector\log\acc.log`.
    -   On an endpoint device, search for **Services** and check the status for Agent Client Collector.


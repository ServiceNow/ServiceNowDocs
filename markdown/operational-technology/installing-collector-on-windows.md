---
title: Install the OT Discovery Collector on a Windows system
description: Install the OT Discovery Collector on a Windows system. The OT Discovery Collector installation is compatible on Windows 10 or Windows 11 systems.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-27"
reading_time_minutes: 2
breadcrumb: [Configure the OT Discovery Collector, Operational Technology \(OT\) Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install the OT Discovery Collector on a Windows system

Install the OT Discovery Collector on a Windows system. The OT Discovery Collector installation is compatible on Windows 10 or Windows 11 systems.

## Before you begin

The required Windows \(10 or 11\) environment for the OT Discovery Collector is x86\_64. No ARM/Apple Silicon devices are supported.

Role required: admin

## Procedure

1.  On your instance, navigate to the Service Graph Connector for ServiceNow OT Discovery Guided Setup page.

2.  Click the **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure** and the **Downloads** page opens.

    **Note:** Read the End User License Agreement \(EULA\) carefully and then check **Agree**.

5.  Download the OT Discovery Collector installation and deployment package for Windows.

6.  Install the Collector on the Discovery Console for OT you intend to use.

7.  On the Discovery Console for OT, navigate to the **Sensors** &gt; **Certificates** &gt; **** page.

8.  To generate the OT Discovery Collector credentials you need, from the list under the Bundle Password section, select the **Generate Password** button.

9.  Select the radio button next to the desired **Bundle Format**.

    The recommended format is ZIP.

10. Select the **Generate Bundle** button.

    The Generate OT Discovery Collector Credential Bundle window opens.

11. Select the **Generate Bundle** button in this window.

    The `ServiceNow_OT_Discovery_Collector_Windows` bundle zip file is downloaded to your machine.

12. Extract the `ServiceNow_OT_Discovery_Collector_Windows.zip` file.

    The zip file contains a `config.json` file and a `cert` folder. The `cert` folder contains the following files:

    -   `ca_root_certificate.pem`
    -   `client.device.rabbit.pem`
    -   `client.device.rabbit.privatekey.pem`
13. Navigate to the `ServiceNow_OT_Discovery_Collector_Windows_Installer_[datestamp]` folder.

14. In this folder, select and hold \(or right-click\) on the `ServiceNow_OT_Discovery_Collector_Windows_Installer` file and select **Run as Administrator**.

15. When prompted, select **Yes** to enable this app to change to your computer.

    The ServiceNow OT Discovery Collector Installer window starts the installation.

    ![OT Discovery Collector Installer window](../../ot-discovery-solution-install-deploy-guide/images/new-scout-installer-screen.png)

16. Select the **View/accept EULA** button to accept the End User License Agreement \(EULA\).

    Read the EULA carefully. If you don’t agree to the EULA, or skip this step, the installation is canceled.

    When you accept the EULA, a dialog window pops up.

17. In the dialog window, select the `SNDiscoveryCollector_install_windows` file and select **OK**.

18. Select the **Select OT Discovery Collector Credentials** button.

    After you select this button, a dialog window opens.

19. In the window, select the `collectorBundle` file and select **OK**.

20. Select the **Install/Update Collector** button on the installation screen.

    When complete, the ServiceNow OT Discovery Collector Installer window displays `Installation Complete`.

    ![Installation complete screen](../images/install-complete-collector.png)

21. Navigate to your local disk program files folder, so that you can see the `SNDiscoveryCollector` folder is present.

22. Navigate back to the Download &amp; Deploy OT Discovery page and select **Mark as complete**.


## Result

In the Discovery Console for OT window, the OT Discovery Collector appears on the Discovery Sensor for OT screen.

The OT Discovery Collector is installed on your Discovery Console.

## What to do next

To update the OT Discovery Collector version, do the following steps.

1.  Re-run the installer.
2.  Select the latest version of the OT Discovery Collector.
3.  Use the same credentials again.
4.  Select the **Install/Update OT Discovery Collector** button.

The updated version is installed.


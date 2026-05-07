---
title: Set up an application with Now Assist for Setup
description: Implement the following steps to set up a specific application or plugin with Now Assist for Setup on your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Set up an application with Now Assist for Setup

Implement the following steps to set up a specific application or plugin with Now Assist for Setup on your instance.

## Before you begin

Before performing this task you must install Now Assist for Setup application from [ServiceNow store](https://store.servicenow.com/store/app/9d063fc34704cf10f43984f8736d43b5) or from the prompt on the Admin Home page.

This application is available to all users with Foundation SKUs for ITSM, CBS, ITOM, and ESM, and Pro+ SKUs for ITSM and HRSD.

Role required: admin

## Procedure

1.  Navigate to your Admin Home page on your instance.

    The system dynamically renders application and plugin cards based on your admin entitlement status.

    ![Screenshot showing the dynamically rendered apps and plugins tiles](../image/ia-install.png)

    **Note:** The Manage your products section is collapsible by default. You can expand it to see all the product family cards.

2.  Select **View product overview** for a specific product family card in the Manage your products section to start the setup process.

    The Product Hub page for the selected product family shows up.

3.  Select **Start setup** from Option 1.

    This step is applicable only if you are setting up ITSM for the first time.

    The detailed Product Hub page for ITSM shows up. You can see the list of app bundles that need to be installed.

    ![Screenshot showing ITSM set up flow](../image/ia-itsm-setup.png)

    **Note:** The above UI is only for ITSM.

4.  Select **Upload batch** from Option 2.

    This step is applicable only if you are setting up ITSM from another ServiceNow instance. See [Manage update set for Now Assist for Setup](ia-update-set.md) for more information.

5.  Select the install icon next to the app bundle mentioned under the Not installed tab to start the installation process of the specific app bundle.

    You can also see the information about the app bundles that have either been installed or have available updates under the Installed and Updates available tabs.

    Once the app bundle is installed, it moves under the Installed tab.

    **Note:** In case of Core Business Suite \(CBS\), it follows two steps installation process. The CBS app is installed first, followed by its corresponding apps mentioned under the Not installed tab. The green banner shows up only for CBS setup process.

6.  Review the information in the Configuration insights section.

    Once an app is installed, corresponding information about the new configurations that have either been added or updated show up in the Configuration insights section.

    **Note:** This section is visible only for CBS setup process. This section shows up only when you have an application under the Installed tab for the CBS setup process.

    Select **More info** to show the total steps configured for each module.

    **Note:** The **More info** count reflects the combined total of manual and default configurations applied.

7.  Select **Upload batch** to upload a batch file and set up the update set for Now Assist for Setup.

    **Note:** This step is applicable only if you need to setup the update set for either ITSM or CBS. See [Manage update set for Now Assist for Setup](ia-update-set.md) for more information.

8.  Expand Whats's included to view the applications included in the app bundle.

    **Note:** The What's included section stays collapsed by default.

9.  Select **Configure** to move to the Configuration Console page.

    See [Configure in Now Assist for Setup](../concept/ia-config-landing.md) for more information.


**Parent Topic:**[Administer Now Assist for Setup](../concept/ia-administer.md)


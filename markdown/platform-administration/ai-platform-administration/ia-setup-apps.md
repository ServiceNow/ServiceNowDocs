---
title: Set up an application with Setup Hub
description: Implement the following steps to set up a specific application or plugin with Setup Hub on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/ia-setup-apps.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Setup Hub, Get started, Administer the ServiceNow AI Platform]
---

# Set up an application with Setup Hub

Implement the following steps to set up a specific application or plugin with Setup Hub on your instance.

## Before you begin

Before performing this task you must install Setup Hub application from [ServiceNow store](https://store.servicenow.com/store/app/9d063fc34704cf10f43984f8736d43b5) or from the prompt on the Admin Home page.

This application is available to all users with Foundation SKUs for ITSM, CBS, ITOM, Employee Slate and ESM, and Pro+ SKUs for Simplified ITSM, ITOM and HRSD.

**Note:** Setup Hub supports tiered SKUs \(Advanced and Prime\) for ITOM, Simplified IT Service Management, HAM and CBS, including entitlement-driven flows and experiences.

Role required: admin

## Procedure

1.  Navigate to your Admin Home page on your instance.

    The system dynamically renders application and plugin cards based on your admin entitlement status.

    \[Omitted image "ia-install.png"\] Alt text: Screenshot showing the dynamically rendered apps and plugins tiles

    **Note:** If you use an earlier version of Admin Center, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md) for installation information about Now Assist. In the latest version of Admin Center, the Now Assist card appears in the Manage your products section.

    **Note:** The Manage your products section is collapsible by default. You can expand it to see all the product family cards.

2.  Select **View product overview** for a specific product family card in the Manage your products section to start the setup process.

    The Product Hub page for the selected product family shows up.

3.  Select **Start setup** from Option 1.

    \[Omitted image "ia-itsm-setup.png"\] Alt text: Screenshot showing Simplified ITSM set up flow

    **Note:** This step is not applicable for all product families. The above UI is visible only for specific product families that are being set up for the first time.

    The detailed Product Hub page for the selected product shows up. You can see the list of app bundles that needs to be installed.

    The Product Hub page displays a single product tier based on entitlements, using a descending order to show the highest tier when multiple tiers are available. For example, if both Foundation and Advanced tiers are installed for Simplified ITSM, only the Advanced tier is displayed. Under the Not installed section, only apps associated with the Advanced tier entitlement are shown. At the Product Hub level, the tiering approach can be configured as either Tiered or All Active Resources; ITSM and CBS use the Tiered approach, while ITOM uses the default \(All Active Resources\) approach.

    \[Omitted image "ia-tier-approach.png"\] Alt text: Screenshot showing tiered approach by ITSM

4.  Select **Upload batch** from Option 2.

    This step is applicable only if you are setting up ITSM from another ServiceNow instance. See [Manage update set for Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-update-set.md) for more information.

5.  Select the install icon next to the app bundle mentioned under the Not installed tab to start the installation process of the specific app bundle.

    You can also see the information about the app bundles that have either been installed or have available updates under the Installed and Updates available tabs.

    Once the app bundle is installed, it moves under the Installed tab.

    **Note:** In case of Core Business Suite \(CBS\), it follows two steps installation process. The CBS app is installed first, followed by its corresponding apps mentioned under the Not installed tab. The green banner shows up only for CBS setup process.

6.  Review the information in the Configuration insights section.

    Once an app is installed, corresponding information about the new configurations that have either been added or updated show up in the Configuration insights section.

    **Note:** This section is visible only for CBS setup process. This section shows up only when you have an application under the Installed tab for the CBS setup process.

    Select **More info** to show the total steps configured for each module.

    **Note:** The **More info** count reflects the combined total of manual and default configurations applied.

7.  Select **Upload batch** to upload a batch file and set up the update set for Setup Hub.

    **Note:** This step is applicable only if you need to setup the update set for either ITSM or CBS. See [Manage update set for Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-update-set.md) for more information.

8.  Expand Whats's included to view the applications included in the app bundle.

    You can also explore the Helpful resources section in Product Hub page that include links to configuration guidance, product documentation, release notes, and the ServiceNow Community.

    **Note:** The What's included section stays collapsed by default.

9.  Select **Configure** to move to the Configuration Console page.

    See [Configure in Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-config-landing.md) for more information.


**Parent Topic:**[Administer Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-administer.md)


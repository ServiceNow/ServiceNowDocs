---
title: Install Hardware Asset Management from Product Hub
description: Install the Hardware Asset Management application on your ServiceNow instance from Product Hub based on your subscription tier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/install-ham-from-product-hub.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Management on Product Hub, Installing Hardware Asset Management, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Install Hardware Asset Management from Product Hub

Install the Hardware Asset Management application on your ServiceNow instance from Product Hub based on your subscription tier.

## Before you begin

-   The Hardware Asset Management application must be licensed for your ServiceNow instance.
-   To access the Admin Home page, install the application that matches your SKU type: ServiceNow Otto for Setup \(sn\_ia\) for AI Native SKUs, or Setup Hub \(sn\_ia\_base\) for non-AI Native SKUs.

Role required: ia\_admin

## About this task

Use this procedure for initial HAM installation. If HAM is already installed, Product Hub does not display the setup option and instead displays the tab view for managing additional applications and plugins.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

    The Admin Home page opens automatically when you log in to your ServiceNow instance.

2.  In the **Manage your products** section of the Admin Home page, select the **Hardware Asset Management** card to open the Product Hub.

3.  Select **Start new setup** to install HAM.

    **Note:** If you are moving an existing HAM setup from another ServiceNow instance, select **Upload new batch** instead of **Start new setup**. You may have to configure some instance-specific settings again after the upload. For details, see [Manage update set for ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-update-set.md).

    The Apps and plugins page opens, displaying the core HAM application for your highest entitled subscription tier in the **Not installed** tab. For example, if you are entitled to Hardware Asset Management Advanced, **Hardware Asset Management - Advanced** appears in the **Not installed** tab.

4.  Select the **Not installed** tab and install the core HAM application.

    -   For Hardware Asset Management - Advanced and Hardware Asset Management - Prime, select the Open Application Manager icon \[Omitted image "open-application-manager-icon.png"\] Alt text: to navigate to Application Manager and then install the application from there.
    -   For Hardware Asset Management - Pro SKU, select the Install icon \[Omitted image "app-install-icon.png"\] Alt text: to install directly in Product Hub.

## Result

-   The core HAM application is installed and appears in the **Installed** tab.
-   The additional applications and plugins included in your subscription tier appear in the **Not installed** tab.
-   The **Configure** card that opens the Configuration Console appears.

## What to do next

-   To install additional HAM applications and plugins for your subscription tier, see [Install additional HAM applications using Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/install-additional-ham-apps.md).
-   To configure HAM, see [Configure Hardware Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/configure-ham-from-console.md).

**Note:** You can configure the HAM application before installing additional applications.


---
title: Install additional HAM applications using Product Hub
description: Install the HAM applications and plugins included in your subscription tier that are not yet installed in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/install-additional-ham-apps.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 1
breadcrumb: [Install Hardware Asset Management from Product Hub, Hardware Asset Management on Product Hub, Installing Hardware Asset Management, Configure, Hardware Asset Management, IT Asset Management]
---

# Install additional HAM applications using Product Hub

Install the HAM applications and plugins included in your subscription tier that are not yet installed in your ServiceNow instance.

## Before you begin

The HAM application must be installed in your ServiceNow instance.

Role required: ia\_admin

## About this task

Use this procedure to install additional HAM applications and plugins after your initial HAM installation. Product Hub displays the applications and plugins included in your subscription tier. If your account was upgraded to a higher subscription tier, the required core application for the new tier appears in the **Not installed** tab. For example, if you upgrade from Hardware Asset Management Pro to Hardware Asset Management Advanced, the Hardware Asset Management Advanced application appears in the **Not installed** tab.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

    The Admin Home page opens automatically when you log in to your ServiceNow instance.

2.  In the **Manage your products** section of the Admin Home page, select the **Hardware Asset Management** card to open the Product Hub.

3.  Select the **Not installed** tab.

    The tab lists additional HAM applications and plugins included in your subscription tier that aren't currently installed.

4.  Select the application or plugin that you want to install.

    -   If the application has an Install icon \[Omitted image "app-install-icon.png"\] Alt text:, select it to install directly from Product Hub.
    -   If the application displays an Open Application Manager icon \[Omitted image "open-application-manager-icon.png"\] Alt text:, select it to navigate to Application Manager and complete the installation from there.

## Result

-   The application appears in the **Installed** tab.
-   The application appears in the **Updates available** tab if updates are available.

## What to do next

To configure the installed application, see [Configure Hardware Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/configure-ham-from-console.md).


---
title: Install Software Asset Management from the Product Hub
description: Install Software Asset Management and its dependent applications and plugins from using Product Hub. The Product Hub applies the default configurations and prepares your instance for the Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/install-sam-product-hub.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Product Hub for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Install Software Asset Management from the Product Hub

Install Software Asset Management and its dependent applications and plugins from using Product Hub. The Product Hub applies the default configurations and prepares your instance for the Configuration Console.

## Before you begin

Check your entitlements to determine whether you have access to the Software Asset Management application.

Install the application matching your subscription from the ServiceNow Store:

-   ServiceNow Otto for Setup \(sn\_ia\) — for AI Native subscriptions
-   [Setup Hub](https://store.servicenow.com/store/app/4f085e4997e9831876b932471153afa8) \(sn\_ia\_base\) — for non-AI Native subscriptions

Role required: admin or sn\_ia\_config.ia\_admin

## About this task

Use this procedure the first time you install the Software Asset Management application on your instance. If the Software Asset Management application is already installed, the Product Hub page does not display the setup option and instead displays the manage view for reviewing components and applying updates.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

    The Admin Home page opens automatically when you log in to your ServiceNow instance.

2.  In the **Manage your products** section of the Admin Home page, select the Software Asset Management card to open the Product Hub.

3.  Choose the install option that fits your instance.

    -   To install on a new instance, select **Start setup**. The Product Hub installs the core application and the dependent components and applies the default configurations.
    -   To move an existing setup from another instance, select **Upload update set**. Upload the batch update set as an XML file, preview the changes in a new tab, and commit the batch.
4.  Follow the guided flow through **Choose what to install in this app bundle**, **Apply default configurations**, and **Ready to configure**.

    The Product Hub tracks progress on each step. For a visual walkthrough of the guided flow, see the Product Hub installation video or workflow diagram.


## Result

-   The Software Asset Management application is installed and appears in the **Installed** tab.
-   The additional applications and plugins included in your subscription tier appear in the **Not installed** tab.
-   The **Configure** card that opens the Configuration Console appears.

## What to do next

After you install Software Asset Management from the Product Hub, complete the following steps to access the Configuration Console:

1.  Install the SAM Admin Experience - v1.0 \(sn\_samp\_admin\) store application from ServiceNow store. This application is required to access the Configuration Console.
2.  Select **Configure** on the Admin Home page for Software Asset Management to open the Configuration Console. For details, see [Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md).

**Parent Topic:**[Product Hub for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-product-hub.md)

**Related topics**  


[Software Asset Management installation methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/installing-sam-app.md)

[Product Hub for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-product-hub.md)

[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)


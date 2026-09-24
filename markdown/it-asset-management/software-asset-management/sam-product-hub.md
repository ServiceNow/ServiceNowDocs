---
title: Product Hub for Software Asset Management
description: The Product Hub provides a guided installation and management interface for the Software Asset Management application. Administrators can install the application, apply default configurations, track progress, and access the Configuration Console from the Software Asset Management Admin Home tile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sam-product-hub.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Product Hub for Software Asset Management

The Product Hub provides a guided installation and management interface for the Software Asset Management application. Administrators can install the application, apply default configurations, track progress, and access the Configuration Console from the Software Asset Management Admin Home tile.

## Purpose and access

The Product Hub gives an administrator a single starting point to install Software Asset Management, apply the default configurations, and open the Configuration Console after the install completes. Product Hub is accessible from the Admin Home page through the **Software Asset Management** tile in the **Manage your products** section.

From the Admin Home page, the Software Asset Management tile is available only when the application matching your subscription is installed on your instance.

**Important:** The Software Asset Management tile is available only when the ServiceNow Otto for Setup \(sn\_ia\) application for AI Native subscriptions, or the Setup Hub \(sn\_ia\_base\) application for non-AI Native subscriptions, is installed on your ServiceNow® instance.

Access to Product Hub requires one of two granular roles, which a system administrator must grant:

|Role|Access level|
|----|------------|
|sn\_ia\_config.ia\_admin|Full access: install, update, and manage Software Asset Management applications and plugins|
|sn\_ia\_config.ia\_user|View-only access: browse Product Hub but can't install applications|

**Note:** System administrators have access to Product hub by default. A system administrator must grant sn\_ia\_config.ia\_admin or sn\_ia\_config.ia\_user role to other users based on the access level required.

## Choose an install option

When you first open the Product Hub, two install options are available. Choose the option that matches the state of your instance.

-   **Start setup**

    Use this option to install the Software Asset Management application on a new instance. The Product Hub installs the core application, installs the dependent applications and plugins, and applies the default configurations.

-   **Upload update set**

    Use this option to move an existing setup from another instance. Upload the batch update set as an XML file, preview the changes in a new tab, and commit the batch. The Product Hub finishes the install using the uploaded configuration.


## Track progress and manage components

The tile status label on Admin Home reflects the current stage of the setup and moves through three states:

-   **Ready to install**

    The label shown before the install starts. The core application isn't installed on your instance.

-   **Installation in progress**

    The label shown while the guided flow runs. The Product Hub installs the core application and its dependent components.

-   **Ready to configure**

    The label shown after the core install completes and the default configurations are applied. The Product Hub landing page changes to a manage view.


The Manage view provides two elements for the post-install phase:

-   **Configure card**

    Opens the Configuration Console so an administrator can complete the remaining configuration items. For details, see [Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md).

-   **Installation progress panel**

    Lists the applications and plugins grouped with Software Asset Management, sorted across three tabs: **Not installed**, **Installed**, and **Updates available**. Use the tabs to install remaining components, review installed components, or apply available updates.


-   **[Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md)**  
Install Software Asset Management and its dependent applications and plugins from using Product Hub. The Product Hub applies the default configurations and prepares your instance for the Configuration Console.

**Parent Topic:**[Software Asset Management installation methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/installing-sam-app.md)

**Related topics**  


[Software Asset Management installation methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/installing-sam-app.md)

[Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md)

[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)


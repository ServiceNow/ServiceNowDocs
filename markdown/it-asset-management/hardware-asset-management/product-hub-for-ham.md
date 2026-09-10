---
title: Hardware Asset Management on Product Hub
description: Product Hub provides a single location to install, update, and manage HAM applications and plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/product-hub-for-ham.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-08-12"
reading_time_minutes: 2
breadcrumb: [Installing Hardware Asset Management, Configure, Hardware Asset Management, IT Asset Management]
---

# Hardware Asset Management on Product Hub

Product Hub provides a single location to install, update, and manage HAM applications and plugins.

The Product Hub gives administrators a single starting point to install Hardware Asset Management and additional applications, and configure them using the Configuration Console.

**Important:** Product Hub and Configuration Console are available starting from Hardware Asset Management version 16.0.0 \(Zurich Patch 12\).

## Key benefits

Product Hub provides the following benefits for HAM:

-   Reduces manual setup effort with a single starting point for HAM installation and configuration.
-   Displays all HAM applications and plugins available for your subscription tier, organized by installation status.
-   Shows available updates for installed HAM applications so administrators can keep HAM current.
-   Displays installation progress so administrators can track the status of HAM applications being installed through the ProductHhub.
-   Links to HAM product documentation, release notes, community resources, and a product overview video.

## Access and roles

Access to Product Hub requires one of two granular roles, which a system administrator must grant:

|Role|Access level|
|----|------------|
|ia\_admin|Full access: install, update, and manage HAM applications and plugins|
|ia\_user|View-only access: browse Product Hub but can't install applications|

**Note:** System administrators have access to Product hub by default. A system administrator must grant ia\_admin or ia\_user role to other users based on the access level required.

## How it works

Product Hub is accessible from the Admin Home page through the **Hardware Asset Management** card in the **Manage your products** section.

**Important:** The **Hardware Asset Management** card is available only after you install one of the following applications on your ServiceNow instance:

-   AI Native SKUs: ServiceNow Otto for Setup \(sn\_ia\)
-   Non-AI Native SKUs: Setup Hub \(sn\_ia\_base\)

-   **First-time installation**

    When the core HAM application isn't installed and the administrator selects the **Hardware Asset Management** card, Product Hub displays the following options:

    -   **Start new setup**: Installs HAM and the required applications and plugins for the first time.
    -   **Upload new batch**: Moves an existing HAM setup from another ServiceNow instance by uploading a batch update set.
-   **Managing applications after installation**

    After the core HAM application is installed, Product Hub displays the following tabs so administrators can manage additional HAM applications and plugins:

    -   **Not installed** - Applications and plugins available for your subscription tier that are not yet installed. If you move to a higher subscription tier, the mandatory core application for that tier also appears here.
    -   **Installed** - Applications and plugins currently installed in the ServiceNow instance.
    -   **Updates available** - Available updates for installed HAM applications.
    The applications and plugins displayed in the **Not installed** tab depend on your subscription tier.

    **Note:** When the HAM application is installed, Product Hub displays the **Installed**, **Not installed**, and **Updates available** tabs instead of the **Start new setup** option. The **Configure** card is also available and links to the Configuration Console, where administrators can track configuration progress. For more details, see [Configuration Console for Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/config-console-ham.md).



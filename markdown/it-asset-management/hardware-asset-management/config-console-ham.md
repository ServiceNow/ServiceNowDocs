---
title: Configuration Console for Hardware Asset Management
description: The Configuration Console gives administrators a centralized, module-by-module setup experience to configure Hardware Asset Management features after installation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/config-console-ham.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management]
---

# Configuration Console for Hardware Asset Management

The Configuration Console gives administrators a centralized, module-by-module setup experience to configure Hardware Asset Management features after installation.

**Important:** Product Hub and Configuration Console are available starting from Hardware Asset Management version 16.0.0 \(Zurich Patch 12\).

## Key benefits

-   Gives administrators a single location to view and complete all hardware asset management configurations, without navigating across multiple application areas.
-   Shows completion status for each module, so administrators can track setup progress at a glance.
-   Links to relevant documentation directly within the console during module configuration.
-   Offers AI assistance to configure items such as assignment groups, users, and roles.

    **Note:** AI-assisted configuration provides suggestions based on your instance data and may not always be accurate. Review and validate all AI-generated configurations before applying them to verify they meet your organization's requirements.


## Access Configuration console

After installing the Hardware Asset Management application, a **Configure** option appears on the Product Hub page. Select this option to open the Configuration Console.

## Configuration console overview

The **Configure Hardware Asset Management** page is the landing page of the Configuration Console. It has three main areas:

-   **Configuration Summary**

    The Configuration Summary pane lists all configuration items organized into four modules: **HAM Foundations**, **Team management**, **Otto**, and **Operations**. Each group expands to show individual setup items.

-   **Setup status**

    Displays a tile for each configuration module with a progress indicator showing the number of items configured out of the total. Select **Get Started** to begin configuring a group, or **Continue** to resume where you left off.

-   **Configuration activity**

    Displays the configuration changes recorded on this instance. Use the **Configured items** tab to review individual items marked as configured. Use the **Completed batches** tab to review changes grouped into completed batched update sets.


## Reuse and AI-assisted configuration

The Configuration Console header provides two options outside the standard item-by-item workflow:

-   **Package and download**

    Groups completed configuration changes into a batched update set and downloads it. Apply the update set on another instance to replicate the same configuration without repeating the manual work.

-   **Configure with AI**

    Opens ServiceNow Otto to configure supported items with AI assistance. Available for Assignment groups, Users, and Roles in the Team management configuration module.


## Modules in Configuration Console

The modules available in the Configuration Console depend on which applications are installed on your ServiceNow instance. Configuration Console modules require specific roles to view and configure setup items.

<table id="table_jpg_xfw_gkc"><thead><tr><th>

Module

</th><th>

Setup items

</th><th>

Roles required

</th></tr></thead><tbody><tr><td rowspan="7">

**HAM Foundations**

</td><td>

**HAM Resource Category**

</td><td>

ham\_admin

</td></tr><tr><td>

**Content Service setup**

</td><td>

ham\_admin

</td></tr><tr><td>

**Hardware Content download**

</td><td>

admin

</td></tr><tr><td>

**Custom model categories**

</td><td>

ham\_admin

</td></tr><tr><td>

**CMDB Success Advisor**

</td><td>

ham\_admin

</td></tr><tr><td>

**Scheduled jobs**

</td><td>

admin

</td></tr><tr><td>

**Properties****Note:** For details on system properties that can be configured from the Configuration Console, see [Hardware Asset Management system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/ham-system-properties.md).

</td><td>

-   **Asset lifecyle and operations**
    -   ham\_admin
    -   sn\_hamp.ham\_system\_admin
    -   asset\_system\_admin
    -   inventory\_admin
    -   procurement\_system\_admin
-   **Procurement and inventory**
    -   ham\_admin
    -   asset\_system\_admin
    -   contract\_system\_admin
    -   procurement\_system\_admin
    -   sn\_hamp.ham\_system\_admin
-   **Reporting**: ham\_admin
-   **System configuration**: model\_manager
-   **Others**: ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td rowspan="3">

**Team management**

</td><td>

**Assignment groups**

</td><td>

admin

</td></tr><tr><td>

**Users**

</td><td>

admin

</td></tr><tr><td>

**Roles**

</td><td>

admin

</td></tr><tr><td>

**Otto**

</td><td>

**Otto skills****Note:** This module appears only when the ServiceNow Otto for Hardware Asset Management \(HAM\) application is installed.

</td><td>

admin

</td></tr><tr><td rowspan="3">

**Operations**

</td><td>

**Asset lifecycle**-   **Contract Workflows**
-   **Asset Automation**
-   **Asset lifecycle category**
-   **Asset lifecycle catalog items**
-   **Asset lifecycle workflows**

</td><td>

-   **Contract Workflows**: ham\_admin
-   **Asset Automation**: ham\_admin
-   **Asset lifecycle category**: ham\_admin and sn\_hamp.ham\_system\_admin
-   **Asset lifecycle catalog items**: ham\_admin and sn\_hamp.ham\_system\_admin
-   **Asset lifecycle workflows**: admin

</td></tr><tr><td>

**Inventory**-   **Stockroom types**
-   **Stockrooms**
-   **Service locations**
-   **Distribution channels**

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

**Asset integrations**-   **Shipping integration profiles**
-   **Shipping carrier profiles**
-   **Zero touch refresh**

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr></tbody>
</table>For more details on setup using these modules, see [Modules in the Configuration Console for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/config-console-modules-ham.md).


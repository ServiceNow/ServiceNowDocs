---
title: Activate Cost Management
description: Activate the Cost Management plugin \(com.snc.cost\_management\) using the admin role.
locale: en-US
release: australia
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# Activate Cost Management

Activate the Cost Management plugin \(com.snc.cost\_management\) using the admin role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

4.  Select **Activate**.

    **Note:** To load the demo data, select the **Load demo data** check box.


-   **[Components installed with Cost Management](../reference/r_InstalledWithCostManagement.md)**  
Several components are installed with the Cost Management application.
-   **[Cost overview module roles](../reference/r_CostOverviewModuleRoles.md)**  
Only certain roles can customize Cost Overview modules. In addition to viewing, roles with access can refresh, add, delete, and rearrange reports.

**Parent Topic:**[Cost Management](../reference/r_CostManagement.md)


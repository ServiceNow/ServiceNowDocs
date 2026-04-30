---
title: Activate Procurement
description: You can activate the Procurement plugin that provides core procurement capabilities.
locale: en-US
release: yokohama
product: Procurement
classification: procurement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Procurement, Asset Management, IT Service Management]
---

# Activate Procurement

You can activate the Procurement plugin that provides core procurement capabilities.

## Before you begin

Role required: procurement\_admin, procurement\_user

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Procurement plugin \(com.snc.procurement\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Procurement](../reference/r_InstalledWithProcurement.md)**  
Several types of components are installed with Procurement.

**Parent Topic:**[Procurement](../concept/c_Procurement.md)

**Related topics**  


[Procurement roles](../reference/r_ProcurementRoles.md)

[Procurement workflows](../concept/c_ProcurementWorkflows.md)

[Use the Procurement Overview module](t_UsingTheProcurementOverviewModule.md)

[Sourcing items in a service catalog request](../concept/c_SourcingRequestItems.md)

[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

[Receive assets](../concept/c_ReceiveAssets.md)

[Domain separation and Procurement](../concept/domain-separation-procurement.md)


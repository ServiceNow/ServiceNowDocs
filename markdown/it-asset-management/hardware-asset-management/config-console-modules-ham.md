---
title: Modules in the Configuration Console for HAM
description: Module-by-module listing of the setup items in the Configuration Console for HAM, with descriptions of what each item configures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/config-console-modules-ham.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 8
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Modules in the Configuration Console for HAM

Module-by-module listing of the setup items in the Configuration Console for HAM, with descriptions of what each item configures.

## HAM Foundations

Setup items for core Hardware Asset Management configurations.

<table id="table_z14_3mb_hkc"><thead><tr><th>

Setup items

</th><th>

Description

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

HAM Resource Category

</td><td>

Opt in or opt out of the Hardware Asset Management resource categories that are part of your HAM subscription. For more details, see [Opt-in or opt-out of HAM license resource categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/optin-optout-ham-license-resource-categories.md).

</td><td>

ham\_admin

</td></tr><tr><td>

Content service setup

</td><td>

Opt in or opt out of the Hardware Asset Management Content Service for each model category. When opted in, your ServiceNow instance shares unrecognized hardware and consumable model details with ServiceNow to improve the normalization library. For more information, see [Opt-in to the Hardware Asset Management Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/opt-in-hardware-normalization.md)

</td><td>

ham\_admin

</td></tr><tr><td>

Hardware content download

</td><td>

View and manage the scheduled jobs that control hardware content downloads. Select a job to review or update its schedule. For more information, see [Import and export content data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/import-export-ham.md).

</td><td>

admin

</td></tr><tr><td>

Custom model categories

</td><td>

Create and manage custom model categories that extend the standard hardware, asset, and consumable model class hierarchy. For more details, see [Create model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/product-catalog/t_CreatingModelCategories.md).

</td><td>

ham\_admin

</td></tr><tr><td>

CMDB Success Advisor

</td><td>

Access the CMDB success advisor dashboard for HAM to configure discovery probing settings that prevent duplicate hardware asset and configuration item records.-   **Prerequisites**
    -   The CMDB Success Advisor plugin must be installed.
    -   The sn\_cmdb\_admin and ham\_admin roles are required for full configuration access. With only the ham\_admin role, the dashboard opens in read-only mode.

For more information, see [Using CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-use.md).

</td><td>

ham\_admin and sn\_cmdb\_admin

</td></tr><tr><td>

Scheduled jobs

</td><td>

View and manage scheduled jobs that support Hardware Asset Management operations, such as Hardware Normalization, lifecycle generation, licensing data, loaner asset allocations, and performance analytics scoring. You can view schedules, enable or disable jobs, and configure run intervals. Select a job to edit its schedule or configuration, or select **New** to create a scheduled job.

</td><td>

admin

</td></tr><tr><td>

Properties

</td><td>

View and configure the system properties that control Hardware Asset Management behavior. Toggle Boolean properties On or Off, enter integer values, or select and enter values for string and choice properties. Properties are grouped into five categories:

1.  Asset lifecycle &amp; Operations
2.  Procurement &amp; Inventory
3.  Reporting
4.  System configuration
5.  Others

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

</td></tr></tbody>
</table>## Team management

Setup items for managing the groups, users, and roles that support HAM operations.

<table id="table_ahg_dhc_hkc"><thead><tr><th>

Setup item

</th><th>

Description

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Assignment groups

</td><td>

Create and manage assignment groups for Hardware Asset ManagementSelect an existing group to edit its members and settings, or select **Add a group** to create a group. For more information, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateAGroup.md).

</td><td>

admin

</td></tr><tr><td>

Users

</td><td>

Create and manage records for users involved in HAM operations, including their details, roles, and group memberships. Select a user to update their details, or select **Add a user** to create a user record. For details, see [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateAUser.md).

</td><td>

admin

</td></tr><tr><td>

Roles

</td><td>

Create and manage the roles assigned to users and groups. Assign roles to control what each user or group can see and do within the application.Select **New** to create a role. For details, see [Create a role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateARole.md).

</td><td>

admin

</td></tr></tbody>
</table>## Otto

If ServiceNow Otto for Hardware Asset Management \(HAM\) is installed, expand the **Otto** module to enable and customize preconfigured AI skills to automate common HAM workflows. Selecting **Otto Skills** opens the \[var.now-assist-admin\] filtered to the **HAM** tab in a new window, where you can edit existing skill configurations. When done, close the window to return to the Configuration Console.

## Operations

Setup items for asset Lifecycle, inventory, and asset integration configurations.

<table id="table_fgz_b4d_hkc"><thead><tr><th>

Setup item

</th><th>

Description

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Contract Workflows

</td><td>

Turn the contract renewal flow on or off. When turned on, administrators can choose between the task-based contract renewal workflow and the classic flow. Toggle the setting to the required state. For more details, see [Contract renewal workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/contract-management/cont-renew-wf.md).

</td><td>

ham\_admin

</td></tr><tr><td>

Asset Automation

</td><td>

Configure the Asset action column to appear automatically in the related lists of incident and change request records. Select **Configure** to add the column automatically. When you set the **Asset action** field to **Swapped**, the **Swapped CI** field also becomes available and must be completed before you can close the record.

For more details, see [Asset life-cycle automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/asset-lifecycle-automation.md).

</td><td>

ham\_admin

</td></tr><tr><td>

Asset lifecycle category

</td><td>

Activate asset lifecycle category so it appears in the Service Catalog.

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

Asset lifecycle catalog items

</td><td>

Activate asset lifecycle catalog items so they appear in the Service Catalog. Toggle the catalog item on to make it available in the Service Catalog.

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

Asset lifecycle workflows

</td><td>

View and manage the workflows that support hardware asset lifecycle processes. From the list, select a workflow to open it in Workflow Studio, where you can review or customize it.

</td><td>

admin

</td></tr></tbody>
</table><table id="table_b13_nqd_hkc"><thead><tr><th>

Setup item

</th><th>

Description

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Stockroom types

</td><td>

Create and manage stockroom types that classify the stockrooms in your ServiceNow instance. Select an existing type to edit it or select**New** to create a stockroom type. For more information, see [Create a new stockroom type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/t_CreateANewStockroomType.md).

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

Stockrooms

</td><td>

Create and manage the stockrooms used to track hardware asset inventory. Select an existing stockroom to update its details or select **Add a stockroom** to create a stockroom.

For more information, see [Create a stockroom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/view-create-stockroom.md).

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

Service locations

</td><td>

View and manage the service locations associated with your stockrooms. Select a record to edit it or select **New** to create a service location. For more information, see [Associate a stockroom with service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/associate-stockroom-with-service-locations.md).

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr><tr><td>

Distribution channels

</td><td>

Create and manage the distribution channels that define how hardware assets move between stockrooms. Select an existing channel to edit it or select **New** to create one. For more information, see [Link stockrooms into a distribution channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/associate-stockroom-with-distribution-channels.md).

</td><td>

ham\_admin and sn\_hamp.ham\_system\_admin

</td></tr></tbody>
</table><table id="table_ap2_vrd_hkc"><thead><tr><th>

Setup item

</th><th>

Description

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Shipping integration profiles

</td><td>

View and manage carrier integration profiles that define the connection between your ServiceNow instance and a shipping carrier API. For more information, see [Create a carrier integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-carrier-integration-profile.md).**Note:** Creating a profile requires completing the carrier API integration separately before the profile can be used. For more information, see [Creating an integration script include for third-party carrier applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/creating-integration-script-include-ham.md).

</td><td>

ham\_admin and asset

</td></tr><tr><td>

Shipping carriers

</td><td>

Create and manage the shipping carriers used to associate with an integration profile.Select **New** to add a carrier and enter the details needed to support API integration with that carrier's shipping system. For more information, see [Create a shipping carrier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-shipping-carrier.md).

</td><td>

ham\_admin

</td></tr><tr><td>

Zero touch refresh

</td><td>

Create and manage zero touch refresh models that define which hardware assets are eligible for refresh. Select **New** to create a model, specifying the hardware model and location. When a model is active, eligible assets are automatically identified for refresh based on the configured criteria. For more information, see [Configure replacement models for a refresh model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-replacement-model.md).

</td><td>

ham\_admin

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/reference-hardware-asset-management.md)


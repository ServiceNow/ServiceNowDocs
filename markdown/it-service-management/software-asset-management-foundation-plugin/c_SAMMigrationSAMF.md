---
title: Software Asset Management Foundation plugin migration
description: Migrate from the Software Asset Management plugin to the Software Asset Management Foundation plugin to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.
locale: en-US
release: xanadu
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Software Asset Management Foundation plugin Administration, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin migration

Migrate from the Software Asset Management plugin to the Software Asset Management Foundation plugin to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.

After automatic changes are performed during plugin activation, successful migration from the Software Asset Management \(com.snc.software\_asset\_management\) plugin to the Software Asset Management Foundation \(com.snc.sams\) plugin requires a [Overwrite customizations for Software Asset Management migration](https://www.servicenow.com/docs/access?context=c_SAMMigration&version=xanadu&pubname=xanadu-it-asset-management&section=t_MigrateSAMCustom&ft:locale=en-US) to be performed by the customer.

Customizations to forms and lists may need to be manually overwritten by the customer after plugin activation. In addition, certain fields in software models, software entitlements, user/device allocations forms require manual configuration by the customer after plugin activation.

## Automatic changes

The Software Asset Management Foundation \(com.snc.sams\) plugin performs these automatic changes:

-   Tables
    -   Table labels renamed

        |Table|Original Label|New Label|
        |-----|--------------|---------|
        |\[alm\_license\]|Software License|Software Entitlement|
        |\[alm\_entitlement\_user\]|User Entitlement|User Allocations|
        |\[alm\_entitlement\_asset\]|Device Entitlement|Device Allocations|

    -   Adds new tables and script includes.
    -   Adds any string value in the Software Entitlements **License key** field to the License Key \[samp\_sw\_license\_key\] table
-   Field names and values
    -   **Inference mandatory** field

        For software models that have suite components \(to bundle software models\), the **Inference mandatory** field value in the Software Suite \[cmdb\_m2m\_suite\_model\] table is transferred to a new **Mandatory** field

    -   **Rights** field

        The Software Entitlements \(formerly Software Licenses\) **Rights** field value in the License Entitlements \[alm\_entitlement\] table is transferred to a new **Purchased rights** field, and name changed from **Rights** to **Active rights**

    -   The **Software model** field for a software entitlement allocation \(Software Entitlement \[alm\_license\] table\) is automatically set to the software model on the entitlement \(License Entitlements \[alm\_entitlement\] table\)
    -   The quantity for a software entitlement allocation \(License Entitlements \[alm\_entitlement\] table\) is set to 1 unless there are multiple allocations

        If there are multiple software entitlement allocations for the same user or device, the allocations are aggregated into one record, the quantity is set to the count of aggregated records, and duplicate allocations are not allowed.

-   Forms and lists

    Software Models, Entitlements \(formerly Software License\), Discovery Models, and Software Installations form and list layouts are modified to fit the new application

    **Note:** Any customizations to these forms and lists must be manually overwritten after plugin activation.

-   Functionality

    |Functionality|Description|
    |-------------|-----------|
    |License and software counters|The scheduled job trigger for SAM License Counters is changed to None so that it is deactivated, and software counters are disabled.|
    |Auto-match functionality|The auto-match functionality, which attempts to match a discovery model to a corresponding software model, is deactivated.|
    |Navigation menu|The navigation menu for the Software Asset Management plugin is deactivated and renamed.|
    |Business rules|Legacy business rules applied to discovery models are disabled.|


-   **[Overwrite customizations for Software Asset Management Foundation plugin migration](../task/t_MigrateSAMCustomSAMF.md)**  
When migrating from the Software Asset Management plugin to the Software Asset Management Foundation plugin, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.

**Parent Topic:**[Software Asset Management Foundation plugin Administration](c_SAMAdministrationSAMF.md)


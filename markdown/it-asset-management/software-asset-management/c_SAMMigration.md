---
title: Software Asset Management migration
description: Migrate from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.When migrating from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Setting up Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software Asset Management migration

Migrate from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.

After automatic changes are performed during plugin activation, successful migration from the Software Asset Management \(com.snc.software\_asset\_management\) plugin to the Software Asset Management Professional \(com.snc.samp\) plugin requires a [manual procedure](c_SAMMigration.md#) to be performed by the customer.

Customizations to forms and lists may need to be manually overwritten by the customer after plugin activation. In addition, certain fields in software models, software entitlements, user/device allocations forms require manual configuration by the customer after plugin activation.

## Automatic changes

The Software Asset Management Professional \(com.snc.samp\) plugin performs these automatic changes:

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
    |Navigation menu|The navigation menu for the Software Asset Management \(com.snc.software\_asset\_management\) plugin is deactivated and renamed.|
    |Business rules|Legacy business rules applied to discovery models are disabled.|


**Parent Topic:**[Setting up Software Asset Management](setup-sam.md)

## Overwrite customizations for Software Asset Management migration

When migrating from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.

### Before you begin

Role required: admin

### About this task

If these lists and forms have been customized before the migration, they may have been skipped during plugin activation and, in that case, require further action.

-   Software Entitlements \(formerly Software Licenses\)
-   Software Allocations \(formerly Software Entitlements\)
-   Software Models
-   Discovery Models
-   Software Installations

You can review plugin activation changes in the [Upgrade History](https://www.servicenow.com/docs/access?context=c_UpgradeHistory&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) module to determine what changes have automatically been skipped so you can [resolve a skipped update](https://www.servicenow.com/docs/access?context=t_ResolveASkippedUpdate&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), if needed.

Certain fields added by the migration also must be configured to take advantage of the new features offered.

### Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Upgrade History**.

2.  Identify the records that correspond to the upgrade history for the activation of the Software Asset Management Professional \(com.snc.samp\) plugin.

    The records in System Upgrades list that represent plugin activation contain the value **n/a** in the **From** field, and plugin name in the **To** field \(such as com.snc.samp, com.snc.samp.core, com.snc.sam.core, com.glide.data\_services\_canonicalization.client, com.snc.asset\_management, com.snc.model, com.snc.procurement\). You can determine the list of related plugins based on the time stamp of when the Software Asset Management plugin was activated by sorting on the **Upgrade started** column.

3.  Open a Software Asset Management upgrade record that has changes skipped.

4.  In the **Upgrade Details** related list, open an Upgraded Details record, and then click **Resolve Conflicts** to view a side-by-side comparison of the base system file with the customized file.

5.  Click **Revert to Base System** to overwrite the skipped change if it applies to form or list customization, and note down the changes.

    Repeat these steps for all upgrade entries with skipped changes relating to customizations.

6.  In the Software Asset Management application, manually reconfigure your original form and list customizations.

7.  In the Software Asset Management application, set new field values \(added as part of the automatic changes performed by plugin activation\) to take advantage of the new features offered.

    1.  Navigate to **Software Asset** &gt; **Licensing** &gt; **Software Models**.

        -   Select the software product in the **Product** reference field.
        -   Select a discovery map, or clear the **Discovery Map** field and set the discovery conditions to find all discovery models that correspond to the software model.
    2.  Navigate to **Software Asset** &gt; **Licensing** &gt; **Software Entitlements** \(formerly Software Licenses\).

        -   Navigate to **Software Asset** &gt; **Licensing** &gt; **Software Entitlements** \(formerly Software Licenses\).
        -   Select the **License Metric** that the software license is counted against when reconciliation is run.
        -   Define the upgrade and downgrade scenarios covered by certain rights.
    3.  In the **User Allocations** and **Device Allocations** related lists \(formerly User/Device Entitlements\), verify that the number of allocated rights are not more than rights owned.

        If so, delete allocations so that the number of allocations does not exceed the number of rights owned.

8.  If you have entitlements that require management of license keys, you can create multiple license keys associated to the same entitlement, as well as allocate these license keys to a user or device.


**Related topics**  


[plugin](https://www.servicenow.com/docs/access?context=c_SoftwareAssetManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)


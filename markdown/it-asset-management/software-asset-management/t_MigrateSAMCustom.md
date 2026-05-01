---
title: Overwrite customizations for Software Asset Management migration
description: When migrating from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Configure, Software Asset Management, IT Asset Management]
---

# Overwrite customizations for Software Asset Management migration

When migrating from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.

## Before you begin

Role required: admin

## About this task

If these lists and forms have been customized before the migration, they may have been skipped during plugin activation and, in that case, require further action.

-   Software Entitlements \(formerly Software Licenses\)
-   Software Allocations \(formerly Software Entitlements\)
-   Software Models
-   Discovery Models
-   Software Installations

You can review plugin activation changes in the [Upgrade History module](https://www.servicenow.com/docs/access?context=uc-history-module&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to determine what changes have automatically been skipped so you can [Resolve a skipped update and set a resolution status](https://www.servicenow.com/docs/access?context=uc-resolve-skipped-update&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US), if needed.

Certain fields added by the migration also must be configured to take advantage of the new features offered.

## Procedure

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


**Parent Topic:**[Configuring Software Asset Management](../concept/Config-sam-workspace.md)

**Related topics**  


[plugin](https://www.servicenow.com/docs/access?context=c_SoftwareAssetManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)


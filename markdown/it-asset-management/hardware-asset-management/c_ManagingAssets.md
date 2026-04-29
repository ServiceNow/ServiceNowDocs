---
title: Asset and CI management
description: Asset and configuration item \(CI\) management refers to creating assets, setting appropriate states and substates, synchronizing assets and CIs, managing consumables, and retiring assets.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset and CI management

Asset and configuration item \(CI\) management refers to creating assets, setting appropriate states and substates, synchronizing assets and CIs, managing consumables, and retiring assets.

## Relationship between asset and CI

It’s important to manage the relationship between assets and associated CIs. Assets are tracked with the Asset Management application, which focuses on the financial aspects of owning property. Configuration items are stored in the CMDB, which is used to track items and make them available to users.

When an asset has a corresponding configuration item, the asset record and the configuration item record are kept synchronized with two business rules.

-   **Update CI fields on change** \(on the Asset \[alm\_asset\] table\)
-   **Update Asset fields on change** \(on the Configuration Item \[cmdb\_ci\] table\)

**Note:** Assets and CIs can be synchronized only if they’re logically mapped.

## Asset-CI mapping and synchronization

The State field of asset record and Status field of CI record are synchronized so that changes made on one form trigger the same update on the corresponding form, ensuring consistent reporting.

**Note:** The ServiceNow AI Platform synchronizes updates between assets and configuration items only if the asset and configuration item are pointed toward each other.

The following diagram illustrates the concept of Asset-CI mapping and synchronization.

![Overview of Asset-CI mapping and synchronization process](../image/AssetCImapsync.png "Overview of Asset-CI mapping and synchronization")

This synchronization and mapping is based on the following factors:

-   Asset state and CI status aren’t mapped on one-to-one basis. Rather they’re mapped to the most logical counterpart on the other table. For example, for a hardware asset set to state **In Stock - Pending disposal**, the corresponding CI is set to **In Disposition** with no substate.
-   This synchronization happens between the asset’s State field and the following CI fields:
    -   Install Status field: Install Status doesn’t have a sub status and must be used for non-hardware CIs.
    -   Hardware Status and Sub status field: Hardware Status is visible only for Hardware CI.
-   Drive changes by updating the state on the Asset form. The Asset-CI synchronization can be driven in the following ways:

    -   Asset to CI synchronization: Change to the asset’s status updates the logically mapped CI’s Install Status or Hardware Status and sub status.
    -   CI to Asset: Change to the CIs Install Status or Hardware Status updates the logically mapped asset’s states and sub states.
-   For a CMDB hardware CI, if both Hardware Status and Install Status is updated, the Hardware Status change is considered for mapping the corresponding state of the asset.
-   CIs Install Status and Hardware Status work independently, so the two fields aren't related. CI’s Hardware Status change doesn’t change CIs Install Status and vice versa. To avoid confusion, keeping both status for CMDB CI Hardware isn’t recommended.

## List of the fields that get synced between Asset and CI

When changing any of the following fields on the asset or CI record, the same field on the corresponding record is automatically updated \(except for the **Cost** field, which is informational-only on the CI record\).

The following is a list of fields that are synchronized.

-   Asset tag
-   Assigned
-   Assigned to
-   Checked in
-   Checked out
-   Company
-   Cost \(synchronizes in only one direction: asset to CI\)
-   Cost center
-   Delivery date
-   Department
-   Due in
-   Due
-   GL account
-   Install date
-   Invoice number
-   Justification
-   Lease id
-   Location
-   Managed by
-   Model \(model\_id in CI\)
-   Order date
-   Order received
-   Ordered
-   Owned by
-   PO number
-   Purchase date
-   Purchased
-   Serial number
-   Support group
-   Supported by
-   Vendor
-   Warranty expiration

## Asset, CI, and IBI synchronization

Any item that is provided as a service or sold to your customer is tracked as an Install Base Item \(IBI\). The Model category table associates Asset, CI, and Install Base Item \(IBI\). The synchronization between the asset and IBI is through the CSDM Life Cycle Stage and Status fields.

When the CSDM \(csdm.lifecycle.migration.activated\) plugin is activated on your ServiceNow instance, synchronization of the CSDM Lifecycle fields between the asset and CI depends on the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property. If you are upgrading to the Xanadu release, this system property is set to **false** by default. Synchronization between the asset and CI happens in one of the following ways:

-   When the system property is set to **false**, synchronization of the CSDM Lifecycle fields is through the legacy State and Substate fields.
-   When the system property is set to **true**, the CSDM Life Cycle Stage and Status fields are directly synchronized.

**Note:** If you are activating the CSDM \(csdm.lifecycle.migration.activated\) plugin on your ServiceNow instance for the first time, and you have custom States and Substates for the asset or CI, then make sure to configure mapping between the legacy fields and the CSDM Lifecycle fields. For more information, see [Enabling life-cycle synchronization from legacy to asset](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

![Synchronization of status fields](../../hardware-asset-management/image/asset-ci-ibi-sync.png "Asset, CI, and IBI synchronization when the csdm.lifecycle.sync.between.ci.and.asset.activated system property is set to false")

-   **Synchronization of updates from asset to IBI and CI**

    Updates made to the State or Substate field of an asset are synchronized with the associated IBI and CI. For example, when the State field of the asset is updated to In use, synchronization happens as follows.

    -   The Life Cycle Stage and Life Cycle Stage Status of the asset are set to Operational and In use, these field values are then synchronized with Stage and Status fields of IBI asset.
    -   The Status and Substatus fields of the CI change to Installed and In use.
-   **Synchronization of updates from IBI to asset and CI**

    Updates made to the Life Cycle Stage and Life Cycle Stage Status fields of an IBI asset are synchronized with the legacy State and Substate fields of the asset through the CSDM fields. The legacy fields of the asset are then synchronized with the associated CI. For example, when the life Life Cycle Stage and Life Cycle Stage Status fields of an IBI asset are updated to Defective and In Stock, synchronization happens as follows.

    1.  The Life Cycle Stage and Life Cycle Stage Status of the asset change to In Stock and Defective. These field values are synchronized with the State and Substate fields of the asset.
    2.  The State and Substate fields of the asset are then synchronized with the corresponding fields of the associated CI.
-   **Synchronization of updates from CI to asset and IBI**

    Updates made to the Status and Substatus fields of a CI are synchronized with the corresponding fields of the asset. The legacy fields of the asset are then synchronized with the Life Cycle Stage and Life Cycle Stage Status fields of the IBI asset through the CSDM fields. For example, when the Status and Substatus fields of a CI are updated to Retired and Donated, the corresponding fields of the asset change. The changes from the asset are synchronized with the IBI asset and the Life Cycle Stage and Life Cycle Stage Status fields change to End of Life and Retired.


![Synchronization through CSDM fields](../../hardware-asset-management/image/asset-ci-ibi-sync-new-prop.png "Asset, CI, and IBI synchronization when the csdm.lifecycle.sync.between.ci.and.asset.activated system property is set to true")

-   **Synchronization of updates from asset to CI and IBI**

    Updates made to the legacy State and Substate fields of the asset are synchronized between the asset and CI as follows:

    -   The Life Cycle Stage and Life Cycle Stage Status fields of the asset are updated with values corresponding to the legacy State and Substate fields of the asset.
    -   The State and Substate fields of the asset are then directly synchronized with the corresponding legacy fields of the associated CI.
    -   The Life Cycle Stage and Life Cycle Stage Status fields of the asset are then directly synchronized with the corresponding CSDM fields of the associated CI.
    However, synchronization of updates from asset to IBI is only through the CSDM Lifecycle fields.

-   **Synchronization of updates from IBI to asset and CI**

    Updates made to the Life Cycle Stage and Life Cycle Stage Status fields of the IBI are synchronized as follows:

    -   The legacy State and Substate fields of the asset are synchronized through the CSDM fields.
    -   The legacy fields of the asset are synchronized with the legacy fields of the associated CI.
    -   The Life Cycle Stage and Status fields of the asset are directly synchronized with the corresponding CSDM fields of the associated CI.
-   **Synchronization of updates from CI to asset and IBI**

    Updates made to the Life Cycle Stage and Status fields of a CI are synchronized as follows:

    -   The Life Cycle Stage and Status fields of the CI are directly synchronized with the corresponding CSDM fields of the asset.
    -   The legacy fields of the asset are then updated with the values corresponding to the CSDM fields.
    -   The legacy fields of the asset are then synchronized with the corresponding fields of the CI.
    -   The legacy fields of IBI are synchronized with the asset through the CSDM Lifecycle fields.

## Asset and CI creation properties

-   **glide.create\_alm\_asset.async**

    The system property **glide.create\_alm\_asset.async** controls whether assets are created immediately when a configuration item \(CI\) is created, or are created after a delay. A delay in asset creation enables large numbers of CIs to be created quickly. When this property is set to **true**, assets are created by the **Asset - Create asset delayed sync** scheduled job that runs every 15 minutes. View the status of the scheduled job in the Asset Job Log table \[asset\_job\_log\]. To view assets waiting to be created and asset creation errors, navigate to **Asset** &gt; **Administration** &gt; **Asset Creation Queue**. To reprocess an error, update the state from **Error** to **Ready**. The next time the scheduled job runs, it reattempts to create the asset.

    When the **glide.create\_alm\_asset.async** property is set to **false**, assets are created immediately from CIs.

    **Note:** If you upgrade to Australia from Orlando or earlier, the default value of this property is **false**. Before updating this property, review your processes that depend on an asset value present on a CI and make any necessary changes to account for delayed asset creation.

-   **glide.asset.create\_ci\_with\_ire**

    The system property **glide.asset.create\_ci\_with\_ire** enables CIs to be created from assets using the ServiceNow® Configuration Management Database \(CMDB\) Identification and Reconciliation engine \(IRE\). This property affects CI classes that have an identification rule on serial number and have no dependent relationships with other CI classes.

    **Note:** This property is applicable to CI classes that are extended from the hardware CI class \[cmdb\_ci\_hardware\].

    CIs created with the IRE are named using the format `Serial number - Model name` and the source is `SNAssetManagement`. The **Serial number** field is required on assets with model categories that correspond to these CI classes. Asset creation fails if its serial number is present on an existing CI or asset. The **Serial number** field is also required to receive purchase order line items for model categories that correspond to these CI classes. The **Serial number** field isn’t required to create pre-allocated assets, but the serial number must be provided when the asset is allocated.

    The default value of this property is false if you upgrade to Australia from Orlando or earlier. Before updating this property, review the customizations on the Serial number field and any integrations or flows that use an existing serial number to create an asset.


## Other Asset and CI system properties

-   **sn\_itam\_enable\_cache\_for\_asset\_ci\_mapping**

    The asset and CI fields are synchronized based on the mappings defined in the relevant mapping tables. Fetching these mappings on the update of an asset or CI has an impact on the performance. The **sn\_itam\_enable\_cache\_for\_asset\_ci\_mapping** system property enables you to cache the following mappings:

    -   Asset and CI fields
    -   Asset state and CI install status
    -   Asset state and CI hardware status
    Unless there isn't any change in the mapping tables, these cached mappings are fetched during the synchronization resulting in the improved system performance.

-   **sn\_itam\_common.mac\_address\_sync**

    The **sn\_itam\_common.mac\_address\_sync** system property enables you to synchronize asset and CI using the Mac address. By default, this system property is set to **false**. To enable synchronization through the Mac address, set the value of this system property to **true** in the Asset Property \[asset\_property\] table.



---
title: Hardware Asset Management system properties
description: System properties control asset lifecycle, procurement, inventory, reporting, and system configuration for the Hardware Asset Management application. You can view and update these properties from the Properties setup item in the Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/ham-system-properties.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-08-19"
reading_time_minutes: 5
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Hardware Asset Management system properties

System properties control asset lifecycle, procurement, inventory, reporting, and system configuration for the Hardware Asset Management application. You can view and update these properties from the Properties setup item in the Configuration Console.

<table id="table_jzq_bkg_jkc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.asset.create\_ci\_with\_ire**

</td><td>

Controls whether a configuration item \(CI\) is created along with an asset using IRE API.

</td></tr><tr><td>

**glide.create\_alm\_asset.async**

</td><td>

Controls when an asset is created relative to its configuration item. When set to true, asset creation is deferred and processed by the scheduled job **Asset - Create asset delayed sync**. When set to **false**, the asset is created immediately when the configuration item is created.

</td></tr><tr><td>

**sn\_itam\_enable\_cache\_for\_asset\_ci\_mapping**

</td><td>

Turns on caching for the following mappings to improve performance:-   Asset and CI fields
-   Asset state and CI install status
-   Asset state and CI hardware status

</td></tr><tr><td>

**sn\_itam\_enable\_pid\_recalculation\_for\_child\_asset**

</td><td>

Controls whether the Product Instance Identifier \(PID\) is recalculated for child assets when the parent asset is updated.

</td></tr><tr><td>

**sn\_itam\_exclude\_ibi\_asset\_reporting**

</td><td>

Excludes Install Base Item \(IBI\) assets from the Asset Workspace reports and Important actions on the Overview page.

</td></tr><tr><td>

**sn\_hamp.update\_assets\_norm\_model\_name**

</td><td>

Controls whether asset records are updated with the normalized model name when normalization runs.

</td></tr><tr><td>

**sn\_hamp.enable\_asset\_tag\_serial\_number\_edits**

</td><td>

Enables user to update asset tag and serial number of the asset to be received on the Employee Center Portal.

</td></tr><tr><td>

**sn\_hamp.approximate\_dates\_in\_hw\_lifecycle**

</td><td>

Boolean flag for hardware lifecycle date calculations. When true, the report uses all content table rows and inherits approximate dates. When false, only researched dates are used.

</td></tr><tr><td>

**sn\_itam\_enable\_caching\_for\_depreciation**

</td><td>

Turns on caching for depreciation formula in **Calculate Depreciation** scheduled job.

</td></tr><tr><td>

**sn\_hamp.enable\_asset\_action\_validation\_incident**

</td><td>

Controls whether an asset action is required to close an incident. When set to **true**, users must specify an asset action before closing an incident. When set to **false**, asset action validation is skipped on incident closure.

</td></tr><tr><td>

**sn\_hamp.enable\_asset\_action\_validation\_change\_request**

</td><td>

Controls whether an asset action is required to close a change request. When set to **true**, users must specify an asset action before closing a change request. When set to **false**, asset action validation is skipped on change request closure.

</td></tr><tr><td>

**glide.asset.procurement.sourcing.local\_stock\_transfer**

</td><td>

Controls whether local stock transfers are used as a sourcing option during procurement.

</td></tr><tr><td>

**sn\_itam\_common.enable\_asset\_attestation\_playbook**

</td><td>

Allows asset manager to enable playbook for asset attestation request

</td></tr><tr><td>

**sn\_itam\_common.close\_attestation\_async**

</td><td>

Controls whether the closure check for attestation records runs asynchronously. When set to **true**, an asynchronous check runs to determine if the attestation record needs to be closed when a user confirms an asset in the attestation request.

</td></tr><tr><td>

**sn\_hamp.migrate\_hamaudit**

</td><td>

Controls whether HAM audit data is migrated to the common audit table. When set to **true**, audit data moves to the common table. Note that migrating audit data removes access for users with the inventory\_user and inventory\_admin roles. Configure the appropriate ACLs before enabling this property to maintain user access to audits.

</td></tr><tr><td>

**sn\_itam\_common.sn\_enable\_indoormap\_for\_assets**

</td><td>

Turns on indoor map functionality for assets forms and dashboards.

</td></tr><tr><td>

**sn\_itam\_common.receive\_assets\_batch\_size**

</td><td>

Determines the batch size of the asset records when logging import and receiving jobs.

</td></tr><tr><td>

**sn\_itam\_trigger\_depreciation\_job\_after\_days**

</td><td>

Sets the number of days that must pass since the last depreciation job run before the depreciation job is allowed to run again. Default is 7 days.

</td></tr><tr><td>

**sn\_hamp.model\_lifecycle\_phase\_order**

</td><td>

Sets the priority order of hardware model lifecycle phases when multiple phases share the same start date. Enter the lifecycle phase names as a comma-separated list in increasing order of priority.

</td></tr><tr><td>

**sn\_itam\_depreciation\_job\_last\_run**

</td><td>

Records the date and time the depreciation job last ran. This is a read-only, system-managed value.

</td></tr><tr><td>

**sn\_itam\_common.put\_away\_task.drop\_off\_location.delimiter**

</td><td>

Sets the delimiter used to separate drop-off location values in put-away tasks. The drop-off location format is `Location||Stockroom||Aisle||Space`. The default delimiter is `||`.

</td></tr><tr><td>

**sn\_itam\_common.set\_default\_include\_consumables**

</td><td>

Sets the default value of the **Include consumables** field on the Asset Audits form.

</td></tr></tbody>
</table>|Property|Description|
|--------|-----------|
|**com.sn\_itam.enable\_flow\_designer.transfer\_order\_line**|Turns on Workflow Studio for processing transfer order line flows.|
|**com.sn\_itam.enable\_flow\_designer.transfer\_order**|Turns on Workflow Studio for processing transfer order flows.|
|**sn\_itam\_common.sn\_contract\_enable\_renewal\_flow**|Turns on the contract renewal flow. When enabled, users can choose between the task-based contract renewal workflow and the classic flow.|
|**sn\_itam\_po\_hide\_edit\_icon\_on\_currency\_fields**|Controls the visibility of the edit icon on currency fields in purchase order and purchase order line item records. When set to **true**, the edit icon is hidden on these fields.|
|**com.sn\_itam.enable\_flow\_designer.source\_request**|Turns on Workflow Studio for processing source requests.|
|**com.sn\_itam.enable\_flow\_designer.contract\_approval**|Turns on Workflow Studio for processing contract approvals.|
|**contract\_compliance\_check\_job.enable\_override**|Controls whether child table compliance checks override parent table checks during contract compliance processing. When set to **true**, child table compliance checks take precedence over parent table checks on the same field during contract compliance processing.|
|**contract\_compliance\_check\_job.batching**|Turns on batching for contract compliance check processing.|
|**glide.model.catalog\_item\_currency**|Sets the currency of catalog items published from a model to the currency defined on that model.|
|**sn\_hamp.enable\_shipping\_carrier\_validation\_asn**|Controls shipping carrier validation during Advanced Shipment Notification imports. When enabled, imported carrier data must exist in the shipping carrier table; rows with unrecognized carriers are ignored. Disable this property to skip validation.|
|**glide.itam\_update\_ci\_status\_from\_ritm**|Controls which configuration items are updated from a requested item. Defaults to **true** for upgraded instances and **false** for new installs and zBoot instances.|
|**sn\_itam\_tol\_bulk\_update\_max\_count**|Sets the maximum number of records that can be updated in a single bulk transfer order line operation.|
|**sn\_itam\_stockrulejob\_batch\_size**|Sets the batch size for processing stock rule data and logging results in the asset job log.|
|**contract\_compliance\_check\_job.batchSize**|Sets the batch size for the Contract Compliance Check job.|

|Property|Description|
|--------|-----------|
|**glide.sg.voice\_search.enabled**|Controls whether voice search is enabled in the Service Graph mobile application. When true, users can use voice input to perform searches.|
|**sn\_itam\_common.asset\_tco\_benchmark\_threshold\_percentage**|Sets the percentage multiplier used to compute the TCO benchmark threshold from the TCO benchmark cost.|

|Property|Description|
|--------|-----------|
|**glide.cmdb\_model.display\_name.shorten**|Generate shorter software model display name if the model name contains the manufacturer.|
|**glide.sg.image.default.cmdb\_model**|Specifies the default placeholder image for hardware asset model records that have no image. When the **picture** field on a **cmdb\_model** record is empty, the My Asset page on the Now Mobile app displays this image instead of a broken or empty thumbnail. Default value is `no_image_itam_mobile.png`.|

|Property|Description|
|--------|-----------|
|**sn\_hamp.enable\_custom\_category\_licensing**|Enables inclusion of custom category assets in HAM licensing for instances on pre-HAM V4 SKUs.|
|**sn\_hamp.sn\_ham\_active\_entitlements**|Comma separated list of active entitlements associated with the Hardware Asset Management application|

**Parent Topic:**[Hardware Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/reference-hardware-asset-management.md)


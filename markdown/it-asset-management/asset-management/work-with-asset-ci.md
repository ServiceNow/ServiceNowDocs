---
title: Work with Asset and CI
description: Asset and configuration item \(CI\) management refers to creating assets, setting appropriate states and substates, synchronizing assets and CIs, managing consumables, and retiring assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/asset-management/work-with-asset-ci.html
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Asset Management, IT Asset Management]
---

# Work with Asset and CI

Asset and configuration item \(CI\) management refers to creating assets, setting appropriate states and substates, synchronizing assets and CIs, managing consumables, and retiring assets.

-   **[Create assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_CreatingAssets.md)**  
Create hardware, software, consumable, bundle, pallet, mobile, and facility assets using the Core UI or the Hardware Asset Workspace.
-   **[Retire assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_RetiringAssets.md)**  
You can retire an asset at any time.
-   **[Delete assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_DeletingAssets.md)**  
You can delete an asset at any time.
-   **[Map asset and CI fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_CreateAssetandCIFieldsMapping.md)**  
When you map the asset and CI fields, synchronization happens both ways. Changes to either the asset or CI record are updated to the logically mapped record. You can synchronize custom mappings and mappings provided with the base instance.
-   **[Map asset state and CI install status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_CreateAssetandCIInstallStatusMapping.md)**  
Map the asset **State** and **Substate** fields to the **CI Install Status** field. The **Substatus** field of the **CI Install Status** field should not be used for hardware CIs.
-   **[Map asset state and CI hardware status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_CreateAssetandCIHardwareStatusMapping.md)**  
Map the asset **State** and **Substate** fields to the **CI Hardware Status** field. Don't use the **Substatus** field on hardware CIs because the CI synchronization does not update the field when assets are updated. When you create the mapping, you can set the synchronization direction from the asset, CI, or both.

**Parent Topic:**[Using Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/using-asset-management.md)

**Related topics**  


[Mobile app for Hardware Asset Management]()

[Manage various assets through asset classes]()

[Create fixed assets]()

[Consumables life cycle]()

[Stockrooms]()

[Manage pre-allocated assets]()

[Manage transfer order]()

[Use Organization Management]()


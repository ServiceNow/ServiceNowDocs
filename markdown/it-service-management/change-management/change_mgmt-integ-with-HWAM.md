---
title: Change Management integration with Hardware Asset Management
description: The Change Management integration with Hardware Asset Management helps in determining the asset action that must be performed on the configuration item \(CI\) that is associated with a hardware asset. Using this capability, change implementers can quickly update asset records directly from change and the Asset Manager can see current state on all assets that were updated by the change request.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Change management integrations, Reference, Change Management, IT Service Management]
---

# Change Management integration with Hardware Asset Management

The Change Management integration with Hardware Asset Management helps in determining the asset action that must be performed on the configuration item \(CI\) that is associated with a hardware asset. Using this capability, change implementers can quickly update asset records directly from change and the Asset Manager can see current state on all assets that were updated by the change request.

This integration requires the Hardware Asset Management Professional \(com.sn\_hamp\) plugin.

**Note:** You must request the activation of the Hardware Asset Management Professional \(com.sn\_hamp\) plugin from the ServiceNow® application store.

When the configuration items listed in the Affected CIs related list have an asset associated, then the **Asset action** field is populated.

You can choose an **Asset action** for the CI, from the Affected CI related list. This **Asset action** field provides three possible actions that can be selected which triggers an event.

-   **Deploy**: When this action is selected, the **sn\_hamp.asset.deploy** event is triggered.
-   **Update/Repair**: No event is triggered for this action.
-   **Retire**: When this action is selected, the **sn\_hamp.asset.retire** event is triggered.

**Note:** The **Asset action** column can be added to the Affected CI related list if not already available.

When a change request is in the **Implement** state, the proposed asset action triggers the corresponding event. When the workflow is complete, the asset action updates the asset and the related records and progresses to the **Review** state.

**Note:** If the asset action is not selected, then the change request will not progress to the **Review** state.

For more information, see [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)

**Parent Topic:**[Change management integrations](change-mgmt-integrations.md)


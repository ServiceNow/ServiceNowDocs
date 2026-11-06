---
title: Change Management integration with Hardware Asset Management
description: The Change Management integration with Hardware Asset Management helps determine the asset action that must be performed on the configuration item \(CI\) that is associated with a hardware asset. Using this capability, change implementers can update asset records directly from change and asset managers can see the current state of all assets that were updated by the change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change\_mgmt-integ-with-HWAM.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Change management integrations, Reference, Change Management, IT Service Management]
---

# Change Management integration with Hardware Asset Management

The Change Management integration with Hardware Asset Management helps determine the asset action that must be performed on the configuration item \(CI\) that is associated with a hardware asset. Using this capability, change implementers can update asset records directly from change and asset managers can see the current state of all assets that were updated by the change request.

This integration requires the Hardware Asset Management Professional \(com.sn\_hamp\) plugin.

**Note:** You must request the activation of the Hardware Asset Management Professional \(com.sn\_hamp\) plugin from the ServiceNow® application store.

When a configuration item in the Affected CIs related list has an associated asset, the **Asset action** field is populated.

You can choose an **Asset action** for the CI from the Affected CIs related list. The **Asset action** field provides the following actions:

-   **Deploy**: Triggers the **sn\_hamp.asset.deploy** event, which sets the asset to its deployed state.
-   **Update/Repair**: No event is triggered, and the asset status is unchanged.
-   **Retire**: Triggers the **sn\_hamp.asset.retire** event. If the asset isn't already retired, the action sets the asset status to **In Stock** and the substatus to **Pending Disposal**. If the asset is already retired, the status is unchanged.

**Note:** If the **Asset action** column isn't on the Affected CIs related list, you can add it.

When a change request is in the **Implement** state, the proposed asset action triggers the corresponding event. When the workflow is complete, the asset action updates the asset and the related records, and the change request moves to the **Review** state.

**Note:** If no asset action is selected, the change request doesn't progress to the **Review** state.

For more information, see [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ham-landing-page.md)

**Parent Topic:**[Change management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-mgmt-integrations.md)


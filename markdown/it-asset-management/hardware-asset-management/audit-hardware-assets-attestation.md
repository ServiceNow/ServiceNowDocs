---
title: Audit your hardware assets by using Asset Attestation
description: Improve the asset utilization by auditing the hardware assets assigned to your employees and validating if the employees are using the assigned assets.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Audit your hardware assets by using Asset Attestation

Improve the asset utilization by auditing the hardware assets assigned to your employees and validating if the employees are using the assigned assets.

As an Asset manager or an Inventory administrator, you can create an asset attestation in any of the following ways:

-   [Create an asset attestation or a schedule using the playbook](../task/create-attestation-using-playbook.md)
-   [Create an asset attestation in the Inventory view](../task/create-attestation-req-ham.md).
-   [Create an asset attestation schedule](../task/create-attest-schedule-ham.md).
-   [Create an attestation for a hardware asset](../task/attest-single-asset-ham.md)

**Important:** Starting with Hardware Asset Management version 13.0.0, the playbook is the default option for the creation of asset attestations and schedules. However, if you set the value of the **sn\_itam\_common.enable\_asset\_attestation\_playbook** system property to **false** with the asset or inventory\_admin role, you will be shown forms to complete the attestation process instead of the playbook.

As an employee, you can confirm the assets assigned to you in any of the following ways:

-   [Confirm the assigned assets using the Now Mobile app](../task/confirm-ham-assets-now-mobile.md).
-   [Confirm the assigned assets on the Employee Center portal](../task/confirm-assets-on-emp-center.md).

For more details, see [Asset Attestation](asset-attestation-ham.md).

-   **[Playbook for asset attestation](playbook-asset-attestation-ham.md)**  
The Create asset attestation playbook provides detailed, step-by-step instructions for creating an asset attestation. This playbook guides you through each stage of the attestation process, starting from filling in the asset attestation details to the completion of attestation.
-   **[Create an asset attestation in the Inventory view](../task/create-attestation-req-ham.md)**  
Create an asset attestation to validate whether the serialized hardware asset that's assigned to an employee is still in use.
-   **[Create an asset attestation schedule](../task/create-attest-schedule-ham.md)**  
Create an attestation schedule so that recurring asset attestations are created based on the frequency that you specify.
-   **[Create an attestation for a hardware asset](../task/attest-single-asset-ham.md)**  
Validate a particular serialized hardware asset by creating an attestation for that asset.
-   **[Confirming the assigned serialized hardware assets](confirming-assets-emp-portal-mobile.md)**  
As an employee, acknowledge whether you have the serialized hardware that's assigned to you either through the Now Mobile app or on the Employee Center portal.
-   **[Raise issue related to your asset on the Employee Center portal](../task/report-asset-issue-attestation.md)**  
Get the issue related to your assets resolved by reporting the issue on the Employee Center portal.
-   **[View attestations for a serialized hardware asset](../task/view-attestations-for-asset-ham.md)**  
View all the attestation records associated with a serialized hardware asset to check the status of previous asset attestations.
-   **[View open asset attestations in the Hardware Asset Workspace](../task/view-open-asset-attest-ham.md)**  
Get the details of all asset attestations that are awaiting action from your employees in the Hardware Asset Workspace.
-   **[Cancel an asset attestation](../task/cancel-asset-attestation-ham.md)**  
Cancel an asset attestation when you no longer have to validate the ownership of the serialized assets.
-   **[Cancel an attestation schedule](../task/cancel-attestation-schedule-ham.md)**  
Cancel an attestation schedule when you no longer want to create recurring asset attestations.
-   **[View open remediation tasks for asset attestations in the Hardware Asset Workspace](../task/view-open-remediations-ham.md)**  
Get the details of all the remediation tasks for asset attestations that are awaiting your action in the Hardware Asset Workspace.
-   **[Complete the remediation task for asset attestation in the Hardware Asset Workspace](../task/complete-attestation-remediation-ham.md)**  
As an asset manager or inventory administrator, complete the open remediation task that was created when your employee denied ownership of the assigned serialized hardware asset.

**Parent Topic:**[Using Hardware Asset Management](using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](Work-with-hardware-normalization.md)

[Manage asset bundles from your inventory](../task/create-bundled-assets.md)

[Manage your inventory through pallet assets](pallets-for-inventory-management.md)

[Manage loaner assets](../task/manage-loaner-asset.md)

[Donate assets to charity organizations](donate-asset-to-charity-organizations.md)

[Use Advanced Shipment Notification](../task/advanced-shipment-notification.md)

[Manage RMA requests](manage-rma-req.md)

[Create an inventory stock order request](../task/create-inventory-stock-order.md)

[Create a disposal order](../task/create-disposal-order.md)

[Use a hardware asset request flow](../task/hardware-request-flow.md)

[Audit hardware asset inventory](ham-inventory-audit.md)

[Request a Hardware Asset Refresh](../task/hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](../task/manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](manage-asset-reclaim.md)

[View RFID information of assets](../task/view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](receive-warranty-details-lenovo.md)

[Manage stockrooms](manage-your-stockrooms.md)

[Track shipments using the integration framework](tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](../task/track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](configure-ham-tco.md)

[Manage Hardware Asset Management subscriptions](managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](manage-asset-picking-stockroom-ham-ws.md)

[Manage hardware asset tasks using the Mobile Agent application](manage-hardware-asset-tasks-mobile-agent.md)

[Manage asset put away using the Hardware Asset Workspace](manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Acknowledge receipt of assets on the Employee Center portal](../task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../task/trigger-flow-ham.md)


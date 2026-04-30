---
title: Audit hardware asset inventory
description: Perform scheduled or blind audits of stockrooms and other locations, such as offices or datacenters, to confirm accurate inventory information.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-01-05"
reading_time_minutes: 8
keywords: [audit inventory, inventory audit, hardware asset inventory audit]
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Audit hardware asset inventory

Perform scheduled or blind audits of stockrooms and other locations, such as offices or datacenters, to confirm accurate inventory information.

The asset audit process involves verifying and reconciling assets between a physical location or stockroom and the ServiceNow instance. First, assets are identified by scanning their asset tag, serial number, or model barcode. Next, the records in the ServiceNow instance are checked to determine whether they match the scanned assets and the audit result is generated. You can view precise inventory information through detailed lists and reports.

You can create an audit record in the Hardware Asset Management application or the ServiceNow Agent app.

-   Use the Hardware Asset Management application to create a scheduled audit record. For more information about creating a scheduled audit record, see [Create an audit record in the Hardware Asset Management application](../task/audit-your-inventory.md).
-   Use the ServiceNow Agent app to create a blind or unscheduled audit record. For more information about creating a blind or unscheduled audit record, see [Create an audit record using the ServiceNow Agent app](../task/create-audit-using-mobile-app.md).

When an inventory audit record is created, it’s saved in the Asset Audits table, depending on the configuration for **sn\_hamp\_migrate\_hamaudit** system property.

-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **true**, the audit record is saved in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table.
-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **false**, the audit record is saved in the Asset Audits \[sn\_hamp\_asset\_audit\] table.

**Note:** Starting with Hardware Asset Management version 15.0.0, the audit inventory has been enhanced to store audit records in the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table. Before enabling audit enhancements and switching to the common Asset Audits table, you must complete all audit records that are in either **In progress** or **New** status.

Using the ServiceNow Agent app, you can scan the assets in the inventory and complete the audit process. The Hardware Asset Management application reconciles scanned assets with ServiceNow records to generate audit results. For more information about scanning assets, see [Complete a single scan inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app.md) and [Complete multi scan inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app.md).

-   **[Create an audit record in the Hardware Asset Management application](../task/audit-your-inventory.md)**  
Create an audit record to audit your inventory to determine the accuracy of your hardware and consumable assets and to optimize the inventory.
-   **[Create an audit record using the ServiceNow Agent app](../task/create-audit-using-mobile-app.md)**  
Create an inventory audit record using the ServiceNow Agent app.
-   **[Complete a single scan inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app.md)**  
Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.
-   **[Complete multi scan inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app.md)**  
Scan your inventory assets by using the ServiceNow Agent app for the multi scan audit records.
-   **[Close an asset remediation task](../task/close-an-asset-remediation-task.md)**  
View the open asset remediation from the **Inventory** view and close the task after updating the **Model category** and **Model** fields value for the asset.
-   **[Create an asset from the inventory audit screen](../task/inventory-audit-create-asset.md)**  
Create an asset record for the scanned asset that doesn't exist in your ServiceNow instance and that is detected when auditing inventory.
-   **[View audit results](../task/view-audit-results.md)**  
View the audit results after you audit your inventory. The Audit Results section is activated and shows the details of the audit result.
-   **[View deprecated audit records](../task/view-deprecated-audit-records.md)**  
View the deprecated asset audit records that are created before switching to the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table and stored in the Asset Audits \[sn\_hamp\_asset\_audit\] table.

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

[Manage and monitor hardware asset performance](manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](manage-hardware-asset-tasks-mobile-agent.md)

[Audit your hardware assets by using Asset Attestation](audit-hardware-assets-attestation.md)

[Acknowledge receipt of assets on the Employee Center portal](../task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../task/trigger-flow-ham.md)


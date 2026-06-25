---
title: Audit hardware asset inventory
description: Perform scheduled or blind audits of stockrooms and other locations, such as offices or datacenters, to confirm accurate inventory information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/ham-inventory-audit.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [audit inventory, inventory audit, hardware asset inventory audit]
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Audit hardware asset inventory

Perform scheduled or blind audits of stockrooms and other locations, such as offices or datacenters, to confirm accurate inventory information.

The asset audit process involves verifying and reconciling assets between a physical location or stockroom and the ServiceNow instance. First, assets are identified by scanning their asset tag, serial number, or model barcode. Next, the records in the ServiceNow instance are checked to determine whether they match the scanned assets and the audit result is generated. You can view precise inventory information through detailed lists and reports.

You can create an audit record in the Hardware Asset Management application or the ServiceNow Agent app.

-   Use the Hardware Asset Management application to create a scheduled audit record. For more information about creating a scheduled audit record, see [Create an audit record in the Hardware Asset Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/audit-your-inventory.md).
-   Use the ServiceNow Agent app to create a blind or unscheduled audit record. For more information about creating a blind or unscheduled audit record, see [Create an audit record using the ServiceNow Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-audit-using-mobile-app.md).

When an inventory audit record is created, it’s saved in the Asset Audits table, depending on the configuration for **sn\_hamp.migrate\_hamaudit** system property.

-   When the **sn\_hamp.migrate\_hamaudit** system property is set to **true**, the audit record is saved in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table.
-   When the **sn\_hamp.migrate\_hamaudit** system property is set to **false**, the audit record is saved in the Asset Audits \[sn\_hamp\_asset\_audit\] table.

**Note:** Starting with Hardware Asset Management version 15.0.0, the audit inventory has been enhanced to store audit records in the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table. Before enabling audit enhancements and switching to the common Asset Audits table, you must complete all audit records that are in either **In progress** or **New** status.

Using the ServiceNow Agent app, you can scan the assets in the inventory and complete the audit process. The Hardware Asset Management application reconciles scanned assets with ServiceNow records to generate audit results. For more information about scanning assets, see [Complete a single scan inventory audit using the ServiceNow Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/scan-assets-agent-app.md).

-   **[Create an audit record in the Hardware Asset Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/audit-your-inventory.md)**  
Create an audit record to audit your inventory to determine the accuracy of your hardware and consumable assets and to optimize the inventory.
-   **[Create an audit record using the ServiceNow Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-audit-using-mobile-app.md)**  
Create an inventory audit record using the ServiceNow Agent app.
-   **[Complete a single scan inventory audit using the ServiceNow Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/scan-assets-agent-app.md)**  
Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.
-   **[Complete multi scan inventory audit using the ServiceNow Agent app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/complete-multi-scan-inventory-audit-using-mobile-app.md)**  
Scan your inventory assets by using the ServiceNow Agent app for the multi scan audit records.
-   **[Close an asset remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/close-an-asset-remediation-task.md)**  
View the open asset remediation from the **Inventory** view and close the task after updating the **Model category** and **Model** fields value for the asset.
-   **[Create an asset from the inventory audit screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/inventory-audit-create-asset.md)**  
Create an asset record for the scanned asset that doesn't exist in your ServiceNow instance and that is detected when auditing inventory.
-   **[View audit results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/view-audit-results.md)**  
View the audit results after you audit your inventory. The Audit Results section is activated and shows the details of the audit result.
-   **[View deprecated audit records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/view-deprecated-audit-records.md)**  
View the deprecated asset audit records that are created before switching to the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table and stored in the Asset Audits \[sn\_hamp\_asset\_audit\] table.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()


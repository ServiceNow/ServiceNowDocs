---
title: Update associated Decision tables for HAM flows
description: Update associated Decision tables for Hardware Asset Management \(HAM\) flows to trigger a new or customized HAM flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/trigger-flow-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Update associated Decision tables for HAM flows

Update associated Decision tables for Hardware Asset Management \(HAM\) flows to trigger a new or customized HAM flow.

## Before you begin

Role required: admin, decision\_table\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Open a decision table that you want to update.

3.  On the flow page, select the Add icon \(\[Omitted image "add\_content\_icon.png"\] Alt text: Add icon\) in the Decision table section.

4.  Select **Add condition column**.

5.  In the NEW CONDITION COLUMN dialog box, fill in the conditions according to the conditions that you want to trigger the flow.

6.  Select **Done**.

    A new row is created and the condition shows up in the Decision table section.

7.  In the Flow column, select the flow that you have created.

8.  Select **Save**.

9.  Navigate to the Decisions \(sys\_decision\_question\) table and search the updated Decision table that you updated.

10. Update the **Order** field with a value less than 100.


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

[Audit hardware asset inventory]()

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


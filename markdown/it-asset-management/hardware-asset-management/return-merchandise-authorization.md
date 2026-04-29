---
title: Return Merchandise Authorization
description: Return Merchandise Authorization \(RMA\) is an agreement between a buyer and seller that lets the buyer return or replace a faulty product. The Asset RMA Order catalog item has prescriptive flows to streamline the RMA process.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Return Merchandise Authorization

Return Merchandise Authorization \(RMA\) is an agreement between a buyer and seller that lets the buyer return or replace a faulty product. The Asset RMA Order catalog item has prescriptive flows to streamline the RMA process.

An RMA request has RMA request lines. When an RMA request is submitted, an RMA request line is created for each asset and consumable that was selected. You can view a list of all the open RMA request lines in the Hardware Asset Dashboard. For details, see [Hardware Asset dashboard](../../../use/dashboards/application-content-packs/hardware-asset-content-pack.md#).

## Workflow for Return Merchandise Authorization

The Flow Designer application creates RMA tasks for every RMA request line. The RMA request is completed through the RMA tasks. An Assessment task is created for each RMA request line. The Assessment task is used to assess the faulty asset. When the state of an RMA task is updated, the **Stage** field on the RMA request line form is updated by default.

When you receive a defective product or if a product becomes defective within its warranty period, you can request an Asset RMA Order. Based on your agreement with the vendor, you can decide to repair the faulty asset either on-site or off-site. On the Assessment task form, when you select off-site repair, the flow designer triggers the Asset RMA Off-site flow. The Asset RMA Off-site flow generates the following RMA tasks to complete the RMA process.

-   Shipment
-   Vendor RMA decision
-   Receive

On the Assessment task from, when you select on-site repair, the flow designer triggers the Asset RMA On-site flow. The Asset RMA On-site flow generates the RMA task \(On-site repair task\) to complete the RMA process.

After attempting an on-site repair, if the faulty asset couldn't be repaired, then you can send the product for an off-site repair. If you want to send the faulty product for an off-site repair, then the Asset RMA Off-site flow is triggered and the RMA process is completed through the Asset RMA Off-site Flow RMA tasks.

You can cancel an RMA request as long none of the assessment tasks are closed for any of the RMA request lines. After an RMA request is canceled, all the associated RMA request lines and RMA tasks are canceled. If you submit RMA for an asset that is part of an existing RMA, the RMA request lines of the existing RMA request are automatically canceled. If an RMA task is canceled, the associated RMA request line is also canceled. If you have the inventory user or itil role, you can cancel an Assessment task, Internal repair task, or a Shipping task.

**Related topics**  


[Manage RMA requests](manage-rma-req.md)


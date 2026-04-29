---
title: Asset operations view
description: Use the Asset operations view in the Hardware Asset Workspace to view the asset operations-related functions such as stock rules, stock orders, procurement sourcing requests, all contract renewal requests, contract renewal line items, custom products, custom models, and take appropriate actions.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset operations view

Use the Asset operations view in the Hardware Asset Workspace to view the asset operations-related functions such as stock rules, stock orders, procurement sourcing requests, all contract renewal requests, contract renewal line items, custom products, custom models, and take appropriate actions.

The Asset operations view includes the following list:

-   Inventory
    -   Stockroom types: View types of stockrooms. For more information, see [Create a new stockroom type](../../asset-management/task/t_CreateANewStockroomType.md).
    -   Stock rules: View stock rules associated with the stockroom. For more details, see [Create a stock rule](../../asset-management/task/t_CreateAStockRule.md).
    -   Stock orders: View stock orders associated with the inventory.
-   Shipment
    -   Shipments: View and track the shipments from different sources or flows. For more information, see [View hardware asset shipment details](../task/view-hardware-asset-shipments.md).
    -   Shipment assets: View the list of assets included in the shipments. For more information, see [View hardware asset shipment details](../task/view-hardware-asset-shipments.md).
    -   Shipping carriers: Create and view the list of shipping carriers. For more information, see [Create a shipping carrier record](../task/create-shipping-carrier.md).
    -   Carrier integration profiles: View the list of carrier integration profiles associated with the shipping carriers. For more information, see [View the carrier integration profile details](../task/view-integration-profiles.md).
-   Procurement-Requests: View and track procurement requests. For more information, see [Sourcing items in a service catalog request](../../procurement/concept/c_SourcingRequestItems.md).
-   Hardware asset normalization
    -   Custom products: View details of custom products that aren't represented in the Asset Management Content Service. For more information, see [Add a custom product](../task/add-custom-hardware-model.md).
    -   Custom models: View details of custom models. For more information, see [Create a hardware or consumable model](../task/create-hardware-consumable-model.md).
    -   Calculated lifecyle templates: View and create life cycle templates and formulas that can be applied on hardware and consumable models. For more information, see [Manage the lifecycle of hardware models with calculated lifecycle templates](manage-ham-lifecycle-temp.md).
-   Contract Renewal

    -   All contract renewal requests: View details of all contract renewal requests.
    -   Contract renewal line items: View details of all line items associated with contract renewal requests.
    For more information, see [Contract renewal workflow](../../contract-management/concept/cont-renew-wf.md).

-   KPI configuration
    -   KPI opt in: Enable the asset performance tracking by opting in to the model categories of the assets. For details, see [Opt in to model categories to track performance KPIs for hardware assets](../task/opt-in-kpi-tracking-ham.md).
    -   Operational schedules: Create and view operational schedules for hardware assets. For details, see [Create an operational schedule for hardware assets](../task/create-operational-schedule-ham.md)
    -   Asset schedules: Link hardware assets to their respective operational schedules and align KPI records accordingly. For details, see [Map hardware assets to an operational schedule](../task/create-asset-schedule-ham.md)
-   TCO configuration
    -   Task rate card: Define the type of task and the method of calculating the associated costs, and view the details of the created task rate cards. For more information, see [Create a task rate card in Hardware Asset Workspace](../task/create-ham-task-rate-card.md).
    -   Labor rate card: Record the time worked on a task and associate a rate to the task, and view the details of the created labor rate cards. For more information, see [Create a labor rate card in Hardware Asset Workspace](../task/create-ham-labor-task.md).
-   Zero touch
    -   Asset requests: View the list of hardware asset requests of your employees submitted through the Zero Touch request flow. For more information, see [Manage hardware asset requests using the Zero Touch request flow](managing-standard-hw-req-ztr.md).
    -   Provider integration profiles: Create a provider integration profile to transform the Scratchpad updates from your provider into a format required for the Zero Touch request flow. For more information, see [Create a provider integration profile](../task/create-int-profile-ztr-ham.md).
-   Zero touch refresh
    -   Requests: View the list of Zero Touch Refresh requests of your employees. For more information, see [Process a Zero Touch Refresh request](../task/process-zero-touch-asset-request.md).
    -   Refresh models: Create and view the list of refresh models with the configured replacement models. For more information, see [Configure replacement models for a refresh model](../task/create-replacement-model.md).
-   Attestation
    -   Attestations: View the list of asset attestation requests. For more information, see [Create an asset attestation in the Inventory view](../task/create-attestation-req-ham.md).
    -   Schedules: View the list of attestation schedules that create recurring attestation requests. For more information, see [Cancel an attestation schedule](../task/cancel-attestation-schedule-ham.md).
-   Hardware asset success
    -   Success goals: Create success goals and view the list of created success goals for Hardware Asset Management. For more information, see [Create a success goal for Hardware Asset Management](../task/create-suc-goal.md).
    -   Success activities: Create success activities and view the list of created success activities for Hardware Asset Management. For more information, see [Create success activities for HAM success goals](../task/create-suc-act-hw.md).
    -   Success categories: Create a category for a success goal and view the list of categories. For more information, see [Create a success goal category for hardware assets](../task/create-ham-suc-cat.md).
    -   Hardware maturity: View items that help you drive the success of your hardware assets. For more information, see [View all maturity items for Hardware Asset Management](../task/view-ham-maturity-items.md).
-   Asset audits: View deprecated audit records created in the Asset Audits \[sn\_hamp\_asset\_audit\] table before upgrading to the audit enhancements introduced in Hardware Asset Management version 15.0.0. For more information, see [View deprecated audit records](../task/view-deprecated-audit-records.md).

    **Important:**

    If you have enabled the audit enhancements and switched to the common audit table, new asset audit records are now stored in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table. After the switch, you can't view deprecated audit records \(created before switching to common table and stored in the Asset Audits \[sn\_hamp\_asset\_audit\] table\) in the **Asset audits** tab from the Inventory view.

    You can view the deprecated audit records from the Asset Operations view, when the **migrate\_hamaudit** system property to **true**.

-   Asset warranty: View the warranty details of Lenovo hardware assets. For more information, see [Track the warranty details of your Lenovo assets](../task/view-asset-warranty-details.md).

You can also create and easily access your custom list views from the **My Lists** tab.

![Asset operation view in the Hardware Asset Workspace.](../image/asset-operations-view.png "Asset operations")

**Related topics**  


[Inventory view](inventory-view.md)

[Request items source](https://www.servicenow.com/docs/access?context=c_SourcingRequestItems&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Work with hardware normalization](Work-with-hardware-normalization.md)


---
title: Enterprise Asset Management release notes
description: The ServiceNow Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Enterprise Asset Management release notes

The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Yokohama release.

## Enterprise Asset Management highlights for the Yokohama release

-   Streamline firmware management with the new Firmware model class.
-   Get normalization coverage for firmware that is embedded into your industrial and IT hardware-based Operational Technology \(OT\) assets.
-   Achieve synchronization between physical assets and configuration items \(CIs\) for Operational Technology \(OT\) assets through MAC addresses.
-   Streamline OT Asset Management \(OTAM\) licensing to include hardware resource categories for OT hardware assets to access OT Asset Management features and workflows.
-   Get support for hardware models and OT hardware assets in the OT Asset Management workspace.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

**Important:** Enterprise Asset Management, Enterprise Asset Management for Healthcare, Operational Technology \(OT\) Asset Management, and Expanded Model and Asset Classes are available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Gain normalization coverage for firmware in your Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=normalizing-firmware-ot-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Achieve enhanced normalization across your OT deployments by normalizing the firmware that is embedded into your OT assets. Use the normalized data to track and manage the life cycles of your firmware separately from your OT assets so that you can directly detect and mitigate firmware vulnerabilities. You can view the firmware model details in the OT model management view of the OT Asset Workspace.

    **Note:** Firmware normalization is applicable only to OT Asset Management.

-   **[Manage hardware models and assets in the Operational Technology \(OT\) Asset Management application](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Enable your OT managers to create hardware models and assets in the OT Workspace. You can integrate hardware models and OT assets into such Enterprise Asset Management flows as asset request, asset refresh, stock order, multi-asset onboarding, Return Merchandise Authorization \(RMA\), repair, and disposal. You can also generate maintenance plans and work orders for your OT hardware assets.

-   **[Synchronize asset and CIs for Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=asset-ci-sync-ot-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Synchronize the MAC addresses between the asset and network adapter CI for OT assets.

-   **[License your OT hardware assets using the new resource categories available in OTAM licensing](https://www.servicenow.com/docs/access?context=licensing-ot-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Access OT Asset Management features and workflows for OT hardware assets through the following hardware resource categories:

    -   OT Servers
    -   OT Network Gear
    -   OT Storage
    -   OT End User Computers
    -   OT Mobile Devices
    -   OT Monitors
    -   OT Printers
    -   OT Unclassified Hardware
    The hardware resource categories are opted in by default. The OT hardware assets are counted only under OTAM licensing. They are excluded from the HAM licensing that is based on the OT entity flag.

    **Note:** The OTAM licensing changes apply only to OT Asset Management.

-   **[Manage mission-critical enterprise assets and linear assets for telecommunications networks](https://www.servicenow.com/docs/access?context=eam-dcnam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application to track and manage mission-critical facility-based enterprise assets and linear assets for telecommunications networks. Get a comprehensive view of these assets throughout their life cycles so that you can help optimize their performance and improve their longevity.

-   **[Fulfill Return Merchandise Authorization \(RMA\) requests as a Device as a Service \(DaaS\) provider, vendor, or manufacturer](https://www.servicenow.com/docs/access?context=eam-providers&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use the Enterprise Asset Management for Providers application to fulfill the RMA requests that you receive from customers as a DaaS provider, vendor, or manufacturer. The application adds support for RMA response orders, which enable you to track and manage the process of repairing or replacing defective assets for your RMA requests. The application also adds support for inbound asset orders, which enable you to track and manage the process of providing assets for your RMA requests. By managing these orders from a consolidated location, you can streamline your operations and improve efficiency.


## UI changes

-   **[MAC address field on the asset form](https://www.servicenow.com/docs/access?context=asset-fields-eam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The asset form shows the **MAC address** field for the following asset classes:

    -   Construction
    -   Facility
    -   Industrial
    -   Medical
    -   Retail
    -   Tactical equipment
    -   Transportation
    -   Wearable
    -   Hardware
    **Note:** The **MAC address** field is shown on the asset form in Enterprise Asset Workspace and OT Asset Workspace.

-   **[Child assets activity and MAC address field in the asset onboarding playbook](https://www.servicenow.com/docs/access?context=create-asset-onboarding-task-eam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The child assets activity was added to the asset onboarding playbook for preassembled industrial assets. The Asset details activity in the playbook shows the **MAC address** field.

    **Note:** These UI changes apply to Enterprise Asset Workspace and OT Asset Workspace.

-   **[MAC address field in multi-asset onboarding](https://www.servicenow.com/docs/access?context=asset-onboarding-eam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The **MAC address** field was added to the Add assets dialog box in multi-asset onboarding through catalog requests and onboarding orders. The Asset details activity in the Multi-asset onboarding playbook shows the MAC address that you provided.

    **Note:** This UI change applies to Enterprise Asset Workspace and OT Asset Workspace.

-   **[MAC address field in an Advanced Shipment Notification](https://www.servicenow.com/docs/access?context=asn-eam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The **MAC address** field was added to the Download template for an Advanced Shipment Notification. After a successful import, the MAC address that you provided in the template is added to the Asset \[alm\_asset\] table. The **MAC address** field is also shown on the asset form for all assets except consumables and pallets.

    **Note:** This UI change applies to Enterprise Asset Workspace and OT Asset Workspace.

-   **[MAC address field in Bulk import](https://www.servicenow.com/docs/access?context=overview-bulk-import-eam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The **MAC address** field was added to the Download template for the following Bulk import modes:

    -   Create assets
    -   Update assets
    -   Create models and assets
    After a successful import, the MAC address that you provided in the template is added to the Asset \[alm\_asset\] table. The **MAC address** field is also shown on the asset form for all assets except consumables and pallets.

    **Note:** This UI change applies to Enterprise Asset Workspace and OT Asset Workspace.

-   **[MAC address field in Receive Purchase Order](https://www.servicenow.com/docs/access?context=t_ReceiveAnAsset&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The Capture asset tags dialog box in the Receive Purchase Order shows the **MAC address** field in addition to the Serial number and Asset tag.

    **Note:** This UI change applies to Enterprise Asset Workspace and OT Asset Workspace.

-   **[OT entity flag](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The asset form shows that the OT entity flag set to true for hardware and industrial assets that were created in the OT Asset Workspace.


## Changed in this release

-   **[Refresh flow in OT workspace](https://www.servicenow.com/docs/access?context=request-eam-assetrefresh&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    For single and multi-model refresh orders, the OT manager can edit the replacement model even after the refresh order has been created in the OTAM workspace. Additionally, the sourcing location is also editable.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The configurable Enterprise Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


## Activation information

Install the following applications by requesting them from ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for details.


## Related ServiceNow applications and features

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    The ServiceNow® Field Service Management application enables your organization to manage location-based work more efficiently and safely.

-   **[Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Procurement application helps you create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)


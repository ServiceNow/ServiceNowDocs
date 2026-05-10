---
title: Hardware Asset Management release notes
description: The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Hardware Asset Management release notes

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Australia release.

## Hardware Asset Management highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)- Gain real-time visibility into critical asset data through generative AI-driven asset analysis summaries.

Australia Patch 0

-   Gain insight into the approximated life-cycle dates for hardware and consumable products.
-   Streamline inventory asset management with the expanded and efficient inventory auditing process.
-   Streamline and improve the asset management process for retired assets with the expanded asset disposal workflow.
-   Streamlined Advanced Shipment \(ASN\) import process with support for users with specific functional roles.
-   Save time and effort by copying a model from the Content lookup portal to create a record in your ServiceNow instance.

See [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-landing-page.md) for more information.

**Important:** Hardware Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Hardware Asset Management to Australia

-   To enhance security and manage admin access precisely, the granular admin roles are now installed. These roles replace broad admin checks by assigning specific privileges based on user tasks, rather than granting full admin access:
    -   sn\_hamp.ham\_system\_admin: Provides access to HAM licensing, HAM Guided Setup, HAM application properties and system properties, and a few tables.
    -   sn\_hamp.ham\_asn\_admin: Provides access to the Advanced Shipment Notification \(ASN\) feature.
    -   asset\_integration\_admin: Provides access to Standard hardware Zero touch request and carrier integration features, and shipment tables.
    -   asset\_system\_admin: Provides access to asset job log, content audit, transfer order, expense management, and model management.
    -   asset\_task\_admin: Provides access to asset tasks.
    -   procurement\_system\_admin: Provides access to procurement module, tables, and tasks.
    -   contract\_system\_admin: Provides access to contract module, tables, and tasks.
    -   asset\_licensing\_admin: Provides access to the ITAM licensing module.
    -   asset\_recommendation\_admin: Provides access to recommendation actions.
-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/read-only-option.md).

## New in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Manage your assets with comprehensive and real-time data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-hardware-asset-management/generate-asset-analysis-now-assist-ham.md)**

    View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


-   **[Gain visibility into approximated life cycle dates for hardware and consumable model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/approximated-lifecycles-hardware-products.md)**

    Enhance the operational efficiency by gaining visibility into the estimated and approximate life- cycle dates for models when manufacturers haven’t explicitly published key dates, such as End of Life \(EoL\) and End of Service \(EoS\). This insight enables you to manage your asset portfolio strategically, reducing unexpected downtime and improve budgeting.

-   **[Enhanced and unified hardware asset inventory auditing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-inventory-audit.md)**

    Streamline and improve your inventory auditing experience with the enhanced and unified hardware asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and verify that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.
-   **[Enhanced asset disposal workflow to streamline the management of retired assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-resale-order.md)**

    Resell the retired assets that are no longer in use to reduce waste and receive credit. The extended asset disposal flow in the Documentation stage enables you to resell planned assets instead of disposing of them, enabling you to receive credit.

-   **[Enable your key functional roles or personas to directly manage Advanced Shipment Notification \(ASN\) imports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/advanced-shipment-notification.md)**

    Upload ASN files and trigger the import process from the Procurement view within the Hardware Asset Workspace without requiring admin privileges. Users with the ham\_admin, ham\_user, procurement\_admin, or asset role can now initiate the ASN workflow themselves, creating asset records seamlessly.

-   **[Streamline model creation by copying a model directly from the Content lookup portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/copy-hardware-model.md)**

    Reduce manual effort by copying a model from the Content lookup portal to create a record in the Product Model \[cmdb\_model\] table. The copied model is automatically normalized, where applicable, and relevant fields are pre-populated with information from the content record.


## UI changes

-   **[Unified audit record storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-inventory-audit.md)**

    Starting with Hardware Asset Management version 15.0.0, the audit inventory has been enhanced to store audit records in the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table. If you have enabled the audit enhancements and switched to the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table, the following user interface changes have been made:

    -   The asset audit records are stored in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table. After switching to the common audit table, deprecated audit records \(created before the switch\) are no longer visible in the **Asset audits** tab from the Inventory view. These records can be accessed from the Asset Operations view, when the **migrate\_hamaudit**system property is set to **true**.
    -   The Asset Audits \[sn\_itam\_common\_asset\_audit\] table can’t be accessed by navigating to **All** &gt; **Asset Audits** &gt; **Asset Audits**. You can access the legacy Asset Audits \[sn\_hamp\_asset\_audit\] table instead.
    -   If your ServiceNow® instance is licensed for both Hardware Asset Management and Enterprise Asset Management, the **Stockroom Details** tab displays a single Asset Audits tile. This unified Asset Audits tile shows the open audit records for both hardware and enterprise inventory, instead of displaying separate tiles for Hardware Asset Audits and Enterprise Asset Audits.

        **Note:** Note: If your ServiceNow instance isn't licensed for Enterprise Asset Management, the Hardware Asset Audits tile shows the number of open asset audit records for the hardware inventory audit.


## Activation information

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SoftwareAssetMgmt.md)**

    The ServiceNow® Software Asset Management application enables you to track, evaluate, and manage the software licenses, software compliance, and software optimization. You can reclaim unused software rights, purchase new software rights, and manage allocations for entitlements.

-   **[Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-asset-management.md)**

    The ServiceNow® Enterprise Asset Management application enables you to manage the entire life cycle of your connected and non-connected enterprise assets. It provides a comprehensive end-to-end solution for maintaining enterprise assets, minimizing costly downtime, and maximizing enterprise asset usability.

-   **[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/c_ContractManagement.md)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/c_Procurement.md)**

    The ServiceNow® Procurement application enables you to create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)


---
title: Combined Enterprise Asset Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Enterprise Asset Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-enterpriseassetmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Enterprise Asset Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Enterprise Asset Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Asset Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.

-   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(\[Omitted image "image.asset-putaway-icon-ma"\] Alt text: Asset put away icon\) is included in the navigation bar
-   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Enterprise Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Gain normalization coverage for firmware in your Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=normalizing-firmware-ot-assets&family=yokohama&ft:locale=en-US)**

Achieve enhanced normalization across your OT deployments by normalizing the firmware that is embedded into your OT assets. Use the normalized data to track and manage the life cycles of your firmware separately from your OT assets so that you can directly detect and mitigate firmware vulnerabilities. You can view the firmware model details in the OT model management view of the OT Asset Workspace.

**Note:** Firmware normalization is applicable only to OT Asset Management.

-   **[Manage hardware models and assets in the Operational Technology \(OT\) Asset Management application](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&family=yokohama&ft:locale=en-US)**

Enable your OT managers to create hardware models and assets in the OT Workspace. You can integrate hardware models and OT assets into such Enterprise Asset Management flows as asset request, asset refresh, stock order, multi-asset onboarding, Return Merchandise Authorization \(RMA\), repair, and disposal. You can also generate maintenance plans and work orders for your OT hardware assets.

-   **[Synchronize asset and CIs for Operational Technology \(OT\) assets](https://www.servicenow.com/docs/access?context=asset-ci-sync-ot-assets&family=yokohama&ft:locale=en-US)**

Synchronize the MAC addresses between the asset and network adapter CI for OT assets.

-   **[License your OT hardware assets using the new resource categories available in OTAM licensing](https://www.servicenow.com/docs/access?context=licensing-ot-asset-management&family=yokohama&ft:locale=en-US)**

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

-   **[Manage mission-critical enterprise assets and linear assets for telecommunications networks](https://www.servicenow.com/docs/access?context=eam-dcnam&family=yokohama&ft:locale=en-US)**

Use the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application to track and manage mission-critical facility-based enterprise assets and linear assets for telecommunications networks. Get a comprehensive view of these assets throughout their life cycles so that you can help optimize their performance and improve their longevity.

-   **[Fulfill Return Merchandise Authorization \(RMA\) requests as a Device as a Service \(DaaS\) provider, vendor, or manufacturer](https://www.servicenow.com/docs/access?context=eam-providers&family=yokohama&ft:locale=en-US)**

Use the Enterprise Asset Management for Providers application to fulfill the RMA requests that you receive from customers as a DaaS provider, vendor, or manufacturer. The application adds support for RMA response orders, which enable you to track and manage the process of repairing or replacing defective assets for your RMA requests. The application also adds support for inbound asset orders, which enable you to track and manage the process of providing assets for your RMA requests. By managing these orders from a consolidated location, you can streamline your operations and improve efficiency.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Organize your assets into hierarchical asset groups to manage your complex asset ecosystems](https://www.servicenow.com/docs/access?context=asset-groups-eam&family=zurich&ft:locale=en-US)**

Organize assets into logical groups and subgroups to represent their dependencies and operational relationships. Use a dependency map to visualize the entire structure of the asset hierarchy, making it easy to see all the subgroups and assets within each asset group.

-   **[Inspect the condition of enterprise assets to determine their health and ensure reliability](https://www.servicenow.com/docs/access?context=asset-conditions-eam&family=zurich&ft:locale=en-US)**

Define condition attributes for enterprise models and assets and associate these attributes with templates to identify any potential issues throughout the asset life cycle. Enable scoring in the templates to calculate asset condition scores to determine whether an asset passes or fails the evaluation. Schedule asset condition evaluations via maintenance plans or work orders. View comprehensive reports on the asset condition outcomes on dashboards across your organization.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=eam-asset-dboard&family=zurich&ft:locale=en-US)**

Track the past performance of assets and get notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification. This tracking helps improve asset availability according to ISO standards.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-reports&family=zurich&ft:locale=en-US)**

Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Enterprise Asset Workspace. These reports help you:

    -   Find replacement options or spare part availability for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Achieve faster diagnostics and enhanced maintenance efficiency with standardized failure and resolution codes](https://www.servicenow.com/docs/access?context=failure-resolution-codes-eam&family=zurich&ft:locale=en-US)**

Enable technicians to record predefined failure reasons and resolution steps with configurable codes. You can create, update, and import these codes through spreadsheets in the Admin center of the Enterprise Asset Workspace. In the Repair flow, these codes help technicians record the reason for the specific issue with the asset and the appropriate solution for repairing it.

-   **[Manage OT hardware models and assets in the OT Asset Workspace](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&family=zurich&ft:locale=en-US)**

Enable OT asset managers to view and fulfill requests for OT hardware assets in the OT Asset Workspace. The reports and dashboards in the OT Asset workspace include OT hardware models, assets, and requests. The following OT Asset Management workflows and features now provide support for OT hardware assets and models, in addition to the workflows and features that continue to support them from the Yokohama release:

    -   Bulk import
    -   Asset reclamation
    -   Advanced Shipment Notification \(ASN\)
    -   Asset audits
    -   Total Cost of Ownership \(TCO\)
    -   Lease contract
    -   Risk
    -   Resale
    -   Loaner
    -   Move
    -   Recall
    -   Stock rule
-   **[Remediate unsuccessful enterprise asset calibrations](https://www.servicenow.com/docs/access?context=remediate-unsuccessful-enterprise-asset-calibration&family=zurich&ft:locale=en-US)**

Remediate failed calibration events by initiating new work orders and corresponding work order tasks for those events. When you select the option to remediate a failed calibration event, you can choose an appropriate work order template to generate a new work order with at least one work order task. The work order and work order task are auto-populated with the asset that you want to calibrate, the location of that asset, the original work order, and all mandatory fields. In addition, the original and new calibration events and their corresponding tasks are linked together through the **Parent** field for full traceability.

-   **[Measure calibration tolerance conformance by using additional value types](https://www.servicenow.com/docs/access?context=add-calibration-attributes-enterprise-model&family=zurich&ft:locale=en-US)**

Use the following additional value types to compare your calibration measurements against the corresponding tolerances that you define:

    -   Range
    -   Less than
    -   Greater than
In addition, use the True/False value type to assess the qualitative elements of your calibrations.

-   **[Manage unique identifiers for enterprise assets using CI identification rules](https://www.servicenow.com/docs/access?context=create-asset-eam&family=zurich&ft:locale=en-US)**

Define required and unique fields on asset records by creating identification rules on associated CI classes in the Identification and Reconciliation engine \(IRE\). When you create an asset whose model category is linked to a CI class with an identification rule, you should provide details for at least one of the fields, such as Asset tag, Serial number, and MAC address, that uniquely identify the asset.

-   **[Drop off and receive assets at a stockroom by using the ServiceNow Mobile Agent application](https://www.servicenow.com/docs/access?context=manage-dropoff-mobile-agent&family=zurich&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task using the ServiceNow® Mobile Agent application. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received assets and closes the Drop off task using the Mobile Agent application.

**Note:** Starting with the Xanadu release, you could create Drop off and Receive tasks in the Enterprise Asset Workspace. However, now you can also use the Mobile Agent application for the same purpose.

-   **[Receive shipment assets at a stockroom through the streamlined and unified receiving process](https://www.servicenow.com/docs/access?context=stockroom-receiving-eam&family=zurich&ft:locale=en-US)**

Receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the following workspaces:

    -   Enterprise Asset Workspace
    -   OT Asset Workspace
    -   Medical Asset Workspace
    -   Facility Asset Workspace
This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset-eam&family=zurich&ft:locale=en-US)**

Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Enterprise Asset Workspace or ServiceNow Agent application.


</td></tr><tr><td>

Australia

</td><td>

-   **[Automate enterprise asset sourcing by using an agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-eam-help-manage-enterprise-asset-requests-workflow&family=australia&ft:locale=en-US)**

Use the help manage enterprise asset requests agentic workflow to automate the process of sourcing assets for your enterprise asset requests. The workflow uses AI agents to fulfill these requests by allocating assets from local stockrooms, creating transfer orders to move assets between stockrooms, or generating purchase orders for the requested assets.

-   **[Automatically generate instructions for enterprise asset repairs by using an agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-eam-help-repair-enterprise-assets-workflow&family=australia&ft:locale=en-US)**

Use the help repair enterprise assets agentic workflow, which is driven by AI agents, to automatically generate step-by-step troubleshooting, diagnostics, and repair instructions for your enterprise asset repairs in real time.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Define, schedule, and track complex asset-centric work tasks through work order plans](https://www.servicenow.com/docs/access?context=manage-work-order-plans&family=australia&ft:locale=en-US)**

Manage complex asset-centric work tasks with unified work order plans that can be applied across assets, asset groups, or locations. The work order plans offer the following benefits:

    -   Save work order plans as reusable templates for use across assets.
    -   Organize sequential operations—shutdowns, safety inspections, calibrations, asset conditions, and restarts—using the structured playbook.
    -   Assign, schedule, and track work order tasks for technicians within the playbook.
    -   Enable technicians to receive assigned work order tasks and update task status through the ServiceNow Mobile Agent application.
-   **[Manage multimedia production equipment models and assets](https://www.servicenow.com/docs/access?context=create-model-eam&family=australia&ft:locale=en-US)**

Create, track, and manage multimedia production equipment models and assets in the Enterprise Asset Workspace. Get a comprehensive view of these models and assets so that you can manage them effectively throughout their life cycles.

-   **[Replace broad admin checks with granular admin roles and ACL updates](https://www.servicenow.com/docs/access?context=eam-roles&family=australia&ft:locale=en-US)**

Manage admin access precisely with granular admin roles. Instead of giving full admin privileges to the users, you can assign specific roles based on the tasks they perform.

-   **[Enhanced and unified enterprise asset inventory auditing experience](https://www.servicenow.com/docs/access?context=audit-eam-assetinventory&family=australia&ft:locale=en-US)**

Streamline and improve your inventory auditing experience with the enhanced and unified enterprise asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and ensure that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Enterprise Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Refresh flow in OT workspace](https://www.servicenow.com/docs/access?context=request-eam-assetrefresh&family=yokohama&ft:locale=en-US)**

For single and multi-model refresh orders, the OT manager can edit the replacement model even after the refresh order has been created in the OTAM workspace. Additionally, the sourcing location is also editable.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The configurable Enterprise Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enterprise Asset Management demo data migration](https://www.servicenow.com/docs/access?context=install-eam-demo-data&family=zurich&ft:locale=en-US)**

All Enterprise Asset Management demo data has migrated from the Enterprise Asset Management application to either the EAM Demo Data application or Indoor Mapping for Assets application. The EAM Demo Data application contains all Enterprise Asset Management demo data except for indoor mapping-related demo data, which is now included in the Indoor Mapping for Assets application.

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&family=zurich&ft:locale=en-US)**

Starting from the Enterprise Asset Management version 9.1.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&family=zurich&ft:locale=en-US)**

Starting from Enterprise Asset Management version 9.1.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Australia

</td><td>

-   **[Multiple assets and asset groups in a work order](https://www.servicenow.com/docs/access?context=create-eam-work-order-task&family=australia&ft:locale=en-US)**

A work order and work order task can now be created for asset groups in addition to individual assets. Additionally, the sn\_eam.enterprise\_asset\_manager role can add more assets to tasks while they're in the draft stage. When technicians start the task, they can take action on all included assets. The Deploy Asset, Swap Asset, and Remove Asset actions within work order tasks support multiple assets and asset groups.

-   **[Shutdown and Startup work types](https://www.servicenow.com/docs/access?context=create-eam-work-order-task&family=australia&ft:locale=en-US)**

The **Shutdown** and **Startup** work types available in the work order tasks enable you to manage asset shutdown and restart tasks.

-   **[Multiple calibration playbooks](https://www.servicenow.com/docs/access?context=complete-eam-work-order&family=australia&ft:locale=en-US)**

When a calibration work order is created for multiple assets or an asset group, the system generates a separate calibration playbook for each asset in the Affected assets list.

-   **[Multiple condition lines](https://www.servicenow.com/docs/access?context=perform-condition-assessment-webui&family=australia&ft:locale=en-US)**

When an asset condition work order is created for multiple assets or an asset group, the system generates a separate condition line for each asset in the Affected assets list. All condition lines must be evaluated before the work order can be completed.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Enterprise Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Enterprise Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The Classification \(classification\) column in the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(Deprecated\). The data from this column is available in the new Classification \(classification\_code\) column in the Product model \[cmdb\_model\] table.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Enterprise Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install the following applications by requesting them from ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes



</td></tr><tr><td>

Australia

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   Enterprise Asset Management for Facilities
-   OT Asset Management
-   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)
-   Enterprise Asset Management for Providers
-   Expanded Model and Asset Classes



</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Enterprise Asset Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Streamline firmware management with the new Firmware model class.
-   Get normalization coverage for firmware that is embedded into your industrial and IT hardware-based Operational Technology \(OT\) assets.
-   Achieve synchronization between physical assets and configuration items \(CIs\) for Operational Technology \(OT\) assets through MAC addresses.
-   Streamline OT Asset Management \(OTAM\) licensing to include hardware resource categories for OT hardware assets to access OT Asset Management features and workflows.
-   Get support for hardware models and OT hardware assets in the OT Asset Management workspace.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Organize related assets into hierarchical asset groups and subgroups to enable consolidated reporting, streamline maintenance workflows, and provide clear dependency mapping.
-   Create scalable templates to evaluate the condition of enterprise assets, which helps to detect issues early, optimize maintenance planning, and maximize asset lifespan.
-   Achieve operational efficiency by evaluating how effectively your assets are functioning and being used, through reports based on asset key performance indicators in the Asset analytics view.
-   Manage supply and demand originating from service locations or other stockrooms through local stock or distribution channels using the Inventory insights tab in the stockroom record. You can also compare multiple stockrooms at the same time.
-   Gain insights into asset failure reasons and resolution actions using the failure and resolution codes in the Enterprise Asset Workspace.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Streamline the enterprise asset request process by using the help manage enterprise asset requests agentic workflow.
-   Automatically generate troubleshooting, diagnostics, and repair instructions for your enterprise asset repairs by using the help repair enterprise assets agentic workflow.

 Early Availability

-   Streamline complex maintenance activities across assets, asset groups, or locations with unified work order plans.
-   Streamline inventory asset management with the expanded and efficient inventory auditing process.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


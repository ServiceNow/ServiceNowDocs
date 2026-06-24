---
title: Combined Enterprise Asset Management release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Enterprise Asset Management from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-enterpriseassetmanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Enterprise Asset Management release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Enterprise Asset Management from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Asset Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

After you upgrade to Washington DC, the model\_component field isn't available in the Enterprise asset \[sn\_ent\_asset\] table. Instead, a new model\_component\_id field is available in the Asset \[alm\_asset\] table. The ENT - Migrate to new model component script moves the existing model\_component field data to the model\_component\_id field.

 Note the following upgrade scenarios for the Total Cost of Ownership \(TCO\) of assets:

-   Upgrade works for all Enterprise Asset Management flow tasks
-   You must have task rate cards for each workflow task.
-   The TCO upgrade populates the **Asset** and **Expense category** fields on expense lines corresponding to each task.
-   Expense category is populated based on the expense lines and the source of the expense line.
-   You need to populate the TCO benchmark cost and the TCO benchmark threshold field on all existing models manually or using the bulk import functionality.
-   TCO upgrade populates following fields on asset forms:
    -   **Asset end of useful life**: The created date plus the useful life in months.
    -   **Asset first used date**: The created date.
    -   **Asset TCO**: The aggregated sum of all the expense lines related to the asset. For simple assets, Asset TCO is the aggregated sum of expense lines under it. For complex assets, Asset TCO is the aggregated sum of expense lines of the parent as well as its child assets.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Enterprise Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Understand and analyze your total cost of ownership of assets](https://www.servicenow.com/docs/access?context=asset-tco-eam&family=washingtondc&ft:locale=en-US)**

Manage resources efficiently by tracking the Total Cost of Ownership \(TCO\) of assets, where the total cost includes initial capital cost. You can also break down costs by expense categories and view comparative reports in a vertical bar chart format where each bar is a data source. Click a segment in the bar chart to view expenses for each asset grouped by asset name.

-   **[Manage your tasks using the ServiceNow® Mobile Agent application](https://www.servicenow.com/docs/access?context=track-tasks-using-mobile-agent-app&family=washingtondc&ft:locale=en-US)**

View and manage all the work order tasks assigned to you and your group using the ServiceNow® Mobile Agent application. For example, you can do the following tasks:

    -   Assign a group task to yourself
    -   Record the time taken to complete a task
    -   Handle part requirements
    -   Manage asset actions
    -   Access knowledge articles
-   **[View the hierarchy and task details of an asset on the asset form](https://www.servicenow.com/docs/access?context=view-asset-hierarchy-eam&family=washingtondc&ft:locale=en-US)**

Gain visibility into hierarchy details of assets directly on the contextual sidebar of Enterprise Asset Workspace. You can view the asset hierarchy up to three levels in a tree-like format and expand and view all the children of the asset. You can also view the tasks associated with the asset and its children.

-   **[Perform all your administrative tasks from a centralized location](https://www.servicenow.com/docs/access?context=admin-center-overview-eam&family=washingtondc&ft:locale=en-US)**

Use the Admin center in the Enterprise Asset Workspace for easy access to perform all administrative tasks. Perform tasks such as risk and TCO configuration, create model categories and linear asset types, and bulk import of models and assets.

-   **[Onboard multiple assets using the multi-asset onboarding playbook](https://www.servicenow.com/docs/access?context=asset-onboarding-eam&family=washingtondc&ft:locale=en-US)**

Use the multi-asset onboarding playbook to onboard multiple assets all at the same time. As you complete each activity in the playbook, you’re taken to the next activity. After you complete all the activities, the multiple assets are successfully onboarded.

-   **[View and manage procurement details using the intuitive Procurement view](https://www.servicenow.com/docs/access?context=procurement-overview-eam&family=washingtondc&ft:locale=en-US)**

Track procurement-related requests and manage purchase orders easily through the Procurement view in the Enterprise Asset Workspace.

-   **[Simplify your work management workflow to increase productivity](https://www.servicenow.com/docs/access?context=bulk-close-wot&family=washingtondc&ft:locale=en-US)**

Optimize your work management workflow by performing bulk closure of work order tasks, partial sourcing of parts requirement, and creation of checklist templates from work order templates.

-   **[Manage the operational assets of your organization using Product Instance](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Manage an asset throughout its life cycles in the Enterprise Asset Management application and workflows by representing the asset as a Product Instance, which is a logical grouping of operational asset, Configuration Item \(CI\), and Install Base Item \(IBI\) classes.

-   **[Classify social benefit service models within the Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Starting with version 2.5.0 of the Expanded Model and Asset Classes application, use the Social benefit model class to classify service models that are based on social insurance programs and means-tested assistance programs. This class is a child of the base Service model \[cmdb\_service\_product\_model\] class.

-   **[Categorize API and Managed API classes within the Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Starting with version 2.5.0 of the Expanded Model and Asset Classes application, use the API and Managed API model categories to create and associate application models with API and Managed API CMDB CI classes. By associating application models with these CMDB CI classes, you can get a more comprehensive version-agnostic view of your APIs.

-   **[Categorize enterprise models and assets using additional model categories](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Starting with version 2.6.0 of the Expanded Model and Asset Classes application, use the following additional model categories to associate enterprise model and enterprise asset classes with Configuration Management Database \(CMDB\) configuration item \(CI\) classes:

    -   Patient Monitoring
    -   Patient Implant
    -   Surgical Instrument
    -   Clinical Device
    -   Lab Equipment
    -   Diagnostic Imaging
    -   Therapeutic Device
    -   Dental Equipment
    -   Operational Equipment

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Define required calibrations for your enterprise assets by using calibration attributes](https://www.servicenow.com/docs/access?context=add-calibration-attributes-enterprise-asset&family=xanadu&ft:locale=en-US)**

Use calibration attributes to define the calibrations that are required for your enterprise assets. Specify the details and requirements of each calibration, such as the calibration frequency, the calibration quality standard, and the accuracy measurement guidelines. Maintain comprehensive and up-to-date records of each calibration so that you can improve the performance, safety, and longevity of your enterprise assets.

-   **[Schedule and track enterprise asset calibrations through work orders](https://www.servicenow.com/docs/access?context=create-manage-wo-enterprise-assets&family=xanadu&ft:locale=en-US)**

Use work orders to schedule, to execute, and to track the progress of your enterprise asset calibrations. View and manage corresponding work order tasks by using the guided playbook experience on either your ServiceNow® instance or the ServiceNow Mobile Agent application.

-   **[Use personalized workspaces and roles tailored for healthcare and facility management industries](https://www.servicenow.com/docs/access?context=medical-facility-workspaces&family=xanadu&ft:locale=en-US)**

Enhance data security within your organization by creating and managing medical and facility assets and models in their customized workspaces. Use specific roles to limit access to these assets and models to improve the confidentiality and integrity of your data.

-   **[Manage repair of defective enterprise assets in the stockroom by using the Repair flow](https://www.servicenow.com/docs/access?context=requesting-repair-eam-assets&family=xanadu&ft:locale=en-US)**

Request repair of assets that are defective or pending repair by using the Repair flow. Enterprise asset manager can submit an asset repair request in the Enterprise Asset Workspace or by using the Service Catalog. The Repair flow includes troubleshooting, repair, and evaluation tasks. Repair orders are processed either in the Enterprise Asset Workspace or the ServiceNow mobile Mobile Agent application.

-   **[Drop off and receive assets at a stockroom](https://www.servicenow.com/docs/access?context=drop-off-receive-assets-eam&family=xanadu&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received asset and closes the Drop off task.

-   **[Manage inventory picking within your stockroom](https://www.servicenow.com/docs/access?context=managing-ent-asset-pickup&family=xanadu&ft:locale=en-US)**

Pick assets in your stockroom easily for sourcing, enterprise asset requests, and enterprise asset refresh workflows by enabling the Pick task for your stockroom. The task lists the assets that you should pick from the stockroom. The aisle and space details of the asset provide the exact location from where the asset should be picked. You can work on pick tasks assigned to you by using the ServiceNow mobile Mobile Agent application. With the indoor mapping capabilities, you can also get directions to the location of the asset in the stockroom on your ServiceNow mobile Mobile Agent application.

-   **[Access Planned Work Management application’s capabilities through the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=create-work-plan-eam&family=xanadu&ft:locale=en-US)**

Enable users of Field Service Management Pro or Field Service Management Enterprise to utilize the Planned Work Management application's functionality to manage work plans from within the Enterprise Asset Workspace.

-   **[Manage your operational assets efficiently in the workspace](https://www.servicenow.com/docs/access?context=ot-asset-management&family=xanadu&ft:locale=en-US)**

Get a comprehensive view of all your Operational Technology \(OT\) and Operational Equipment \(OE\) assets and manage them efficiently in the OT Asset Workspace. The OT asset manager and OT asset technician roles enable you to manage these assets.

-   **[View the hierarchy details of an enterprise model in the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=view-model-hierarchy-eam&family=xanadu&ft:locale=en-US)**

Gain visibility into hierarchy details of enterprise models directly on the contextual sidebar of the Model form. You can view all the model components of the pre-assembled and user-assembled models in a tree-like format.

-   **[Manage the life cycle of enterprise models efficiently](https://www.servicenow.com/docs/access?context=create-calculated-model-lc-template-eam&family=xanadu&ft:locale=en-US)**

Manage the complete life cycle of your enterprise models efficiently by applying calculated model life-cycle templates. When you associate any life-cycle template with an enterprise model record, details of all the life-cycle phases are calculated and shown on the Model form.

-   **[Start the process of onboarding multiple assets directly in the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=onboarding-multi-asset-from-ws&family=xanadu&ft:locale=en-US)**

Onboard multiple assets in one go by creating Onboarding orders in the Enterprise Asset Workspace. The asset onboarding playbook is a guided experience that includes a deployment activity. This activity enables you to create deployment tasks for assets using Enterprise asset deployment tasks or Work order tasks. You can also specify the location where you want to deploy the assets.

-   **[Firmware model classes added to the Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&family=xanadu&ft:locale=en-US)**

Manage the firmware details by using Discovered firmware model and Firmware model classes available with the Expanded Model and Asset Classes Store application.


</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Enterprise Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Refresh flow in OT workspace](https://www.servicenow.com/docs/access?context=request-eam-assetrefresh&family=yokohama&ft:locale=en-US)**

For single and multi-model refresh orders, the OT manager can edit the replacement model even after the refresh order has been created in the OTAM workspace. Additionally, the sourcing location is also editable.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The configurable Enterprise Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Enterprise Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Enterprise Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

Install Enterprise Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install the following applications by requesting them from ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Enterprise Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

-   Gain insights into the total cost of assets and use the information for strategic planning and execution within the asset estate. Additionally, access a thorough overview of the breakdown of expenses.
-   View and manage work order tasks assigned to you and your group using the ServiceNow® Mobile Agent application.
-   Gain more visibility into task details and hierarchy of an asset with a parent-child relationship using the improved asset form in the Enterprise Asset Workspace.
-   Use the Admin center as a central hub for all your configuration and administrative tasks in the Enterprise Asset Workspace.
-   Onboard multiple assets simultaneously for the same model via the multi-asset onboarding playbook. Use a single playbook to guide you through the onboarding process.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Track and manage the calibrations that are made to your enterprise assets throughout their life cycles.
-   Use designated roles to manage industry-specific assets and models through customized workspaces.
-   Optimize your inventory by getting the defective enterprise assets in the stockroom repaired quickly using the Repair flow.
-   Return assets that are in your personal stockroom easily by creating Drop off tasks.
-   Locate and pick the assets in your stockroom efficiently and with little effort by using the ServiceNow Mobile Agent application.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Streamline firmware management with the new Firmware model class.
-   Get normalization coverage for firmware that is embedded into your industrial and IT hardware-based Operational Technology \(OT\) assets.
-   Achieve synchronization between physical assets and configuration items \(CIs\) for Operational Technology \(OT\) assets through MAC addresses.
-   Streamline OT Asset Management \(OTAM\) licensing to include hardware resource categories for OT hardware assets to access OT Asset Management features and workflows.
-   Get support for hardware models and OT hardware assets in the OT Asset Management workspace.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)


---
title: Combined Enterprise Asset Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Enterprise Asset Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-enterpriseassetmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 22
breadcrumb: [Products combined by family]
---

# Combined Enterprise Asset Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Enterprise Asset Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Asset Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.

-   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(\[Omitted image "image.asset-putaway-icon-ma"\] Alt text: Asset put away icon\) is included in the navigation bar
-   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Enterprise Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Understand and analyze your total cost of ownership of assets](https://servicenow-staging.fluidtopics.net/access?context=asset-tco-eam&family=washingtondc&ft:locale=en-US)**

Manage resources efficiently by tracking the Total Cost of Ownership \(TCO\) of assets, where the total cost includes initial capital cost. You can also break down costs by expense categories and view comparative reports in a vertical bar chart format where each bar is a data source. Click a segment in the bar chart to view expenses for each asset grouped by asset name.

-   **[Manage your tasks using the ServiceNow® Mobile Agent application](https://servicenow-staging.fluidtopics.net/access?context=track-tasks-using-mobile-agent-app&family=washingtondc&ft:locale=en-US)**

View and manage all the work order tasks assigned to you and your group using the ServiceNow® Mobile Agent application. For example, you can do the following tasks:

    -   Assign a group task to yourself
    -   Record the time taken to complete a task
    -   Handle part requirements
    -   Manage asset actions
    -   Access knowledge articles
-   **[View the hierarchy and task details of an asset on the asset form](https://servicenow-staging.fluidtopics.net/access?context=view-asset-hierarchy-eam&family=washingtondc&ft:locale=en-US)**

Gain visibility into hierarchy details of assets directly on the contextual sidebar of Enterprise Asset Workspace. You can view the asset hierarchy up to three levels in a tree-like format and expand and view all the children of the asset. You can also view the tasks associated with the asset and its children.

-   **[Perform all your administrative tasks from a centralized location](https://servicenow-staging.fluidtopics.net/access?context=admin-center-overview-eam&family=washingtondc&ft:locale=en-US)**

Use the Admin center in the Enterprise Asset Workspace for easy access to perform all administrative tasks. Perform tasks such as risk and TCO configuration, create model categories and linear asset types, and bulk import of models and assets.

-   **[Onboard multiple assets using the multi-asset onboarding playbook](https://servicenow-staging.fluidtopics.net/access?context=asset-onboarding-eam&family=washingtondc&ft:locale=en-US)**

Use the multi-asset onboarding playbook to onboard multiple assets all at the same time. As you complete each activity in the playbook, you’re taken to the next activity. After you complete all the activities, the multiple assets are successfully onboarded.

-   **[View and manage procurement details using the intuitive Procurement view](https://servicenow-staging.fluidtopics.net/access?context=procurement-overview-eam&family=washingtondc&ft:locale=en-US)**

Track procurement-related requests and manage purchase orders easily through the Procurement view in the Enterprise Asset Workspace.

-   **[Simplify your work management workflow to increase productivity](https://servicenow-staging.fluidtopics.net/access?context=bulk-close-wot&family=washingtondc&ft:locale=en-US)**

Optimize your work management workflow by performing bulk closure of work order tasks, partial sourcing of parts requirement, and creation of checklist templates from work order templates.

-   **[Manage the operational assets of your organization using Product Instance](https://servicenow-staging.fluidtopics.net/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Manage an asset throughout its life cycles in the Enterprise Asset Management application and workflows by representing the asset as a Product Instance, which is a logical grouping of operational asset, Configuration Item \(CI\), and Install Base Item \(IBI\) classes.

-   **[Classify social benefit service models within the Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Starting with version 2.5.0 of the Expanded Model and Asset Classes application, use the Social benefit model class to classify service models that are based on social insurance programs and means-tested assistance programs. This class is a child of the base Service model \[cmdb\_service\_product\_model\] class.

-   **[Categorize API and Managed API classes within the Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

Starting with version 2.5.0 of the Expanded Model and Asset Classes application, use the API and Managed API model categories to create and associate application models with API and Managed API CMDB CI classes. By associating application models with these CMDB CI classes, you can get a more comprehensive version-agnostic view of your APIs.

-   **[Categorize enterprise models and assets using additional model categories](https://servicenow-staging.fluidtopics.net/access?context=enterprise-model-asset-classes-app&family=washingtondc&ft:locale=en-US)**

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

-   **[Define required calibrations for your enterprise assets by using calibration attributes](https://servicenow-staging.fluidtopics.net/access?context=add-calibration-attributes-enterprise-asset&family=xanadu&ft:locale=en-US)**

Use calibration attributes to define the calibrations that are required for your enterprise assets. Specify the details and requirements of each calibration, such as the calibration frequency, the calibration quality standard, and the accuracy measurement guidelines. Maintain comprehensive and up-to-date records of each calibration so that you can improve the performance, safety, and longevity of your enterprise assets.

-   **[Schedule and track enterprise asset calibrations through work orders](https://servicenow-staging.fluidtopics.net/access?context=create-manage-wo-enterprise-assets&family=xanadu&ft:locale=en-US)**

Use work orders to schedule, to execute, and to track the progress of your enterprise asset calibrations. View and manage corresponding work order tasks by using the guided playbook experience on either your ServiceNow® instance or the ServiceNow Mobile Agent application.

-   **[Use personalized workspaces and roles tailored for healthcare and facility management industries](https://servicenow-staging.fluidtopics.net/access?context=medical-facility-workspaces&family=xanadu&ft:locale=en-US)**

Enhance data security within your organization by creating and managing medical and facility assets and models in their customized workspaces. Use specific roles to limit access to these assets and models to improve the confidentiality and integrity of your data.

-   **[Manage repair of defective enterprise assets in the stockroom by using the Repair flow](https://servicenow-staging.fluidtopics.net/access?context=requesting-repair-eam-assets&family=xanadu&ft:locale=en-US)**

Request repair of assets that are defective or pending repair by using the Repair flow. Enterprise asset manager can submit an asset repair request in the Enterprise Asset Workspace or by using the Service Catalog. The Repair flow includes troubleshooting, repair, and evaluation tasks. Repair orders are processed either in the Enterprise Asset Workspace or the ServiceNow mobile Mobile Agent application.

-   **[Drop off and receive assets at a stockroom](https://servicenow-staging.fluidtopics.net/access?context=drop-off-receive-assets-eam&family=xanadu&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received asset and closes the Drop off task.

-   **[Manage inventory picking within your stockroom](https://servicenow-staging.fluidtopics.net/access?context=managing-ent-asset-pickup&family=xanadu&ft:locale=en-US)**

Pick assets in your stockroom easily for sourcing, enterprise asset requests, and enterprise asset refresh workflows by enabling the Pick task for your stockroom. The task lists the assets that you should pick from the stockroom. The aisle and space details of the asset provide the exact location from where the asset should be picked. You can work on pick tasks assigned to you by using the ServiceNow mobile Mobile Agent application. With the indoor mapping capabilities, you can also get directions to the location of the asset in the stockroom on your ServiceNow mobile Mobile Agent application.

-   **[Access Planned Work Management application’s capabilities through the Enterprise Asset Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-work-plan-eam&family=xanadu&ft:locale=en-US)**

Enable users of Field Service Management Pro or Field Service Management Enterprise to utilize the Planned Work Management application's functionality to manage work plans from within the Enterprise Asset Workspace.

-   **[Manage your operational assets efficiently in the workspace](https://servicenow-staging.fluidtopics.net/access?context=ot-asset-management&family=xanadu&ft:locale=en-US)**

Get a comprehensive view of all your Operational Technology \(OT\) and Operational Equipment \(OE\) assets and manage them efficiently in the OT Asset Workspace. The OT asset manager and OT asset technician roles enable you to manage these assets.

-   **[View the hierarchy details of an enterprise model in the Enterprise Asset Workspace](https://servicenow-staging.fluidtopics.net/access?context=view-model-hierarchy-eam&family=xanadu&ft:locale=en-US)**

Gain visibility into hierarchy details of enterprise models directly on the contextual sidebar of the Model form. You can view all the model components of the pre-assembled and user-assembled models in a tree-like format.

-   **[Manage the life cycle of enterprise models efficiently](https://servicenow-staging.fluidtopics.net/access?context=create-calculated-model-lc-template-eam&family=xanadu&ft:locale=en-US)**

Manage the complete life cycle of your enterprise models efficiently by applying calculated model life-cycle templates. When you associate any life-cycle template with an enterprise model record, details of all the life-cycle phases are calculated and shown on the Model form.

-   **[Start the process of onboarding multiple assets directly in the Enterprise Asset Workspace](https://servicenow-staging.fluidtopics.net/access?context=onboarding-multi-asset-from-ws&family=xanadu&ft:locale=en-US)**

Onboard multiple assets in one go by creating Onboarding orders in the Enterprise Asset Workspace. The asset onboarding playbook is a guided experience that includes a deployment activity. This activity enables you to create deployment tasks for assets using Enterprise asset deployment tasks or Work order tasks. You can also specify the location where you want to deploy the assets.

-   **[Firmware model classes added to the Expanded Model and Asset Classes Store application](https://servicenow-staging.fluidtopics.net/access?context=enterprise-model-asset-classes-app&family=xanadu&ft:locale=en-US)**

Manage the firmware details by using Discovered firmware model and Firmware model classes available with the Expanded Model and Asset Classes Store application.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Gain normalization coverage for firmware in your Operational Technology \(OT\) assets](https://servicenow-staging.fluidtopics.net/access?context=normalizing-firmware-ot-assets&family=yokohama&ft:locale=en-US)**

Achieve enhanced normalization across your OT deployments by normalizing the firmware that is embedded into your OT assets. Use the normalized data to track and manage the life cycles of your firmware separately from your OT assets so that you can directly detect and mitigate firmware vulnerabilities. You can view the firmware model details in the OT model management view of the OT Asset Workspace.

**Note:** Firmware normalization is applicable only to OT Asset Management.

-   **[Manage hardware models and assets in the Operational Technology \(OT\) Asset Management application](https://servicenow-staging.fluidtopics.net/access?context=ot-asset-ws-otam&family=yokohama&ft:locale=en-US)**

Enable your OT managers to create hardware models and assets in the OT Workspace. You can integrate hardware models and OT assets into such Enterprise Asset Management flows as asset request, asset refresh, stock order, multi-asset onboarding, Return Merchandise Authorization \(RMA\), repair, and disposal. You can also generate maintenance plans and work orders for your OT hardware assets.

-   **[Synchronize asset and CIs for Operational Technology \(OT\) assets](https://servicenow-staging.fluidtopics.net/access?context=asset-ci-sync-ot-assets&family=yokohama&ft:locale=en-US)**

Synchronize the MAC addresses between the asset and network adapter CI for OT assets.

-   **[License your OT hardware assets using the new resource categories available in OTAM licensing](https://servicenow-staging.fluidtopics.net/access?context=licensing-ot-asset-management&family=yokohama&ft:locale=en-US)**

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

-   **[Manage mission-critical enterprise assets and linear assets for telecommunications networks](https://servicenow-staging.fluidtopics.net/access?context=eam-dcnam&family=yokohama&ft:locale=en-US)**

Use the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application to track and manage mission-critical facility-based enterprise assets and linear assets for telecommunications networks. Get a comprehensive view of these assets throughout their life cycles so that you can help optimize their performance and improve their longevity.

-   **[Fulfill Return Merchandise Authorization \(RMA\) requests as a Device as a Service \(DaaS\) provider, vendor, or manufacturer](https://servicenow-staging.fluidtopics.net/access?context=eam-providers&family=yokohama&ft:locale=en-US)**

Use the Enterprise Asset Management for Providers application to fulfill the RMA requests that you receive from customers as a DaaS provider, vendor, or manufacturer. The application adds support for RMA response orders, which enable you to track and manage the process of repairing or replacing defective assets for your RMA requests. The application also adds support for inbound asset orders, which enable you to track and manage the process of providing assets for your RMA requests. By managing these orders from a consolidated location, you can streamline your operations and improve efficiency.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Organize your assets into hierarchical asset groups to manage your complex asset ecosystems](https://servicenow-staging.fluidtopics.net/access?context=asset-groups-eam&family=zurich&ft:locale=en-US)**

Organize assets into logical groups and subgroups to represent their dependencies and operational relationships. Use a dependency map to visualize the entire structure of the asset hierarchy, making it easy to see all the subgroups and assets within each asset group.

-   **[Inspect the condition of enterprise assets to determine their health and ensure reliability](https://servicenow-staging.fluidtopics.net/access?context=asset-conditions-eam&family=zurich&ft:locale=en-US)**

Define condition attributes for enterprise models and assets and associate these attributes with templates to identify any potential issues throughout the asset life cycle. Enable scoring in the templates to calculate asset condition scores to determine whether an asset passes or fails the evaluation. Schedule asset condition evaluations via maintenance plans or work orders. View comprehensive reports on the asset condition outcomes on dashboards across your organization.

-   **[Optimize your operations with asset performance reports](https://servicenow-staging.fluidtopics.net/access?context=eam-asset-dboard&family=zurich&ft:locale=en-US)**

Track the past performance of assets and get notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification. This tracking helps improve asset availability according to ISO standards.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://servicenow-staging.fluidtopics.net/access?context=manage-stockroom-inventory-reports&family=zurich&ft:locale=en-US)**

Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Enterprise Asset Workspace. These reports help you:

    -   Find replacement options or spare part availability for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Achieve faster diagnostics and enhanced maintenance efficiency with standardized failure and resolution codes](https://servicenow-staging.fluidtopics.net/access?context=failure-resolution-codes-eam&family=zurich&ft:locale=en-US)**

Enable technicians to record predefined failure reasons and resolution steps with configurable codes. You can create, update, and import these codes through spreadsheets in the Admin center of the Enterprise Asset Workspace. In the Repair flow, these codes help technicians record the reason for the specific issue with the asset and the appropriate solution for repairing it.

-   **[Manage OT hardware models and assets in the OT Asset Workspace](https://servicenow-staging.fluidtopics.net/access?context=ot-asset-ws-otam&family=zurich&ft:locale=en-US)**

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
-   **[Remediate unsuccessful enterprise asset calibrations](https://servicenow-staging.fluidtopics.net/access?context=remediate-unsuccessful-enterprise-asset-calibration&family=zurich&ft:locale=en-US)**

Remediate failed calibration events by initiating new work orders and corresponding work order tasks for those events. When you select the option to remediate a failed calibration event, you can choose an appropriate work order template to generate a new work order with at least one work order task. The work order and work order task are auto-populated with the asset that you want to calibrate, the location of that asset, the original work order, and all mandatory fields. In addition, the original and new calibration events and their corresponding tasks are linked together through the **Parent** field for full traceability.

-   **[Measure calibration tolerance conformance by using additional value types](https://servicenow-staging.fluidtopics.net/access?context=add-calibration-attributes-enterprise-model&family=zurich&ft:locale=en-US)**

Use the following additional value types to compare your calibration measurements against the corresponding tolerances that you define:

    -   Range
    -   Less than
    -   Greater than
In addition, use the True/False value type to assess the qualitative elements of your calibrations.

-   **[Manage unique identifiers for enterprise assets using CI identification rules](https://servicenow-staging.fluidtopics.net/access?context=create-asset-eam&family=zurich&ft:locale=en-US)**

Define required and unique fields on asset records by creating identification rules on associated CI classes in the Identification and Reconciliation engine \(IRE\). When you create an asset whose model category is linked to a CI class with an identification rule, you should provide details for at least one of the fields, such as Asset tag, Serial number, and MAC address, that uniquely identify the asset.

-   **[Drop off and receive assets at a stockroom by using the ServiceNow Mobile Agent application](https://servicenow-staging.fluidtopics.net/access?context=manage-dropoff-mobile-agent&family=zurich&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task using the ServiceNow® Mobile Agent application. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received assets and closes the Drop off task using the Mobile Agent application.

**Note:** Starting with the Xanadu release, you could create Drop off and Receive tasks in the Enterprise Asset Workspace. However, now you can also use the Mobile Agent application for the same purpose.

-   **[Receive shipment assets at a stockroom through the streamlined and unified receiving process](https://servicenow-staging.fluidtopics.net/access?context=stockroom-receiving-eam&family=zurich&ft:locale=en-US)**

Receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the following workspaces:

    -   Enterprise Asset Workspace
    -   OT Asset Workspace
    -   Medical Asset Workspace
    -   Facility Asset Workspace
This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://servicenow-staging.fluidtopics.net/access?context=managing-inventory-by-putting-away-asset-eam&family=zurich&ft:locale=en-US)**

Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Enterprise Asset Workspace or ServiceNow Agent application.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Enterprise Asset Management features.

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

-   **[Refresh flow in OT workspace](https://servicenow-staging.fluidtopics.net/access?context=request-eam-assetrefresh&family=yokohama&ft:locale=en-US)**

For single and multi-model refresh orders, the OT manager can edit the replacement model even after the refresh order has been created in the OTAM workspace. Additionally, the sourcing location is also editable.

-   **[Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The configurable Enterprise Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enterprise Asset Management demo data migration](https://servicenow-staging.fluidtopics.net/access?context=install-eam-demo-data&family=zurich&ft:locale=en-US)**

All Enterprise Asset Management demo data has migrated from the Enterprise Asset Management application to either the EAM Demo Data application or Indoor Mapping for Assets application. The EAM Demo Data application contains all Enterprise Asset Management demo data except for indoor mapping-related demo data, which is now included in the Indoor Mapping for Assets application.

-   **[Shipment asset table label](https://servicenow-staging.fluidtopics.net/access?context=view-enterprise-asset-shipments&family=zurich&ft:locale=en-US)**

Starting from the Enterprise Asset Management version 9.1.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://servicenow-staging.fluidtopics.net/access?context=view-enterprise-asset-shipments&family=zurich&ft:locale=en-US)**

Starting from Enterprise Asset Management version 9.1.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Enterprise Asset Management features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Enterprise Asset Management features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

The Classification \(classification\) column in the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(Deprecated\). The data from this column is available in the new Classification \(classification\_code\) column in the Product model \[cmdb\_model\] table.

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

Install Enterprise Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install the following applications by requesting them from ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes



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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

-   ****

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

</td></tr><tr><td>

Zurich

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

 See [Enterprise Asset Management](https://servicenow-staging.fluidtopics.net/access?context=enterprise-asset-management&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Track and manage the calibrations that are made to your enterprise assets throughout their life cycles.
-   Use designated roles to manage industry-specific assets and models through customized workspaces.
-   Optimize your inventory by getting the defective enterprise assets in the stockroom repaired quickly using the Repair flow.
-   Return assets that are in your personal stockroom easily by creating Drop off tasks.
-   Locate and pick the assets in your stockroom efficiently and with little effort by using the ServiceNow Mobile Agent application.

 See [Enterprise Asset Management](https://servicenow-staging.fluidtopics.net/access?context=enterprise-asset-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Streamline firmware management with the new Firmware model class.
-   Get normalization coverage for firmware that is embedded into your industrial and IT hardware-based Operational Technology \(OT\) assets.
-   Achieve synchronization between physical assets and configuration items \(CIs\) for Operational Technology \(OT\) assets through MAC addresses.
-   Streamline OT Asset Management \(OTAM\) licensing to include hardware resource categories for OT hardware assets to access OT Asset Management features and workflows.
-   Get support for hardware models and OT hardware assets in the OT Asset Management workspace.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Enterprise Asset Management](https://servicenow-staging.fluidtopics.net/access?context=enterprise-asset-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Organize related assets into hierarchical asset groups and subgroups to enable consolidated reporting, streamline maintenance workflows, and provide clear dependency mapping.
-   Create scalable templates to evaluate the condition of enterprise assets, which helps to detect issues early, optimize maintenance planning, and maximize asset lifespan.
-   Achieve operational efficiency by evaluating how effectively your assets are functioning and being used, through reports based on asset key performance indicators in the Asset analytics view.
-   Manage supply and demand originating from service locations or other stockrooms through local stock or distribution channels using the Inventory insights tab in the stockroom record. You can also compare multiple stockrooms at the same time.
-   Gain insights into asset failure reasons and resolution actions using the failure and resolution codes in the Enterprise Asset Workspace.

 See [Enterprise Asset Management](https://servicenow-staging.fluidtopics.net/access?context=enterprise-asset-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)


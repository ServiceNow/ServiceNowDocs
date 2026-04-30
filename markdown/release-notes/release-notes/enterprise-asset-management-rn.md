---
title: Enterprise Asset Management release notes
description: The ServiceNow Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 12
---

# Enterprise Asset Management release notes

The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtimes. Enterprise Asset Management was enhanced and updated in the Zurich release.

## Enterprise Asset Management highlights for the Zurich release

-   Organize related assets into hierarchical asset groups and subgroups to enable consolidated reporting, streamline maintenance workflows, and provide clear dependency mapping.
-   Create scalable templates to evaluate the condition of enterprise assets, which helps to detect issues early, optimize maintenance planning, and maximize asset lifespan.
-   Achieve operational efficiency by evaluating how effectively your assets are functioning and being used, through reports based on asset key performance indicators in the Asset analytics view.
-   Manage supply and demand originating from service locations or other stockrooms through local stock or distribution channels using the Inventory insights tab in the stockroom record. You can also compare multiple stockrooms at the same time.
-   Gain insights into asset failure reasons and resolution actions using the failure and resolution codes in the Enterprise Asset Workspace.

See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

**Important:** Enterprise Asset Management, Enterprise Asset Management for Healthcare, Operational Technology \(OT\) Asset Management, and Expanded Model and Asset Classes are available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Enterprise Asset Management to Zurich

Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.

-   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![Asset put away icon](../image/asset-putaway-icon-ma.png)\) is included in the navigation bar
-   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.

## New in the Zurich release

-   **[Organize your assets into hierarchical asset groups to manage your complex asset ecosystems](https://www.servicenow.com/docs/access?context=asset-groups-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Organize assets into logical groups and subgroups to represent their dependencies and operational relationships. Use a dependency map to visualize the entire structure of the asset hierarchy, making it easy to see all the subgroups and assets within each asset group.

-   **[Inspect the condition of enterprise assets to determine their health and ensure reliability](https://www.servicenow.com/docs/access?context=asset-conditions-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Define condition attributes for enterprise models and assets and associate these attributes with templates to identify any potential issues throughout the asset life cycle. Enable scoring in the templates to calculate asset condition scores to determine whether an asset passes or fails the evaluation. Schedule asset condition evaluations via maintenance plans or work orders. View comprehensive reports on the asset condition outcomes on dashboards across your organization.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=eam-asset-dboard&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Track the past performance of assets and get notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification. This tracking helps improve asset availability according to ISO standards.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-reports&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Enterprise Asset Workspace. These reports help you:

    -   Find replacement options or spare part availability for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Achieve faster diagnostics and enhanced maintenance efficiency with standardized failure and resolution codes](https://www.servicenow.com/docs/access?context=failure-resolution-codes-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Enable technicians to record predefined failure reasons and resolution steps with configurable codes. You can create, update, and import these codes through spreadsheets in the Admin center of the Enterprise Asset Workspace. In the Repair flow, these codes help technicians record the reason for the specific issue with the asset and the appropriate solution for repairing it.

-   **[Manage OT hardware models and assets in the OT Asset Workspace](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

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
-   **[Remediate unsuccessful enterprise asset calibrations](https://www.servicenow.com/docs/access?context=remediate-unsuccessful-enterprise-asset-calibration&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Remediate failed calibration events by initiating new work orders and corresponding work order tasks for those events. When you select the option to remediate a failed calibration event, you can choose an appropriate work order template to generate a new work order with at least one work order task. The work order and work order task are auto-populated with the asset that you want to calibrate, the location of that asset, the original work order, and all mandatory fields. In addition, the original and new calibration events and their corresponding tasks are linked together through the **Parent** field for full traceability.

-   **[Measure calibration tolerance conformance by using additional value types](https://www.servicenow.com/docs/access?context=add-calibration-attributes-enterprise-model&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use the following additional value types to compare your calibration measurements against the corresponding tolerances that you define:

    -   Range
    -   Less than
    -   Greater than
    In addition, use the True/False value type to assess the qualitative elements of your calibrations.

-   **[Manage unique identifiers for enterprise assets using CI identification rules](https://www.servicenow.com/docs/access?context=create-asset-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Define required and unique fields on asset records by creating identification rules on associated CI classes in the Identification and Reconciliation engine \(IRE\). When you create an asset whose model category is linked to a CI class with an identification rule, you should provide details for at least one of the fields, such as Asset tag, Serial number, and MAC address, that uniquely identify the asset.

-   **[Drop off and receive assets at a stockroom by using the ServiceNow Mobile Agent application](https://www.servicenow.com/docs/access?context=manage-dropoff-mobile-agent&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task using the ServiceNow® Mobile Agent application. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received assets and closes the Drop off task using the Mobile Agent application.

    **Note:** Starting with the Xanadu release, you could create Drop off and Receive tasks in the Enterprise Asset Workspace. However, now you can also use the Mobile Agent application for the same purpose.

-   **[Receive shipment assets at a stockroom through the streamlined and unified receiving process](https://www.servicenow.com/docs/access?context=stockroom-receiving-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the following workspaces:

    -   Enterprise Asset Workspace
    -   OT Asset Workspace
    -   Medical Asset Workspace
    -   Facility Asset Workspace
    This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

    You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Enterprise Asset Workspace or ServiceNow Agent application.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Asset performance dashboard in the Asset analytics view](https://www.servicenow.com/docs/access?context=eam-asset-dboard&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Asset performance dashboard in the Asset analytics view of the Enterprise Asset Workspace includes scorecards for Availability, Mean time to repair device \(MTTR\), and Mean time between failures \(MTBF\).

    The Asset availability and related KPIs report and the Asset total time spent report are displayed in the contextual sidebar of the asset form.

-   **[Stock orders and Transfer orders tabs for stock rules in Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=create-eamstockrules&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Stock orders** tab on a stock rule shows all the stock orders that were created using that specific stock rule. The **Transfer orders** tab on a stock rule lists all the transfer orders that were generated using that particular stock rule.

-   **[Inventory availability tab on the asset form in the Enterprise Asset Workspace](https://www.servicenow.com/docs/access?context=identify-inventory-availability-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Inventory availability** tab on the asset form lists all available replacement assets and parts or their substitutes in local and remote stockrooms. The Purchase lead time column displays the average number of days that it would take to procure a new asset through a new purchase order.

-   **[Failure and resolution list in the Admin center](https://www.servicenow.com/docs/access?context=manage-failure-res-codes-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Failure and resolution list in the Admin center of the Enterprise Asset Workspace provides options to create, update, and import failure and resolution codes.

-   **[Failure code and Resolution code fields on repair order task forms](https://www.servicenow.com/docs/access?context=troubleshoot-eam-assets-for-repair&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Failure code** and **Resolution code** fields appear on repair order task forms. As an asset technician, you can do the following:

    -   On the Troubleshoot asset task form, select a predefined code in the **Failure code** field.
    -   On the Repair asset task form, select predefined codes in both the **Failure code** and **Resolution code** fields.
    -   On the Evaluate asset task form and the Repair order line form, only view the failure code and resolution code selected in the previous tasks.
-   **[Location field on the work order and work order task forms for linear assets](https://www.servicenow.com/docs/access?context=create-eam-work-order&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    For a linear asset, the **Location** field on the work order and work order task forms in the Enterprise Asset Workspace shows a pencil icon \(![Pencil icon.](../../reuse/icons/product-icons/pencil-outline-24.svg)\). Selecting this icon opens a map where you can select a marker location between the start and end markers.

-   **[Acknowledge Recall button and Enterprise Recall Tasks tab](https://www.servicenow.com/docs/access?context=acknowledge-recalled-assets-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    When an enterprise recall order is created in the Enterprise Asset Workspace, the **Acknowledge Recall** button appears. When you select this button, an Acknowledgment task is generated and listed under the **Enterprise Recall Tasks** tab to confirm whether you want to continue with the recall process.

-   **[Aisle and space field on the stockroom audit form](https://www.servicenow.com/docs/access?context=audit-eam-assetinventory&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    When the audit is for a stockroom, the **Aisle and space** field appears on the audit form in the Enterprise Asset Workspace.

-   **[Custom Firmware CPE mapping in the Enterprise Asset Management Content Service](https://www.servicenow.com/docs/access?context=optin-cs-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Custom Firmware CPE mapping** option enables you to opt in to the Enterprise Asset Management Content Service to improve the normalization process.

    The **Exclude from content service** option on the Custom firmware CPE mapping form enables you to exclude these transactions from being shared with the Content Service.

-   **[Columns for OT entity and Parent asset attribute in the bulk import templates](https://www.servicenow.com/docs/access?context=overview-bulk-import-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The bulk import templates include the OT entity and Parent asset attribute columns.

    When the OT Asset Management application is activated, you can bulk import hardware assets and models in both the Enterprise Asset Workspace and the OT Asset Workspace only if the OT entity column is marked as **TRUE**.

    With the Parent asset attribute, you can choose to identify the parent of a child asset using either the asset tag, serial number, or MAC address.

-   **[OT entity column in the Advanced Shipment Notification template](https://www.servicenow.com/docs/access?context=asn-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Advanced Shipment Notification template includes the OT entity column. When this column is set to **TRUE** for hardware models, it creates OT hardware assets in the OT Asset Workspace.

-   **[Hardware Asset Reclamation Lines tab on OT hardware asset reclamation requests](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    When a reclamation request for an OT hardware asset is created, a hardware reclamation request line is generated and displayed on the **Hardware Asset Reclamation Lines** tab in the OT Asset Workspace.

-   **[OT stock rule check box on the Stock rule form](https://www.servicenow.com/docs/access?context=create-eamstockrules&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **OT stock rule** check box appears on the stock rule form only for hardware models in both the OT Asset Workspace and Enterprise Asset Workspace. However, only the OT asset manager can select or clear this check box in the OT Asset Workspace. The OT stock rule check box indicates whether the stock rule was created in the OT Asset Workspace.

-   **[Bulk import instructions for assets](https://www.servicenow.com/docs/access?context=overview-bulk-import-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Bulk import instructions** option that appears on the contextual sidebar provides guidance on assigning a parent asset when importing assets in bulk.

-   **[Report table field values on the TCO comparative report](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Report table** field on the TCO comparative report shows the **Hardware** option in the OT Asset Workspace.

-   **[Renamed the Pick task required field in the Stockroom details form](https://www.servicenow.com/docs/access?context=enable-pick-task-for-stockroom-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Pick task required** field in the Stockroom details form has been renamed **Warehouse tasks required**. This field supports enabling both the Asset put away task and the Asset pick task for the stockroom in the Hardware Asset Workspace.


## Changed in this release

-   **[Enterprise Asset Management demo data migration](https://www.servicenow.com/docs/access?context=install-eam-demo-data&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    All Enterprise Asset Management demo data has migrated from the Enterprise Asset Management application to either the EAM Demo Data application or Indoor Mapping for Assets application. The EAM Demo Data application contains all Enterprise Asset Management demo data except for indoor mapping-related demo data, which is now included in the Indoor Mapping for Assets application.

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Starting from the Enterprise Asset Management version 9.1.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Starting from Enterprise Asset Management version 9.1.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


## Deprecations

The Classification \(classification\) column in the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(Deprecated\). The data from this column is available in the new Classification \(classification\_code\) column in the Product model \[cmdb\_model\] table.

## Activation information

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The ServiceNow® Field Service Management application enables your organization to manage location-based work more efficiently and safely.

-   **[Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Procurement application helps you create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)


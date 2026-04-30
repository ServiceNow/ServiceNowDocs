---
title: Hardware Asset Management release notes
description: The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Zurich release. This release notes includes Hardware Asset Management version 13.0.0 and 14.0.0 updates.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
---

# Hardware Asset Management release notes

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Zurich release. This release notes includes Hardware Asset Management version 13.0.0 and 14.0.0 updates.

## Hardware Asset Management highlights for the Zurich release

-   Benefit from enhanced Asset Attestation features, including a guided attestation creation process, a mobile-friendly interface for confirming assets, and automated remediation tasks to address non-compliant assets.
-   Achieve real-time tracking of assets that are in transit and maintain asset data accuracy by enabling employees to confirm receipt of assets through the Employee Center portal.
-   Receive shipment assets at a stockroom from any workflow through the streamlined and unified receiving process.
-   Track asset movement from the receiving bay to an aisle and space in the stockroom using the Asset put away task.
-   Evaluate how effectively your assets are functioning and being used through reports based on asset key performance indicators in the Asset analytics view. Also, manage supply and demand in your stockrooms effectively with inventory demand reports.

See [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

**Important:** [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Hardware Asset Management to Zurich

-   Starting from the Zurich release, a few workflows have been migrated to Workflow Studio as flows.

    **Note:** The migration of workflows to Workflow Studio applies to Asset Management, Procurement, and Contract Management applications.

    -   The following workflows have been migrated to Workflow Studio as flows:
        -   Procurement Process Flow – Hardware
        -   Transfer Order
        -   Transfer Order Line
        -   Source Request
        -   Contract Approval
    -   When upgrading to the Zurich release, a fix script identifies whether the workflows were customized and takes necessary action.
        -   If the workflows weren’t customized before the upgrade, the legacy workflows are deactivated from the instance, and Workflow Studio flows are installed and executed post-upgrade.
        -   If the impacted workflows were customized before the upgrade, the Workflow Studio flows are installed but aren’t executed for any of the impacted flows post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered custom code and aren’t supported for maintenance.
-   After upgrading to the Zurich release, if an approval history record exists for a contract that is no longer required, reject the record instead of deleting it. If the approval history record is deleted, Workflow Studio doesn’t support updating the contract’s **Substate** field value to display the correct state.
-   Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.
    -   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![Asset put away icon](../image/asset-putaway-icon-ma.png)\) is included in the navigation bar
    -   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.
-   A new role, sn\_itam\_recomm.recommendations\_read, helps ensure that only valid users can execute APIs related to the Important Actions menu in the Asset Workspace. The following roles, which have access to the Asset Workspace, now include the sn\_itam\_recomm.recommendations\_read role:
    -   procurement\_user
    -   inventory\_admin
    -   inventory\_user
    -   model\_manager
    -   contract\_manager
    -   itil
    -   catalog\_manager
    -   catalog\_admin
    -   sam
    -   ham\_user
    -   asset
-   Control sensitive data leakage from range queries accessed by unauthenticated users through the following access control lists \(ACLs\):
    -   Contract \[ast\_contract\] table: Only users with the contract\_manager role can perform the query\_range operation on the Start date, Contract number, PO number, and Vendor columns.
    -   Contract user M2M \[clm\_m2m\_contract\_user\] table: Only users with the contract\_manager and asset roles can perform the query\_range operation on the Contract and User columns.
    -   HAMP Success Activity \[sn\_hamp\_success\_activity\] table: Only users with the ham\_admin and asset roles can perform the query\_range operation on the Description, Short description, and Success goals columns.
-   Only users with the admin role can update the following system properties:
    -   glide.sg.voice\_search.enabled
    -   glide.ui.sn\_hamp\_asset\_reclaim\_task\_activity.fields
    -   glide.ui.sn\_hamp\_loaner\_asset\_order\_activity.fields
    -   glide.ui.sn\_hamp\_ztr\_task\_activity.fields
    -   sn\_hamp.enable\_shipping\_carrier\_validation\_asn
    -   sn\_hamp.model\_lifecycle\_phase\_order
    -   sn\_hamp.update\_assets\_norm\_model\_name

## New in the Zurich release

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Hardware Asset Workspace or ServiceNow Agent application.

-   **[Improve asset data accuracy and usage by tracking and managing unassigned assets through asset attestation](https://www.servicenow.com/docs/access?context=asset-attestation-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Validate whether assets are in use and confirm asset assignments by initiating the attestation using the Asset Attestation playbook in the Hardware Asset Workspace. Employees can then confirm whether they’re using the assigned serialized hardware assets on the go by using the intuitive Now Mobile app. Reports on open remediation tasks in the Hardware Asset Workspace, generated when employees confirm they don’t have assets, provide actionable insights for asset managers.

-   **[Confirm receipt of hardware and consumable assets through the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Enable your employees to acknowledge the receipt of assets that are in transit and reserved for them through the Employee Center portal. When employees confirm that they have received the assets, the **State** and the **Assigned to** fields are updated in real time, minimizing the risk of data errors.

-   **[Receive shipment assets at a stockroom in the Hardware Asset Workspace](https://www.servicenow.com/docs/access?context=stockroom-receiving-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Complete the receive tasks for hardware and consumable assets that you received from any workflow at the stockroom using the unified receiving functionality in the Hardware Asset Workspace. This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

    You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=asset-analytics-view&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Improve asset availability according to ISO standards by tracking the past performance of assets and getting notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-report-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Hardware Asset Workspace. These reports provide the following benefits:

    -   Find replacement options for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-lookup-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options enables you to view the records for a particular period or release.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Renamed the Pick task required field in the Stockroom details form](https://www.servicenow.com/docs/access?context=enable-pick-task-for-stockroom-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Pick task required** field in the Stockroom details form has been renamed **Warehouse tasks required**. This field supports enabling both the Asset put away task and the Asset pick task for the stockroom in the Hardware Asset Workspace.

-   **[Stage status for the Transfer Order and Transfer Order Line flow](https://www.servicenow.com/docs/access?context=transfer-orders-for-am&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The stage status text in the **Stage** column for the Transfer Order and Transfer Order Line in the Hardware Asset Workspace Core UI has been updated. When a stage is completed and the next stage hasn’t yet begun in the asset transfer process, the revised status is displayed as **Completed-next stage initiated** instead of **In progress**. When a stage isn’t yet begun in the asset transfer process, the revised status is displayed as **Pending not started** instead of **Pending-has not started**. These changes accurately reflect the current action in the asset transfer process and enhances the user experience.

-   **[Asset attestation playbook](https://www.servicenow.com/docs/access?context=create-attestation-using-playbook&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **New** button on the Asset attestation tab opens a playbook instead of the attestation form to create an asset attestation.

-   **[Receive asset button on the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    On the Employee Center portal, assets assigned to you that are in transit display a **Receive asset** button to confirm you have received them.

-   **[Stock orders and Transfer orders tabs for stock rules](https://www.servicenow.com/docs/access?context=t_CreateAStockRule&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Stock Orders** tab on a stock rule shows all the stock orders that were created using that specific stock rule. The **Transfer Orders** tab on a stock rule lists all the transfer orders that were generated using that particular stock rule.

-   **[Inventory availability tab on the asset form](https://www.servicenow.com/docs/access?context=identify-inventory-availability-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Inventory availability** tab on the asset form lists all available replacement assets or their substitutes in local and remote stockrooms. The **Purchase lead time** column displays the average number of days that it would take to procure a new asset through a new purchase order.

-   **[Asset performance dashboard in the Asset analytics view](https://www.servicenow.com/docs/access?context=asset-analytics-view&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Asset performance dashboard in the Asset analytics view of the Hardware Asset Workspace includes scorecards for Availability, Mean time to repair device \(MTTR\), and Mean time between failures \(MTBF\).

    The Asset availability and related KPIs report and the Asset task time summary report are displayed in the contextual sidebar of the asset form.


## Changed in this release

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Starting from the Hardware Asset Management version 14.0.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    With Hardware Asset Management version 14.0.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


## Deprecations

Starting from the Zurich release, the following workflows are being prepared for future deprecation:

-   Procurement Process Flow – Hardware
-   Procurement Process Flow – Mobile
-   Procurement Process Flow - Default
-   Transfer Order
-   Transfer Order Line
-   Source Request
-   Contract Approval

**Note:** Procurement Process Flow-Default and Procurement Process Flow – Mobile are demo data workflows displayed in the workflow studio when the Workflow Authoring Tools \(com.glideapp.workflow.authoring\) plugin is installed.

These impacted workflows are migrated to Workflow Studio flows. After upgrading to the Zurich release, you must transition to the new Workflow Studio flows. For more information about the deprecation process and its impact, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Software Asset Management application enables you to track, evaluate, and manage the software licenses, software compliance, and software optimization. You can reclaim unused software rights, purchase new software rights, and manage allocations for entitlements.

-   **[Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Enterprise Asset Management application enables you to manage the entire life cycle of your connected and non-connected enterprise assets. It provides a comprehensive end-to-end solution for maintaining enterprise assets, minimizing costly downtime, and maximizing enterprise asset usability.

-   **[Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Procurement application enables you to create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)


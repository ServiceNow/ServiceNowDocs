---
title: Combined Hardware Asset Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Hardware Asset Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-hardwareassetmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Hardware Asset Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Hardware Asset Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Hardware Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Hardware Asset Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

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
    -   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(\[Omitted image "image.asset-putaway-icon-ma"\] Alt text: Asset put away icon\) is included in the navigation bar
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

</td></tr><tr><td>

Australia

</td><td>

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
-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Hardware Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset&family=zurich&ft:locale=en-US)**

Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Hardware Asset Workspace or ServiceNow Agent application.

-   **[Improve asset data accuracy and usage by tracking and managing unassigned assets through asset attestation](https://www.servicenow.com/docs/access?context=asset-attestation-ham&family=zurich&ft:locale=en-US)**

Validate whether assets are in use and confirm asset assignments by initiating the attestation using the Asset Attestation playbook in the Hardware Asset Workspace. Employees can then confirm whether they’re using the assigned serialized hardware assets on the go by using the intuitive Now Mobile app. Reports on open remediation tasks in the Hardware Asset Workspace, generated when employees confirm they don’t have assets, provide actionable insights for asset managers.

-   **[Confirm receipt of hardware and consumable assets through the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&family=zurich&ft:locale=en-US)**

Enable your employees to acknowledge the receipt of assets that are in transit and reserved for them through the Employee Center portal. When employees confirm that they have received the assets, the **State** and the **Assigned to** fields are updated in real time, minimizing the risk of data errors.

-   **[Receive shipment assets at a stockroom in the Hardware Asset Workspace](https://www.servicenow.com/docs/access?context=stockroom-receiving-ham&family=zurich&ft:locale=en-US)**

Complete the receive tasks for hardware and consumable assets that you received from any workflow at the stockroom using the unified receiving functionality in the Hardware Asset Workspace. This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=asset-analytics-view&family=zurich&ft:locale=en-US)**

Improve asset availability according to ISO standards by tracking the past performance of assets and getting notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-report-ham&family=zurich&ft:locale=en-US)**

Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Hardware Asset Workspace. These reports provide the following benefits:

    -   Find replacement options for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-lookup-ham&family=zurich&ft:locale=en-US)**

Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options enables you to view the records for a particular period or release.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Manage your assets with comprehensive and real-time data](https://www.servicenow.com/docs/access?context=generate-asset-analysis-now-assist-ham&family=australia&ft:locale=en-US)**

View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


-   **[Gain visibility into approximated life cycle dates for hardware and consumable model](https://www.servicenow.com/docs/access?context=approximated-lifecycles-hardware-products&family=australia&ft:locale=en-US)**

Enhance the operational efficiency by gaining visibility into the estimated and approximate life- cycle dates for models when manufacturers haven’t explicitly published key dates, such as End of Life \(EoL\) and End of Service \(EoS\). This insight enables you to manage your asset portfolio strategically, reducing unexpected downtime and improve budgeting.

-   **[Enhanced and unified hardware asset inventory auditing experience](https://www.servicenow.com/docs/access?context=ham-inventory-audit&family=australia&ft:locale=en-US)**

Streamline and improve your inventory auditing experience with the enhanced and unified hardware asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and verify that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.
-   **[Enhanced asset disposal workflow to streamline the management of retired assets](https://www.servicenow.com/docs/access?context=create-resale-order&family=australia&ft:locale=en-US)**

Resell the retired assets that are no longer in use to reduce waste and receive credit. The extended asset disposal flow in the Documentation stage enables you to resell planned assets instead of disposing of them, enabling you to receive credit.

-   **[Enable your key functional roles or personas to directly manage Advanced Shipment Notification \(ASN\) imports](https://www.servicenow.com/docs/access?context=advanced-shipment-notification&family=australia&ft:locale=en-US)**

Upload ASN files and trigger the import process from the Procurement view within the Hardware Asset Workspace without requiring admin privileges. Users with the ham\_admin, ham\_user, procurement\_admin, or asset role can now initiate the ASN workflow themselves, creating asset records seamlessly.

-   **[Streamline model creation by copying a model directly from the Content lookup portal](https://www.servicenow.com/docs/access?context=copy-hardware-model&family=australia&ft:locale=en-US)**

Reduce manual effort by copying a model from the Content lookup portal to create a record in the Product Model \[cmdb\_model\] table. The copied model is automatically normalized, where applicable, and relevant fields are pre-populated with information from the content record.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Hardware Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&family=zurich&ft:locale=en-US)**

Starting from the Hardware Asset Management version 14.0.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&family=zurich&ft:locale=en-US)**

With Hardware Asset Management version 14.0.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Hardware Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Hardware Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Hardware Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Hardware Asset Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Hardware Asset Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Hardware Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Hardware Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Hardware Asset Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Hardware Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Hardware Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Benefit from enhanced Asset Attestation features, including a guided attestation creation process, a mobile-friendly interface for confirming assets, and automated remediation tasks to address non-compliant assets.
-   Achieve real-time tracking of assets that are in transit and maintain asset data accuracy by enabling employees to confirm receipt of assets through the Employee Center portal.
-   Receive shipment assets at a stockroom from any workflow through the streamlined and unified receiving process.
-   Track asset movement from the receiving bay to an aisle and space in the stockroom using the Asset put away task.
-   Evaluate how effectively your assets are functioning and being used through reports based on asset key performance indicators in the Asset analytics view. Also, manage supply and demand in your stockrooms effectively with inventory demand reports.

 See [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)- Gain real-time visibility into critical asset data through generative AI-driven asset analysis summaries.

 Australia Patch 0

-   Gain insight into the approximated life-cycle dates for hardware and consumable products.
-   Streamline inventory asset management with the expanded and efficient inventory auditing process.
-   Streamline and improve the asset management process for retired assets with the expanded asset disposal workflow.
-   Streamlined Advanced Shipment \(ASN\) import process with support for users with specific functional roles.
-   Save time and effort by copying a model from the Content lookup portal to create a record in your ServiceNow instance.

 See [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


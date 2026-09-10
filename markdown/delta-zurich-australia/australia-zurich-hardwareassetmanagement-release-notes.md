---
title: Combined Hardware Asset Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Hardware Asset Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-hardwareassetmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
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

-   **Upgrade information**
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
    -   A new system property, **sn\_itam\_restrict\_asset\_read**, introduced in Zurich Patch 12, controls read access to the Asset \[alm\_asset\] table and its child tables for users with only the snc\_internal role. When set to **true**, these users can only read asset records assigned to them or where they are referenced in fields such as Reserved for, Managed by, or Owned by. Users with any additional role retain full read access. By default, this property is set to **false**.

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**
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
    -   A new system property, **sn\_itam\_restrict\_asset\_read**, introduced in Australia Patch 5, controls read access to the Asset \[alm\_asset\] table and its child tables for users with only the snc\_internal role. When set to **true**, these users can only read asset records assigned to them or where they are referenced in fields such as Reserved for, Managed by, or Owned by. Users with any additional role retain full read access. By default, this property is set to **false**.

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

-   **[Hardware Asset Management installation from Product Hub](https://www.servicenow.com/docs/access?context=product-hub-for-ham&family=zurich&ft:locale=en-US)**

Install Hardware Asset Management and dependent applications from the Product Hub, the central location to view and manage all applications included in your subscription.

-   **[Set up Hardware Asset Management using the Configuration Console](https://www.servicenow.com/docs/access?context=config-console-ham&family=zurich&ft:locale=en-US)**

Streamline your asset management setup by configuring all Hardware Asset Management settings from a single location using the Configuration Console. Set up users, roles, asset lifecycle, inventory, asset integrations, and generative AI skills. You can also use the AI conversational interface to configure groups, users, and content service setup.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Manage your assets with comprehensive and real-time data](https://www.servicenow.com/docs/access?context=generate-asset-analysis-now-assist-ham&family=australia&ft:locale=en-US)**

View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


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

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Renamed the Pick task required field in the Stockroom details form](https://www.servicenow.com/docs/access?context=enable-pick-task-for-stockroom-ham&family=zurich&ft:locale=en-US)**

The **Pick task required** field in the Stockroom details form has been renamed **Warehouse tasks required**. This field supports enabling both the Asset put away task and the Asset pick task for the stockroom in the Hardware Asset Workspace.

-   **[Stage status for the Transfer Order and Transfer Order Line flow](https://www.servicenow.com/docs/access?context=transfer-orders-for-am&family=zurich&ft:locale=en-US)**

The stage status text in the **Stage** column for the Transfer Order and Transfer Order Line in the Hardware Asset Workspace Core UI has been updated. When a stage is completed and the next stage hasn’t yet begun in the asset transfer process, the revised status is displayed as **Completed-next stage initiated** instead of **In progress**. When a stage isn’t yet begun in the asset transfer process, the revised status is displayed as **Pending not started** instead of **Pending-has not started**. These changes accurately reflect the current action in the asset transfer process and enhances the user experience.

-   **[Asset attestation playbook](https://www.servicenow.com/docs/access?context=create-attestation-using-playbook&family=zurich&ft:locale=en-US)**

The **New** button on the Asset attestation tab opens a playbook instead of the attestation form to create an asset attestation.

-   **[Receive asset button on the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&family=zurich&ft:locale=en-US)**

On the Employee Center portal, assets assigned to you that are in transit display a **Receive asset** button to confirm you have received them.

-   **[Stock orders and Transfer orders tabs for stock rules](https://www.servicenow.com/docs/access?context=t_CreateAStockRule&family=zurich&ft:locale=en-US)**

The **Stock Orders** tab on a stock rule shows all the stock orders that were created using that specific stock rule. The **Transfer Orders** tab on a stock rule lists all the transfer orders that were generated using that particular stock rule.

-   **[Inventory availability tab on the asset form](https://www.servicenow.com/docs/access?context=identify-inventory-availability-ham&family=zurich&ft:locale=en-US)**

The **Inventory availability** tab on the asset form lists all available replacement assets or their substitutes in local and remote stockrooms. The **Purchase lead time** column displays the average number of days that it would take to procure a new asset through a new purchase order.

-   **[Asset performance dashboard in the Asset analytics view](https://www.servicenow.com/docs/access?context=asset-analytics-view&family=zurich&ft:locale=en-US)**

The Asset performance dashboard in the Asset analytics view of the Hardware Asset Workspace includes scorecards for Availability, Mean time to repair device \(MTTR\), and Mean time between failures \(MTBF\).

The Asset availability and related KPIs report and the Asset task time summary report are displayed in the contextual sidebar of the asset form.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


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

-   Procurement Process Flow – Hardware
-   Procurement Process Flow – Mobile
-   Procurement Process Flow - Default
-   Transfer Order
-   Transfer Order Line
-   Source Request
-   Contract Approval

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

-   **Activation information**

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)- ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Hardware Asset Management \(HAM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)- Prepare for Now LLM Service to be deprecated in a future release.

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


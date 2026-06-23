---
title: Combined Telecommunications Network Inventory release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Telecommunications Network Inventory from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-telecommunicationsnetworkinventory-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Network Inventory release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Telecommunications Network Inventory from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Network Inventory release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Network Inventory to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

If you are an existing user of previous releases, both legacy and new product models will be available in the Network Inventory Workspace menu after upgrading to Xanadu. To rectify this issue, you must migrate your legacy product model data to the new product model tables in your current instance. For more details about the procedure, see [KB1695167](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695167).

</td></tr><tr><td>

Yokohama

</td><td>

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&family=xanadu&ft:locale=en-US)**

Gain visibility of your data centers infrastructure through advanced rack and cabinet insights. Edit a rack or cabinet to add, reserve, move, and remove any equipment. This enables you to create equipment from the rack or cabinet view.

-   **[Revise a configuration item](https://www.servicenow.com/docs/access?context=revise-a-configuration-item&family=xanadu&ft:locale=en-US)**

Perform a comparative validation between the revision and the original connections to identify any changes between them.

-   **[Import Models and Templates](https://www.servicenow.com/docs/access?context=import-models-and-templates&family=xanadu&ft:locale=en-US)**

Import the models and templates from an external system via XLS template.

-   **[Visualization of circuits](https://www.servicenow.com/docs/access?context=unified-map-view-of-connection-elements&family=xanadu&ft:locale=en-US)**

Provide a visualization of the circuit and its underlying connection elements on a dedicated window. View the revisions and protection paths of a logical connection, and selectively collapse expanded layers instead of collapsing the entire structure.

-   **[Create a cable record by using design and assign](https://www.servicenow.com/docs/access?context=create-cable-record-using-design-assign&family=xanadu&ft:locale=en-US)**

Instantiate cables and associated strands using a cable template.

-   **[Modify a network topology record using design and assign](https://www.servicenow.com/docs/access?context=modify-network-topology-record-design-assign&family=xanadu&ft:locale=en-US)**

Modify a network topology for adding or removing the nodes and edges by using a new change model.

-   **[Create capacity function](https://www.servicenow.com/docs/access?context=create-capacity-function&family=xanadu&ft:locale=en-US)**

Identify and prioritize the capacity function by using the category and order attributes. Access the capacity management forms from the Workspace lists view.

-   **[Network Inventory Workspace](https://www.servicenow.com/docs/access?context=exploring-network-inventory-workspace&family=xanadu&ft:locale=en-US)**

View your and your team's work in the new landing page.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Design and assign your network services](https://www.servicenow.com/docs/access?context=design-assign-playbook&family=yokohama&ft:locale=en-US)**

Create and configure playbooks for design and assign a configuration item. The Design and Assign playbook provides step-by-step guidance for designing a network service. Use the playbook to complete guided activities to instantiate a network inventory record.

-   **[Design and Assign function for logical connections](https://www.servicenow.com/docs/access?context=design-logical-connection-design-assign-playbook&family=yokohama&ft:locale=en-US)**

Use the Design and Assign playbook to instantiate a logical connection and its associated connection elements. Once each activity completes, view the circuit map to visualize the logical connection elements.

-   **[Visualization of geo map](https://www.servicenow.com/docs/access?context=visualization-map&family=yokohama&ft:locale=en-US)**

Use the Network site map to view the geographical location of your network sites and the information such as site details, connectivity, and capacity.

-   **[Creating an inventory template for a logical composite](https://www.servicenow.com/docs/access?context=creating-inventory-template-logical-composite&family=yokohama&ft:locale=en-US)**

Instantiate a logical composite record and associated equipment and racks using a logical composite template.

-   **[Add an equipment or rack to logical composite](https://www.servicenow.com/docs/access?context=add-equipment-rack-logical-composite&family=yokohama&ft:locale=en-US)**

Add equipment or rack to a logical composite using a change model.

-   **[Remove an equipment or rack from logical composite](https://www.servicenow.com/docs/access?context=remove-equipment-rack-logical-composite&family=yokohama&ft:locale=en-US)**

Remove a rack or equipment from a logical composite using a change model.

-   **[Create an equipment record by using design and assign](https://www.servicenow.com/docs/access?context=create-equipment-record-design-and-assign&family=yokohama&ft:locale=en-US)**

Create a change request for an equipment record from the All Equipment list view using the **Create equipment** UI action.

-   **[Import models and templates in JSON format](https://www.servicenow.com/docs/access?context=import-models-templates-json&family=yokohama&ft:locale=en-US)**

Create an import request to import your collection of models and templates in JSON format.

-   **[Export hierarchy of models and templates](https://www.servicenow.com/docs/access?context=export-hierarchy-of-models-and-template&family=yokohama&ft:locale=en-US)**

Export the hierarchy and all related records of a model or inventory template in JSON format.

-   **[Managing your network functions](https://www.servicenow.com/docs/access?context=services&family=yokohama&ft:locale=en-US)**

The xNF and xNF instances records are added in the Inventory menu and retained the Services menu for application services.

-   **[Create a telephone infrastructure](https://www.servicenow.com/docs/access?context=telephone_block_telephone_number_and_telephone_number&family=yokohama&ft:locale=en-US)**

Supports all types of telephone numbers.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Telecommunications Network Inventory features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&family=xanadu&ft:locale=en-US)**

The new rack visualization provides new power, weight, and capacity metrics.

-   **[Creating your inventory models](https://www.servicenow.com/docs/access?context=creating-your-inventory-models&family=xanadu&ft:locale=en-US)**

The legacy product model tables are deprecated and they are migrated to Enterprise product model app.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Telecommunications Network Inventory features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Telecommunications Network Inventory features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Telecommunications Network Inventory application is a ServiceNow AI Platform feature that is available with activation of the Network Inventory Advanced plugin \(sn\_ni\_adv\). For details, see [Install Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Telecommunications Network Inventory by requesting it from the ServiceNow Store. For details about the installation procedure, see [Install Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Telecommunications Network Inventory, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Provide a visualization of the circuit and its underlying connection elements with revisions and protection paths on a dedicated canvas.
-   Get enhanced rack and cabinet visualization capabilities, including viewing, editing, and updating features, along with new KPIs for better capacity planning and prioritization.
-   Archive current configurations while operationalizing a planned revision and compare them with original connections to detect changes.
-   Export equipment models and templates along with related hardware to an Excel data source, and import them to another ServiceNow instance.
-   TMF conformance for TMF 639 Resource Inventory API.

 See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   View the geographical location and the details of your network site
-   Design and assign a configuration item using a playbook and add custom states to a Change model.
-   Define a logical composite to track and manage its CI.
-   Import and export your collection of models and templates in JSON format.
-   Enable Deny ACL to ensure the compliance with the enhanced security model.

 See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)


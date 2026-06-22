---
title: Combined Telecommunications Network Inventory release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Telecommunications Network Inventory from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-telecommunicationsnetworkinventory-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Network Inventory release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Telecommunications Network Inventory from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Network Inventory release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Network Inventory to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

If you are an existing user of previous releases, both legacy and new product models will be available in the Network Inventory Workspace menu after upgrading to Xanadu. To rectify this issue, you must migrate your legacy product model data to the new product model tables in your current instance. For more details about the procedure, see [KB1695167](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695167).

</td></tr><tr><td>

Yokohama

</td><td>

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Visualization of rack](https://servicenow-staging.fluidtopics.net/access?context=visualization-of-rack&family=washingtondc&ft:locale=en-US)**

Visualize your rack details such as placement of equipment at the front or rear, available and occupied rack slots, occupied equipment or shelf details.

-   **[Revision, operationalization, and decommission of a Configuration Item](https://servicenow-staging.fluidtopics.net/access?context=revision-of-a-confiuguration-item&family=washingtondc&ft:locale=en-US)**

Revise a CI to make changes, including modifications to related tables like attributes, connections, and relations. Operationalization enables you to merge these changes with the original CI, while decommissioning lets you retire or remove the CI from operation.

-   **[Visualization of network topology](https://servicenow-staging.fluidtopics.net/access?context=visualization-of-topology&family=washingtondc&ft:locale=en-US)**

Use the network topology view to see nodes \(equipment\), edges \(connections\), and termination points \(interfaces\) in your network to understand how they are organized and connected. You can visualize multiple topologies simultaneously using the search option.

-   **[Capacity management](https://servicenow-staging.fluidtopics.net/access?context=capacity-management-reporting&family=washingtondc&ft:locale=en-US)**

Use capacity management to calculate and report the capacity of your network assets. This involves calculating the maximum, occupied, and available resources like ports, slots, or racks in your telecommunication network using functions and metrics.

-   **[Inventory management view](https://servicenow-staging.fluidtopics.net/access?context=inventory-management-view&family=washingtondc&ft:locale=en-US)**

Check the Inventory Management view to understand inventory details, including the total count of equipment grouped by model, manufacturer, and life cycle state. Additionally, you can see the availability of racks, ports, and slots within a network site.

-   **[Define the cable details](https://servicenow-staging.fluidtopics.net/access?context=define-cable&family=washingtondc&ft:locale=en-US)**

Define the following network inventory instances.

    -   Cable - Optical fiber cables link sites with open endpoints, indicating that they don't terminate directly to equipment.
    -   Strand - Strands are the individual wires within the cables.
    -   Channel - Channelization involves sub-rating the available bandwidth into smaller bandwidths.
-   **[Create a change request from Network Inventory Workspace](https://servicenow-staging.fluidtopics.net/access?context=create_a_change_request_in_tni&family=washingtondc&ft:locale=en-US)**

Use Telecommunications Network Inventory \(TNI\) design assign to modify physical and logical connection endpoints details, as well as add or remove members of a Link Aggregation Group \(LAG\).


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Visualization of a rack or cabinet](https://servicenow-staging.fluidtopics.net/access?context=visualization-of-rack&family=xanadu&ft:locale=en-US)**

Gain visibility of your data centers infrastructure through advanced rack and cabinet insights. Edit a rack or cabinet to add, reserve, move, and remove any equipment. This enables you to create equipment from the rack or cabinet view.

-   **[Revise a configuration item](https://servicenow-staging.fluidtopics.net/access?context=revise-a-configuration-item&family=xanadu&ft:locale=en-US)**

Perform a comparative validation between the revision and the original connections to identify any changes between them.

-   **[Import Models and Templates](https://servicenow-staging.fluidtopics.net/access?context=import-models-and-templates&family=xanadu&ft:locale=en-US)**

Import the models and templates from an external system via XLS template.

-   **[Visualization of circuits](https://servicenow-staging.fluidtopics.net/access?context=unified-map-view-of-connection-elements&family=xanadu&ft:locale=en-US)**

Provide a visualization of the circuit and its underlying connection elements on a dedicated window. View the revisions and protection paths of a logical connection, and selectively collapse expanded layers instead of collapsing the entire structure.

-   **[Create a cable record by using design and assign](https://servicenow-staging.fluidtopics.net/access?context=create-cable-record-using-design-assign&family=xanadu&ft:locale=en-US)**

Instantiate cables and associated strands using a cable template.

-   **[Modify a network topology record using design and assign](https://servicenow-staging.fluidtopics.net/access?context=modify-network-topology-record-design-assign&family=xanadu&ft:locale=en-US)**

Modify a network topology for adding or removing the nodes and edges by using a new change model.

-   **[Create capacity function](https://servicenow-staging.fluidtopics.net/access?context=create-capacity-function&family=xanadu&ft:locale=en-US)**

Identify and prioritize the capacity function by using the category and order attributes. Access the capacity management forms from the Workspace lists view.

-   **[Network Inventory Workspace](https://servicenow-staging.fluidtopics.net/access?context=exploring-network-inventory-workspace&family=xanadu&ft:locale=en-US)**

View your and your team's work in the new landing page.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Design and assign your network services](https://servicenow-staging.fluidtopics.net/access?context=design-assign-playbook&family=yokohama&ft:locale=en-US)**

Create and configure playbooks for design and assign a configuration item. The Design and Assign playbook provides step-by-step guidance for designing a network service. Use the playbook to complete guided activities to instantiate a network inventory record.

-   **[Design and Assign function for logical connections](https://servicenow-staging.fluidtopics.net/access?context=design-logical-connection-design-assign-playbook&family=yokohama&ft:locale=en-US)**

Use the Design and Assign playbook to instantiate a logical connection and its associated connection elements. Once each activity completes, view the circuit map to visualize the logical connection elements.

-   **[Visualization of geo map](https://servicenow-staging.fluidtopics.net/access?context=visualization-map&family=yokohama&ft:locale=en-US)**

Use the Network site map to view the geographical location of your network sites and the information such as site details, connectivity, and capacity.

-   **[Creating an inventory template for a logical composite](https://servicenow-staging.fluidtopics.net/access?context=creating-inventory-template-logical-composite&family=yokohama&ft:locale=en-US)**

Instantiate a logical composite record and associated equipment and racks using a logical composite template.

-   **[Add an equipment or rack to logical composite](https://servicenow-staging.fluidtopics.net/access?context=add-equipment-rack-logical-composite&family=yokohama&ft:locale=en-US)**

Add equipment or rack to a logical composite using a change model.

-   **[Remove an equipment or rack from logical composite](https://servicenow-staging.fluidtopics.net/access?context=remove-equipment-rack-logical-composite&family=yokohama&ft:locale=en-US)**

Remove a rack or equipment from a logical composite using a change model.

-   **[Create an equipment record by using design and assign](https://servicenow-staging.fluidtopics.net/access?context=create-equipment-record-design-and-assign&family=yokohama&ft:locale=en-US)**

Create a change request for an equipment record from the All Equipment list view using the **Create equipment** UI action.

-   **[Import models and templates in JSON format](https://servicenow-staging.fluidtopics.net/access?context=import-models-templates-json&family=yokohama&ft:locale=en-US)**

Create an import request to import your collection of models and templates in JSON format.

-   **[Export hierarchy of models and templates](https://servicenow-staging.fluidtopics.net/access?context=export-hierarchy-of-models-and-template&family=yokohama&ft:locale=en-US)**

Export the hierarchy and all related records of a model or inventory template in JSON format.

-   **[Managing your network functions](https://servicenow-staging.fluidtopics.net/access?context=services&family=yokohama&ft:locale=en-US)**

The xNF and xNF instances records are added in the Inventory menu and retained the Services menu for application services.

-   **[Create a telephone infrastructure](https://servicenow-staging.fluidtopics.net/access?context=telephone_block_telephone_number_and_telephone_number&family=yokohama&ft:locale=en-US)**

Supports all types of telephone numbers.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create logical connection record](https://servicenow-staging.fluidtopics.net/access?context=create-logical-connection-record-design-assign-playbook&family=zurich&ft:locale=en-US)**

Logical interfaces created are now automatically related to their corresponding cards or parent equipment. This enhancement ensures consistency across systems and helps prevent duplicate CI creation by improving the alignment between logical and physical interfaces.


-   **[Visualize your network infrastructure](https://servicenow-staging.fluidtopics.net/access?context=data-center-inventory-management&family=zurich&ft:locale=en-US)**

Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology. The following roles are introduced to manage datacenter infrastructure.

    -   DC Floor Designer \(sn\_ni\_core.dc\_floor\_designer\) – Design floor layout in Map Studio.
    -   DC Ops Agent \(sn\_ni\_core.dc\_ops\_agent\) – Oversee the operations of the data center floor.
    -   DC Ops Viewer \(sn\_ni\_core.dc\_ops\_viewer\) – View the Network Inventory Workspace and its components.
-   **[Floor map](https://servicenow-staging.fluidtopics.net/access?context=visualization-floor-maps&family=zurich&ft:locale=en-US)**

Use the floor map to view the layout of your datacenter infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.

-   **[Geo map](https://servicenow-staging.fluidtopics.net/access?context=visualization-map&family=zurich&ft:locale=en-US)**

Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.

-   **[Manage datacenter floor map](https://servicenow-staging.fluidtopics.net/access?context=create-floor-map-data-center&family=zurich&ft:locale=en-US)**

Upload and manage your datacenter map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.

-   **[Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=service-operations-workspace-network-inventory&family=zurich&ft:locale=en-US)**

Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.

-   **[Capacity management](https://servicenow-staging.fluidtopics.net/access?context=capacity-management-reporting&family=zurich&ft:locale=en-US)**

Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the datacenter floor map to monitor overall health and take appropriate action.

-   **[Collect operational values for datacenter](https://servicenow-staging.fluidtopics.net/access?context=enter-operational-values-data-center&family=zurich&ft:locale=en-US)**

Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for datacenter performance tracking.

-   **[Define the datacenter details](https://servicenow-staging.fluidtopics.net/access?context=define-data-center-details&family=zurich&ft:locale=en-US)**

Define your datacenter record to view the location-specific attributes for each datacenter, including the campus, buildings, and floors where your network asset is located.

-   **[Define the power circuit details](https://servicenow-staging.fluidtopics.net/access?context=define-power-circuit-details&family=zurich&ft:locale=en-US)**

Define the power circuit record to represent the electrical pathway that delivers power within a data center.

-   **[Define the facility hardware details](https://servicenow-staging.fluidtopics.net/access?context=define-facility-hardware-details&family=zurich&ft:locale=en-US)**

Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.

-   **[Create a facility model](https://servicenow-staging.fluidtopics.net/access?context=create-facility-model&family=zurich&ft:locale=en-US)**

Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.

-   **[Create a equipment record](https://servicenow-staging.fluidtopics.net/access?context=create-equipment-record-design-and-assign&family=zurich&ft:locale=en-US)**

View datacenter records listed in the Equipment task attribute form.

-   **[Define the network interface details](https://servicenow-staging.fluidtopics.net/access?context=define-tni-interfaces&family=zurich&ft:locale=en-US)**

Add **Wavelength** attribute to the Network Interface form and **Port position** attribute to Interface Model form.

-   **[Create an equipment holder model](https://servicenow-staging.fluidtopics.net/access?context=create-equipment-holder-models&family=zurich&ft:locale=en-US)**

Added **RU numbering direction** attribute to define the numbering sequence of rack units in the Rack view.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Telecommunications Network Inventory features.

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

-   **[Visualization of a rack or cabinet](https://servicenow-staging.fluidtopics.net/access?context=visualization-of-rack&family=xanadu&ft:locale=en-US)**

The new rack visualization provides new power, weight, and capacity metrics.

-   **[Creating your inventory models](https://servicenow-staging.fluidtopics.net/access?context=creating-your-inventory-models&family=xanadu&ft:locale=en-US)**

The legacy product model tables are deprecated and they are migrated to Enterprise product model app.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Define network service instance details](https://servicenow-staging.fluidtopics.net/access?context=create_application_services&family=zurich&ft:locale=en-US)**

**xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://servicenow-staging.fluidtopics.net/access?context=create_business_applications&family=zurich&ft:locale=en-US)**

**xNF** is renamed to **Network Function**.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Telecommunications Network Inventory features or functionality were removed.

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

Between your current release family and Zurich, some Telecommunications Network Inventory features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The Telecommunications Network Inventory application is a ServiceNow AI Platform feature that is available with activation of the Network Inventory Advanced plugin \(sn\_ni\_adv\). For details, see [Install Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=installing-telecommunications-network-inventory&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

The Telecommunications Network Inventory application is a ServiceNow AI Platform feature that is available with activation of the Network Inventory Advanced plugin \(sn\_ni\_adv\). For details, see [Install Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=installing-telecommunications-network-inventory&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Telecommunications Network Inventory by requesting it from the ServiceNow Store. For details about the installation procedure, see [Install Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=installing-telecommunications-network-inventory&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install TNI](https://servicenow-staging.fluidtopics.net/access?context=installing-telecommunications-network-inventory&family=zurich&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

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

-   You must install Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin to view incident and alert details.
-   You must install the Indoor Mapping plugin \(sn\_map\_core\) to create and manage floor maps for data centers.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

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

Review details on accessibility information for Telecommunications Network Inventory, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Telecommunications Network Inventory we have noted them here.

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

If there are specific highlight considerations for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Visualise the front and rear view of a rack with occupied equipment and shelf along with rack unit utilization KPI.
-   Use Revision to modify, operationalize, and decommission a connection. Use the TNI design assign to modify connections, such as adding or removing endpoints with or without revisions.
-   View a visual representation of your network topologies, including equipment, connections, and interfaces, to understand how everything is organized and connected.
-   Calculate the capacity of physical entities in your network by using the capacity management feature. Check the Inventory management view to get the network inventory details such as equipment information and availability of racks, ports, and slots at a network site.
-   Define your cables, strands, channels to track and manage the configuration items \(CI\).

 See Telecommunications Network Inventory for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Provide a visualization of the circuit and its underlying connection elements with revisions and protection paths on a dedicated canvas.
-   Get enhanced rack and cabinet visualization capabilities, including viewing, editing, and updating features, along with new KPIs for better capacity planning and prioritization.
-   Archive current configurations while operationalizing a planned revision and compare them with original connections to detect changes.
-   Export equipment models and templates along with related hardware to an Excel data source, and import them to another ServiceNow instance.
-   TMF conformance for TMF 639 Resource Inventory API.

 See [Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=telecom-network-inventory&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   View the geographical location and the details of your network site
-   Design and assign a configuration item using a playbook and add custom states to a Change model.
-   Define a logical composite to track and manage its CI.
-   Import and export your collection of models and templates in JSON format.
-   Enable Deny ACL to ensure the compliance with the enhanced security model.

 See [Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=telecom-network-inventory&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   The Logical interfaces \(such as VLANs\) and physical interfaces \(such as Gigabit Ethernet ports\) are now related to their parent equipment or card to help prevent duplicate CI creation.
-   Get converged experience for Network Inventory workflows using Service Operations Workspace.
-   Upload and manage CAD/PNG of floor maps to view the datacenter layout with physical asset placements over the floor.
-   Ingest operational data and show time series metrics on the datacenter floor map to monitor health.
-   Capture an inventory of operational facilities and define their relationships to respective network hardware such as the power chain.

 See [Telecommunications Network Inventory](https://servicenow-staging.fluidtopics.net/access?context=telecom-network-inventory&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)


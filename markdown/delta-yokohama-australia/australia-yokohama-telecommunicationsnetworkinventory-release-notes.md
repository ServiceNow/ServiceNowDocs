---
title: Combined Telecommunications Network Inventory release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Telecommunications Network Inventory from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-telecommunicationsnetworkinventory-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Network Inventory release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Telecommunications Network Inventory from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Network Inventory release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Network Inventory to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create logical connection record](https://www.servicenow.com/docs/access?context=create-logical-connection-record-design-assign-playbook&family=zurich&ft:locale=en-US)**

Logical interfaces created are now automatically related to their corresponding cards or parent equipment. This enhancement ensures consistency across systems and helps prevent duplicate CI creation by improving the alignment between logical and physical interfaces.


-   **[Visualize your network infrastructure](https://www.servicenow.com/docs/access?context=data-center-inventory-management&family=zurich&ft:locale=en-US)**

Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology. The following roles are introduced to manage datacenter infrastructure.

    -   DC Floor Designer \(sn\_ni\_core.dc\_floor\_designer\) – Design floor layout in Map Studio.
    -   DC Ops Agent \(sn\_ni\_core.dc\_ops\_agent\) – Oversee the operations of the data center floor.
    -   DC Ops Viewer \(sn\_ni\_core.dc\_ops\_viewer\) – View the Network Inventory Workspace and its components.
-   **[Floor map](https://www.servicenow.com/docs/access?context=visualization-floor-maps&family=zurich&ft:locale=en-US)**

Use the floor map to view the layout of your datacenter infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.

-   **[Geo map](https://www.servicenow.com/docs/access?context=visualization-map&family=zurich&ft:locale=en-US)**

Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.

-   **[Manage datacenter floor map](https://www.servicenow.com/docs/access?context=create-floor-map-data-center&family=zurich&ft:locale=en-US)**

Upload and manage your datacenter map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=service-operations-workspace-network-inventory&family=zurich&ft:locale=en-US)**

Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.

-   **[Capacity management](https://www.servicenow.com/docs/access?context=capacity-management-reporting&family=zurich&ft:locale=en-US)**

Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the datacenter floor map to monitor overall health and take appropriate action.

-   **[Collect operational values for datacenter](https://www.servicenow.com/docs/access?context=enter-operational-values-data-center&family=zurich&ft:locale=en-US)**

Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for datacenter performance tracking.

-   **[Define the datacenter details](https://www.servicenow.com/docs/access?context=define-data-center-details&family=zurich&ft:locale=en-US)**

Define your datacenter record to view the location-specific attributes for each datacenter, including the campus, buildings, and floors where your network asset is located.

-   **[Define the power circuit details](https://www.servicenow.com/docs/access?context=define-power-circuit-details&family=zurich&ft:locale=en-US)**

Define the power circuit record to represent the electrical pathway that delivers power within a data center.

-   **[Define the facility hardware details](https://www.servicenow.com/docs/access?context=define-facility-hardware-details&family=zurich&ft:locale=en-US)**

Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.

-   **[Create a facility model](https://www.servicenow.com/docs/access?context=create-facility-model&family=zurich&ft:locale=en-US)**

Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.

-   **[Create a equipment record](https://www.servicenow.com/docs/access?context=create-equipment-record-design-and-assign&family=zurich&ft:locale=en-US)**

View datacenter records listed in the Equipment task attribute form.

-   **[Define the network interface details](https://www.servicenow.com/docs/access?context=define-tni-interfaces&family=zurich&ft:locale=en-US)**

Add **Wavelength** attribute to the Network Interface form and **Port position** attribute to Interface Model form.

-   **[Create an equipment holder model](https://www.servicenow.com/docs/access?context=create-equipment-holder-models&family=zurich&ft:locale=en-US)**

Added **RU numbering direction** attribute to define the numbering sequence of rack units in the Rack view.


</td></tr><tr><td>

Australia

</td><td>

Australia Early Availability

-   **[Remote Hands Request Management](https://www.servicenow.com/docs/access?context=remote-hands-request-management&family=australia&ft:locale=en-US)**

Enable your customers to request services such as power usage enquiries, equipment installation, equipment restarts, and more by connecting with onsite operations agents at your facility. Securely store your customer requests in the Remote Hands Case table, with role-based access controls. View an auto-generated summary of your requests for quick reference.


-   **[Remote hands case record](https://www.servicenow.com/docs/access?context=generate-summary-for-remote-hands-case-record&family=australia&ft:locale=en-US)**

Remote Hands Request Summarization generates contextual summary of a Remote Hands case by combining current case data with insights from similar historical cases, using information submitted by the DCIM user through the CSM portal.


 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   **[IP address management](https://www.servicenow.com/docs/access?context=ip-address-management&family=australia&ft:locale=en-US)**

Multi-layer nested IP Subnetworks with CIDR validation: You can now create IP Subnetworks within IP Subnetworks, supporting recursive nesting for both IPv4 and IPv6. When creating a subnetwork at any level, the system validates that the CIDR is correctly formatted, falls within the parent's range, is more specific than the parent, and is unique within the parent.


-   **[Naming patterns in inventory templates](https://www.servicenow.com/docs/access?context=naming-patterns-in-inventory-templates&family=australia&ft:locale=en-US)**

Author patterns from a variable library with real-time validation, verify resolved names across the full template hierarchy from a new Overview tab at design time, and add custom validation rules.


-   **[Assign user role](https://www.servicenow.com/docs/access?context=telecom-inventory-roles&family=australia&ft:locale=en-US)**

Standard ServiceNow platform roles no longer have read access to specific TNI tables. This change affects both new installations and upgrades.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Telecommunications Network Inventory features.

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

-   **[Define network service instance details](https://www.servicenow.com/docs/access?context=create_application_services&family=zurich&ft:locale=en-US)**

**xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://www.servicenow.com/docs/access?context=create_business_applications&family=zurich&ft:locale=en-US)**

**xNF** is renamed to **Network Function**.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Telecommunications Network Inventory features or functionality were removed.

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

Between your current release family and Australia, some Telecommunications Network Inventory features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Telecommunications Network Inventory.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Telecommunications Network Inventory by requesting it from the ServiceNow Store. For details about the installation procedure, see [Install Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install TNI](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&family=zurich&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install TNI](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&family=australia&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

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

-   You must install Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin to view incident and alert details.
-   You must install the Indoor Mapping plugin \(sn\_map\_core\) to create and manage floor maps for data centers.

</td></tr><tr><td>

Australia

</td><td>

You must install Customer service install base management \(sn\_cs\_sm\_request\) plugin and Remote Hands plugin from the ServiceNow Store to use the Remote Hands feature.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Telecommunications Network Inventory we have noted them here.

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

Review details on accessibility information for Telecommunications Network Inventory, such as specific requirements or compliance levels.

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

Improved overall accessibility across Network Inventory application, focusing on keyboard navigation, screen readers, zoom levels, colour contrast, and text spacing.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Telecommunications Network Inventory we have noted them here.

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

If there are specific highlight considerations for Telecommunications Network Inventory we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   View the geographical location and the details of your network site
-   Design and assign a configuration item using a playbook and add custom states to a Change model.
-   Define a logical composite to track and manage its CI.
-   Import and export your collection of models and templates in JSON format.
-   Enable Deny ACL to ensure the compliance with the enhanced security model.

 See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   The Logical interfaces \(such as VLANs\) and physical interfaces \(such as Gigabit Ethernet ports\) are now related to their parent equipment or card to help prevent duplicate CI creation.
-   Get converged experience for Network Inventory workflows using Service Operations Workspace.
-   Upload and manage CAD/PNG of floor maps to view the datacenter layout with physical asset placements over the floor.
-   Ingest operational data and show time series metrics on the datacenter floor map to monitor health.
-   Capture an inventory of operational facilities and define their relationships to respective network hardware such as the power chain.

 See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Australia Early Availability

-   Enable customers to request services for equipment housed in your facility using Remote Hands.
-   View a concise summary of Remote Hands Request

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Create IP addresses directly within an IP subnetwork.
-   Define reusable naming patterns using the new TNI CI Naming application with real-time validation, hierarchical name construction, and interactive preview before applying to the inventory.
-   Access control update — TNI table permissions

 See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


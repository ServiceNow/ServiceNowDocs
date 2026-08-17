---
title: Telecommunications Network Inventory release notes
description: The ServiceNow Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services. Telecommunications Network Inventory was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Telecommunications Network Inventory release notes

The ServiceNow® Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services. Telecommunications Network Inventory was enhanced and updated in the Zurich release.

## Telecommunications Network Inventory highlights for the Zurich release

-   The Logical interfaces \(such as VLANs\) and physical interfaces \(such as Gigabit Ethernet ports\) are now related to their parent equipment or card to help prevent duplicate CI creation.
-   Get converged experience for Network Inventory workflows using Service Operations Workspace.
-   Upload and manage CAD/PNG of floor maps to view the datacenter layout with physical asset placements over the floor.
-   Ingest operational data and show time series metrics on the datacenter floor map to monitor health.
-   Capture an inventory of operational facilities and define their relationships to respective network hardware such as the power chain.

See [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/telecom-network-inventory.md) for more information.

**Important:** Telecommunications Network Inventory is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Create a logical connection record using the Design and Assign function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-logical-connection-record-design-assign-playbook.md)**

    Logical interfaces created are now automatically related to their corresponding cards or parent equipment. This enhancement ensures consistency across systems and helps prevent duplicate CI creation by improving the alignment between logical and physical interfaces.


-   **[Visualize your network infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/data-center-inventory-management.md)**

    Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology. The following roles are introduced to manage datacenter infrastructure.

    -   DC Floor Designer \(sn\_ni\_core.dc\_floor\_designer\) – Design floor layout in Map Studio.
    -   DC Ops Agent \(sn\_ni\_core.dc\_ops\_agent\) – Oversee the operations of the data center floor.
    -   DC Ops Viewer \(sn\_ni\_core.dc\_ops\_viewer\) – View the Network Inventory Workspace and its components.
-   **[Floor map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/visualization-floor-maps.md)**

    Use the floor map to view the layout of your datacenter infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.

-   **[Geo map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/visualization-map.md)**

    Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.

-   **[Upload and manage floor map for your datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-floor-map-data-center.md)**

    Upload and manage your datacenter map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.

-   **[Service Operations Workspace for TNI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/service-operations-workspace-network-inventory.md)**

    Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.

-   **[Capacity management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/capacity-management-reporting.md)**

    Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the datacenter floor map to monitor overall health and take appropriate action.

-   **[Collect operational values for datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/enter-operational-values-data-center.md)**

    Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for datacenter performance tracking.

-   **[Define the datacenter details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-data-center-details.md)**

    Define your datacenter record to view the location-specific attributes for each datacenter, including the campus, buildings, and floors where your network asset is located.

-   **[Define the power circuit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-power-circuit-details.md)**

    Define the power circuit record to represent the electrical pathway that delivers power within a data center.

-   **[Define the facility hardware details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-facility-hardware-details.md)**

    Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.

-   **[Create a facility model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-facility-model.md)**

    Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.

-   **[Create an equipment record by using design and assign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-equipment-record-design-and-assign.md)**

    View datacenter records listed in the Equipment task attribute form.

-   **[Define the network interface details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-tni-interfaces.md)**

    Add **Wavelength** attribute to the Network Interface form and **Port position** attribute to Interface Model form.

-   **[Create an equipment holder model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-equipment-holder-models.md)**

    Added **RU numbering direction** attribute to define the numbering sequence of rack units in the Rack view.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Visualize your network infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/data-center-inventory-management.md)**

    The Network Visualization L1 menu is added to the Telecommunications Network Inventory Workspace. The Topology L1 menu has been removed and is available as **Topology** tab within the Network Visualization view.

-   **[Geo map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/visualization-map.md)**

    Network site map L1 menu is removed and repositioned as **Geo map** tab in the Network visualization view.

-   **[Define the power circuit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-power-circuit-details.md)**

    The **Power Circuits** inventory is added.

-   **[Define the facility hardware details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/define-facility-hardware-details.md)**

    The **All Facilities** inventory is added.

-   **[Create a facility model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create-facility-model.md)**

    The **Facility Models** inventory model is added.

-   **[Lists view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/network-inventory-workspace-list-view.md)**

    The **Network site** is renamed to **Site**.


## Changed in this release

-   **[Define network service instance details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create_application_services.md)**

    **xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create_business_applications.md)**

    **xNF** is renamed to **Network Function**.


## Activation information

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/installing-telecommunications-network-inventory.md). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Additional requirements

-   You must install Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin to view incident and alert details.
-   You must install the Indoor Mapping plugin \(sn\_map\_core\) to create and manage floor maps for data centers.

## Related ServiceNow applications and features

-   **[Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/c_ITILConfigurationManagement.md)**

    With the CMDB application, build logical representations of assets, services, and the relationships between them that comprises the infrastructure of your organization. Details about these components are stored in the CMDB, which you can use to monitor the following infrastructure, helping promote integrity, stability, and continuous service operation.

-   **[Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/telecom-media-tech-landing.md)**

    The Order Management for Telecommunications, Media, and Technology \(TMT\) product suite brings together customer care, operations, order management, and partner ecosystems so that service providers can scale their business to capitalize on the fast-growing “everything-as-a-service" opportunity.

-   **[Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/Indoor-mapping.md)**

    The Indoor Mapping Map Studio provides building visualization and wayfinding capabilities to workplace users within a campus, building, floor, and work spaces. Indoor Mapping Map Studio is the interface where you visualize and design your maps to create digitalized interactive locations within workplaces and buildings.

-   **[MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/metricbase.md)**

    The MetricBase application stores time-series data, which is data that is sampled at regular intervals. You can graph the stored data or use it with triggers to execute Workflow Studio flows.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/technology-industry-rn-landing.md)


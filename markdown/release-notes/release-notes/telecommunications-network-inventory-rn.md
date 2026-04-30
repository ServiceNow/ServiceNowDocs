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

See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US) for more information.

**Important:** Telecommunications Network Inventory is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Create a logical connection record using the Design and Assign function](https://www.servicenow.com/docs/access?context=create-logical-connection-record-design-assign-playbook&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Logical interfaces created are now automatically related to their corresponding cards or parent equipment. This enhancement ensures consistency across systems and helps prevent duplicate CI creation by improving the alignment between logical and physical interfaces.


-   **[Visualize your network infrastructure](https://www.servicenow.com/docs/access?context=data-center-inventory-management&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology. The following roles are introduced to manage datacenter infrastructure.

    -   DC Floor Designer \(sn\_ni\_core.dc\_floor\_designer\) – Design floor layout in Map Studio.
    -   DC Ops Agent \(sn\_ni\_core.dc\_ops\_agent\) – Oversee the operations of the data center floor.
    -   DC Ops Viewer \(sn\_ni\_core.dc\_ops\_viewer\) – View the Network Inventory Workspace and its components.
-   **[Floor map](https://www.servicenow.com/docs/access?context=visualization-floor-maps&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Use the floor map to view the layout of your datacenter infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.

-   **[Geo map](https://www.servicenow.com/docs/access?context=visualization-map&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.

-   **[Upload and manage floor map for your datacenter](https://www.servicenow.com/docs/access?context=create-floor-map-data-center&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Upload and manage your datacenter map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.

-   **[Service Operations Workspace for TNI](https://www.servicenow.com/docs/access?context=service-operations-workspace-network-inventory&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.

-   **[Capacity management](https://www.servicenow.com/docs/access?context=capacity-management-reporting&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the datacenter floor map to monitor overall health and take appropriate action.

-   **[Collect operational values for datacenter](https://www.servicenow.com/docs/access?context=enter-operational-values-data-center&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for datacenter performance tracking.

-   **[Define the datacenter details](https://www.servicenow.com/docs/access?context=define-data-center-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Define your datacenter record to view the location-specific attributes for each datacenter, including the campus, buildings, and floors where your network asset is located.

-   **[Define the power circuit details](https://www.servicenow.com/docs/access?context=define-power-circuit-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Define the power circuit record to represent the electrical pathway that delivers power within a data center.

-   **[Define the facility hardware details](https://www.servicenow.com/docs/access?context=define-facility-hardware-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.

-   **[Create a facility model](https://www.servicenow.com/docs/access?context=create-facility-model&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.

-   **[Create an equipment record by using design and assign](https://www.servicenow.com/docs/access?context=create-equipment-record-design-and-assign&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    View datacenter records listed in the Equipment task attribute form.

-   **[Define the network interface details](https://www.servicenow.com/docs/access?context=define-tni-interfaces&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Add **Wavelength** attribute to the Network Interface form and **Port position** attribute to Interface Model form.

-   **[Create an equipment holder model](https://www.servicenow.com/docs/access?context=create-equipment-holder-models&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Added **RU numbering direction** attribute to define the numbering sequence of rack units in the Rack view.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Visualize your network infrastructure](https://www.servicenow.com/docs/access?context=data-center-inventory-management&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    The Network Visualization L1 menu is added to the Telecommunications Network Inventory Workspace. The Topology L1 menu has been removed and is available as **Topology** tab within the Network Visualization view.

-   **[Geo map](https://www.servicenow.com/docs/access?context=visualization-map&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    Network site map L1 menu is removed and repositioned as **Geo map** tab in the Network visualization view.

-   **[Define the power circuit details](https://www.servicenow.com/docs/access?context=define-power-circuit-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    The **Power Circuits** inventory is added.

-   **[Define the facility hardware details](https://www.servicenow.com/docs/access?context=define-facility-hardware-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    The **All Facilities** inventory is added.

-   **[Create a facility model](https://www.servicenow.com/docs/access?context=create-facility-model&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    The **Facility Models** inventory model is added.

-   **[Lists view](https://www.servicenow.com/docs/access?context=network-inventory-workspace-list-view&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    The **Network site** is renamed to **Site**.


## Changed in this release

-   **[Define network service instance details](https://www.servicenow.com/docs/access?context=create_application_services&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    **xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://www.servicenow.com/docs/access?context=create_business_applications&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

    **xNF** is renamed to **Network Function**.


## Activation information

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

-   You must install Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin to view incident and alert details.
-   You must install the Indoor Mapping plugin \(sn\_map\_core\) to create and manage floor maps for data centers.

## Related ServiceNow applications and features

-   **[Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    With the CMDB application, build logical representations of assets, services, and the relationships between them that comprises the infrastructure of your organization. Details about these components are stored in the CMDB, which you can use to monitor the following infrastructure, helping promote integrity, stability, and continuous service operation.

-   **[Telecommunications, Media, and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=telecom-media-tech-landing&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

    The Order Management for Telecommunications, Media, and Technology \(TMT\) product suite brings together customer care, operations, order management, and partner ecosystems so that service providers can scale their business to capitalize on the fast-growing “everything-as-a-service" opportunity.

-   **[Indoor Mapping](https://www.servicenow.com/docs/access?context=Indoor-mapping&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The Indoor Mapping Map Studio provides building visualization and wayfinding capabilities to workplace users within a campus, building, floor, and work spaces. Indoor Mapping Map Studio is the interface where you visualize and design your maps to create digitalized interactive locations within workplaces and buildings.

-   **[MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The MetricBase application stores time-series data, which is data that is sampled at regular intervals. You can graph the stored data or use it with triggers to execute Workflow Studio flows.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)


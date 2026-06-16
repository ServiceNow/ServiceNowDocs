---
title: Network Inventory Advanced release notes
description: Version history for the Network Inventory Advanced application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-network-inventory-advanced.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Network Inventory Advanced release notes

Version history for the Network Inventory Advanced application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.1 - June 2026**
    -   This release delivers major enhancements to IP address management, improves data center design workflows, and includes security and usability fixes.
    -   IP Address Management  - IP address creation against subnetworks — You can now create IP addresses directly against an IP subnetwork, with the ability to enable or disable this behavior as  needed.  - Allocated IP creation from subnets — Allocate and create IP addresses directly from a subnet for a more streamlined workflow.  - Subnetwork uniqueness validation — IP subnetworks are now validated for uniqueness to prevent duplicate or conflicting definitions.  - Improved related lists — Added related lists for IP Subnetworks from the IP Pool table, refined the ordering of allocated-IP related lists, and improved filtering on  the IP Address related list.  - Workspace refinement — Removed the IP Pools list from workspaces where it no longer applies and added new applicability rules for cleaner navigation.
    -   Design &amp; Workflow  - Added a new state transition from Design In Progress to Design Complete to better reflect the data center design lifecycle.  - Fixed the read-only description preset on the Data Center Infrastructure allocation change model.  - Restored the Open Record icon on reference fields within Design &amp; Assign playbook steps.
    -   Security &amp; Platform  - Expanded access control coverage across advanced inventory tables to fully support secure query-range operations.  - Added support for the latest scripting standard \(ECMAScript\) in related-list logic.
    -   Localization &amp; Quality  - Resolved localization issues and applied translation updates.
-   **Version 6.0.1 - March 2026**

    This version have same features as before.

-   **Version 5.1.0 - December 2025**
    -   New: No new changes.
    -   Changes: Create Logical Connection Utilities now creates relationships between logical interfaces and respective telco equipment.
-   **Version 5.0.1 - August 2025**
    -   New:
        -   Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology.
        -   Use the floor map to view the layout of your data center infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.
        -   Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view all connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.
        -   Upload and manage your data center map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.
        -   Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.
        -   Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the data center floor map to monitor overall health and take appropriate action.
        -   Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for data center performance tracking.
        -   Define your data center record to view the location-specific attributes for each data center, including the campus, buildings, and floors where your network asset is located.Define the power circuit record to represent the electrical pathway that delivers power within a data center.
        -   Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.
        -   Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.
        -   View data center records listed in the Equipment task attribute form.
        -   Add Wavelength attribute to the Network Interface form and Port position attribute to Interface Model form.
        -   Added RU numbering direction attribute to define the numbering sequence of rack units in the Rack view.
    -   Changed:
        -   The Network Visualization L1 menu is added to the Telecommunications Network Inventory Workspace. The Topology L1 menu has been removed and is available as Topology tab within the Network Visualization view.
        -   xNF Instance is renamed to Service Instance.
        -   xNF is renamed to Network Function.
-   **Version 4.0.0 - February 2025**

    -   New:
        -   Create and configure playbooks for design and assign a configuration item. Design and Assign playbook provides step-by-step guidance for designing a network service. Use the playbook to complete guided activities to instantiate a network inventory record.
        -   Use the Design and Assign playbook to instantiate a logical connection and its associated connection elements. Once each activity completes, view the circuit map to visualize the logical connection elements.
        -   Use the Network site map to view the geographical location of your network sites and the information such as site details, connectivity, and capacity.
        -   Instantiate a logical composite record and associated equipment and racks using a logical composite template.
        -   Add equipment or rack to a logical composite using a change model.
        -   Remove a rack or equipment from a logical composite using a change model.
        -   Create a change request for equipment record from the All Equipment list view using the Create equipment UI action.
        -   Create a request to import or export your collection of models and templates in JSON format.
        -   The xNF and xNF instance records are added in the Inventory menu and retained the Services menu for application services.
        -   Supports all types of telephone numbers.
        -   Enable Deny ACL to ensure the compliance with improved security model.
    -   Removed: Export of models and templates to XML.
     

-   **Version 3.1.1 - November 2024**
    -   New: Enabled Deny ACL \(effective from Yokohama release onwards\)
    -   Fixed:
        -   Performance issue fix design assign workflow
        -   Interface naming generation logic enhancement
        -   Execution defect on capacity functions
-   **Version 3.0.1 - August 2024**
    -   New:
        -   Feature to Edit Rack in rack visualization enabling the user to drag-drop equipment, move equipment, reserve slot, remove equipment from the rack
        -   Feature to create new equipment from Rack visualization
        -   Feature to import export inventory models and templates
        -   Feature to view protection and revision in circuit visualization
        -   Feature to validate original configuration item against revision for any changes
        -   TMF 639 conformance
        -   Feature to instantiate Cable and Strand
        -   Feature to modify topology
    -   Changed:
        -   Rack view experiences improved
        -   Additional KPIs for Rated Power and Bearable weight are added to the rack visualization
-   **Version 2.0.0 - February 2024**
    -   New:
        -   Support for Capacity Management
        -   Rack Visualization
        -   Topology Visualization
-   **Version 1.4.7 - January 2024**
    -   Fixed:
        -   Misconfiguration of table/field ACLs within the 'com.app-ni-core' plugin has been resolved
        -   Add Card use case failure due to service offering being present has been resolved.
-   **Version 1.4.2 - September 2023**

    Fixed: Changed dependant core version.

-   **Version 1.4.1 - August 2023**
    -   New: Network Visualization
    -   Changed: TNI Function Flow actions
    -   Network visualization only works with the Utah+ version and may not work with Tokyo.
-   **Version 1.3.2 - March 2023**

    Fixed: Added additional validations to ensure the cross-impact of TNI Workspace and SOW Workspace.

-   **Version 1.3.1 - February 2023**
    -   Changed:
        -   Updated business logic to work with a broader network inventory data model.
        -   Integrated OMT-TNI to initiate change requests for the order tasks of Order Management for Telecommunications and Media application.
        -   Defined a catalog of inventory functions and subflows to execute the network inventory design and assign activities via user-defined flows/subflows.
-   **Version 1.1.0 - August 2022**
    -   New:
        -   Path Computation logic
        -   Workspace for TNI persona's.


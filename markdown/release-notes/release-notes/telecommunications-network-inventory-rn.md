---
title: Telecommunications Network Inventory release notes
description: The ServiceNow Telecommunications Network Inventory application enables a network planner to model the physical, logical, or virtual network and perform design and assign services based on those network models. Telecommunications Network Inventory was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Telecommunications Network Inventory release notes

The ServiceNow® Telecommunications Network Inventory application enables a network planner to model the physical, logical, or virtual network and perform design and assign services based on those network models. Telecommunications Network Inventory was enhanced and updated in the Yokohama release.

## Telecommunications Network Inventory highlights for the Yokohama release

-   View the geographical location and the details of your network site
-   Design and assign a configuration item using a playbook and add custom states to a Change model.
-   Define a logical composite to track and manage its CI.
-   Import and export your collection of models and templates in JSON format.
-   Enable Deny ACL to ensure the compliance with the enhanced security model.

See [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/telecom-network-inventory.md) for more information.

**Important:** Telecommunications Network Inventory is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Telecommunications Network Inventory to Yokohama

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

## New in the Yokohama release

-   **[Design and assign your network services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/design-assign-playbook.md)**

    Create and configure playbooks for design and assign a configuration item. The Design and Assign playbook provides step-by-step guidance for designing a network service. Use the playbook to complete guided activities to instantiate a network inventory record.

-   **[Design and Assign function for logical connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/design-logical-connection-design-assign-playbook.md)**

    Use the Design and Assign playbook to instantiate a logical connection and its associated connection elements. Once each activity completes, view the circuit map to visualize the logical connection elements.

-   **[Visualization of geo map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/visualization-map.md)**

    Use the Network site map to view the geographical location of your network sites and the information such as site details, connectivity, and capacity.

-   **[Creating an inventory template for a logical composite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/creating-inventory-template-logical-composite.md)**

    Instantiate a logical composite record and associated equipment and racks using a logical composite template.

-   **[Add an equipment or rack to logical composite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/add-equipment-rack-logical-composite.md)**

    Add equipment or rack to a logical composite using a change model.

-   **[Remove an equipment or rack from logical composite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/remove-equipment-rack-logical-composite.md)**

    Remove a rack or equipment from a logical composite using a change model.

-   **[Create an equipment record by using design and assign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/create-equipment-record-design-and-assign.md)**

    Create a change request for an equipment record from the All Equipment list view using the **Create equipment** UI action.

-   **[Import models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/import-models-templates-json.md)**

    Create an import request to import your collection of models and templates in JSON format.

-   **[Export hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/export-hierarchy-of-models-and-template.md)**

    Export the hierarchy and all related records of a model or inventory template in JSON format.

-   **[Managing your network functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/services.md)**

    The xNF and xNF instances records are added in the Inventory menu and retained the Services menu for application services.

-   **[Create a telephone infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/telephone_block_telephone_number_and_telephone_number.md)**

    Supports all types of telephone numbers.


## Activation information

Install Telecommunications Network Inventory by requesting it from the ServiceNow Store. For details about the installation procedure, see [Install Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/installing-telecommunications-network-inventory.md).

## Related ServiceNow applications and features

-   **[Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_ITILConfigurationManagement.md)**

    With the [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_ITILConfigurationManagement.md) application, build logical representations of assets, services, and the relationships between them that comprises the infrastructure of your organization. Details about these components are stored in the CMDB, which you can use to monitor the following infrastructure, helping promote integrity, stability, and continuous service operation.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/technology-industry-rn-landing.md)


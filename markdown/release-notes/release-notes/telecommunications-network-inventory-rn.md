---
title: Telecommunications Network Inventory release notes
description: The ServiceNow Telecommunications Network Inventory application enables a network planner to model the physical, logical, or virtual network and perform design and assign services based on those network models. Telecommunications Network Inventory was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Telecommunications Network Inventory release notes

The ServiceNow® Telecommunications Network Inventory application enables a network planner to model the physical, logical, or virtual network and perform design and assign services based on those network models. Telecommunications Network Inventory was enhanced and updated in the Xanadu release.

## Telecommunications Network Inventory highlights for the Xanadu release

-   Provide a visualization of the circuit and its underlying connection elements with revisions and protection paths on a dedicated canvas.
-   Get enhanced rack and cabinet visualization capabilities, including viewing, editing, and updating features, along with new KPIs for better capacity planning and prioritization.
-   Archive current configurations while operationalizing a planned revision and compare them with original connections to detect changes.
-   Export equipment models and templates along with related hardware to an Excel data source, and import them to another ServiceNow instance.
-   TMF conformance for TMF 639 Resource Inventory API.

See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US) for more information.

**Important:** Telecommunications Network Inventory is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Telecommunications Network Inventory to Xanadu

If you are an existing user of previous releases, both legacy and new product models will be available in the Network Inventory Workspace menu after upgrading to Xanadu. To rectify this issue, you must migrate your legacy product model data to the new product model tables in your current instance. For more details about the procedure, see [KB1695167](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695167).

## New in the Xanadu release

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Gain visibility of your data centers infrastructure through advanced rack and cabinet insights. Edit a rack or cabinet to add, reserve, move, and remove any equipment. This enables you to create equipment from the rack or cabinet view.

-   **[Revise a configuration item](https://www.servicenow.com/docs/access?context=revise-a-configuration-item&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Perform a comparative validation between the revision and the original connections to identify any changes between them.

-   **[Import Models and Templates](https://www.servicenow.com/docs/access?context=import-models-and-templates&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Import the models and templates from an external system via XLS template.

-   **[Visualization of circuits](https://www.servicenow.com/docs/access?context=unified-map-view-of-connection-elements&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Provide a visualization of the circuit and its underlying connection elements on a dedicated window. View the revisions and protection paths of a logical connection, and selectively collapse expanded layers instead of collapsing the entire structure.

-   **[Create a cable record by using design and assign](https://www.servicenow.com/docs/access?context=create-cable-record-using-design-assign&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Instantiate cables and associated strands using a cable template.

-   **[Modify a network topology record using design and assign](https://www.servicenow.com/docs/access?context=modify-network-topology-record-design-assign&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Modify a network topology for adding or removing the nodes and edges by using a new change model.

-   **[Create capacity function](https://www.servicenow.com/docs/access?context=create-capacity-function&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Identify and prioritize the capacity function by using the category and order attributes. Access the capacity management forms from the Workspace lists view.

-   **[Network Inventory Workspace](https://www.servicenow.com/docs/access?context=exploring-network-inventory-workspace&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    View your and your team's work in the new landing page.


## UI changes

-   **[Revise a configuration item](https://www.servicenow.com/docs/access?context=revise-a-configuration-item&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The Validate Revision button is implemented within the revised CI to facilitate comparison with the modified CI \(Configuration Item\) and revision history tracking of the modified CI.

-   **[Export hierarchy of models and templates](https://www.servicenow.com/docs/access?context=export-hierarchy-of-models-and-template&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The Export button is added to export the hierarchy and all related records of a model or inventory template.

-   **[Optimizing rack and cabinet usage](https://www.servicenow.com/docs/access?context=subsequent-actions&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    Create equipment, edit rack or cabinet, calculate capacity, and perform other actions from the new rack or cabinet visualization.

-   **[Visualization of circuits](https://www.servicenow.com/docs/access?context=unified-map-view-of-connection-elements&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The View connection button is introduced to replace the tab-based experience of the circuit diagram in the logical connection record, allowing the diagram to open in a dedicated window.

-   **[Network Inventory Workspace](https://www.servicenow.com/docs/access?context=exploring-network-inventory-workspace&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The Map widget is removed from the Workspace landing page. The Usage metric widget is moved from the Workspace landing page to the Inventory management view.


## Changed in this release

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The new rack visualization provides new power, weight, and capacity metrics.

-   **[Creating your inventory models](https://www.servicenow.com/docs/access?context=creating-your-inventory-models&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

    The legacy product model tables are deprecated and they are migrated to Enterprise product model app.


## Activation information

The Telecommunications Network Inventory application is a ServiceNow AI Platform feature that is available with activation of the Network Inventory Advanced plugin \(sn\_ni\_adv\). For details, see [Install Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=installing-telecommunications-network-inventory&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    With the [Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) application, build logical representations of assets, services, and the relationships between them that comprises the infrastructure of your organization. Details about these components are stored in the CMDB, which you can use to monitor the following infrastructure, helping promote integrity, stability, and continuous service operation.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)


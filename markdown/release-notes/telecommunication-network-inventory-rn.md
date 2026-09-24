---
title: Telecommunication Network Inventory release notes
description: The ServiceNow Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services. See the following sections for release notes by version.Telecommunications Network Inventory now supports facility models in inventory templates and provides direct visibility into network interfaces and physical connections from rack and cabinet records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/telecommunication-network-inventory-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Telecommunication Network Inventory release notes

The ServiceNow® Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services. See the following sections for release notes by version.

## About Telecommunication Network Inventory

-   Model and manage physical, logical, and virtual network assets across your telecom infrastructure
-   Design and assign network services with end-to-end visibility across equipment, connections, racks, and IP address space.
-   Visualize network topology, physical connections, and rack configurations to support faster network planning and operational decision-making.
-   Support datacenter infrastructure management with rack space planning, allocation, and visualization.

See [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/telecom-network-inventory.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/installing-telecommunications-network-inventory.md). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 13.0

Telecommunications Network Inventory now supports facility models in inventory templates and provides direct visibility into network interfaces and physical connections from rack and cabinet records.

### What's new

-   **[Viewing rack or cabinet equipment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/viewing-rack-or-cabinet-equipment-details.md)**

    View all network interfaces and physical connections for equipment in a rack or cabinet directly from the rack or cabinet record.

-   **[Create an inventory template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-inventory-templates.md)**

    You can now create inventory templates that reference facility models. The full flow: facility model, inventory template, change request, and change task is now supported end to end.

-   **[Query range access for TNI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/query-range-access-for-tni-tables.md)**

    Added query range access control lists to 23 TNI tables. These include 14 NI Core tables, 2 CMDB CI class model tables, 6 TNI CMDB CI tables, and the Phone Territory table. Authenticated users with existing read roles automatically receive query range access. No new roles are required.


### What's changed

-   **[Define a network model relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-network-model-relationships.md)**
    -   Hardware models visible in Inventory Template picker: Template Managers can now select hardware models \(cmdb\_hardware\_product\_model\) from the Inventory Model picker when creating or editing an inventory template. Previously, models of this type were not visible in the picker if they were not tagged with a TNI inventory category. Hardware models created anywhere in the model catalog are now always included in the picker.
    -   Parent Model selection retained when relationship type changes: When a Catalog Manager changes the relationship type after already selecting a Parent Model, the selected model value is now retained if it is a valid model type. Previously, changing the relationship type could clear a validly selected Parent Model value.
-   **[Create an equipment model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-equipment-models.md)**

    All model types are made visible in Model Relationship Parent Model picker: Catalog Managers can select any model type, including hardware models and product models, as the Parent Model when creating a model relationship, regardless of which relationship type is selected.



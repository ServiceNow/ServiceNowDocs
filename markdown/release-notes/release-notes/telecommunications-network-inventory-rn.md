---
title: Telecommunications Network Inventory Release Notes
description: The ServiceNow Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services Telecommunications Network Inventory was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Telecommunications Network Inventory Release Notes

The ServiceNow® Telecommunications Network Inventory application enables network planners to model physical, logical, or virtual networks, support datacenter infrastructure management, and perform design and assign services Telecommunications Network Inventory was enhanced and updated in the Australia release.

## Telecommunications Network Inventory highlights for the Australia release

Australia Early Availability

-   Enable customers to request services for equipment housed in your facility using Remote Hands.
-   View a concise summary of Remote Hands Request

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Create IP addresses directly within an IP subnetwork.
-   Define reusable naming patterns using the new TNI CI Naming application with real-time validation, hierarchical name construction, and interactive preview before applying to the inventory.
-   Access control update — TNI table permissions

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   Reserves rack unit space in a datacenter with rack allocation agentic workflow
-   TNI Data Model Navigator, a CMDB framework that presents a curated, domain-specific view of telecom

See [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecom-network-inventory.md) for more information.

**Important:** Telecommunications Network Inventory is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

Australia Early Availability

-   **[Remote Hands Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/remote-hands-request-management.md)**

    Enable your customers to request services such as power usage enquiries, equipment installation, equipment restarts, and more by connecting with onsite operations agents at your facility. Securely store your customer requests in the Remote Hands Case table, with role-based access controls. View an auto-generated summary of your requests for quick reference.


-   **[Remote hands case record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/generate-summary-for-remote-hands-case-record.md)**

    Remote Hands Request Summarization generates contextual summary of a Remote Hands case by combining current case data with insights from similar historical cases, using information submitted by the DCIM user through the CSM portal.


[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   **[IP address management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/ip-address-management.md)**

    Multi-layer nested IP Subnetworks with CIDR validation: You can now create IP Subnetworks within IP Subnetworks, supporting recursive nesting for both IPv4 and IPv6. When creating a subnetwork at any level, the system validates that the CIDR is correctly formatted, falls within the parent's range, is more specific than the parent, and is unique within the parent.


-   **[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/naming-patterns-in-inventory-templates.md)**

    Author patterns from a variable library with real-time validation, verify resolved names across the full template hierarchy from a new Overview tab at design time, and add custom validation rules.

-   **[Telecom Network Inventory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecom-inventory-roles.md)**

    Standard ServiceNow platform roles no longer have read access to specific TNI tables. This change affects both new installations and upgrades.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   **[Rack allocation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/rack-allocation-workflow.md)**

    The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.


-   **[TNI Data Model Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/data-model-navigator.md)**

    A Data Model Navigator is a CMDB framework feature that presents a curated, domain-specific view of the CMDB. With TNI context, it organizes thousands of CMDB CI classes into a focused, hierarchical structure relevant to telecom operations.


## UI changes

Australia Early Availability

-   **[Network topology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/using-network-topology.md)**

    Topology map icons updated to support dark theme colour contrast.


[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   **[IP address management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/ip-address-management.md)**

    The IP Pool menu and records are now labeled as IP Address Block throughout the Network Inventory Workspace and Service Operations Workspace.


## Changed in this release

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## Activation information

Install Network Inventory Advanced plugin \(sn\_ni\_adv\) by requesting it from the ServiceNow Store. For installation details, see [Install Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/installing-telecommunications-network-inventory.md). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Remote Hands Request Management \(sn\_remote\_hands\): Remote Hands plugin enables you to use the Remote Hands request feature in the Customer Service Management portal.
    -   Racks Allocation Workflow \(sn\_genai\_platform 12.1.0\): Enables rack allocation via the Rack placement AI agent in the Telecommunication Network Inventory Workspace and Service Operation Workspace. The agent reserves the racks that meet the capacity requirements, based on the physical and logical constraints specified in the change request.

## Additional requirements

You must install Customer service install base management \(sn\_cs\_sm\_request\) plugin and Remote Hands plugin from the ServiceNow Store to use the Remote Hands feature.

## Accessibility information

Improved overall accessibility across Network Inventory application, focusing on keyboard navigation, screen readers, zoom levels, colour contrast, and text spacing.

## Related ServiceNow applications and features

-   **[Using the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/use-the-customer-portal.md)**

    Customer Service Management Service Portal activity usually begins on the homepage. Organizations usually customize their landing pages, and logged-in users often see different information than users who are not logged in.

-   **[Request an item or service from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-request-from-portal.md)**

    Browse the catalog and create a request from the Customer or Consumer Service Portals.


-   **[Hardware Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/hardware-asset-management-rn.md)**

    Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Australia release.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/technology-industry-rn-landing.md)


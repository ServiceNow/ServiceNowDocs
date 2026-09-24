---
title: Sales CRM for Telecommunications PSR catalog
description: The Sales CRM for Telecommunications Product, Service, and Resource \(PSR\) catalog is a unified catalog that defines all required entities in a single location. It is based on the TM Forum \(TMF\) Shared Information and Data \(SID\) model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/somt-psr-catalog.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Sales CRM for Telecommunications PSR catalog

The Sales CRM for Telecommunications Product, Service, and Resource \(PSR\) catalog is a unified catalog that defines all required entities in a single location. It is based on the TM Forum \(TMF\) Shared Information and Data \(SID\) model.

The Sales CRM for Telecommunications PSR catalog consolidates product, service, and resource definitions into a single catalog structure, eliminating the need for product data synchronization between separate sales and fulfillment catalogs. It provides a consistent framework for managing telecom product offerings across multiple domains like B2C Retail Mobile, B2C Retail Wireline, B2B Enterprise Connectivity, and Beyond Connectivity. The following table contains examples of Mobile, Broadband and Dedicated leased lines.

The catalog defines and maps all necessary entities in a single location. This eliminates the need for explicit entity-to-entity API mapping or separate product data harmonization across sales and service catalogs.

\[Omitted image "psr\_catalog.png"\] Alt text: PSR catalog hierarchy showing product offerings, specifications, and service-resource relationships

## PSR catalog hierarchy

Each level in the catalog maps to a specific layer of the product-service-resource model:

-   Product offering: Defines the item to be sold to a customer. Pricing attributes include recurring charges \(RC\), one-time charges \(OTC\), ramp-up pricing, mark-up and mark-down percentages, and discounts. A product offering references a product specification which in turn can have child product specifications.
-   Product specification: The structured definition of a product. One product specification maps to Zero to many Service specifications and Resource Specifications.
-   Service specification: Defines the service layer. Service specifications are of two types:
    -   CFSS: Represents the service provided to the customer, for example, Voice and Text CFSS or home fiber FTTH Access CFSS.
    -   RFSS: Represents the underlying network resource services that are used to deliver service to the customer, for example, Home Subscriber Server \(HSS\), RFSS or Optical Line Terminal \(OLT\) RFSS.
-   Resource specification: Defines the physical or logical network resources that fulfill the service, for example, IMSI or Modem RS.

## Commercial features

The PSR catalog supports the following commercial capabilities:

-   Product bundling and hierarchy: Supports product offer grouping, product offer-to-product specification definitions, and product specification hierarchies with relationships between specifications.
-   Product offer pricing rules: Supports multiple pricing rule types, including recurring charges, one-time charges, ramp-up pricing, markup pricing, markdown pricing, contract-based pricing, and characteristic value-based pricing.
-   Multidimensional rules and relationships: Supports product offer-to-product offer relationships, product offer-to-product specification relationships, specification-level relationships, characteristic value-based rules, and context-based rules such as location and customer type.

## Fulfillment features

The PSR catalog supports the following order fulfillment capabilities:

-   Catalog-based decomposition: Decomposes a customer order into order line items based on product offerings and product specifications. Order line items are further decomposed into child or domain orders, such as product orders, service orders, and resource orders.
-   Quote data carry-over into orchestration: Maps attributes from the quote through to order tasks, making the correct data available to southbound APIs during service order orchestration.
-   Orchestration dependencies: Supports staggered decomposition based on catalog characteristic values and decomposition rules. This eliminates complex workflow rules when order line items have dependencies on each other.

## Explanation of specifications

**Product Specification**: The structured definition of a product. One product specification maps to one or more service specification\(s\) and can reference one or more resource specifications. A product specification is a detailed description of a tangible or intangible object that serves as the template from which customer products and subscriptions are instantiated. Represents the product as perceived by business users, not as technical network components i.e. Product Specification is the blueprint of a product that defines its characteristics, pricing model, eligibility, life-cycle rules, and the mapping to one or more underlying Resource and Service Specifications required to realize it.

-   Structure: Can be simple \(atomic\) or a composition of other product specifications.
-   Attributes: Includes characteristics such as Bandwidth, Routing, SLA, Modem make and model, and Router type, etc.
-   Relationships: Has relationships with other specifications, and characteristic value to characteristic value relationships. For example, if attribute Value A is selected on the PS, then Attribute value C is defaulted on the RS that is related to the PS.
-   Realization: Realized through customer-facing service specifications \(CFSS\) and Resource specifications \(RS\).

**Resource Specification**: Resource Specification defines the technical characteristics of a physical or logical resource \(HW device, Software, port, circuit, IP block, VNF, cloud endpoint\) and provides the template used to instantiate actual resource inventory objects during fulfillment.

-   It is related to a PS via a REQUIRED relationship.
-   ServiceNow has extended TMF SID by adding a relationship between Resource Specification and CFSS.
-   A detailed example or a Resource Specification is:
    -   Resource Specification: "ONT Model XYZ‑GPON‑1GE"
    -   Type: Optical Network Terminal
    -   Vendor/Model: XYZ Networks GPON‑1GE
    -   Capabilities:
        -   1× GPON uplink
        -   1× GE LAN port
        -   Max throughput: 1 Gbps
    -   Constraints: indoor installation, requires optical power −27 to −8 dBm
    -   Lifecycle: stock → shipped → installed → active → retired
    -   Used by RFSS:
        -   Access Activation Workflow
        -   CPE Provisioning Workflow

This ResourceSpec defines what the ONT is, its capabilities, and how orchestration can allocate and configure it.

**Customer-facing service specification**: Customer‑Facing Service Specification \(CFSS\) is the service definition exposed to the customer, describing what the service delivers and its functional behavior.It sits between the commercial Product Specification and the technical Resource‑Facing Service Specification.

-   A customer-facing service specification \(CFSS\) defines technology-agnostic service characteristics that a customer directly purchases.
-   It connects product specifications to resource-facing service specifications, focusing on service parameters, service level agreements \(SLAs\), and features.
-   Customer-centric view: Describes services from the customer's perspective, for example, internet access rather than a specific DSL or fiber profile.
-   Product realization: Represents the realization of a product specification.
-   Service components: Includes service characteristics such as service name and service rate, parameters that customers can configure during ordering, and links to related product offerings.
-   A detailed example:
    -   CFSS: "Internet Access"
    -   Bandwidth = 500 Mbps access
    -   IPv4/IPv6 connectivity
    -   Optional static IP
    -   QoS/SLA attributes:
        -   99.9% uptime
        -   Latency ≤ 20 ms within region
        -   Packet loss ≤ 0.1%
    -   Customer options:
        -   Add‑on: static IP
        -   Add‑on: managed router
    -   Mapped RFSS:
        -   Access Bearer RFSS \(GPON/XGS‑PON circuit\)
        -   IP Addressing RFSS \(DHCP/static assignment\)
        -   CPE Management RFSS \(if managed router selected\)

**Resource‑Facing Service Specification \(RFSS\)**: The technical service definition that describes how the network delivers a customer‑facing service. It defines the network‑level behaviors, protocol actions, activation parameters, and resource interactions required to realize a CFSS. It sits directly below the CFSS and is related to the Resource Specifications via a requires relationship. ServiceNow CRM Sales for Telecom does not perform the actual Design and Assign or Resource Provisioning. The RFSS is not defined in this context, but the data model supports defining and maintaining the RFSS.


---
title: Mapping of Sales CRM for Telecommunications PSR catalog to TMF SID
description: The Sales CRM for Telecommunications PSR catalog entities, product offering, product specification, customer facing service specification, resource facing service specification, and resource specification map directly to the corresponding entities in the TM Forum \(TMF\) shared information and data \(SID\) model.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 4
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Mapping of Sales CRM for Telecommunications PSR catalog to TMF SID

The Sales CRM for Telecommunications PSR catalog entities, product offering, product specification, customer facing service specification, resource facing service specification, and resource specification map directly to the corresponding entities in the TM Forum \(TMF\) shared information and data \(SID\) model.

## TMF SID model

The TMF SID model is an industry-agreed framework by TM Forum that provides a common language and data model for communications service providers \(CSPs\). It defines business entities such as customer, product, service, and resource and their relationships across enterprise systems. The Sales CRM for Telecommunications PSR catalog maps its core entities to the product, service, and resource layers of the TMF SID model. The TMF APIs that the catalog supports, including TMF 620 and TMF 633, are also based on the SID model.

![Diagram showing relationships between Product Offering, Product Specification, CFSS, RFSS, and Resource Specification entities in TMF SID model.](../image/somt-psr-sid.jpg)

## Product offering

A product offering defines how a product specification is made available to the market, including its pricing, terms, and conditions.

-   Market view: Represents the commercial view of a product that customers see in a catalog and agree to contractually.
-   Relationship to product specification: References a product specification to define what is being sold. One product specification can have multiple product offerings, for example, the same product can be offered with different price points for different time periods.
-   Components: Can be structured as a simple item or a bundle of other product offerings.
-   Commercial parameters: Includes price, market segments, valid dates, and allowed actions such as subscription or upgrade.
-   Catalog management: Categorized in a catalog and can be constrained so that it is sold only within a bundle.

## Bundle product offering

A bundle product offering is a type of product offering that groups two or more product offerings into a single package. Unlike a simple product offering which represents a single, atomic item such as a mobile handset, a bundle product offering represents a combination of offerings, such as a triple play package \(internet, TV, and voice\).

-   Inheritance: Inherits all attributes of a standard product offering.
-   Composition: Can contain other bundle product offerings or simple product offerings, supporting hierarchical, multi-level bundling.
-   Reusability: References simple product offerings rather than embedding them, so the same component can appear across different bundles.
-   Pricing and marketing: Supports bundle-specific pricing, price adjustments, and rules such as eligibility, compatibility, and commitment terms.
-   Containment: Indicates whether a product offering represents a single item or a collection.

## Product specification

A product specification is a detailed description of a tangible or intangible object that serves as the template from which customer products and subscriptions are instantiated.

-   Commercial focus: Represents the product as perceived by business users, not as technical network components.
-   Structure: Can be simple \(atomic\) or a composition of other product specifications.
-   Attributes: Includes characteristics such as color, relationships with other specifications, and characteristic values.
-   Realization: Realized through customer-facing service specifications \(CFSS\) and resource-facing service specifications \(RFSS\).
-   Lifecycle: Manages the product lifecycle status.

## Resource specification

A resource specification defines the characteristics, behaviors, and relationships of a managed or unmanaged resource, and serves as the template for instantiating specific resource instances of the same type.

-   Template functionality: Defines the resource type. The resource class defines a specific instance based on that specification.
-   Definition scope: Captures common attributes such as name, version, and lifecycle status, along with physical or logical parameters that apply to all instances of a resource type.
-   Resource types: Can describe physical components such as a router or SIM card, or logical components such as software or virtual network functions.
-   Service realization: Defines the technical components that RFSS requires to deliver a service.

## Customer-facing service specification

A customer-facing service specification \(CFSS\) defines technology-agnostic service characteristics that a customer directly purchases. It connects product specifications to resource-facing service specifications, focusing on service parameters, service level agreements \(SLAs\), and features.

-   Customer-centric view: Describes services from the customer's perspective, for example, internet access rather than a specific DSL or fiber profile.
-   Product realization: Represents the realization of a product specification.
-   Service components: Includes service characteristics such as service name and service rate, parameters that customers can configure during ordering, and links to related product offerings.
-   Structure: Can be atomic \(single\) or composite \(a grouping of services\).
-   Product offering support: A single CFSS can support multiple similar product offerings.

## Resource-facing service specification

A resource-facing service specification \(RFSS\) defines the technical characteristics, attributes, and requirements of a service that maps to underlying resources. Unlike a CFSS, an RFSS is domain-specific or technology-specific.

-   Definition and purpose: Defines the technical implementation of a service and serves as the blueprint for managing the lifecycle of resource-facing service instances.
-   Relationship to resource-facing service: Serves as the specification used to instantiate actual resource-facing service instances.
-   Technology specific: Represents reusable, technology specific components such as DSL, VPN, or MPLS connections to network infrastructure.
-   Structure: Can be atomic or composite \(containing other RFSSs\) and defines relationships with physical or logical resources such as routers and IP addresses.
-   Mapping: Maps a logical service requirement from the CFSS layer to the network resources needed to deliver it.

## Product definition in the Sales CRM for Telecommunications catalog

The following example shows how the SASE Custom Solution Bundle is defined in the Sales CRM for Telecommunications catalog. The bundle product offering contains three child product offerings, internet connectivity, SD WAN GW, and SD WAN Controller each of which is linked to its own product specification. The product specifications are mapped to service specifications. For example, Site Connectivity PS is mapped to SD WAN Edge and Connectivity service specifications, which in turn require resource specifications such as Edge Router, VNF, OLT Port, and ONT.

![Catalog hierarchy showing SASE Custom Solution Bundle with three child offerings mapped to product specifications and resource specifications.](../image/somt-psr-sid-example.jpg)


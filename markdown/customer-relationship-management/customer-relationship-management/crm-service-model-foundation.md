---
title: Service Model Foundation
description: The Service Model Foundation \(SMF\) framework enables you to model your business organization structure, customer organizations, and the relationships between them.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 3
---

# Service Model Foundation

The Service Model Foundation \(SMF\) framework enables you to model your business organization structure, customer organizations, and the relationships between them.

## SMF overview

The service model foundation defines and connects the core entities in the customer service value chain: service organizations, business locations, staff members, and the relationships between them. It extends the customer service data model to support complex organizational structures, including those with internal and external locations, franchise networks, dealer relationships, and Business-to-Business-to-Consumer \(B2B2C\) service models.

## SMF benefits

SMF provides benefits to organizations that manage complex service delivery across multiple domains.

-   **For service agents and fulfillers:** Service Model Foundation reduces the effort required to navigate and act on service requests by providing a unified data model. Agents and fulfillers can access assignment details, related assets, location information, and task dependencies from a single record without switching between applications. The structured task hierarchy ensures that work is tracked and escalated consistently across service domains.
-   **For administrators and configuration teams:** Administrators can extend the foundation to meet domain-specific requirements without rebuilding the structures, reducing configuration overhead and maintaining consistency across implementations. Common service entities such as skills, territories, and service contracts are centrally managed and reused across workflows.
-   **For implementation partners and architects:** The shared data model reduces duplication across applications. This enables faster implementation and simplifies the design of cross-domain workflows.

## Products and contexts

The service model foundation operates across CRM products and adapts to a range of deployment contexts.

|Product|How SMF works|
|-------|-------------|
|CSM|Underpins case routing, account hierarchy modeling, and agent access control within the CSM workspace.|
|B2B2C scenarios|Models both the business relationship and the consumer relationship within a single framework, supporting intermediary service models.|
|Contracts and entitlements|Service contracts and entitlements complement SMF by defining customer support terms and automatically applying the applicable SLA when a case is opened.|
|B2E \(Business to Employee\)|SMF supports scenarios where internal employees act as consumers of a service, such as a corporate retailer where store staff raise cases for in-store facilities through the same platform used for customer service.|
|B2B2E|Similar to B2B2C, the business supports its own employees instead of end consumers. For example, a franchisor providing a service channel through which franchise owners raise and manage cases on behalf of their store staff.|
|Industry deployments|Supports financial services, manufacturing, and retail models where complex location and responsibility hierarchies are common.|

## Use cases

-   **Retail**

    A retail franchise network with hundreds of outlet locations uses the BOSC persona to allow individual franchise owners to create and manage cases for their stores directly. Each franchise owner sees only their own location's cases and assets. The franchisor retains consolidated visibility across all locations for SLA and case tracking.

    **Note:** BOSC \(Business Organization Self Contributor\) is a role for front-line and location-based workers. This role enables self-service case management for business partners with access scoped to their location.

-   **Manufacturing**

    A manufacturing company operating through an authorized dealer network configures external business locations for each dealer. Dealers can create warranty cases and service requests on behalf of their customers, scoped to the products and entitlements associated with their dealership. The enterprise gains a unified view of dealer-initiated cases alongside direct customer cases, with responsibility definitions linking regional account managers to the dealers they oversee.

-   **Financial services**

    A financial institution configures internal business locations for each of its regional branches. Agents are assigned to their branch location, giving them access to cases for customers served at that branch. Relationship definitions connect personal relationship managers to the individual accounts they manage, providing targeted access to those customers' cases regardless of which branch the customer visits.


**Related topics**  


[Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-industry-data-model.md)

[Configure Service Model Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-industry-data-model.md)

[Service Model Foundation business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/industry-data-model-locations.md)


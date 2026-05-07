---
title: CSDM terms
description: Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM terms

Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.

<table id="table_kqt_czw_hsb"><thead><tr><th>

Term

</th><th>

Definition

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Application

</td><td>

Any deployed program, module, or group of programs that provides specific functionality on a computer infrastructure.

</td><td>

Defines behavior and has specific functionality associated with it. Applications are typically discoverable functionality, like Apache Web Server.

</td></tr><tr><td>

Asset

</td><td>

An item whose financial value is tracked.

</td><td>

Many, but not all, assets are CIs and many, but not all, CIs are assets. Assets have a life cycle with financial considerations, for example, Microsoft 365.

</td></tr><tr><td>

Business Application

</td><td>

Represents all software and infrastructure environments \(dev, test, prod\) that are configured to provide functionality.

</td><td>

Used to increase productivity and perform other business functions accurately. For example, Dell Online.

</td></tr><tr><td>

Business capability

</td><td>

High-level capability that an organization requires to execute its business model or fulfill its mission.

</td><td>

Typically described in the context of performing one or more specific tasks to achieve business outcomes. For example, demand management or financial planning.

</td></tr><tr><td>

Business service

</td><td>

A business service is a service type that is published to business users. A business service typically implements one or more business capabilities.

</td><td>

Usually, business users order business services. Business users can select the desired offering and service commitment levels via the Service Catalog. For example, procurement, shipping, and finance.

-   A business service is an operational CI.
-   A business service must be a one-level service and not a hierarchy of business services.
-   A business service can be used for impact in Incident Management, Problem Management, and Change Management and for approvals for Change.
-   A business service must be focused on the consumer or seller.

</td></tr><tr><td>

Business service offering

</td><td>

Business service offerings are the starting point for configuring Service Portfolio Management. Business service offerings inherit from Business Services. Business service offerings consist of one or more service commitments that define the level of service in terms of availability, scope, pricing, and other factors. For example, an organization might offer two levels of desktop support:

-   A silver offering of upgrades and virus protection.
-   A gold offering with the silver commitments plus a response time guarantee of 30 minutes between the hours of 8:00 a.m. and 5:00 p.m., Monday through Friday.

</td><td>

See [Service Consumption domain in the CSDM model](../concept/sell-consume-domain.md) for details.

</td></tr><tr><td>

Configuration item \(CI\)

</td><td>

Physical and logical components of an infrastructure that are currently or soon will be under configuration management.

</td><td>

Might be a single module such as a server, database, or router or a more complex item, such as a complete system. For example, a web server, database, or infrastructure.

</td></tr><tr><td>

Operating model

</td><td>

An abstract and ideally visual representation \(model\) of how an organization delivers value to its customers or beneficiaries.

</td><td>

Typically represents the various elements of how an organization operates. It usually incorporates strategy positions such as the innovation model, degree of intelligent automation, industry alignment, provider delivery models, and the business expectations of IT.

</td></tr><tr><td>

Portfolio

</td><td>

Collection of services, products, projects, or applications.

</td><td>

Used to manage like items together for a business. Portfolios may be grouped by objective, capabilities, organization, like projects, or services.

</td></tr><tr><td>

Service

</td><td>

Means of delivering value to customers by facilitating outcomes that users want to achieve without the ownership of specific costs and risks.

</td><td>

Typically has three aspects:-   Interaction
-   Offering
-   Service system

ServiceNow provides three base service types:

-   Business
-   Technical
-   Application

You can extend the base types to align with the service types in your organization.

</td></tr><tr><td>

Service catalog

</td><td>

Provides consumable view of available products, services, service commitment options, and offerings.

</td><td>

Helps manage which services a user may have access to. Also, catalogs are the starting point for access to available services. For example, IT services catalog.

</td></tr><tr><td>

Service commitment

</td><td>

Defines the service delivery obligations agreed to between the consumer and the provider.

</td><td>

Often manifested in the form of contracts such as service level agreements, operational level agreements, and underpinning contracts. Service commitments include specific performance characteristics that differentiate one offering from another.

</td></tr><tr><td>

Service instance \(formerly Application service\)

</td><td>

A service type that is a logical representation of a deployed application stack.

</td><td>

Examples of service instances are hosting, data backup, and recovery. **Note:** Applications and service instances do not have a one-to-one relationship. A service instance can include multiple applications. An application can be included in multiple service instances.

See [Use Service instance \(Application Services\) dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

</td></tr><tr><td>

Service offering

</td><td>

A stratification of a service into capability, availability, pricing, and packaging options.

</td><td>

Different levels of performance and features for a given service can be made available. For example, ITSM Standard and ITSM Pro.

</td></tr><tr><td>

Technology management service \(formerly Technical service\)

</td><td>

A service type that is published to service owners and typically underpins a business or service instance.

</td><td>

Can typically be ordered by service owners. Service owners can select the desired offering and service commitment levels via the Service Catalog. For example, computers, storage, and networks.

</td></tr><tr><td>

Technology management offering

</td><td>

A Technology management offering is a service offering with a service classification of "technical service". Technical service offerings may be further divided as follows:

-   Location and geography
-   Environment \(production or non-production\)
-   Pricing
-   Availability
-   Support group \(for Incident Management\)
-   Technical approval group \(for Change Management\)
-   Packaging options \(commitments\)

The technical service offering comes from the service, based on how the parent serves a specific technical need. Every operational technical service must be associated with at least one technology management offering.

</td><td>

**Note:** Not all Technology management offerings must be related to applications or infrastructure CIs. Managed Service Providers can provide technical service offerings.

</td></tr></tbody>
</table>**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

**Related topics**  


[CSDM resources](csdm-resources.md)


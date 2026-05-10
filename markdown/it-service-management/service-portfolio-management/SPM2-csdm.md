---
title: Applying the CSDM guidelines to Service Portfolio Management
description: Service data relates to each other using different applications in different ways. Service Portfolio Management references the Common Service Data Model \(CSDM\) framework to bring service-related data together in a single view.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Service Portfolio Management, IT Service Management]
---

# Applying the CSDM guidelines to Service Portfolio Management

Service data relates to each other using different applications in different ways. Service Portfolio Management references the Common Service Data Model \(CSDM\) framework to bring service-related data together in a single view.

Since both ServiceNow® products of Service Portfolio Management and Digital Portfolio Management \(DPM\) closely align with the CSDM, it's helpful to know the common terms and life-cycle fields when working in these applications.

**Tip:** For CSDM set-up information, see [Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md).

## CSDM life-cycle fields for business and technical services

After the CSDM activation plugin is installed \[**com.snc.cmdb.csdm.activation**\], you can use the CSDM life-cycle fields in Service Portfolio Management. To see the field names, navigate to **All** &gt; **Service Portfolio Management** &gt; **Services**, and set the view to Service Portfolio.

Using the CSDM life-cycle fields helps you manage the end-to-end life cycle of services and service offerings. The shared field names provide you with consistency and alignment as you use other ServiceNow applications. For more information about the CSDM, see [Enabling life-cycle synchronization from legacy to asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-life-cycle-standard-values.md).

**Important:** For the Australia release and later, the labels for the items in the \[cmdb\_ci\_service\_technical\] table and \[service\_offering\] table are Technology Management Service and Technology Management Service Offering, respectively. The label changes align with the CSDM, version 5. Prior to the Australia release, the labels are Technical Service and Technical Service Offering.

The following comparison shows the differences from the traditional Service Portfolio Management phase and status fields to the CSDM life-cycle stage and status fields.

These fields also display when you use the Performance Analytics \(PA\) indicators.

|Service Portfolio Management Phase and Status field names|CSDM life-cycle Stage and life-cycle Status field names|
|---------------------------------------------------------|-------------------------------------------------------|
|Pipeline \| Requirements|Ideation \| Under evaluation|
|Pipeline \| Definition|Ideation \| Under evaluation|
|Pipeline \| Analysis|Ideation \| Under evaluation|
|Pipeline \| Approved|Ideation \| Under evaluation|
|Pipeline\| Chartered|Design \| Chartered|
|Catalog\| Design|Design \| Design|
|Catalog \| Development|Design \| Design|
|Catalog \| Build/Test/Release|Deploy \| Test|
|Catalog \| Operational|Operational \| In-use|
|Catalog \| Retiring|Operational \| Pending Retirement|
|Retired \| Retired|End of life \| Retired|
|Retired \| Obsolete|End of life \| Obsolete|

## Common CSDM terms used in Service Portfolio Management and in DPM

<table id="table_c1p_w4f_nzb"><thead><tr><th>

Term

</th><th>

Definition

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Portfolio

</td><td>

Collection of services, products, projects, or applications.

</td><td>

Used to manage like items together for a business. Portfolios may be grouped by objective, capabilities, organization, like projects or services.

</td></tr><tr><td>

Business capability

</td><td>

High-level capability that an organization requires to execute its business model or fulfill its mission.

</td><td>

Typically described in the context of performing one or more specific tasks to achieve business outcomes. For example, demand management or financial planning.

</td></tr><tr><td>

Service

</td><td>

Means of delivering value to customers by facilitating outcomes customers want to achieve without the ownership of specific costs and risks.

</td><td>

Typically has three aspects:-   Interaction
-   Offering
-   Service system

 ServiceNow provides three base service types:

-   Business
-   Technical
-   Application

 Customers can extend the base types to align with the service types in their organization.

</td></tr><tr><td>

Business service

</td><td>

A service type that is published to business users and it typically underpins one or more business capabilities.

</td><td>

Typically orderable by business users. Business users are able to select the desired offering and service commitment levels via the ServiceNow Service Catalog. For example, procurement, shipping, and finance.

</td></tr><tr><td>

Technical service

</td><td>

A service type that is published to service owners and typically underpins a business or application service.

</td><td>

Typically orderable by service owners. Service owners are able to select the desired offering and service commitment levels via the Service Catalog. For example, computers, storage, and networks\).

</td></tr><tr><td>

Application service

</td><td>

A service type that is a logical representation of a deployed application stack.

</td><td>

Examples of application services are hosting, data backup, and recovery. **Note:** There isn’t a 1-to-1 relationship between application and application services.

</td></tr><tr><td>

Application

</td><td>

Any deployed program, module, or group of programs that is designed to provide specific functionality on a computer infrastructure.

</td><td>

Defines behavior and has specific functionality associated with it. Applications are typically discoverable functionality, like Apache Web Server.

</td></tr><tr><td>

Business Application

</td><td>

Represents all software and infrastructure environments \(dev, test, prod\) configured to provide functionality.

</td><td>

Used to increase productivity and perform other business functions accurately. For example, Dell Online.

</td></tr><tr><td>

Service catalog

</td><td>

Provides a consumable view of available products, services, service commitment options, and offerings.

</td><td>

Helps manage what services a user may have access to. Also, catalogs are the initiation point for access to available services. For example, the IT services catalog.

</td></tr><tr><td>

Service offering

</td><td>

A stratification of a service into capability, availability, pricing, and packaging options.

</td><td>

Different levels of performance and features for a given service can be made available. For example, ITSM Standard and ITSM Pro.

</td></tr><tr><td>

Service commitment

</td><td>

Defines service delivery obligations agreed to between the consumer and the provider.

</td><td>

Often manifested in the form of contracts such as service level agreements, operational level agreements, and underpinning contracts. Service commitments include specific performance characteristics that differentiate one offering from another.

</td></tr><tr><td>

Configuration item \(CI\)

</td><td>

Physical and logical components of an infrastructure that are currently or soon will be under configuration management.

</td><td>

A single module such as a server, database, or router or a more complex item, such as a complete system. For example, a web server, database, or infrastructure.

</td></tr><tr><td>

Asset

</td><td>

An item whose financial value is tracked.

</td><td>

Many assets are CIs and vice versa, but that's not always the case. Assets have a life cycle with financial considerations, for example Microsoft Office 365.

</td></tr><tr><td>

Operating model

</td><td>

An abstract and ideally visual representation \(model\) of how an organization delivers value to its customers or beneficiaries.

</td><td>

Typically represents the various elements of how an organization operates. It usually incorporates strategy positions such as the innovation model, degree of intelligent automation, industry alignment, provider delivery models, and the business expectations of IT.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Service Portfolio Management](SPM2-configuring.md)

**Related topics**  


[Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md)


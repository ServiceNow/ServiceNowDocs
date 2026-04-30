---
title: Set up services and commitments in Service Portfolio Management
description: Set up services and commitments in Service Portfolio Management to define services and track their performance against availability commitments. You can relay the performance information in real-time to your stakeholders.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Set up services and commitments in Service Portfolio Management

Set up services and commitments in Service Portfolio Management to define services and track their performance against availability commitments. You can relay the performance information in real-time to your stakeholders.

## Before you begin

Role required: portfolio\_admin or service\_editor

## Procedure

1.  Define the service offerings and commitments.

    Create service offering records that define different levels of service for an existing service. For example, you might offer two levels of desktop support in your organization. You offer a standard offering for upgrades and virus protection and an executive offering that also includes availability guarantee. Create a complete set of [service offerings](../concept/SPM2-service-offerings.md) with [service commitments](define-SPM2-service-commitments.md) that define the specifics of the offering.

2.  Define the scope of the service offerings.

    Scope in Service Portfolio Management refers to the detailed service parameters that define the limits of a service. Define specific additional services related to the service as **In Scope** or **Out of Scope**. For instructions to apply scope definitions to services, refer to [Apply scope to a service in Service Portfolio Management](SPM2-apply-scope-to-service.md).

3.  Configure the price of the service offering.

    Each service offering may have a pricing model and a price unit. Values are set on the parent service and inherited by the offerings. The actual price per unit that is charged for the service is established in the offering. For information about price modeling, refer to [Service Portfolio Management service offering price](../concept/SPM2-set-service-offer-price.md).

4.  Configure the service catalog for the end user.

    All the data created in the previous steps display on the service catalog page for a service. The layout is not configurable, but an administrator can control how the service is categorized and who can view the service in the catalog. For more information, see [Service Catalog administration](https://www.servicenow.com/docs/access?context=t_ServiceCatalogAdministration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

5.  Subscribe to service offerings.

    With Service Portfolio Management, service owners can subscribe various business entities to [Service offerings in Service Portfolio Management](../concept/SPM2-service-offerings.md).

6.  Opt in to the updated availability calculator system property \[com.snc.availability.v2\].

    This updated availability system property \[com.snc.availability.v2\] offers improved calculations and maintenance. For more information, see [Set the time zone for availability results in Service Portfolio Management](spm2-set-timezone.md) or [View Service Level Agreement \(SLA\) results in Service Portfolio Management](../concept/SPM2-view-sla-result.md).


**Parent Topic:**[Configuring Service Portfolio Management](../concept/SPM2-configuring.md)


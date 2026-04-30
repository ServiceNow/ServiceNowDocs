---
title: Service offerings in Service Portfolio Management
description: A service offering derives from a service, refining the parent service to a specific business need and performance level.
locale: en-US
release: zurich
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Service Portfolio Management, IT Service Management]
---

# Service offerings in Service Portfolio Management

A service offering derives from a service, refining the parent service to a specific business need and performance level.

## Service offerings and commitments

Offering records define different levels of performance for an existing service. For example, you might offer two levels of desktop support in your organization. You can offer a standard offering for upgrades and virus protection and an executive offering that also includes availability guarantee.

Service offering types include business service offerings and technical service offerings.

**Important:** For the Zurich release and later, the label for the items in the \[cmdb\_ci\_service\_technical\] table is Technology Management Service, respectively. Prior to the Zurich release, the label is Technical Service.

Create a complete set of service offerings defined by commitments that define the specifics of the offering. Each service must have at least one defined offering to move to the Catalog phase. This is because service offerings are where you define Service Level Agreements \(SLAs\) and where metrics are collated.

For detailed information about SLAs, including SLA definitions and results, refer to [Service Level Management](../../service-level-management/reference/service-level-mgmt-landing-page.md).

## Service offering pricing

Each service offering may have a pricing model and a price unit. Use this pricing data towards creating catalog items.

## Service offering subscriptions

You can subscribe different entities to a service offering. This data is then used to determine the total subscriber count on the offering form.

## Technical service offerings

Technical service offerings can be shown as inherited relationships to business services and offerings. They are not included in metric models and do not use the weighting model.

## Re-parenting service offering types

You can change a service offering parent from one type of service to another. For example, changing an offering parent from a business service to a technical service or vice versa. Offerings cannot be re-parented to an application service. Some important information and guidelines concerning re-parenting service offering types, include:

-   When you change the offering parent from a business service to a technical service you will receive a message alerting you that performance scoring is not available with technical service offerings.
-   When you re-parent from one service type to another, existing weighting rules will apply.
-   If you try to re-parent and the parent service is in Catalog phase with only one offering, you will receive a message that you cannot make this change.
-   If the metric weight on the parent service is &gt;0, you will receive a message alerting you to adjust the data before re-parenting the offering. You cannot re-parent the offering to a different service type until the weight for the offering on the former service type is set to zero.

## Service offering topics in this section

-   **[View a service offering in Service Portfolio Management](../task/SPM2-view-service-offering.md)**  
View service offerings in Service Portfolio Management to find offerings that add value to your organization and external users. You can also view service offerings in the Service Builder application.
-   **[Create a service offering in Service Portfolio Management](../task/create-or-mod-SPM2-service-offerings.md)**  
Create service offerings to define services, document them, track performance against defined availability commitments, and relay the performance information in real time to your end users.
-   **[Add a commitment to a service offering in Service Portfolio Management](../task/define-SPM2-service-commitments.md)**  
Service commitments are specific services that define the unique availability guarantees, scope, and pricing for a service offering.
-   **[Assign multiple teams to support a service offering](../task/spm2-assign-teams.md)**  
You can assign multiple teams to support a single service offering when several teams are responsible for that offering.
-   **[Subscribe users to a service offering in Service Portfolio Management](../task/SPM2-subscribe-to-service-offering.md)**  
Subscribe users to a service offering so they can order it from the catalog. You can also subscribe offerings for companies, locations, groups, and departments.
-   **[Create catalog items for service offering subscribers in Service Portfolio Management](../task/SPM2-create-catalog-items.md)**  
As a service owner or service offering subscriber, you can create one or more catalog items for your service regardless of the offering phase or status. You can also relate an existing catalog item to a service offering.
-   **[Reporting for services and service offerings in Service Portfolio Management](SPM2-reporting.md)**  
See what's impacting your services and service offerings and report on them by using related list information in Service Portfolio Management.
-   **[Service Portfolio Management service offering price](SPM2-set-service-offer-price.md)**  
Service offerings inherit the pricing structure of the associated parent service. If the price model for each service offering in Service Portfolio Management is defined in the parent service as per unit, then each service offering must also have an associated price unit. The actual price for that unit is established in the service offering record.
-   **[Service Portfolio Management Premium notifications](../../service-owner-workspace/reference/SPM2-premium-notifications.md)**  
Notifications are added with Service Portfolio Management Premium to manage your service offering to catalog item relationships.

**Parent Topic:**[Using Service Portfolio Management](SPM2-using.md)


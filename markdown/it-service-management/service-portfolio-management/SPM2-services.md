---
title: Use Service Portfolio Management services
description: Configure IT services within your portfolios to add the most value to your organization. The IT services defined in your portfolios may, or may not be, aligned to an application. IT services defined in your portfolios may, or may not be, represented in a request catalog.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Use Service Portfolio Management services

Configure IT services within your portfolios to add the most value to your organization. The IT services defined in your portfolios may, or may not be, aligned to an application. IT services defined in your portfolios may, or may not be, represented in a request catalog.

The phase and status of a service indicates the life-cycle position of the service. You can view, track, and monitor the services by phase and status with platform lists and reports. The lists can also include retired services for viewing purposes.

Each service record has a unique number to identify the record.

To reflect the importance or impact of each service on the operations of your organization, you can select a criticality level for them. For example, you might select a high level for a service that supports sales functionality using the organization's website. You might then select a lower level for a service that provides internal printing for the organization's employees.

## Business services

Business services make up the structure of your service portfolio taxonomy. You can manage associated service and offering details via the dependency tabs of the related list on the Service and Service Offering forms. Business services reside in the \[cmdb\_ci\_service\_business\] table.

Create offerings as children of services. Offerings are created in the Service Offering \[service\_offering\] table. Refer to [Service offerings in Service Portfolio Management](SPM2-service-offerings.md) for more details.

You can designate services as **Services I depend On** or **Services Dependent On Me** via form related lists.

## Technical services

You can add technical services as part of your service portfolio taxonomy. Even if you don't, you can still gain insight into these services by adding them as **Services I depend On** or **Services Dependent On Me** in the related list section of the Service form.

Starting with the Yokohama release, technical services align with the Common Service Data Model \(CSDM\), version 5. With this alignment, technical services remain in the \[cmdb\_ci\_service\_technical\] table and are labeled in the user interface as Technology Management Service. Service offerings remain in the \[service\_offering\] table and are labeled Service Offering.

|Table name|Label in Xanadu and prior releases|Label in Yokohama and later releases|
|----------|----------------------------------|------------------------------------|
|\[cmdb\_ci\_service\_technical\]|Technical Service|Technology Management Service|

To create or modify services, see [Create or modify Service Portfolio Management services](../task/create-or-modify-SPM2-services.md).

To learn about service offerings, see [Service Portfolio Management service offerings](SPM2-service-offerings.md).

To subscribe users to a service offering, see [Subscribe users to a service offering in Service Portfolio Management](../task/SPM2-subscribe-to-service-offering.md).

**Parent Topic:**[Exploring Service Portfolio Management](c_ServicePortfolioManagementv2.md)


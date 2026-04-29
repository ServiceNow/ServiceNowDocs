---
title: HR Service Delivery integration with Service Portfolio Management and Digital Portfolio Management
description: HR Service Delivery integration with Service Portfolio Management and Digital Portfolio Management enables you to manage HR services in a standardized, structured format as suggested in the Common Service Data Model \(CSDM\) methodology. It ensures that the hierarchy in which you define services is consistent with the hierarchy of other business units.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery integration with Service Portfolio Management and Digital Portfolio Management

HR Service Delivery integration with Service Portfolio Management and Digital Portfolio Management enables you to manage HR services in a standardized, structured format as suggested in the Common Service Data Model \(CSDM\) methodology. It ensures that the hierarchy in which you define services is consistent with the hierarchy of other business units.

## Integration with Service Portfolio Management and Digital Portfolio Management Overview

Larger enterprise customers on their journey to embrace the vision of Enterprise Service Management face the problem of different work flows following different data models and hierarchy which makes it difficult to provide a uniform view of all services. These customers require a common interface, a single place for monitoring metrics, viewing services, and getting similar information across the work flows. With this integration:

-   HR Services are mapped within the hierarchy of CSDM, providing a consistent way for the service owners to define appropriate business services.

<table id="table_zhx_1y3_nzb"><thead><tr><th>

HR Service Delivery

</th><th>

Common Service Data Model

</th></tr></thead><tbody><tr><td>

COE \(Center of Excellence\)For example: Total Rewards

</td><td>

-

</td></tr><tr><td>

Topic CategoryFor example: Benefits

</td><td>

Taxonomy NodeFor example: Laptop Support \(Service\)

</td></tr><tr><td>

Topic DetailsFor example: Dental

</td><td>

ServicesFor example: Laptop Support \(Service\)

</td></tr><tr><td>

HR Service - Record ProducerFor example: Dental Benefits Inquiry

</td><td>

Service OfferingsFor example:

-   Executive Laptop Support \(Service Offering\): 15 " Portal Plan laptop \(Catalog Item\)
-   Standard laptop Support \(Service Offering\): 13" Portals Plan Laptop \(Catalog Item\)


</td></tr></tbody>
</table>-   HR Services appear as part of the overall services in Human Resource Portfolio in Enterprise Portfolios in Digital Portfolio Management. With Digital Portfolio Management, you can manage and maintain all your services, applications, and products from a single location. It enables you to surface data from solutions you own as well as from solutions that you don't own but rely on from other ServiceNow products.

## Activation information

First, activate the Human Resources Scoped App: Core \[com.sn\_hr\_core\] application. Activating the application automatically activates Service Portfolio Management.

Next, activate Digital Portfolio Management to view HR services in Digital Portfolio Management dashboard.

## Work flow

1.  Activate the required applications.
2.  [Create a service table configuration in Service Portfolio Management](../task/config-service-table.md).

    **Note:** Default HR service table configuration is available for use.

3.  [Configure CSDM service mappings](../task/config-csdm-ser-map.md).

    **Note:** Demo data for HR CSDM service mappings is available for use.



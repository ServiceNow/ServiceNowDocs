---
title: Adopt CSDM methodology
description: Manage services of your business unit in a standardized, structured format as suggested in the Common Service Data Model \(CSDM\) methodology. Ensure that the hierarchy in which you define services is consistent with the hierarchy of other business units.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration with SPM and DPM, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Adopt CSDM methodology

Manage services of your business unit in a standardized, structured format as suggested in the Common Service Data Model \(CSDM\) methodology. Ensure that the hierarchy in which you define services is consistent with the hierarchy of other business units.

## Before you begin

Role required: admin

## About this task

Customers require a common interface, a single place for monitoring metrics, viewing services, and getting similar information across the work flows. With this feature, you can:

-   Map your services in the hierarchy of CSDM, providing a consistent way for the service owners to define appropriate business services.
-   View your services as part of the overall services in Digital Portfolio Management. With Digital Portfolio Management, you can manage and maintain all your services, applications, and products from a single location. Surface data from solutions you own as well as from solutions that you don't own but rely on from other ServiceNow products.

## Procedure

1.  Create a business or technical service and corresponding service offering records for your business unit.

2.  [Create a service table configuration in Service Portfolio Management](config-service-table.md).

3.  Map your BU service to CSDM Service or Service Offering.

    For more information, see [Configure CSDM service mappings](config-csdm-ser-map.md).

4.  Add your business unit logic to populate Service and Service Offering columns in task records or resulting BU records that are created by using the BU service \(For example: HR service use case\).

    The table must have Service and Service Offering columns.

5.  Create a service portfolio and add the required taxonomy nodes.

    For more information, see [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

6.  Map BU service to the taxonomy nodes in the Services related list.

    **Note:** After the Service is mapped, related offerings are automatically selected. You can create or edit the offerings related to the service.

7.  Configure KPI group and indicators for your business unit in the Digital Portfolio Management dashboard.

    For more information, see [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

    -   To display the KPIs in Digital Portfolio Management, create a KPI group and add the required KPIs. Once KPIs are added, add group mapping to associate the group with correct taxonomy node where you want to display indicator data.
    -   The PA indicators must have the correct breakdown assigned. For example, if you are creating an indicator for service offering, add the **DPM: Service Offerings breakdown** to that indicator. Before adding the breakdown, make sure the record table exists in breakdown mappings.

        **Note:** Make sure that the service is in operational state, so that indicators can work as expected.

    -   After you have added the above configurations and the required data, you can view analytics in Digital Portfolio Management dashboard.


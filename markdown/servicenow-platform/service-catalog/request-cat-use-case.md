---
title: Service Catalog and CSDM tables
description: Service Catalog manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Service Catalog.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Catalog and CSDM, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog and CSDM tables

Service Catalog manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Service Catalog.

## CSDM tables managed by the Service Catalog

The Service Catalog primarily manages business services in the Sell/Consume domain. Technical Services are also viewed from the Operate domain of Event Management.

The Service Catalog manages the Catalog Item table \[sc\_cat\_item\]. The Catalog Item table creates requests in Request Management. The requests usually have an automated, semi-automated, or business workflow for fulfilling the request, which can consist of approvals and tasks. When part of Service Portfolio Management, the CIs are associated with service offerings. When you link a catalog item, you can track request activity for all catalog items associated with a service offering. An offering can have multiple catalog items.

The CIs can include:

-   PC Hardware Item \(pc\_hardware\_cat\_item\): Submits hardware asset requests included in Asset Management workflows.
-   PC Software Item \(pc\_software\_cat\_item\): Submits software asset requests included in Asset Management workflows.
-   Record Producer \(sc\_cat\_item\_producer\): Submits requests or generates records other than Request Management tables for services that aren't serviced by Request Management \(for example, HR Cases, Facilities Requests, or Legal Requests\).

![CSDM tables managed by Request Catalog.](../image/csdm-v5-tables-managed-by-req-cat.png "CSDM tables managed by the Service Catalog")

## CSDM tables used by the Service Catalog

1.  Configuration Item tables \[cmdb\_ci\*\]
2.  Service Offering table \[sc\_cat\_item\_subscribe\]
3.  Application Service table \[cmdb\_ci\_service\_discovered\]
4.  Product Model tables \[cmdb\_model\]

    **Note:** The following legacy CMDB relationships that once provided access to catalog items are no longer supported. To provide access, use the new relationships listed in the table.

    |CMDB table|Catalog item relationship table|New relationship to use instead|
    |----------|-------------------------------|-------------------------------|
    |User \(sys\_user\)|sc\_cat\_item\_user\_mtom, sc\_cat\_item\_user\_no\_mtom|User criteria|
    |Group \(sys\_user\_group\)|sc\_cat\_item\_group\_mtom, sc\_cat\_item\_group\_no\_mtom|User criteria|
    |Department \(cmn\_department\)|sc\_cat\_item\_dept\_mtom, sc\_cat\_item\_dept\_no\_mtom|User criteria|
    |Location \(smn\_location\)|sc\_cat\_item\_location\_mtom, sc\_cat\_item\_location\_no\_mtom|User criteria|
    |Company \(core\_company\)|sc\_cat\_item\_company\_mtom, sc\_cat\_item\_company\_no\_mtom|User criteria|


![CSDM tables used by Request Catalog.](../image/csdm-v5-tables-used-by-req-cat.png "CSDM tables used by the Service Catalog")

## Products that benefit from the Service Catalog

-   **Service Portfolio Management \(Service Portfolio Management\)**

    Ties catalog items to service offerings. Lets service owners create and maintain catalog items more easily, and gives more visibility into the service offerings.

-   **Hardware Asset Management and Software Asset Management**

    Self-service catalog lets you order an asset and track service delivery.

-   **Human Resources \(HR\)**

    Exposes the creator \(Record Producer\) of HR cases and displays the Record Producer in the relevant self-service catalogs \(for example, Portal, Mobile, and Virtual Agent\).

-   **Customer Service Management \(CSM\)**

    Exposes the creator \(Record Producer\) of customer service cases and displays the Record Producer in the relevant self-service catalogs \(for example, Self-service Portal, Mobile, and Virtual Agent\).


**Parent Topic:**[Service Catalog and CSDM](../concept/request-cat-use-case-product-view.md)


---
title: Create a request from the Customer and Consumer Service Portals
description: As customers, you can create and submit requests from the Customer and Consumer Service Portals. The request process is integrated with Service Catalog.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with IT Service Management, Integrate, Customer Service Management]
---

# Create a request from the Customer and Consumer Service Portals

As customers, you can create and submit requests from the Customer and Consumer Service Portals. The request process is integrated with Service Catalog.

## Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner, sn\_customerservice.customer\_case\_manager, sn\_customerservice.customer, sn\_customerservice.consumer, sn\_customerservice.proxy\_contact

## About this task

**Note:** Creating a request from the Customer and Consumer Service Portals requires activation of the Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\). It also requires that the system administrator provide external customers with access to request records.

Partners, partner administrators, and proxy contacts can submit requests on behalf of other accounts or contacts with the addition of the following variable set to the desired catalog items: **csm\_request\_variable\_set**. This variable set adds the **Account** and **Contact** fields. For more information, see [Service catalog variable sets](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariableSets&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Do one of the following to create a request:

    -   Click the **Request Something** link on the portal landing page.
    -   Click **Requests** &gt; **Request Something** in the portal menu header.
2.  Browse the service catalog and select the desired item or service.

    You can also use the Category filters to filter the available items.

3.  Fill in any necessary information related to the request.

4.  Click **Submit**.

    The following information is copied from the request to the case:

    |Request fields|Case fields|
    |--------------|-----------|
    |Short description|Short description|
    |Requested for|Contact|
    |Account|Account|


## Result

-   A new case is created, which becomes the parent of the request. One request is associated with a case and a request contains one item.
-   The case is used as the reference for the customer, who can see the request status and updates from the case on the Customer Service Portal.
-   All cases associated with a request appear on the request record in the **Cases** related list.


---
title: Request Management integration with Universal Request
description: Integration of Request Management with the Universal Request application extends the capabilities of Universal Request and enables your employees and agents to create a universal request by submitting a request from a catalog item or record producer. This integration provides a consistent ticketing experience and facilitate inter-department request transfers.
locale: en-US
release: zurich
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Request Management, IT Service Management]
---

# Request Management integration with Universal Request

Integration of Request Management with the Universal Request application extends the capabilities of Universal Request and enables your employees and agents to create a universal request by submitting a request from a catalog item or record producer. This integration provides a consistent ticketing experience and facilitate inter-department request transfers.

**Note:** To use this capability, enable the **sn\_uni\_req.com.snc.ur.request\_integration** property under Universal Request properties in the Universal Request application. For more information, see [Universal Request properties](https://www.servicenow.com/docs/access?context=ur-properties&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Configure the catalog item or record producer to create a universal request. The associated requested item \(for catalog item\) or task-based record \(for record producer\) becomes the primary ticket for that universal request. For more information on Universal Request, see [Exploring Universal Request](https://www.servicenow.com/docs/access?context=explore-universal-request&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)

## Benefits of integrating with Universal Request

The integration enables you to perform the following actions:

-   Create a request directly from the Universal Request application using the **Create Request** option.
-   Transfer a request to another department or back to the Universal Request queue by using the **Transfer** option.
-   Configure a catalog item as Universal Request and automatically associate the request as a primary ticked for the universal request. For more information, see [Configure a catalog item or record producer to create a universal request](https://www.servicenow.com/docs/access?context=create-ur-recordproducer&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).
-   View all the associated requests and request items as a related list for a universal request.
-   Employees can view the details related to their Universal Request from Employee Center.

## System requirements to integrate Request Management with Universal Request

Ensure that you have installed the Universal Request plugin \(com.snc.universal\_request\) to create a universal request from a request item.

After the plugins are installed, in the Universal Request application properties, set the **sn\_uni\_req.com.snc.ur.request\_integration** to true. For more information, see [Universal Request properties](https://www.servicenow.com/docs/access?context=ur-properties&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

-   **[Create a request from Universal Request](../task/create-request-from-ur.md)**  
As a routing agent, create a request from a universal request and then assign it to the appropriate assignment group. The request manager handles the requested items and takes further actions to fulfill the request.
-   **[Requested item state mapping](../task/req-item-state-mapping.md)**  
Map your requested items states to the universal request \(UR\) states to provide a better user experience during the requested item state transition and to track the progress of the request.
-   **[Transfer a request to another department](../task/req-transfer-ur.md)**  
Transfer a request to another department with or without resolution to fulfill the request.

**Parent Topic:**[Configuring Request Management](configuring-request-management.md)


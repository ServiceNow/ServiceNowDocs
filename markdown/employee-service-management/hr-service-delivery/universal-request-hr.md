---
title: Universal Request for HR Service Delivery
description: With the integration of HR Service Delivery and Universal Request applications, you can provide a consistent user experience for employees while creating service requests. You can hide the complexities of inter-department request transfers and multi-department use cases by providing a common help desk for all employees.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Universal Request for HR Service Delivery

With the integration of HR Service Delivery and Universal Request applications, you can provide a consistent user experience for employees while creating service requests. You can hide the complexities of inter-department request transfers and multi-department use cases by providing a common help desk for all employees.

## About Universal Request for HR Service Delivery

A universal request gets created when an employee clicks the **Request help** option in Employee Center. A universal request routing agent analyses the issue \(as HR department related\) and creates an HR case from that universal request. After the case gets resolved by an HR agent, the state of the HR case changes to **Awaiting Acceptance**. Automatically, the state of the universal request changes to **Awaiting response**. Finally, after the employee accepts the resolution, the universal request gets closed and in turn the HR case gets closed.

At any point in time, the HR agent can [transfer the HR case back](../task/route-ur-hr-case.md) to the universal request queue with or without resolution.

All the important details, such as, users who are working on the issue, inter-department transfers, and work notes, are recorded in the universal request ticket, providing complete visibility to the employee who has raised the request.

## Activating the necessary plugins

After you have activated the Universal Request \(com.snc.universal\_request\), Human Resources Scoped App: Core \(com.sn\_hr\_core\), and Employee Center \(com.sn\_hr\_service\_portal\) plugins, you notice that:

-   The Universal Request form contains a UI action to create an HR case.
-   The **Universal Request** field appears on the HR case form when an HR case is associated with a universal request record.
-   The **Transfer** button appears on the HR case form to let an HR agent transfer an HR case back to Universal Request, another department, or service.
-   An HR case created from a record producer automatically creates a universal request. It happens only when the **Create Universal Request** check box is enabled on the record producer.

    Similarly in the Create a test case topic block, if the **Create Universal Request**check box is enabled on the record producer, then a universal request ticket is created and shared with the employee on the Virtual Agent conversation.

-   When an HR case associated to a universal request goes through a state change, a notification is sent to the employee \(requester\) with the universal request number and not the HR case number.
-   On ServiceNow AI Platform, HR cases that are associated with Universal Request appear under **HR Case Management** &gt; **All**.
-   On Employee Center, HR requests that are associated with Universal Request appear under **Employee Center** &gt; **Requests**.

-   **[Custom configurations in Universal Request](../task/setup-hr-ur.md)**  
Transferring and state mappings are preconfigured for all the base system HR states. Do these configurations only when you have a custom state.
-   **[Create an HR case from Universal Request](../task/create-ur-hr-case.md)**  
Restore service to a customer as soon as possible. After creating the HR case, you can investigate potential solutions.
-   **[Work on an HR case of Universal Request](../task/work-hr-ur-case.md)**  
Provide resolution to an HR case that is initiated from a universal request.
-   **[Transfer an HR case in Universal Request](../task/route-ur-hr-case.md)**  
Transfer an HR case back to the Universal Request, or to another department or service with or without resolution.
-   **[Creating a universal request from an HR case](hr-ur-omnichannel.md)**  
Create a universal request for every HR case that is created, using any channel. Extend the unified ticket experience that Universal Request provides for all the HR cases, irrespective of the channels they are created from.
-   **[Create associated tickets from an HR case](../task/associate-tickets.md)**  
From an HR case that is the primary ticket of a universal request, create tickets for another department and associate them to the same universal request as the HR case. This feature enables agents from various departments to collaborate and work on their tickets in parallel. It also enables organizations to trace back efforts against a single universal request.

**Parent Topic:**[Integration of HR Service Delivery with ServiceNow applications](integrate-hr-platform-apps.md)


---
title: Universal Request for Legal Service Delivery
description: Integrating Universal Request and Legal Service Delivery enables you to create a unified user experience for your employees to request services from the Legal department. Legal services can be provided to employees seamlessly without them having to deal with the difficulties of interdepartmental collaboration for resolution.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Universal Request for Legal Service Delivery

Integrating Universal Request and Legal Service Delivery enables you to create a unified user experience for your employees to request services from the Legal department. Legal services can be provided to employees seamlessly without them having to deal with the difficulties of interdepartmental collaboration for resolution.

## Journey of a universal request for a legal service

The ServiceNow® Universal Request application enables cross-departmental reporting from the time of an initial employee request through the final issue resolution. For more information, see [Universal Request](../../universal-request/concept/ur-landing-limitedaccess.md).

The Legal Request Management application provides a unified mechanism for employees to get all the information, services, and help that they need from the legal department.

You can fulfill requests across the organization to improve the employee experience by integrating legal requests with universal requests.

-   An employee submits a universal request using the **Request help** option in the Employee Center portal. The employee can also submit a direct legal request attached to a universal request.
-   A routing agent identifies this request related to the Legal department and creates a legal request from the universal request. The legal request becomes the primary ticket of the universal request.
-   Based on the services requested, a legal fulfiller can do the following while working on the legal request:
    -   Provides a resolution and closes the legal request. The universal request also gets closed.
    -   Transfers the request to another department or back to the universal request routing group with or without resolution.
    -   Creates associated tickets for the tasks to be done by users in the Legal or any other department required to fulfill the request.
    -   Marks the legal request as Restricted if it contains any sensitive or confidential information. Routing agents from the current assignment group with the sn\_uni\_req.sensitiveinfo\_agent role, and the primary ticket agent can view the complete details of the ticket. Other routing agents cannot see fields in the universal request that may contain sensitive information, such as **Short description** and **Description**.

The universal request gives requesters complete visibility into the status of their requests. They can view all the relevant details from the Activities stream of the universal request, including users who are working on the issue, transfers between departments, and other updates.

When the universal request is closed, the requester can reopen it if not satisfied with the resolution.

For more information about submitting and tracking a universal request, see [Using Universal Request](../../universal-request/concept/using-ur.md).

For more information on submitting and managing ethics complaints, see [Better together solution: Legal Investigations and HR Service Delivery Employee Relations](../../legal-investigations/concept/lsd-investigations-hr-emp-relations.md).

## Required ServiceNow plugins and apps

For integrating universal requests for legal services, you must have the following ServiceNow plugins and application installed:

-   Universal Request plugin \(com.snc.universal\_request\)
-   Legal Request Management app 6.1 or later version
-   Employee Center app

Also, you've to configure various settings in Universal Request. For more information, see [Configure Universal Request for legal services](../task/configure-universal-request-legal.md).

-   **[Configure Universal Request for legal services](../task/configure-universal-request-legal.md)**  
Review the base system configurations for integration of legal requests with universal requests and configure as per your business needs.
-   **[Create a legal request from a universal request](../task/create-legal-request-universal-request.md)**  
Create a legal request from a universal request to get the Legal department's assistance in resolving the request.
-   **[Transfer a legal ticket to another department](../task/transfer-legal-request-universal-request.md)**  
Transfer a legal ticket \(legal request or legal matter\) associated with a universal request to another department or back to the universal request for processing and resolution.

**Parent Topic:**[Integration of Legal Service Delivery with ServiceNow applications](../../lsd-sn-legal-contracts/concept/snclc-integrate-lsd-lp.md)


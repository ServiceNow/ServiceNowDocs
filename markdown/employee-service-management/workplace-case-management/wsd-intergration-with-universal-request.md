---
title: Workplace Service Delivery integration with Universal Request
description: Combine Workplace Service Delivery services with Universal Request so that you can provide a convenient workplace experience to your employees. Provide a common help desk so that your employees can submit requests that are related to their workplace without having to search the Workplace services catalog.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace Service Delivery integration with Universal Request

Combine Workplace Service Delivery services with Universal Request so that you can provide a convenient workplace experience to your employees. Provide a common help desk so that your employees can submit requests that are related to their workplace without having to search the Workplace services catalog.

The integration with Universal Request enables an employee to submit a general inquiry for any workplace-related issue. An employee can get support by selecting a single-help option for services that are not included in the catalog.

For more information about a Universal Request, see [Universal Request](../../universal-request/concept/ur-landing-limitedaccess.md).

## Benefits of integrations with Universal Request

The integration enables you to perform the following actions:

-   Create a workplace case directly from the Universal Request application using the **Create a workplace case** option.
-   Transfer a workplace case to another department or back to the Universal Request queue by using the **Transfer** option.
-   Configure a workplace service as a Universal Request.
-   View workplace cases created by Universal Request under **Workplace Cases** &gt; **All**.
-   On the Workplace Service Portal, an employee can view the Universal Request raised by them in **Workplace Service Portal** &gt; **Requests**.

## System requirements to integrate Workplace Service Delivery with Universal Request

The following plugins must be installed:

-   Universal Request \(com.snc.universal\_request\)
-   Workplace Service Delivery - Core \(sn\_wsd\_core\)
-   Workplace Case Management \(sn\_wsd\_case\)

## Universal Request and workplace cases

When employees cannot find a workplace service that is suitable to their issue on the Workplace Service Portal, they can select the **Request help** option. The following actions are performed when an employee selects **Request help**:

1.  The option navigates the employee to a help form where the employee can specify any issue details. This help request triggers a Universal Request.
2.  The Universal Request is assigned to a routing agent. The agent analyzes the request as a workplace-related query and creates a workplace case.
3.  The workplace manager handles the workplace case and changes the state of the case depending on the progress.
4.  The Universal Request is then closed only when the employee accepts the resolution.

As a workplace manager, you can transfer a workplace case that was created by Universal Request back to the Universal Request queue if it does not relate to workplace services.

Employees can view the details related to their Universal Request anytime.

-   **[Configure a workplace service record producer as a Universal Request](../task/configure-workplace-service-record-prod-as-universal-req.md)**  
Enable an employee to submit a universal request using a workplace service record producer from the Workplace Service Portal. Configure a workplace service to create Universal Request whenever an employee makes a selection.
-   **[Create a workplace case from Universal Request](../task/create-workplace-case-from-universal-req.md)**  
As a routing agent, create a workplace case from a universal request and then assign it to the Workplace services assignment group. The workplace manager handles the workplace case and takes further actions to fulfill the request.
-   **[Work on a workplace case from a Universal Request](../task/work-on-workplace-case-of-universal-req.md)**  
As a workplace manager, work on a workplace case that is created from a Universal Request. Provide a resolution to the workplace case.
-   **[Transfer a workplace case created from a universal request](../task/transfer-a-workplace-case-created-from-a-universal-request.md)**  
Transfer a workplace case back to the Universal Request, to another department, or to another service. You can transfer the request with or without providing a resolution.

**Parent Topic:**[Workplace Case Management](workplace-case-mgmt-feat.md)


---
title: Fine-tune application services to implement owner requests
description: As an administrator, you tweak and fine-tune maps based on comments from the application service owner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/review-implement-business-service-maps.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fine-tune application services to implement owner requests

As an administrator, you tweak and fine-tune maps based on comments from the application service owner.

## Before you begin

Role required: service\_mapping\_admin

## About this task

You can edit discovered and manually created service instances.

**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Reviewing and implementing owner requests is part of the [review and approval process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/business-service-approval.md).

To see documentation for another review phase, click the relevant box in the diagram.

![Approval flow for individual application services](../image/ApproveBSFlow.png)

## Procedure

1.  Navigate to the relevant application service:

    1.  Click **Approve** on the **Home** page.

        The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

    2.  Click **Fix Rejected**.

    3.  Right-click the required application service and select **Open Service Form**.

        The form for this application service opens.

2.  Click **Reject Messages** on the left.

    The owner comments are displayed under the **Service Discovery Messages tab**.

3.  Review the reject messages to see comments that the application service owner left.

4.  Click **View Map**.

5.  Implement changes requested by the application service owner.

6.  Click the discovery message describing the service defect that you have fixed and click **Mark as Resolved** under **Action On Selected** on the right.

7.  If necessary, resend the application service for review.


-   **[Manually add CIs to an application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/manually-add-ci-to-business-service.md)**  
Add configuration items to manually created application services or to services discovered by Service Mapping.
-   **[Remove CIs not belonging to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/remove-cis-not-belonging-business-services.md)**  
Remove CIs erroneously mapped as part of an application service by Service Mapping. Unnecessary CIs included in the map can generate irrelevant alerts in Event Management. For example, when creating an application service for a web portal, Service Mapping might automatically discover a connection to unaffiliated external services, such as PayPal.
-   **[Transfer a map segment into another application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/add-segment-to-business-service-map.md)**  
You can remove a branch of a service and place it into another application service, either new or existing. Transfer map segments to split large services or when you want to organize services differently from the initial mapping result.
-   **[Link application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/link-services-to-services.md)**  
You can manually link two application services by adding a reference to one application service into another application service. The service that contains the reference, becomes a dependent service. The service that you include as a reference is a contained service. You can link application services to create dependencies for impact monitoring in Event Management.
-   **[Discover CIs identified as generic applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/create-pattern-from-generic-application.md)**  
Service Mapping identifies application configuration items \(CIs\) that it failed to properly discover as generic applications. Correctly identify generic applications by creating a simplified discovery pattern from an application service map, rather than creating a fully functional pattern from scratch using the Pattern Designer.

**Parent Topic:**[Application service mapping using classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping]()

[Map application services using tags with classic Service Mapping]()

[Map multiple application services from a CSV file using classic Service Mapping]()

[Map a single application service using classic Service Mapping]()

[Fix application service errors in bulk]()

[Fix errors in individual application service maps]()

[Review and approval of application service maps]()

[Application service completion]()

[Application service analysis and maintenance using classic Service Mapping]()


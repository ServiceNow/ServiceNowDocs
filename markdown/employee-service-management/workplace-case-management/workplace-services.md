---
title: Workplace Services
description: The ServiceNow Workplace Case Management application enables you to create a workplace service with pre-defined steps for fulfillment. You can create workplace services for requests like cleanliness, IT, office setup, and travel requests. For example, you can create a request for HVAC issues, broken chairs, floor spills, move requests, and more.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 2
breadcrumb: [Explore, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace Services

The ServiceNow® Workplace Case Management application enables you to create a workplace service with pre-defined steps for fulfillment. You can create workplace services for requests like cleanliness, IT, office setup, and travel requests. For example, you can create a request for HVAC issues, broken chairs, floor spills, move requests, and more.

The workplace services that you create using the Workplace Case Management application are displayed in the Workplace Service Portal in a Workplace Service Catalog under various categories as follows:![The workplace services created using the Workplace Case Management application are displayed in the Workplace Service Portal in a Workplace Service Catalog](../image/wcasemgmt-workplace-services--ws-portal.png)

When you create a workplace service, you can configure the steps based on the type of fulfillment required. The ServiceNow® Workplace Case Management application provides the following fulfillment types:

-   **Manual**: The Manual option enables you to configure a workplace service with human response. This works for services like general inquiries or complaints, and similar requests. Following is an example of how a manual workplace service is configured and displayed in the Workplace Service Portal.

    Manual Workplace Service created as 'General Workplace Enquiry' in the Workplace Case Management application:

    The workplace service 'General Enquiry' displayed as 'Submit a general request' in the Workplace Service Portal:![The workplace service 'General Enquiry' displayed as 'Submit a general request' in the Workplace Service Portal.](../image/wcasemgmt-general-request-wsportal.png)

-   **Service Activity**: The Service activity option enables you to select the type of activity triggered when a request is raised. You can specify the order in which these activities must be executed. You can select from the following types of workplace service activities:
    -   **Approval**: Enables you to set approvals on workplace service activity. You can configure what type of approval is required on selecting the workplace service. You cannot set more than one approval activity in a single order.
    -   **Task**: Enables you to add a task using a task template. When the workplace service is selected, the task is created based on the order specified.
    -   **Child case**: Enables you to trigger child cases on selecting the workplace service. A workplace service must be provided for a child case. The child case is created based on the order specified.
    -   **Execute service item**: Executes the tasks or cases created for workplace service items ordered by an employee along with the workplace service. For more information, see [Add a workplace service item to a workplace service](../task/add-workplace-service-items.md).
    -   **Automated task**: Creates an automated task that will be closed without any manual intervention.
-   **Flow**: The flow option enables you to select an existing sub-flow from the application. For more information about Flows, see Flows.

**Parent Topic:**[Exploring Workplace Case Management](workplace-case-mgmt-ovw.md)

**Related topics**  


[Raise workplace service requests](request-workplace-service.md)

[Case and Task Templates](wsd-templates.md)


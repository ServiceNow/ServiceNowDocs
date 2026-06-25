---
title: Resource Management reports
description: Resource Management reports provide the resource requester and resource managers with resource allocations, availability, and utilization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/c\_UsingResourceManagementReports.html
release: australia
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Management reports

Resource Management reports provide the resource requester and resource managers with resource allocations, availability, and utilization.

**Important:** Resource Management reports is deprecated starting Zurich release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Alternatively, resource managers are encouraged to use the interactive Overview Dashboard in the Resource Management Workspace. For more information about dashboards, see [Overview dashboard in Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/using-rmw.md).

You can generate reports for the following types of information:

-   **Availability**

    Total time that the resources are available after both [Soft and hard allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/r_AllocatingResources.md). Availability is capacity minus allocation. \[Omitted image "group\_availability\_report1.png"\] Alt text: A group availability report

-   **Forecasted Utilization**

    Percentage of forecasted resource time utilization. It is calculated as sum of allocated and confirmed hours, divided by the total capacity. \[Omitted image "group\_utilization\_forecasted.png"\] Alt text: Forecasted utilization report for a group

-   **Committed Utilization**

    Percentage of committed resource time utilization. It is calculated as allocated hours divided by the total capacity. \[Omitted image "group\_utilization\_committed.png"\] Alt text: Committed utilization report for a group

-   **Allocation**

    Resource capacity, allocations, availability, and utilization. \[Omitted image "allocation\_report\_user1.png"\] Alt text: Allocation report for a group

-   **Allocation details**

    A tabular breakdown of all allocation requests \(soft bookings\), committed allocations \(hard bookings\), availability, capacity, and actual hours.

    If the actual hours for a resource is greater than the allocated hours, the actual hour's cell is highlighted and a message is displayed on mouse hover.

    \[Omitted image "group\_member\_allocation\_details1.png"\] Alt text: Allocation details


-   **[View availability, utilization, and allocation reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/t_GenAvailUtilAllocationReport.md)**  
You can view resource reports that focus on resource availability, utilization, and allocations.
-   **[Edit a resource management report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/ReportsNew.md)**  
Resource management reports show resource allocation details in different formats for different time periods. Configure and use these reports according to your business requirements.

**Parent Topic:**[Resource Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/c_ResourceManagement.md)


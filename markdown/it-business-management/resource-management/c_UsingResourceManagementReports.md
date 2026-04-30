---
title: Resource Management reports
description: Resource Management reports provide the resource requester and resource managers with resource allocations, availability, and utilization.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Management reports

Resource Management reports provide the resource requester and resource managers with resource allocations, availability, and utilization.

You can generate reports for the following types of information:

-   **Availability**

    Total time that the resources are available after both [hard and soft allocations](../reference/r_AllocatingResources.md#booking_typ). Availability is capacity minus allocation. ![A group availability report](../image/group_availability_report1.png)

-   **Forecasted Utilization**

    Percentage of forecasted resource time utilization. It is calculated as sum of allocated and confirmed hours, divided by the total capacity. ![Forecasted utilization report for a group](../image/group_utilization_forecasted.png)

-   **Committed Utilization**

    Percentage of committed resource time utilization. It is calculated as allocated hours divided by the total capacity. ![Committed utilization report for a group](../image/group_utilization_committed.png)

-   **Allocation**

    Resource capacity, allocations, availability, and utilization. ![Allocation report for a group](../image/allocation_report_user1.png)

-   **Allocation details**

    A tabular breakdown of all allocation requests \(soft bookings\), committed allocations \(hard bookings\), availability, capacity, and actual hours.

    If the actual hours for a resource is greater than the allocated hours, the actual hour's cell is highlighted and a message is displayed on mouse hover.

    ![Allocation details](../image/group_member_allocation_details1.png)


-   **[View availability, utilization, and allocation reports](../task/t_GenAvailUtilAllocationReport.md)**  
You can view resource reports that focus on resource availability, utilization, and allocations.
-   **[Edit a resource management report](../task/ReportsNew.md)**  
Resource management reports show resource allocation details in different formats for different time periods. Configure and use these reports according to your business requirements.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)


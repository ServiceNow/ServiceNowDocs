---
title: Creating bulk cases
description: You can create the same type of HR case, for multiple employees, without having to create the same case multiple times. Segments for a bulk case help you define specific values for groups of employees.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Creating bulk cases

You can create the same type of HR case, for multiple employees, without having to create the same case multiple times. Segments for a bulk case help you define specific values for groups of employees.

Bulk case creation can save you time and effort. For example, onboarding 20 new hires, a payroll run issue, or an annual recertification process, are cases that can be created as a bulk case.

Bulk HR cases can be created for all active users. For users without an HR profile, like new hires, an HR profile is automatically created.

You can create one bulk case that creates individual HR cases for each employee in a group. Examples include:

-   Sending an annual recertification task to a group of employees every year.
-   Onboarding multiple new hires.
-   Managing a payroll issue that affects multiple employees.

-   **Bulk case process**

    Perform the following steps to create a number of similar cases using bulk case request:

    -   Create and save a bulk case request.

        A bulk case request starts the process and contains basic information about the types of cases you are creating.

        **Note:** You must create and associate at least one user segment group to a bulk case request.

    -   Create one or multiple user segment groups.
        -   User segment groups allow you to specify values for a group of users. You can create multiple segments for a bulk case request that defines different values for different groups of users.
        -   User segment groups allow admins to ensure their bulk case creation is correct before executing.
        -   After creating a user segment group, you can see the number and the users the bulk case request has targeted. You can also remove specific users.
    -   If your user segment groups look accurate, you can create cases.
-   **Number of cases and performance**

    HR bulk case creation is designed to create up to 10,000 basic HR cases, or 1,000 cases using workflows such as Lifecycle Event cases.

    **Note:** Performance declines when attempting to create more bulk cases than the system is designed to handle.

-   **Bulk cases from previous releases**

    You must complete or close all existing bulk case requests from previous release versions. Incomplete bulk case requests in previous release versions cannot be completed in Rome.

    When opening completed bulk case requests from a previous release version, some fields are not editable and segments do not appear.

-   **Bulk cases queued and asynchronously updated**

    The request to process bulk cases are queued and asynchronously updated in the background.

    **Note:** In previous releases, the **Bulk case creation** scheduled job processed bulk case requests. This scheduled job is now deprecated.

-   **HR admin \(sn\_hr\_core.admin\) and bulk case creation**

    Previously, the HR case writer \(sn\_hr\_core.case\_writer\) role was required. Because bulk case creation involves a large number of cases, it was decided to change the required role to HR admin \(sn\_hr\_core.admin\).

    If you want employees with the HR case writer \(sn\_hr\_core.case\_writer\) role to create bulk cases, you can update the Access Control List \(ACL\) for the following table:

    Bulk Case Request \(sn\_hr\_core\_bulk\_case\_request\).

    To allow user segment groups under the request, update the ACLs for:

    -   Bulk Case User Segment \(sn\_hr\_core\_bulk\_case\_user\_segment\)
    -   Bulk Case User Segment Group \(sn\_hr\_core\_bulk\_case\_user\_segment\_group\)
    For more information on ACLs, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).


-   **[Create a bulk case request](../task/t_CreateBulkCases.md)**  
Use bulk case request to create the same type of HR case, for multiple employees, without having to create the same case multiple times.
-   **[Create a user segment group](../task/bulk-case-segment.md)**  
User segment groups allow you to specify values for a group of users, or with multiple segments specify different values for different groups of users. Segments allows you to ensure that your bulk case creation is correct before executing.
-   **[Manage a user group segment](../task/bulk-case-segment-manage.md)**  
After creating a user group segment, you can review and edit it before you create cases.

**Parent Topic:**[HR Case Management](c_HRCaseManagement.md)


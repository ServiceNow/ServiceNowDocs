---
title: HR profile and HR case security
description: Because HR profile information is sensitive and confidential, the System Administrator \[admin\] cannot view it. The same is true for some of the information in HR cases and HR tasks.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use HR Profile, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR profile and HR case security

Because HR profile information is sensitive and confidential, the System Administrator \[admin\] cannot view it. The same is true for some of the information in HR cases and HR tasks.

HR profile information is confidential and viewed only by authorized HR personnel who are assigned a role that includes sn\_hr\_core.profile\_reader or sn\_hr\_core.profile\_writer, such as sn\_hr\_core.secure\_info\_reader.

For HR cases and HR tasks, only authorized HR personnel are allowed to view attachments, work notes and comments, description, calendar, and payload \(configurable\). Authorized HR personnel are assigned a role with sn\_hr\_core.case\_reader and sn\_hr\_core.case\_writer, such as sn\_hr\_core.secure\_info\_reader.

HR administrators \[sn\_hr\_core.admin\] will be able to perform all tasks and view all data.

## HR profile information that system administrators can access

System Administrators cannot create an HR profile. They can see the list of HR profiles and open HR profile records, but only have access to the following information.

-   The HR profile number and prefix of an employee.
-   Employment information that is synchronized with the user record \[sys\_user\]. This information includes name, employee number, department, manager, and location.
-   Work contact information, such as work email address and work phone number. Personal information is hidden.
-   Information that appears in the following related lists.
    -   Employment Information
    -   Contact Information
    -   Beneficiaries
    -   Who is Covered
    -   Emergency Contacts
    -   Direct Reports
    -   Colleagues
    -   Cases

## HR case and task information accessible by HR Administrators

HR Administrators can view the employee user information, such as location and department, and the short description. Activities, such as state changes, are displayed in the activity stream, but comments and work notes are hidden. System Administrators cannot view this information.

When the HR Administrator opens an HR case or HR task, a message describes the information that is not displayed.

An HR case can be created from an HR profile. Click **Create New Case** under **Related Links** and **Case Creation** appears.

## Impersonating a user

You can prevent a user from accessing HR information by impersonating a user that has HR access by using the **If true, ACLs check if the user is being impersonated.** property.

-   Navigate to **HR Administration** &gt; **Properties**.
-   Scroll to **If true, ACLs check if the user is being impersonated.**
-   Check **Yes** \(true\) to enable ACLs to check when a user is impersonating another user and prevent the user from viewing HR information.

    COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   Even if the logged in user has HR access and impersonates another HR user with the same access, HR information is not visible.

    **Note:** This property was introduced for the HR Service Delivery scoped application and not applicable to the HR Services Delivery Non-scoped application.


See [Add field security in HR](../task/FieldSecurity.md).

See [Restricted caller access for HR](hr-security.md#).

See [Manage HR roles](c_ManageRoles.md).

**Parent Topic:**[Use HR Profile](c_HRProfileRecords.md)


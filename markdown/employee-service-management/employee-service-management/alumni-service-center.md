---
title: Alumni Center
description: The Alumni Center is your dedicated hub to stay connected with the organization after your tenure.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Alumni Center

The Alumni Center is your dedicated hub to stay connected with the organization after your tenure.

## Benefits of an Alumni Center

The Alumni Center portal provides the following benefits to the alumni and organization:

-   **Alumni**
    -   Alumni can conveniently retrieve payroll information, tax documents, and employment verification letters without manual requests or delays. This self-service capability saves time and ensures secure access to sensitive data.
    -   The portal provides tailored job recommendations based on alumni profiles, previous roles, and preferences. Alumni can also track application status and set up notifications for new opportunities.
    -   Alumni can update personal contact details, manage preferences, and control visibility settings \(public/private\) for their profile, ensuring accurate and secure records.
    -   The portal offers access to company news, announcements, and knowledge resources, helping alumni remain updated on organizational developments and industry insights.
-   **Organization**
    -   Maintain relationships with former employees, making it easier to rehire skilled talent when needed.
    -   Reduce recruitment costs and shortens onboarding time, as returning employees are already familiar with company processes.
    -   Enhance organization's brand and networking by offering a structured alumni experience, and creating a positive impression even after employees leave.
    -   Access to a broader and pre-qualified talent pool through job listings and personalized recommendations offered in the alumni portal.

## Content analytics

The Alumni Center provides a separate content analytics tracking profile. For more information, see [Create a Content Analytics tracking profile](../../employee-center/task/ecpro-content-analytics-setup.md).

## Employee to alumni transition

A personal email is required to transition from an employee to an alumnus.

You can perform this transition for individuals or in bulk. To access the Alumni Center, users must have one of the following roles:

-   \[sn\_asc.admin\]
-   \[sn\_asc.manager\]

**Note:**

-   You can add the alumni roles \(sn\_asc.admin\) and \(sn\_asc.manager\) to any user. For more information, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).
-   To be able to login and access all the alumni features, you must be a user in the Alumni table \(sn\_asc\_user\) and not in the User table \(sys\_user\).

## Verify that alumni aren't included in your UU licensing counts

When an employee transitions to an alumnus, and you're using Unrestricted User \(UU\) licensing, you’ll want to avoid inflating user counts when providing services to your alumni. Verify that the following parameters are updated in the \[sys\_user\] table.

-   If you have HRSD Enterprise, with HR or unrestricted users, and you use Alumni Center, you must make users inactive in the \[sys\_user\] table as part of the offboarding process. Once the record is inactivated, it won't be counted in the UU count.

    **Note:** The Alumni Center offboarding workflow creates a new alumni record in the Alumni Users \[sn\_asc\_user\] table that provides alumni access to the Alumni Center services and resources when the User \[sys\_user\] profile is inactive.

-   If you have HRSD Professional, with HR or unrestricted users, and are providing alumni services outside of Alumni Center, to help avoid former employees from being included in the UU count, you must create a custom alumni table. The custom alumni table extends the \[sys\_user\] table. When an employee leaves the organization, you can change the user class of the employee in the \[sys\_user\] table from **User** to the sys class name that corresponds to the custom alumni table.

    **Note:** Creating a custom alumni table to service alumni outside of Alumni Center is considered a custom implementation. Refer to [Create a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateATable.md) for more information.


For additional information, see the [DEF1000205 \| HR User \[KB1125071\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1125071) article in the Now Support Knowledge Base.

## Get started

<table id="table_z4y_wjs_3hc" class="nav-card"><tbody><tr><td>

[Explore ![](../../../reuse/icons/brand-icons/bus-explore.svg) Detailed information on Alumni Center](asc-explore.md)

</td><td>

[Configure ![](../../../reuse/icons/brand-icons/bus-sdlc.svg) Configure the application to get started](asc-configure.md)

</td><td>

[Use ![](../../../reuse/icons/brand-icons/bus-agent-workspace-1.svg) Know how you can use Alumni Center](asc-use.md)

</td></tr></tbody>
</table>## Additional resources

-   Learn more about what's new and changed, see the .
-   Log in to your ServiceNow® account and find additional information about implementing and deploying  features at [Employee Service Management](https://mynow.servicenow.com/now/best-practices/collections/employee-service-management-best-practices).
-   Access real-time courses, self-paced training, and career resources at [ServiceNow University](https://learning.servicenow.com/lxp/en/pages/servicenow)
-   Find useful resources related to your role and explore best practices at the [Customer Success Center](https://www.servicenow.com/success.html).
-   Connect with other Customer Service Management users at [Now Community](https://www.servicenow.com/community/).


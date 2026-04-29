---
title: Embedded Help roles
description: Embedded help content can be targeted to users with a specified role who access the UI page. All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Embedded Help planning, Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Embedded Help roles

Embedded help content can be targeted to users with a specified role who access the UI page. All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page.

For example, if you add embedded help content for the itil role that describes your business process for entering incidents, the itil\_admin role also sees the content. If you write a different topic with the itil\_admin role, the itil\_admin sees that content instead of the itil content.

## Embedded help role priority

The embedded help role priority is stored in the Embedded Help Role Priority \[sys\_embedded\_help\_role\] table. Each role is assigned a default priority order number based on the role name in the Roles \[sys\_user\_role\] table.

<table id="table_txw_bc5_2z"><thead><tr><th>

Order number

</th><th>

Role name

</th></tr></thead><tbody><tr><td>

10

</td><td>

admin Examples: admin, chat\_admin, pa\_admin, survey\_admin

 Exception: itil\_admin

</td></tr><tr><td>

100

</td><td>

manager or itil\_adminExamples: itil\_admin, catalog\_manager, content\_manager, sla\_manager

</td></tr><tr><td>

300

</td><td>

itil \(only\)

</td></tr><tr><td>

1000

</td><td>

All other roles or no role \(ESS user\)Examples: approver\_user, financial\_management\_user, personalize\_form, template\_editor

</td></tr></tbody>
</table>The priority executes from the lowest number to the highest, meaning that embedded help content with no role displays only if no other content is available for the UI page and the user's role. All base system content is targeted to a role unless the content is intended for all users, including ESS users. When you add a role, such as a role for a custom application, it is automatically added to the Embedded Help Role Priority \[sys\_embedded\_help\_role\] table with the appropriate default order. You can modify the order of priority as needed.

If a page requires different help content for different roles, separate topics must be added. For example, users with any role can access the `incident.do` page, and it opens with a view appropriate for their role.

The following list describes how content for different roles can be targeted for the Incident form.

-   **Admin**

    Provides information and links to help with configuring the Incident form.

-   **itil\_admin**

    Describes how to monitor the progress of the incident.

-   **itil**

    Describes how to work on an incident.

-   **No role**

    Explains what the user can review and modify in the Self-Service view of the Incident form.


-   **[Modify embedded help role priority](../task/modify-embedded-help-role-priority.md)**  
You can modify the default order of priority that is assigned to a role in the Embedded Help Role Priority \[sys\_embedded\_help\_role\] table. The priority order determines what embedded help content a user accesses on a UI page, based on roles assigned to the user.

**Parent Topic:**[Embedded Help planning](embedded-help-planning.md)


---
title: Pre-hire experience
description: The Pre-hire experience is a portal that caters to employees who are in transition between the applicant phase and the onboarding phase. This onboarding portal is a solution that facilitates the preboarding process by enabling employees who have been selected by your organization to embark on their first journey.
locale: en-US
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Exploring Journey designer features, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Pre-hire experience

The Pre-hire experience is a portal that caters to employees who are in transition between the applicant phase and the onboarding phase. This onboarding portal is a solution that facilitates the preboarding process by enabling employees who have been selected by your organization to embark on their first journey.

The Pre-hire experience streamlines the preboarding process for newly hired employees. This portal provides your organization with the necessary elements that help newly hired employees integrate quickly into your company's culture. This portal supplies a centralized location for new hires to perform the following tasks so they can be ready for work from their first day on the job:

-   Complete necessary paperwork
-   Review benefits
-   Review HR policies and company resources
-   View training and orientation schedules

The Pre-hire experience assists new hires with connecting seamlessly to team members, mentors, and managers to whom they report so they can foster meaningful workplace relationships. This onboarding portal serves as a gateway into your organization to support new hires with assimilating faster into their roles while grasping the dynamics of their responsibilities.

## Pre-hire experience system requirements

To enable and use the Pre-hire experience, you must satisfy the following minimum system requirements:

-   **Application requirements**
    -   Upgrade the Journey designer application to version 7.0.
    -   Install and activate the Explicit Roles \[com.glide.explicit\_roles\] plugin.
    -   Install and activate Journey Accelerator \[sn\_ja\] Version 6.7.1 or higher.
-   **Software release requirements**

    Upgrade your instance to the Zurich release Patch 1.


## Pre-hire experience security components

To protect the data in your instance, the following components were created for the Pre-hire experience:

-   **Roles**

    The sn\_jny.pre\_hire role is created for the individual who is transitioning from applicant to employee and using the Pre-hire experience to initiate your organization's preboarding process. This role inherits the snc\_external role to restrict access to the sensitive data that resides in your instance.

-   **Access control lists**

    New access controls lists \(ACLs\) were created to provide an added layer of security for the sn\_jny.pre\_hire role. These new ACLs help to avoid the modification of existing ACLs that may be in use by your organization. New ACLs ensure that access to sensitive data is restricted by deterring you from using existing ACLs that provide access to data associated with specific roles. You can navigate to the Access Roles \[sys\_security\_acl\_role\] table to view the list of ACLs that support the sn\_jny.pre\_hire role.


## Lifecycle Events activities for the Pre-hire experience

The following Lifecycle Events activities were created to facilitate the transition of roles through which the employee navigates during the preboarding process:

<table id="table_jfz_w3d_yfc"><thead><tr><th>

Activity name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account/role setup and notification

</td><td>

The Account/role setup and notification activity is used to facilitate the employee's transition from the applicant role to the pre-hire role. This activity is a replacement for the Account setup and notification activity. This activity is nested in the Pre-hire activity set, which is associated with the following Lifecycle Events type: Onboarding \(Demo\). This activity contains the Account setup and notification subflow, which performs the following actions when the Pre-hire activity set is triggered:-   Creates an account for the employee to enable access to the onboarding portal.
-   Adds the sn\_jny.pre\_hire and snc\_external roles to the employee's user record.
-   Sends an email to the employee with a link to the onboarding portal.

The Pre-hire activity set is triggered immediately after you create an onboarding journey for the onboarding employee.

</td></tr><tr><td>

Transition pre-hire to employee

</td><td>

The Transition pre-hire to employee activity is used to facilitate the employee's transition from the pre-hire role to the internal employee role. This activity is nested in the Day 1 activity set, which is associated with the following Lifecycle Events type: Onboarding \(Demo\). This activity contains the Transition to employee subflow, which performs the following actions when the Day 1 activity set is triggered:-   Removes the sn\_jny.pre\_hire and snc\_external roles from the employee's user record.
-   Adds the snc\_internal role to the employee's user record.

The Day 1 activity set is triggered when the date in the **Employment start date** field in the HR profile record of the onboarding employee is equal to the system date.

</td></tr></tbody>
</table>## Pre-hire experience widgets

The Pre-hire experience is composed of the following widgets to help your onboarding employee become acclimated to their new role and environment:

<table id="table_yxp_3jd_yfc"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Getting started resources

</td><td>

This widget contains quick links for accessing internal and external resources. Administrators can provide links to knowledge base articles, catalog items, pages, or other pertinent information contained in your organization's repository. Administrators can configure the links that appear in this widget.

</td></tr><tr><td>

Onboarding journey

</td><td>

This widget contains a link that onboarding employees can select to view and complete the tasks associated with their preboarding journey.

</td></tr><tr><td>

Our culture

</td><td>

This widget contains rich content, such as videos, images, or other forms of engaging media to enhance the employee's onboarding experience. Administrators can configure the content that appears in this widget by accessing the Our culture content record. The Our culture content record resides in the Content \[sn\_cd\_content\_base\] table.

</td></tr><tr><td>

Start onboarding

</td><td>

This widget is a banner that's used to welcome the onboarding employee to your organization. Administrators can configure the content and design associated with the banner to meet the needs of your organization. You must access the Start Onboarding record to configure the components associated with this banner. The Start Onboarding record resides in the Content \[sn\_cd\_content\_base\] table.

</td></tr><tr><td>

Your onboarding team

</td><td>

This widget reflects the employee's onboarding team. A list of the following individuals and teams appear in this widget:-   The onboarding specialist. The onboarding specialist is the individual to whom the corresponding Lifecycle Events case is assigned.
-   The manager to whom the employee reports.
-   The mentor assigned to aid the employee's growth and development.
-   The IT help desk.

</td></tr></tbody>
</table>**Related topics**  


[Enable and configure the Pre-hire Experience](jny-pre-hire-enable-configure.md)


---
title: Create roles in the Oracle HCM Cloud
description: Create roles to execute all actions in the Oracle HCM spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create roles in the Oracle HCM Cloud

Create roles to execute all actions in the Oracle HCM spoke.

## Before you begin

Role required: admin

Access to the Oracle HCM Cloud tenant with the IT Security Manager role.

## About this task

You need both seeded and custom roles in the Oracle HCM Cloud. The table provides the roles that you need.

|Role Name|Role Code|
|---------|---------|
|Application Administrator|ORA\_FND\_APPLICATION\_ADMINISTRATOR\_JOB|
|Application Implementation Administrator|ORA\_ASM\_APPLICATION\_IMPLEMENTATION\_ADMIN\_ABSTRACT|
|Application Implementation Consultant|ORA\_ASM\_APPLICATION\_IMPLEMENTATION\_CONSULTANT\_JOB|
|Application Implementation Manager|ORA\_ASM\_APPLICATION\_IMPLEMENTATION\_MANAGER\_JOB|
|Employee\_SN|PER\_EMPLOYEE\_ABSTRACT\_SN|
|Human Capital Management Integration Specialist\_SN|HUMAN\_CAPITAL\_MANAGEMENT\_INTEGRATION\_SPECIALIST\_SN\_DATA|
|Human Resource Analyst\_ViewAll|PER\_HUMAN\_RESOURCE\_ANALYST\_JOB\_VIEWALL|
|Human Resource Manager\_ViewAll|PER\_HUMAN\_RESOURCE\_MANAGER\_JOB\_VIEWALL|
|Human Resource Specialist\_ViewAll|PER\_HUMAN\_RESOURCE\_SPECIALIST\_JOB\_VIEWALL|
|Line Manager\_SN|PER\_LINE\_MANAGER\_ABSTRACT\_CUSTOM|
|Product Management VP|ORA\_ACE\_PRODUCT\_MANAGEMENT\_VP\_JOB|
|Product Manager|ORA\_EGP\_PRODUCT\_MANAGER\_JOB|
|Recruiter|ORA\_IRC\_RECRUITER\_JOB|
|Recruiting Administrator|ORA\_PER\_RECRUITING\_ADMINISTRATOR\_JOB|
|Recruiting Agent|ORA\_IRC\_RECRUITING\_AGENT\_JOB|
|Recruiting Manager|ORA\_IRC\_RECRUITING\_MANAGER\_JOB|
|SN\_Access Opportunity Marketplace|SN\_Access\_Opportunity\_Marketplace|

## Procedure

1.  Log in to the Oracle HCM Cloud.

2.  On the left panel, navigate to **Tools** &gt; **Security Console**.

3.  Select Roles.

4.  Select **Create Role**.

    ![Create Role button.](../image/oracle-hcm-spoke-create-role-button.png)

5.  In the Search field, enter the role name and press **Enter**.

    The search results display the role name as one of the results.

6.  Select the Actions button and select **Copy Role**.

    ![Copy Role option.](../image/oracle-hcm-spoke-copy-role-option.png)

7.  In the Copy Options window, select **Copy Role**.

8.  In the Role Name field, enter the role name and select **Next**.

9.  To move to the next pages and review the information shown, select **Next** on the subsequent pages.

    Page information

    1.  Basic information
    2.  Function Security Policies
    3.  Data Security Policies
    4.  Role Hierarchy
    5.  Segregation of Duties
    6.  Users
    7.  Summary
    ![Next button.](../image/oracle-hcm-spoke-next-button.png)

10. Select **Submit and Close**.

11. Select your profile icon and then select Settings and Actions.

    ![Settings and Actions option.](../image/oracle-hcm-spoke-settings-and-actions.png)

12. Select **Setup and Maintenance**.

13. Select the task and then select Search.

    ![Task and Search option.](../image/oracle-hcm-spoke-task-search-option.png)

14. In the Search field, enter `Manage Data Role and Security Profiles` and press **Enter**.

    ![Search input.](../image/oracle-hcm-spoke-search-ops.png)

15. In the Role field, enter the role name and select **Edit**.

    ![Edit button.](../image/oracle-hcm-spoke-edit.png)

16. Select **Next**.

17. Provide inputs for the required fields and select **Next**.

    ![Required fields.](../image/oracle-hcm-required-fields.png)

18. To navigate through the next few pages, select **Next** on the subsequent pages.

19. Select **Submit**.

20. Assign the role to the user.

    1.  On the left panel, navigate to **Tools** &gt; **Security Console**.

    2.  On the left panel, select Users.

        ![Users link.](../image/oracle-hcm-users-left-nav.png)

    3.  In the User Name field, enter a user name and select the search icon.

        The user name and its details are displayed.

        ![User details.](../image/oracle-hcm-spoke-user-details.png)

    4.  Select the user name link.

    5.  On the Edit User Account page, select **Edit**.

    6.  On the Edit User Account page, select **Add Role**.

    7.  In the Search field, ensure that the Roles option is selected and then enter the role name.

    8.  Select **Add Role Membership**.

    9.  Select **Done**.

    10. Select **Save and Close**.



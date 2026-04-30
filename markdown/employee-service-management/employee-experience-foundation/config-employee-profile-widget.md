---
title: Configure the Employee Profile overview widget
description: Configure your instance options to control the appearance of the Employee Profile overview widget, such as the title, number of items to display, icons, and what category of items you want to view.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
breadcrumb: [Employee profile, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Configure the Employee Profile overview widget

Configure your instance options to control the appearance of the Employee Profile overview widget, such as the title, number of items to display, icons, and what category of items you want to view.

## Before you begin

Role required: sn\_employee.admin

## About this task

The Employee Profile overview widget displays useful information about an employee enabling you to view information that is most relevant to you. You can have a comprehensive view of the employee information to drive business decisions, create intelligent workflows, and deliver personalization across end-user facing applications. Using the employee profile, you can do the following:

-   Organize the employee profile into sections.
-   Add fields to display in a section.
-   Select fields from the Employee, User, and HR profiles.

## Procedure

1.  Navigate to **All** &gt; **Employee Profile** &gt; **Overview UI Configuration**.

2.  From the Overview Sections list, select **New**.

3.  On the Overview Section form, fill in the fields.

    For a description of the field values, see [Employee Profile Overview section form](../reference/profile-overview-section-form.md).

4.  Select **Save**.

    If you select **Submit**, you're redirected to the previous page containing the list of all sections.

    The new section is created. You can proceed to the associated fields suitable for the section.

5.  In the Overview Section Fields section, select **New**.

    A new record page opens.

6.  Select **Field Name**, then select an element from the tree based on your preference.

7.  Select the appropriate Field visibility option based on your preferences.

    For example, you can select the visibility of your preferred pronoun or any private information according to your choice.

    -   Employee only
    -   Manager only
    -   Employee and Manager
    -   Everyone
    -   Manager and Other Managers
    -   Employee, Manager and Other Managers
    -   User Criteria: Provide the access only to specific users, groups, and roles with the user criteria. The field is visible to the users based on:
        -   Available For: User group for whom the field is visible. Define and select the user group based on your business needs.
        -   Not Available For: User group for whom the field isn’t visible. Define and select the user group based on your business needs.
    Values that are defined in the Not Available For group take precedence over values defined in the Available For group. If both values aren’t defined, the field is visible to all users. For more information on field visibility based on user criteria, see [User Criteria output](../reference/user-criteria-output.md).

    **Note:** Use the user criteria cautiously because the profile page load time can take longer based on your criteria.

8.  From the available list, select a suitable icon for the field.

9.  Select **Submit**.


## What to do next

You can add the following default sections and associated fields for your employee profile:

-   About
-   Bio
-   Personal information
-   Contact details
-   Employment details
-   My team

Configure any additional sections based on your business needs.

You can edit or remove the banner by navigating to **All** &gt; **Employee Profile** &gt; **Background banner**.

**Related topics**  


[Modify the employee profile widget display](config-employee-profile-instance-options.md)

[Employee profile](../concept/employee-profile-portal.md)


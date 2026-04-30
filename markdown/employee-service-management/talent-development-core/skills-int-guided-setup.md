---
title: Skills Foundation guided setup
description: Install and set up Skills Foundation and Company Job Architecture confidently with step-by-step instructions using guided setup.
locale: en-US
release: zurich
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Skills Foundation guided setup

Install and set up Skills Foundation and Company Job Architecture confidently with step-by-step instructions using guided setup.

## Before you begin

Role required: sn\_skills\_int.admin

The advantages of using the guided setup for Skills Foundation are:

-   A single interface enables you to access in one place all the information necessary for installation like data loading and creating roles.
-   Provides guidance for planning the roll-out of the application and performing the basic configuration.
-   Configuration activities are organized into categories for more efficient access.
-   Enables you to track your implementation progress.

## Procedure

1.  Navigate to **All** &gt; **Skills Foundation** &gt; **Guided Setup**.

2.  On the welcome page, select **Continue**.

3.  Read through the checklist and keep the files handy.

    -   Prepare the Job Architecture Data for the installation.
    -   Prepare the list of custom skills specific to your organization.
    -   Prepare employee mappings with Job Architecture Data from your organization.
4.  Select **Get started**.

5.  Expand any category to view detailed status and related tasks.

    -   Select **Start** button on each setup category to start the configuration.
    -   Select **Mark as complete** after you finish a category.
    -   Select **Skip** to leave out a category.
    -   Select **Back** to go back to the previous category.
<table id="table_jzt_xwp_rfc"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skills Foundation Onboarding

</td><td>

Learn about the concepts and working of Skills Foundation through product documentation.Related task - Product Documentation.

</td></tr><tr><td>

Set up Relevant Plugin\(s\)

</td><td>

Install the optional plugins that enhance the Skills Foundation experience.Related tasks:

-   Skills Workspace plugin.
-   Proactive Prompts plugin.


</td></tr><tr><td>

Set up Access Roles

</td><td>

Assign roles to employees in your organization to ensure appropriate access in Skills Foundation.Related task - Assign Access Roles to users.

</td></tr><tr><td>

Skills Management

</td><td>

Upload your skills data into your ServiceNow instance. These skills are the basis for all the activities in your Skills Foundation application.Related task - Onboard Custom Skills. For more information, see [Load your custom skills into Skills Foundation](skills-int-load-custom-skills.md).

</td></tr><tr><td>

Company Job Architecture

</td><td>

Upload your existing company job architecture data, set the growth path using job level progressions, and automatically assign the proficiency for each skill across role levels, providing a structure to the imported data. Related tasks:

-   Upload Company Job Architecture. For more information, see [Load job architecture data into your ServiceNow instance](load-data-skills-tables.md).
-   Create Job Level Progressions. For more information, see [Creating a job level progression](skills-int-job-level-progress.md).
-   Create Proficiency Autofill Configurations. For more information, see [Set the job proficiency level automatically](proficiency-autofill-config.md).


</td></tr><tr><td>

Employee Profile Upload and Setup

</td><td>

Upload the employee data and set up the roles and profiles required in your organization to associate jobs to the employees based on roles and skills. This category is crucial in making the employee and job data connection.Related tasks - Upload Employee Data - Uploading an excel sheet with employee data or manually map job profile with the employee. For more information, see [Adding a job profile to the employee](map-employee-job-profile.md).

**Note:**

-   If the Human Resources Scoped App \(sn\_hr\_core\) is installed, all setup steps like uploading employee data, adding profiles, and assigning roles are completed automatically.
-   You must have Human Resources Scoped App: Core \(sn\_hr\_core\) plugin on Australia family release. For earlier releases, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. Approve the RCA and re-import the skills manually. You can also manually create the required RCA to avoid re-work prior to skills import.


</td></tr><tr><td>

Configure System Properties

</td><td>

Control various Skills Foundation features using these system properties.Related task - Enable Skills Foundation for Employee Growth and Development.

</td></tr></tbody>
</table>6.  Select **Complete** after you have finished all the tasks within all categories.



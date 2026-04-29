---
title: Workday spoke integration in Skills Foundation
description: Import skills from Workday Learning and Workday HR spoke into your Skills Foundation application using the skills import flow.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Skills import, Skills Workspace, Exploring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Workday spoke integration in Skills Foundation

Import skills from Workday Learning and Workday HR spoke into your Skills Foundation application using the skills import flow.

Prerequisites for Workday Spoke integration.

-   Required plugins - Workday Learning Spoke and Workday HR spoke.
-   After the Workday HR spoke plugin is installed and configured, set the following properties:
    -   sn\_skills\_int.workday\_hr\_report\_owner: The workday username of the report owner.
    -   sn\_skills\_int.workday\_hr\_look\_up\_skills\_report: The “All skills” report.
    -   sn\_skills\_int.workday\_hr\_look\_up\_employee\_skills\_report: The “User skills” report.

The integration options available are:

-   Workday - All: Imports all skills found in Workday. If you want to import only a subset of skills, modify the report used for the import. This option is available when any one of the Workday Learning Spoke or Workday HR Spoke plugins is installed.
-   Workday - Course skills: Imports course-related skills depending on the learning courses that you have in Workday. This option is available when the Workday Learning Spoke plugin is installed.
-   Workday - User skills: Imports all skills employees have in their Workday profiles. This option is available when the Workday HR Spoke plugin is installed.

    Internally, the user skills are imported in the following steps:

    1.  Skills \(general definitions\) are imported. This step is similar to the Workday - All import.
    2.  Skills are added to employee profiles.

        **Note:** To add user skills to the employee profiles, make sure the sys\_user.employee\_number values match with the workdays employee numbers.

    3.  Skill levels are imported. The following defaults are taken for the skill levels:

        -   Minimum level: 1
        -   Maximum level: 5
        -   Skill Level Type for newly created skills: General
        However, these defaults can be changed by modifying the import flow.

    **Note:** To import Skill levels, Skills Cloud must be enabled in Workday.



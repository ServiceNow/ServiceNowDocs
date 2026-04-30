---
title: Career tab in Employee Center
description: View update, and manage all aspects of your career using the Career tab in Employee Center.
locale: en-US
release: yokohama
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Exploring Skills Foundation, Skills Foundation, Talent Development, Employee Service Management]
---

# Career tab in Employee Center

View update, and manage all aspects of your career using the **Career** tab in Employee Center.

Role required: sn\_skills\_int.emp

The **Career** tab contains various widgets to manage your work data like, experience, aspirations, and skills in your profile.

**Note:** The **Career** tab and the widgets are activated with the installation of the Skills Foundation application driven by the sn\_skills\_int.enable\_skills property. For more information, see [Add the Career tab and enable the Skills widget in the Employee Profile](../task/add-career-tab.md).

## Role details

View your business title, role group and your role specialty that accurately reflect your position in the organization and enable you to get personalized skill recommendations.

![image.skills-role-details]

**Note:**

-   The Business title is derived from the Employee position table \(sn\_employee\_position\) where the primary role is marked as true because an employee can have multiple job profiles.
-   The Employee position table updates whenever the HR profile table \(sn\_skills\_int\_job\_profile\) is updated.
-   A scheduled job synchronizes the HR jobs table \(sn\_hr\_core.job\) and HR profiles table, ensuring accurate data during integration.
-   The Job code in the Job profile table \(sn\_skills\_int\_job\_profile\) and HR jobs table \(sn\_hr\_core.job\) should match for the Role specialty to be populated.

## Shared aspirations

View objectives that enable you to excel in your career and also promote growth in your organization. Aspirations can be based on your interest, skill, or role. For more information on aspirations, see [Create a Talent Development Aspiration](../../employee-service-management/task/egd-create-aspirations.md).

![Shared aspirations](../image/skills-int-shared-aspirations.png)

## Achievements

Import and view your accomplishments as credentials from Credly by syncing the badges into your organization’s Credly account.

![Credentials](../image/career-achievments-credentials.png)

## Upload Resume/LinkedIn Profile

Get your existing skill set quickly by uploading your resume or LinkedIn profile to your Employee Profile using the **Upload resume or LinkedIn profile** button. For more information on the import process, see [Import skills from your resume or LinkedIn profile](../task/import-skills-from-resume.md).

## Skills

Manage your skills data by adding skills, removing skills, adding skills via a role level, and updating the proficiencies of the skills. Use the skills profile to understand your skill gaps and learn new skills to stay relevant to your role in your organization. A skill in your profile is displayed as an individual UI component called Skill pill.

![Skill pill](../image/skill-widget-menu.png)

|UI elements|Description|
|-----------|-----------|
|1|A numerical indication of your proficiency level in that skill.|
|2|Skill name.|
|3|A green tick on the skill signifies validation by your manager, indicating their approval of your proficiency in that skill. After a skill is validated, you can only increase the proficiency level of the skill, you can’t decrease the proficiency level or delete the skill from the profile. For more information on how to validate a skill, see [Validate skills in Manager Hub](../task/skills-intelligence-manager-hub.md).|
|4|Menu to access proficiency level or delete options. The skill proficiency level indicates your level of competency in that skill. To learn how to change a skill proficiency level, see [Update your skill proficiency level](../task/update-skill-proficiency-level.md).|

There are three sections within the skills widget. All the skills within these sections are sorted by the highest \(required\) to the lowest \(recommended\) skill rating.![Skills profile](../image/manage-skills-profile.png)

-   **Essential skills**

    This section displays the skills that are derived from your associated role group based on your current position. You can use the essential skills section to determine the skills required for the role and see the recommended learning opportunities to bridge the skill gaps. You can also focus on excelling in the skills and pursue growth opportunities. For more information, see [Selecting a Role specialty](../task/select-role-speciality.md).

-   **Additional skills**

    Skills in your profile that are not part of your role level are displayed in the additional skills section. The skills that have been derived from your resume or added manually using the **Add skill** option are also part of the additional skills. For more information, see [Add skills by using the skill recommender](../task/add-skills-using-skill-recommender.md).

-   **Recommended skills**

    The Recommended skills section displays the additional skills that are related to your profile. These details are based on your role and existing profile.


## Experience

Displays the experience journey in your organization with the roles that you have taken up and the duration in each role along with the starting and ending months.

![Experience](../image/skills-int-experience.png)


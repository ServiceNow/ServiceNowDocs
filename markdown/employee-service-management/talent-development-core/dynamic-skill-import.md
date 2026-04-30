---
title: Dynamic skill import for harmonization
description: Import, review, and harmonize the new skills brought in from third-party sources \(currently only through Credly\) into the skills library \(cmn\_skills table\).
locale: en-US
release: yokohama
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2025-04-11"
reading_time_minutes: 2
breadcrumb: [Skills import, Skills Workspace, Exploring Skills Foundation, Skills Foundation, Talent Development, Employee Service Management]
---

# Dynamic skill import for harmonization

Import, review, and harmonize the new skills brought in from third-party sources \(currently only through Credly\) into the skills library \(cmn\_skills table\).

## Before you begin

Role required: sn\_skills\_int.admin

Let's see how dynamic skills are processed in the context of Credly:

-   Skills associated with the Credly badges are analyzed.
-   Skills are validated to check if they don't already exist in the skills library and also not mapped to an existing skill.
-   New skills are pushed to the queue pipeline for harmonization.

For example, an employee Abel Tuter receives a badge which has three skills - Java, Python, and J2EE. The system checks the skills library \(cmn\_skills table\) to determine the skills that already exist. Java and J2EE are already present in the system, so they are immediately added to the Abel Tuter’s employee profile. Python skill is not available in the system, so it’s moved to the queue for skill harmonization. Once the admin reviews and harmonizes the Python skill, it’s also added to the skills library and Abel Tuter’s employee profile.

Working of skill mapping - Skill mapping is the process of linking a skill, either imported or from a badge to an existing skill in the skill library. The mapping can be done automatically or manually, to avoid duplicates.

-   System Mapping \(Automatic\): If a new skill, for example, Java 1.8 is similar to the existing skill, for example, Java in the cmn\_skills table, the system detects it as a duplicate and maps it automatically.
-   Admin Mapping \(Manual\): An administrator can manually map a skill. For instance, if Python is imported, the admin might map it to Jupyter Notebook depending on the relevance.

Important behavior - When a skill is mapped, a new entry is not created for the imported skill. Instead, the existing skill is used in the employee profile. For example, if Java 1.8 is mapped to Java, and Python is mapped to Jupyter Notebook, only Java and Jupyter Notebook appear in the employee profile, not Java 1.8 and Python.

**Note:** You can also customize your skill data and use it as a source by calling specific APIs.

## Procedure

1.  Navigate to **All** &gt; **Skills Workspace**.

2.  Select the Lists icon \(![Lists icon](../../ohs-incident-management/image/list-icon-hs.png)\).

3.  Select **Import history** &gt; **Queue**.

4.  Select one or more records for the import.

    **Note:** Use **Select all** option to bulk import the skills. Alternatively, use the Custom import option in the Skill import playbook to import all the skills in the dynamic queue. For more information, see [Bring in skills through Skills import](import-and-validate-custom-skills-onboarding.md).

5.  Select the **Edit** option to update missing data in the Description, Skill import tracker, Level type, and Source fields.

6.  Select **Update**.

7.  Select **Import**.

    You are redirected to the Playbook experience and the custom import option is selected automatically.

8.  Select **Next**.

    Follow the next steps to complete the import. For more information, see [Bring in skills through Skills import](import-and-validate-custom-skills-onboarding.md).


## Result

The harmonized new skills are added to the skills library \(cmn\_skills table\) and updated in the credentials badge skills metadata. For more information, see [Achievements and Credentials in Talent Development Core](../../employee-service-management/concept/achievements-and-credentials-in-td.md).


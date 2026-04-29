---
title: Achievements and Credentials in Talent Development Core
description: View all types of user credentials acquired outside the current organization \(currently populated from Credly\) in Achievements and Credentials.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer and maintain the Talent Development Core app, Talent Development Core, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Achievements and Credentials in Talent Development Core

View all types of user credentials acquired outside the current organization \(currently populated from Credly\) in Achievements and Credentials.

Achievement credentials, like badges, are digital or physical symbols that recognize and verify an individual's accomplishment, skill, or participation in a specific activity or goal.

The credentials imported from Credly have skills data, and other metadata such as user and badge information. Skills associated with the Credly badges are analyzed as follows:

-   If Credly badge skills match exactly or mapped to the skills in the skills library, they are added to the employee profile, in case the employee doesn't already have them.
-   If a skill exists in the employee profile and also receives a badge associated with the same skill, then the employee gets a Prompt \(Review Skills Profile Prompt\) to update the skill's proficiency. For more information, see [Proactive Prompts for Skills Foundation](../../skills-intelligence/concept/proactive-prompts-skills.md).
-   If the skill is new, it’s added to the queue pipeline for harmonization. For more information, see [Dynamic skill import for harmonization](../../skills-intelligence/task/dynamic-skill-import.md).
-   The harmonized new skills are added to the skills library \(cmn\_skills table\) and updated in the credential badge skills metadata after the import is complete.
-   Employee's skill profile is updated with the new skill\(s\) linked to their earned badge.

-   **[View achievement credential templates](../task/view-ach-credential-templates.md)**  
View achievement credential templates in Achievements and Credentials.

**Parent Topic:**[Administer and maintain the Talent Development Core app](egd-administration.md)


---
title: SAP SuccessFactors integration Skills Foundation
description: Import skills \(skill data and user-specific skill data\) from SAP SuccessFactors into your Skills Foundation application using the skills import flow to maintain data consistency.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Skills import, Skills Workspace, Exploring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# SAP SuccessFactors integration Skills Foundation

Import skills \(skill data and user-specific skill data\) from SAP SuccessFactors into your Skills Foundation application using the skills import flow to maintain data consistency.

Prerequisites for SAP SuccessFactors integration.

-   Upgrade to SAP SuccessFactors Spoke\(sn\_successfactors\) plugin v 4.6.1-7 or later.
-   You must have Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin on Australia family release.
-   For earlier releases, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. Approve the RCA and re-import the skills manually. You can also manually create the required RCA to avoid re-work prior to skills import.
-   After the SAP SuccessFactors plugin is installed and configured, set the following properties:
    -   sn\_skills\_int.default\_skill\_level\_type: The sys\_id of a skill level type has unique number in the Value field. In case the Value field has an invalid number, an error message is displayed saying that the user has to restart the flow after providing the correct value.
    -   sn\_skills\_int.allow\_import\_to\_override\_skill\_level: This system property when set to True will override the proficiency of the existing skills of an employee. The highest proficiency whether it's from the import or the existing proficiency value will be retained.

        If the system property is False, there is will be no change in the proficiency values, but if a skill is validated for an employee, the same will be reflected in employee profile after the import.


The integration options available are:

-   SuccessFactors - All: Imports all the skills from SuccessFactors.
-   SuccessFactors - User skills: Imports all the skills from the user profiles SuccessFactors. After the import and harmonization is complete, the skills are added to the respective employee profiles and also validated by the manager.


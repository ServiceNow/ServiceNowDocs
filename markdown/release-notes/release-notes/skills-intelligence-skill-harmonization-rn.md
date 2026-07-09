---
title: Skills Foundation release notes
description: The ServiceNow Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Skills Foundation release notes

The ServiceNow® Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Yokohama release.

## Skills Foundation highlights for the Yokohama release

-   Skill Harmonization lets you import and combines skills from the external learning management system \(LMS\) to have one source for skills.
-   Integrating Workday Learning skills and Workday Employee skills into the current import flow and relate them to the respective employees in the ServiceNow system.
-   Support for dynamic skills import requests from Credly \(OOTB source\) and other external sources. The skills are verified with the skills library \(exact or mapped match\), and new skills are added to the queue for processing. The harmonized skills are then linked back to the source using metadata.

See [Skills Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/skills-intelligence.md) for more information.

**Important:** Skills Foundation is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Bring in skills through Skills import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/import-and-validate-custom-skills-onboarding.md)**

    Import skill sets from the Workday Employee spoke using the existing import flow in the Skills Workspace. The imported sets of skills can either be the full list of skills from a given input or a subset.

    Import skills data from the external systems with the new Integration option in the Skills import.

    Automatically identify skills that are similar to the existing skills in the library \(cmn\_skills\) and display them in the Existing matches section.

    Import skills from any external source and harmonize them with the new **Custom import** option.


## Activation information

Install Skills Foundation by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Skills Workspace plugin \(sn\_skills\_int\_ws\) must be installed to access the workspace experience.

## Related ServiceNow applications and features

-   **[Workday Learning Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/wd-learning-spk.md)**

    Use the Workday Learning spoke to import course related skills from the Workday Learning instance to your ServiceNow instance.

-   **[Workday HR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/workday-hr-spoke.md)**

    Use the Workday HR spoke to import all skills users have in their Workday profiles to your ServiceNow instance.


**Parent Topic:**[Talent Development release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/employee-growth-development-landing.md)


---
title: Health and Safety Core release notes
description: Version history for the Health and Safety Core on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-health-safety-incident-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Health and Safety release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Health and Safety Core release notes

Version history for the Health and Safety Core on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.2.0 - June 2026**
    -   New: Contextual Action Planner to create and manage actions in context while reviewing a Health and Safety record
    -   Fixed:
        -   Scheduled job issue where the H&amp;S pattern detection job was hitting LLM rate limits
        -   Missing confirmation message after selecting the "Copy Action" button
-   **Version 13.1.0 - May 2026**
    -   New:
        -   L1 automated workers \(user and worker\) and worker template for Health and Safety.
        -   Task and work assignment and reassignment in L1 automated workers for Health and Safety.
        -   Worker and search profile for L1 automated workers in Health and Safety.
        -   UI changes for Worker card and Now Assist Context Menu \(to post draft notes\).
-   **Version 13.0.1 - March 2026**

    Fixed: Resolved ACL and localization \(L10N\) warnings.

-   **Version 12.1.0 - January 2026**

    Changed: Renamed the Migrate records button in the Document migration tool

-   **Version 12.0.0 - December 2025**
    -   New:
        -   Document management
            -   Added a global list of Health and Safety documents.
            -   Integrated ServiceNow Document Management with Health and Safety applications.
            -   Implemented a migration tool for moving documents to new document management.
        -   Made knowledge articles available to Health and Safety users.
        -   Added bulk management options for Health and Safety core records.
        -   Enabled clearing of mappings in PDF report mapping.
        -   Moved assignment roles and groups into application data for easier management.
        -   Added connectors for improved integration with Health and Safety records.
    -   Fixed:
        -   Improved support for encoded queries in Health and Safety core features.
        -   Fixed issues when working with large PDF report templates.
        -   Fixed comparison functions for knowledge base articles.
        -   Addressed certificate installation errors.
        -   Improved document accessibility across different records.
        -   Fixed access issues for Health and Safety profiles.
        -   Updated PDF library for enhanced security.
        -   Ensured collection type records are available when needed.
        -   Fixed blank spaces in risk analyses when using demo data.
        -   Improved accessibility hints for creating new controls.
-   **Version 11.0.1 - August 2025**
    -   Changed:
        -   Replaced the landing page dashboard with the following tabs:
            -   Highlights
            -   Incident management
            -   Risk management
        -   Changed the dashboard filters to align with the WSD location model and included a date range filter
-   **Version 10.0.0 - May 2025**
    -   Changed:
        -   This Health and Safety Incident Management application has been renamed to Health and Safety Core, which now includes the data model and core functionality for all Health and Safety applications.
        -   A new separate listing called Health and Safety Incident Management is now available on ServiceNow store.
        -   Both Health and Safety Core and Health and Safety Incident Management are listed as a v10 version on the store.
-   **Version 9.0.0 - February 2025**
    -   New:
        -   Safety meetings list:
            -   Keep track of health and safety related meetings and attendees
            -   Meeting manager role
            -   Sensitive meeting flag and new sensitive meeting content role
        -   Flexible total hours worked framework enabling total hours for an establishment to be broken up into different periods in a year
    -   Removed: Auto population of dates on incident catalog items in Employee Center
    -   Fixed:
        -   Case tab not shown under H&amp;S user profile when only Health and Safety Incident Management and Health and Safety Case Management were installed
        -   Home page not showing for certain demo users
        -   Various accessibility issues
        -   Issue with incident and observation reports showing in the incorrect location
        -   Issue with conflicting error message showing when generating OSHA reports
-   **Version 8.0.1 - December 2024**

    Changed: Removed the auto-assignment of the HR case to the user who created it from Health and Safety Incident Management.

-   **Version 8.0.0 - November 2024**
    -   New:
        -   Contractor Management:
            -   Contractor Onboarding
        -   Integration with Critical Event Management \(CEM\) to associate safety incidents with any emergencies you are managing in CEM.
        -   Learning actions:
            -   Assign training materials as an action
        -   Dot walking without scripting added to the report mapping tool
        -   Action tracking enabled on the Employee Center in My Tasks list
        -   Injured party option enabled for any person type
        -   Public type option added to Injury and illness
        -   Location reference added to the establishment list
    -   Fixed:
        -   Missing incident details on My Requests on mobile
        -   Missing quick links in Employee Center on Washington DC and Xanadu
        -   Incorrect ACLs applied to a few demo users
        -   Missing button on private notes/comments in the contextual sidebar when enlarged
        -   l10n and i18n issues on the injury picker in the Employee Center
        -   Date time picker on injury/illness forms
-   **Version 7.0.0 - August 2024**
    -   New:
        -   Shareable actions. Actions can be copied and shared with other teams as standalone actions. This allows teams to help prevent the same or similar incidents from happening at other locations or with other teams.
        -   Improved injury picker. Includes more body parts.
        -   Injury picker has been added to the Employee Center Advanced Incident form.
        -   Advanced incident reporting has been enabled on Now Mobile.
    -   Fixed:
        -   Issues with deleting/editing injured body parts.
        -   Issues with saving injury date/time in the classic view.
        -   Injury and illness info missing when the visitor plugin was not installed.
        -   Advanced incident form people involved issues.
        -   Issues with incident and observation location field showing values that were removed.
        -   Incorrect default value field on body picker.
        -   Injury records ordering fixed so that the newest is on top.
        -   Unused back button on body picker when using tab navigation.
        -   l10n and i18n prefixes fixed.
        -   Performance issue with location model tree picker in Employee Center.
        -   Removed filter on Assigned to the field on the action form.
        -   Removed duplicate error messages on the injury/illness form.
        -   Fixed incorrect tooltips when generating OSHA reports.
        -   Fixed info boxes in lists on the playbook.
        -   Severity value indicator showing incorrectly until the record is saved.
-   **Version 6.0.0 - May 2024**
    -   New:
        -   Report field mapping: Safety teams can import any fillable PDF and map its fields to incident, observation, or injury/illness records. Reports can be exported using the imported PDF template with the mapped fields auto-filled.
        -   Advanced and basic incident reporting in the Employee Center: An additional incident intake form that enables employees to add more details to the initial report, such as injury details and hazards.
        -   Location field added to all Health and Safety Incident Management lists.
    -   Changed: "Near miss" category moved from the observation record to the incident record so that a full investigation playbook is available for near misses.
    -   Fixed:
        -   Localization issues
        -   Mobile performance issues
        -   Inability to log total hours per establishment
        -   Visibility of Hierarchy of controls and Risk category lists in All menu
        -   Field validation issues on injury and illness
        -   SQL error when installing
        -   Employee Center menu options in Washington DC
        -   ACL configuration issues
        -   Date and time discrepancies between forms and lists
    -   Removed:
        -   Near miss category from observation record
        -   Empty ACLs
-   **Version 5.0.0 - February 2024**
    -   New:
        -   "Other non-recordable" choice added to the injury/illness classification.
        -   A unified workspace that includes the Health and Safety Risk Management capabilities when that application is installed.
        -   Date range and location filters added to the Health and Safety Workspace landing page dashboard.
        -   New Employee Center icons.
    -   Changed:
        -   Hospital address entry fields changed to free text.
        -   Actions can be assigned to any user.
        -   Only the date field can be used when "Unsure of time" is chosen in the Describe Injury or Illness playbook step.
        -   Injury or illness step is skippable in the incident playbook.
    -   Fixed: All fixes from v4 patch release.
-   **Version 4.0.3 - December 2023**
    -   New: A system property that enables users to turn off the use of Playbook for reporting Health and Safety incidents.
    -   Changed: Enabled free text entry for hospital address in injury and illness reports in Health and Safety incidents.
-   **Version 4.0.2 - September 2023**
    -   Fixed:
        -   Timezone offset issues when upgrading.
        -   Added missing field required for OSHA compliance.
        -   Fixed missing data on OSHA exports when using OSHA plugin.
-   **Version 4.0.0 - August 2023**
    -   New:
        -   Incident Playbook provides step-by-step guidance for resolving safety incidents through sequences of activities and tasks.
        -   Incident Overview tab that enables a centralized view of all the important details about a safety incident.
        -   Roles: New roles that are aligned with KPIs when viewing and interacting with Health and Safety landing page:
            -   Safety operations role that can view the supervisor landing page and has limited access to safety records.
            -   Safety exec role that can view the executive landing page and has read-only access to lists and data.
        -   Landing Pages:
            -   Safety ops landing page with KPIs, and a layout to prioritize the information most important to personas such as line managers and supervisors.
            -   Safety exec landing page with KPIs, and a layout to prioritize the information most important to personas such as directors and company executives.
        -   Public people involved are included in the Incident Playbook, enabling non-employees and non-visitors to be added as involved parties.
        -   Domain separated lists
    -   Changed:
        -   Simplified incident data model:
            -   Incident and investigation have been merged to enable the playbook experience.
            -   Simplified the injury and illness logging to allow for only one injury record per incident.
    -   Removed: Investigation workbench
-   **Version 3.0.0 - May 2023**
    -   New:
        -   Enabled tracking and notifications for H&amp;S incidents in Employee Center My Requests
        -   Drill-down capability added to Workspace landing page dashboard
        -   Various navigation and layout improvements such as:
            -   Hyperlinks to parent records
            -   Hyperlinks between Incident and Observations in Employee Center
            -   Descriptive tooltips on each record tab
        -   Added support for internationalization
    -   Fixed:
        -   ACL issues
        -   Issues related to incident occurrence date and time
        -   Workbench loading issues
        -   SQL related exceptions
        -   Localization issues
        -   RCA UI issues
        -   Affected employee issues
    -   Removed: Tokyo family release no longer supported
-   **Version 2.0.2 - March 2023**
    -   Fixed:

        -   Observation state field
        -   OSHA report export
        -   Injury / illness mandatory fields
        -   Report view ACL fixed
        -   Landing page inclusion of standalone injuries
-   **Version 2.0.0 - February 2023**
    -   ServiceNow Health and Safety Incident Management includes Employee Center and Now Mobile based incident and observation submission tools. Employees can easily submit incident and observation reports to safety teams.
    -   Featuring a Health and Safety Workspace, safety teams can conduct investigations into safety incidents using tools like the investigation workbench, injury and illness logs, root cause analysis, and corrective and preventative actions.

**Parent Topic:**[ServiceNow Store - Health and Safety release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-health-safety.md)


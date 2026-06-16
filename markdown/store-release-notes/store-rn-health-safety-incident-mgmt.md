---
title: Health and Safety Incident Management release notes
description: Version history for the Health and Safety Incident Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-health-safety-incident-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Health and Safety release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Health and Safety Incident Management release notes

Version history for the Health and Safety Incident Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.2.0 - June 2026**
    -   Changed:
        -   Applied timezone-safe date and time handling to the incident Occurred\_onfield to prevent timezone conversion errors
        -   Added the ability to hide the map location search field via a system property configuration
        -   Automated candidate test cases for Incident Management
        -   Expanded domain separation test coverage for Incident Management tables
    -   Fixed:
        -   Role access issue blocking the sn\_ohs\_im.executiverole from workspace access due to unapplied conditional sys\_user\_role\_containsrecords
        -   Data update issue where the email field did not refersh when changing employee selection in the safety incident's People Involved section
        -   Injury body part picker issue incorrectly displaying injuries on the opposite side when selecting upper leg, knee, or lower leg
        -   Issues affecting the leading indicator dashboard
        -   Internationalization issue causing map-selected addresses not getting populated in correct fields under a Japanese language session
        -   Incorrect Japanese language translations
-   **Version 13.1.0 - May 2026**
    -   Changed: Replaced service\_viewerrole with cmdb\_readin sn\_ohs\_im.incident\_reader ACL.
    -   Fixed:
        -   Fixed missing H&amp;S catalog items under Safety Incident &amp; Observation in the Now Mobile app.
        -   Improved Workspace Homepage first-view performance.
        -   Fixed issue related to injury records saving under Advanced Incident on Now Mobile.
        -   Fixed saving issue with “People involved”, “Type”, and “What was observed” fields captured via Conversational AI for safety observation.
        -   Internationalization: Corrected overlapping front and back body switch arrows in Health and Safety Workspace for RTL \(Right-to-Left\) languages like Arabic.
        -   Fixed WSD dashboard location filters \(Site, Campus, Building, Floor\).
        -   Improved multiple-injuries entry flow on incidents.
-   **Version 13.0.1 - March 2026**
    -   New:
        -   Added a Conversational catalog item for reporting Health and Safety observations via a guided conversational interface.
        -   Added support for related lists in PDF mapping within the Workspace, enabling richer PDF document generation.
        -   Dashboard filters in the Workspace now apply consistently across supported metrics on each dashboard tab.
    -   Fixed:
        -   Fixes to ensure employee names are consistently carried over from the People Involved section when creating Observation cases.
        -   Resolved an issue preventing the Observation record from loading in the Health &amp; Safety Workspace.
        -   Fixed Playbook issues such as the refresh list button, unintended overwrites of the first record in a list, and an infinite loading state.
-   **Version 12.1.0 - January 2026**

    Changed: Updates to support the CSV export updates to the Health and Safety OSHA Content pack application.

-   **Version 12.0.0 - December 2025**
    -   New:
        -   Configurable fields in the injury picker.
        -   Tracking of multiple injuries per body part.
        -   Default map location setting for incidents and location search for incident maps.
        -   Enhanced PDF mapping with security, attachment controls, and choice for fillable exported PDFs.
    -   Fixed:
        -   Improved speed of meeting host search.
        -   Fixed impersonation issues for demo users.
        -   Improved accessibility for playbook steps and resizable panes.
        -   Fixed empty address fields in observations.
        -   Corrected display of tasks in People involved and Action tabs.
        -   Fixed security issues with encoded queries.
        -   Fixed missing search bars and improved heading levels for accessibility.
        -   Fixed visitor fields display on forms.
        -   Restored demo data for Health and Safety Incident Management.
        -   Updated visitor hints and geo property access.
        -   Improved translations for interface elements.
        -   Fixed comparison functions for Knowledge Base articles.
-   **Version 11.0.0 - August 2025**
    -   New:
        -   Conversational incident reporting using Now Assist AI on the Employee Center
        -   Additional incident management capabilities to Agent Mobile application
    -   Fixed:
        -   Minor i18n issues
        -   a11y issue with injured people widget
        -   Issue where injury / illness page was blank
        -   Issue with incorrect mandatory fields on injury picker on mobile
        -   Error messages shown when editing an injury/illness record
        -   Issue on Now Mobile that prevented body parts from being added on Advanced incidents
        -   Issues with incident playbook not working
        -   Issues where records would not show when clicking on dashboard metrics
        -   Issue where playbook didn't trigger for Advanced incidents coming from the Employee Center
        -   Issues with visitor lists and fields being blank in certain scenarios
        -   Issue where anonymous safety concern reports did not show up in the search
        -   Incorrect user sometimes able to delete injury/illness records
-   **Version 10.0.0 - May 2025**

    ServiceNow Health and Safety Incident Management includes Employee Center and Now Mobile based incident and observation submission tools. Employees can easily submit incident and observation reports to safety teams.Featuring a Health and Safety Workspace, safety teams can conduct investigations into safety incidents using tools like the incident playbook, injury and illness logs, root cause analysis, and corrective and preventive actions. If Critical Event Management is also installed, safety incidents can be linked to any of the emergencies that your company is managing.


**Parent Topic:**[ServiceNow Store - Health and Safety release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-health-safety.md)


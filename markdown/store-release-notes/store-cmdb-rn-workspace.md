---
title: CMDB Workspace release notes
description: Version history for the CMDB Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# CMDB Workspace release notes

Version history for the CMDB Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.2.0 - June 2026**
    -   New:
        -   Data Manager
            -   Added 'Run policy' button on the Published policies list in the Policies section, to allow a user with the data\_manager\_admin or sn\_cmdb\_admin role, to run an Attestation or Certification policy on-demand.
            -   Ability to export and import CMDB Data Manager policies using update sets.
        -   Data Certification
            -   Notification added to a Certification task to prompt a user to submit the task when all records for a task have been certified.
        -   CMDB Groups form
            -   Added a 'Show all group CIs' button to CMDB Groups pages, to list all the CIs in a CMDB Group.
        -   Cloud vs Non-cloud resources dashboard
            -   Use the Latest updates link to activate/deactivate the display and collection of data for CI classes.
    -   Fixed: Non-compliant accessibility issues involving zooming to 400%.
-   **Version 8.1.0 - March 2026**

    This is a quality release that specifically focused on fixing defects.

-   **Version 9.0.0 - March 2026**
    -   New:
        -   Service Graph Workspace - Initial release of a re-designed CMDB Workspace for a simplified, persona-driven experience. The new workspace is available to try for users with the sn\_cmdb\_admin role and can co-exist with CMDB Workspace.
            -   Data Owner Home: Manage CMDB data that you own or manage, view related data sources, health, tasks and activity.
            -   Ingestion: Manage data ingested by Service Graph Connectors and IntegrationHub-ETL.
            -   Governance: Consolidated tools and dashboard for Administrators to monitor and manage CMDB data.
            -   Explore &amp; Search: Browse CMDB data without understanding the data model, use AI-driven search to find data in the CMDB.
            -   Tasks: Centralized access to Certification, Attestation and Lifecycle approval tasks created by CMDB Data Manager.
            -   Insights: Centralized access to all OOB CMDB dashboards including CMDB Health, CMDB 360, Data Foundation dashboards and more.
            -   Lists: Access CMDB related lists.
-   **Version 8.0.0 - December 2025**
    -   New: Improved previewing of de-duplication templates.
    -   Fixed: Fixed several issues to resolve various usability and performance issues identified in CMDB Workspace including CI form, CMDB 360, CMDB Health dashboards, Data Manager, Data Certification, Create CI, My Tasks, and Unified Map.
-   **Version 7.6.2 - September 2025**

    Fixed: Resolved an issue with the experience of manually creating a CI when used in Industrial Workspace.

-   **Version 7.6.1 - August 2025**
    -   New:
        -   CI Form - Completely redesigned for an improved experience. CI records can now be viewed and edited using a modern layout with easy navigation. Changes to CI attributes are processed via IRE, creating related CIs makes use of the new manual CI creation experience, and CI tags can be managed. CMDB Administrators can configure CI attribute sections, CI attributes, and related resources \(i.e. related lists\).
        -   Data Certification Dashboard - View certification policy instances, their tasks and certification records. The dashboard can be accessed via a Quick Link on the CMDB Workspace home page.
        -   Data Manager
            -   Allow a user to be specified to run scheduled jobs for Attestation and Certification policies.
            -   View scheduled jobs for Attestation and Certification policies.
            -   Policy option added to allow a user or group to be specified for unassigned tasks.
            -   Ability for users to view closed tasks in My Work.
        -   Unified Map - Shared filter presets allow a CMDB Administrator to define OOB filter presets that can be applied by users in Unified Map.
    -   Changed: Unified Map - Filter presets user experience has been changed to support personal and shared filter presets.
    -   Fixed:
        -   Data Manager:
            -   Dot-walking functionality in policy task assignment.
-   **Version 7.5.2 - June 2025**
    -   Changed: Access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and sn\_cmdb\_admin \(CMDB Admin\) user roles. The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Fixed: Data Certification Fixed a performance issue that affected bulk certification of 10k records.
-   **Version 6.5.2 - June 2025**

    Changed: Access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and sn\_cmdb\_admin \(CMDB Admin\) user roles. The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.

-   **Version 7.5.0 - May 2025**
    -   New:
        -   CMDB Data Manager
            -   Supports flow-based notifications for Certification and Attestation policies.
            -   Allows managers to view tasks assigned to users or groups they manage.
            -   Support the ability to delete retirement definitions.
            -   Improved support for rejecting an approval task for Retire/Archive/Delete policies.
        -   Unified Map: Edit dependency maps - allow adding CIs to a map, creating, modifying and deleting relationships between CIs.
        -   De-duplication templates: Schedule when to run de-duplication templates.
    -   Changed:
        -   CMDB Data Manager
            -   Ensure that the retirement definition for the cmdb\_ci class is always active - and so preventing the situation in which all definitions are in an inactive state.
-   **Version 7.4.1 - March 2025**
    -   New:
        -   Manually create CI records via IRE.
        -   Added dot-walking support for task assignment in CMDB Data Manager policies.
    -   Changed: Improved Policy UX performance in CMDB Data Manager.
-   **Version 7.4.0 - February 2025**
    -   New:
        -   Manually create CI records via IRE
        -   Added dot-walking support for task assignment in CMDB Data Manager policies
    -   Changed: Improved Policy UX performance in CMDB Data Manager
-   **Version 6.4.1 - February 2025**
    -   New: Added dot-walking support for task assignment in CMDB Data Manager policies
    -   Changed: Improved Policy UX performance in CMDB Data Manager
-   **Version 7.3.0 - November 2024**
    -   New:
        -   Overview section added to the contextual side panel in Unified Map, providing information for the map that is showing.
        -   Data Manager certification policy option now prevents records with empty fields from being certified.
        -   Added filtering options for CMDB 360 discovery sources charts similar to coverage charts.
        -   Added filtering for de-duplication templates allowing users to add de-duplication tasks to a template.
    -   Fixed:
        -   Remediated various accessibility issues identified in CMDB Workspace.
        -   Fixed various notifications and configuration issues in Unified Map.
-   **Version 6.3.0 - November 2024**
    -   New
        1.  Overview section added to the contextual side panel in Unified Map, providing information for the current map that is showing.
        2.  Data Manager certification policy option now prevents records with empty fields from being certified.
        3.  Added filtering options for CMDB 360 discovery sources charts similar to coverage charts.
        4.  Added filtering for de-duplication templates allowing users to add de-duplication tasks to a template.
    -   Fixed
        -   Remediated various accessibility issues identified in CMDB Workspace.
        -   Fixed various notifications and configuration issues in Unified Map.
-   **Version 7.2.0 - August 2024**
    -   New:
        -   CMDB Health dashboard - There is a new and improved version of CMDB Health dashboard which is now accessible from CMDB Workspace. Below are some key highlights of the new CMDB Health dashboard:
            -   Simplified counts - Counts of CIs based on whether they are failing or passing completeness, compliance and correctness checks.
            -   For failing CIs, you can see breakdown by discovery source and by owners and easily drill down by these pivots.
    -   Fixed:
        -   Performance improvements on:
            -   CMDB Workspace landing page
            -   Lists
    -   Changed:
        -   Fixed Updated CIs Updated Application services indicator filter. This might affect the trend line after upgrading.
        -   CIs processed via IRE donut count job now runs once a month \(previously once a day\).
    -   Removed: Deleted deprecated indicators not visible to customers.
-   **Version 6.2.0 - August 2024**
    -   Fixed:
        -   Performance improvements on
            -   CMDB Workspace landing page
            -   Lists
    -   Changed:
    -   -   Fixed Updated CIs Updated Application services indicator filter. This might affect the trendline after upgrading.
-   CIs processed via IRE donut count job now runs once a month \(previously once a day\).
    -   Removed: Deleted the following deprecated indicators:
        -   Rejected CIs \(Deprecated\)
        -   Stale CIs \(Deprecated\)
        -   Total CIs \(Deprecated\)
        -   Duplicate CIs \(Deprecated\)
-   **Version 5.5.0 - August 2024**
    -   Fixed: Performance improvements on CMDB Workspace landing page
    -   Changed:
        -   Fixed Updated CIs Updated Application services indicator filter. This change might affect the trend line after the upgrade.
        -   CIs processed via IRE donut count job now runs once a month \(previously a daily job\).
    -   Removed: Deleted deprecated indicators that were not actually visible on the interface.
-   **Version 6.1.1 - May 2024**

    New: Added the ability to select all records in a certification task for bulk processing with the 'Certify' and 'Fail' actions. You can't use this select all capability with the 'Review records' action.

-   **Version 5.4.1 - May 2024**

    Changed: Performance improvements for loading maps in Unified Map.

-   **Version 4.3.0 - May 2024**
    -   New: More robust and intuitive groupings in the CMDB 360 coverage chart:
        -   For CIs and related items with a single discovery source, easily see the breakdown across sources.
        -   Filter coverage using the following filter options:
            -   All - See the breakdown by discovery source for all data, including CIs from CMDB and non-CMDB classes.
            -   CMDB CI - See the breakdown by discovery source only for CIs from CMDB classes, excluding non-CMDB classes.
            -   Principal Class - See the breakdown by discovery source for all CIs in Principal classes only.
-   **Version 6.0.1 - February 2024**
    -   New:
        -   Data Certification
            -   New Certification policy type added to CMDB Data Manager in CMDB Workspace
            -   Certification task tab added to My Work view in CMDB Workspace
            -   Certification task form allowing you to certify/fail/update fields in records for specified tables
            -   View certification exceptions
    -   Changed:
        -   Unified Map
            -   Tooltip for CIs changed to show name and class
    -   Fixed:
        -   CMDB Data Manager
            -   Task details now updated after task status changes to "closed cancelled"
            -   System properties no longer show as read-only in CMDB Data Manager Settings
-   **Version 5.1.0 - February 2024**
    -   New:
        -   De-duplication templates
            -   Provided an option to create and assign a library while creating a template
    -   Changed:
        -   Unified Map
            -   Tooltip for CIs changed to show name and class
    -   Fixed:
        -   CMDB Workspace
            -   Fixed issue with breadcrumb when clicking the browser back button
            -   Fixed visualization of large numbers
        -   Data Manager
            -   Timeline now refreshes after publishing an Attestation policy
            -   Fixed issues with validation on policy flow
            -   Scheduled job no longer activated when creating a draft policy
            -   Fixed performance issues when loading the policy form or policy details on large CMDBs
        -   De-duplication templates
            -   De-duplication template insights now shows correct data for Top 5 discovery sources
            -   Fixed slow loading of De-duplication Template dashboard
            -   Library field now displays properly in template preview
            -   Fixed library appearance when lots of libraries exist and window is resized
            -   Score card now shows abbreviated count for large numbers
        -   Unified Map
            -   Level params in URL is now updated
            -   CIs now remains filtered \(hidden\) when an application service map is opened
            -   Timeline no longer reappears when a CI is selected
        -   Insights
            -   Application Services dashboard now loads from outset
-   **Version 5.0.5 - December 2023**
    -   Fixed:
        -   CMDB Workspace
            -   Fixed a problem where cards with a zero count were showing up as loading constantly in the Important actions section.
            -   Fixed an issue that saw Open tasks and Overdue tasks count on the home page not matching with Open and Overdue tasks counts in 'My work' landing page.
            -   Fixed a problem where information displayed for the 'CI Health' widget was not consistent with the CMDB Health dashboard.
            -   Fixed an issue that prevented a message \(using gs.addInfoMessage\) associated with an action from being displayed in CMDB Workspace.
            -   System property added to allow disabling of portions of the "CMDB Workspace - Populate aggregates Daily" scheduled job.
        -   Data Manager
            -   Fixed an issue where a user with the sn\_cmdb\_admin role didn't have roles required to read tables for a Data Manager policy filter condition using a Related Entry.
            -   Fixed an issue where the Data Manager create/update policy form loads in a broken state.
            -   Fixed an issue where the % percent complete column not working for Policy execution details.
            -   Fixed an issue where an error was generated when a policy that was created and published in the legacy Data Manager application was viewed in the new UX.
            -   Fixed an issue where the time value being cleared when the date-time widget was selected in the Schedule section of the policy form.
            -   Corrected a problem where the 'Needs review' checkbox being checked even when the value on the backend was false.
            -   Corrected text in various sections of the Data Manager UX.
-   **Version 3.6.4 - December 2023**
    -   Fixed:
        -   Fixed an issue where users with sn\_cmdb\_admin or sn\_cmdb\_editor roles weren't able to modify cmdb\_ci records.
        -   Fixed an issue that prevented a message \(using gs.addInfoMessage\) associated with an action from being displayed in CMDB Workspace.
        -   System property added to allow disabling of portions of the 'CMDB Workspace - Populate aggregates Daily' scheduled job.
        -   Fixed an i18n translation issue caused by a hardcoded string.
-   **Version 5.0.4 - November 2023**
    -   New:
        -   Data Manager
            -   Re-imagined user exrperience for Data Manager, accessed via Management page
        -   Unified Map
            -   New toolbar consolidates controls
            -   CIs displayed in maps according to Life Cycle Stage value \(default is Operational\)
            -   Relationship level depth control is now available for application service maps
            -   Related CIs for Dynamic CI Groups can be viewed as Attributes or displayed in a list
        -   Bulk CI de-duplication
            -   A new template-based capability and experience for handling duplicate CI tasks
            -   Process multiple duplicate CI tasks at the same time when they have similar remediation requirements
            -   Two new hyprlinks on Management tab of CMDB workspace to navigate to the De-duplication Dashboard and De-duplication Template Library
    -   Changed:
        -   "Governance" page was renamed "My Work"
        -   Unified Map
            -   Changed layout of attribute cards for Connections, and expanded attributes for connections created by Service Mapping
-   **Version 3.6.2 - November 2023**

    Changed: CMDB 360 Coverage charts will now only show cmdb\_ci data by default. You can modify a system property to change this default behavior and show both ci and non-ci data.

-   **Version 3.6.0 - August 2023**

    CMDB Performance Insights:

    -   New sub-section added under the Insights view.
    -   Makes it easier to debug issues related to partial payloads and Service Graph Connector executions.
    -   Based on insights and analysis, provides recommendations for potential areas of performance improvements for CMDB.
    Application services cloud/non-cloud breakdown:

    -   Understand which of your application services are running on cloud environments, non-cloud environments, or are hybrid.
-   **Version 3.4.6 - July 2023**
    -   Changed
        -   The Total CIs tile on the CMDB Workspace landing page and the Rejected CIs card in theManagement view, have been modified to improve performance on instances with a large CMDBs.
            -   -   For optimized performance, the CI.Activity indicator source, now includes additional filter conditions.
-   Total CIs:
    -   A new 'Total CIs' Performance Analytics \(PA\) indicator replaces the existing 'Total CIs' indicator.
    -   The new 'Total CIs' indicator is now associated with the 'CMDB Workspace Aggregates Daily Collection' job.
    -   For upgraded instances, historical data is migrated to preserve the trends.
-   Rejected CIs:
    -   Total number of records is directly derived from the cmdb\_ci table, with attestation\_status=rejected.
    -   Collected and stored in aggregated table on a schedule.
    -   Last updated time stamp now shows on the card.
    -   Removed
        -   The previous 'Total CIs' indicator is now renamed to 'Total CIs \(deprecated\) and is disassociated with the CMDB Workspace Collection job.
-   **Version 3.4.1 - May 2023**
    -   New:
        -   NLQ Changes:
            -   Improved ability to handle utterances missing conjunctions
            -   Ability to search for CI by name
            -   Improved validation for utterances related to non-cmdb tables
        -   Insights Module:
            -   Provides built-in dashboards and reports showing health and usage of the CMDB.
            -   CMDB Feature Adoption Dashboard: Provides an overview and details of all the features and tools available under CMDB. Provides links to documentation, demo videos, installation and getting started pages, and metrics related to usage of these features, wherever applicable.
            -   Application Services Dashboard: Get insights related to application services.
            -   Cloud vs Non-Cloud Resources: Views of CIs broken down across cloud and non-cloud environments.
-   **Version 3.3.0 - February 2023**
    -   New:
        -   Cloud vs. Non-Cloud Resources - This chart is now available on the CMDB Workspace home page. Compare cloud versus on-prem resources. Drill down into CI details for each number. Leverage these base system insights to easily understand and manage your overall technology position.
        -   CMDB 360 - Create and schedule sophisticated reports using CMDB 360 records found in multiple sources. Shorten time to value and drive up trust.
-   **Version 3.1.0 - November 2022**
    -   New:
        -   Appshell featuring horizontal menu and breadcrumb navigation
        -   Important actions
        -   CI total count
        -   What's New section
        -   Editable quick links
        -   CMDB 360 dashboard
        -   Management dashboard
    -   Changed:
        -   CI overview - combined overview and my CIs into one section
        -   My work - compact layout
        -   Quick links - some links moved to Management page
        -   ""Data Attestation"" landing page renamed to ""Governance""
    -   Removed:
        -   Lists
        -   Discovery and Service Mapping activity charts
-   **Version 3.0.0 - August 2022**
    -   New:
        -   Search
            -   Intelligent Search - NLQ-based search capability for the CMDB
            -   Conditional Search - Use a filter condition to search for records in a selected CI class
        -   CI Overview
            -   Added a system property that allows a simplified filter condition to be used to reduce the time taken by scheduled jobs to collect CI counts for large numbers of records
        -   Health
            -   Added color-coded badges to better understand Health scores
        -   Data Attestation
            -   Added a section to display groups a user belongs to
            -   Option to auto-attest CIs found by Smart Detection
            -   Attestation policies that would generate a task with more than 10,000 CIs now generate separate tasks each limited to a maximum of 10,000 CIs
    -   Removed: CI Search - previous search method replaced by Intelligent and Conditional Search
-   **Version 2.2.0 - May 2022**
    -   New:
        -   Added an Attestation module for accessing the:
            -   Data Attestation dashboard
            -   Data Attestation tasks assigned to you by CMDB Data Manager
    -   Changed:
        -   Renamed "7-day activity ..." charts to "Recent activity ..."
        -   Discovery Activity
            -   New devices changed to New hardware and now references cmdb\_ci\_hardware table
    -   Fixed: Activity trend timescale set to 7-day range
-   **Version 2.0.4 - February 2021**
    -   New:
        -   Banner added to workspace
        -   Theme support for San Diego
    -   Changed: CMDB Workspace is installed by default in the San Diego release
-   **Version 1.0.2 - November 2021**

    The CMDB Workspace is a central place for working with the CMDB. Use the workspace to search and explore the CMDB, understand health, view activity trends, access various tools, and interact with the CMDB to support tasks in your organization.



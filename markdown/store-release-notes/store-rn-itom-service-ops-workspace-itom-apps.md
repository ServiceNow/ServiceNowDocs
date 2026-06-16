---
title: Service Operations Workspace ITOM Apps release notes
description: Version history for the Service Operations Workspace ITOM Apps on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-workspace-itom-apps.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 13
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace ITOM Apps release notes

Version history for the Service Operations Workspace ITOM Apps on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.1.1 - June 2026**
    -   New:
        -   AIOps Supervisor Homepage - A new dedicated homepage for NOC supervisors is now available in the Service Operations Workspace, providing a real-time operational view of the AIOps AI Specialist activity, recent alert actions, and team performance.
        -   AIOps Manager Homepage - A new homepage for the AIOps Manager role gives IT operations managers a centralized landing experience tailored to their persona, with an AI Supervising tab where widgets refresh on demand and navigation links open in the correct workspace context.
        -   Onboarding experience for the AIOps AI Specialist \(limited availability\)
        -   Proactive grouping recommendations in the Alert Automation grouping definition
    -   Changed: Link View enhancement to better support Mixed alert groups
    -   Fixed:
        -   The Express List layout broke when the browser window was resized to certain widths.
        -   An "update available" banner was incorrectly displayed when resuming the live list.
        -   Express List columns were untranslated when viewed in Japanese.\(Backport\)
        -   CJK \(Chinese, Japanese, Korean\) translations in the Express List were displaying vertically instead of horizontally.\(Backport\)
        -   Double scrollbars appeared in the Express List when at high zoom levels.
        -   Saving an Alert Management Rule with "Create Incident Advanced" failed in certain scenarios.
        -   Operators with more than 5 assignment groups could not see their created Enrich automations in the Enrich module.
        -   Alerts that were manually removed from a group were automatically re-added. This behavior has been corrected.
        -   A broken documentation link in the alert automation configuration has been fixed.
        -   The Dynatrace Monitor setup instructions in the Launchpad no longer matched the current Dynatrace console. Instructions have been updated.
        -   The "Tags" label in the Launchpad was shared across contexts, causing incorrect translations in some languages.
        -   Two concatenated strings caused grammatical issues in certain target languages. The strings have been separated to allow correct localization.
        -   Launchpad forms at high zoom levels did not match the approved design. Layout corrected at 400% zoom.
        -   Dotted connection lines were not appearing in the Link View even when connected CIs were returned correctly from the backend.
        -   The Simulation UI was displaying "MIXED" or "CMDB" labels instead of "This automation" or the saved automation name when the group type was Mixed or CMDB.
    -   The "All Time \(Last 180 days\)" option was not showing as selected in the time range picker, and was also not being translated correctly.
    -   Service health percentages used a hardcoded decimal separator, causing display errors in locales that use a comma as the decimal separator.
    -   Ellipsis menu items in the Log Viewer were always displayed in English regardless of the user's language setting.
    -   Backspace behavior in Extended mode was incorrect.
    -   The evt\_mgmt\_adminrole was missing write access to Express List properties.
-   **Version 27.0.17 - May 2026**
    -   New:
        -   Create incident unification -  change UI to fit the new flow with create incident advanced
        -   Improve regex error message
-   **Version 27.0.6 - April 2026**
    -   Fixed:
        -   AI Insights in Express List breaks when AIOps Experience version doesn't match Now Assist \(affects Yokohama and Zurich &lt; ZP5\).
        -   Integration Launchpad shows "No content available" after upgrading app-sow-integrations-launchpad to v27.0.3 on Yokohama.
        -   Activate with AI modal colour not rendering correctly.
        -   Grouping Automation rules cannot be saved or updated when active is set to false.
-   **Version 27.0.0 - March 2026**
    -   New:
        -   Express List – Advanced Filter Mode: Users can use advanced filters to set complex filters on the Express List form, even for previously unsupported filter options.
        -   Express List – Search Secondary Alerts: Users can now search secondary alerts directly within the Express List.
        -   Express List – Anomaly charts in the alert record: Users can now open anomaly charts for log analytics-based alerts and metric intelligence alerts directly in the alert record.
        -   Unified Incident Creation: 'Create Incident' in the Express List and Alert Automation now uses a unified flow with customizable field mapping.
        -   CI Binding Enhancements: Improved CI binding workflow with fallback support, binding simulation, and a refreshed UI for selecting and mapping alert fields to CI attributes.
        -   AI Alert Insights – Styled Output: Alert insight panels now render rich HTML content, enabling formatted AI-generated summaries directly within the workspace.
        -   AI Gradient Tokens
        -   Configuration Intelligence AI Agent – Activate with AI: The Overview page now shows an 'Activate with AI' button per data input, allowing HLA configuration to be AI-assisted.
        -   EM + HLA Unified Grouping: Alert Automation rules now support unified grouping across Event Management and Health Log Analytics.
        -   Vector Agent Integration: New Push data input for Vector Agent is available in the Integration Launchpad.
        -   AWS Integrations: New data inputs for AWS CloudWatch and AWS S3 are available in the Integration Launchpad.
        -   Push Data Input UI: The Integration Launchpad Overview page for push data inputs now includes dedicated 'Set Up Instructions' and 'Set Up Connection' tabs.
        -   Accessibility \(WCAG 2.1 AA\): Integration Launchpad pages for HLA data inputs now support responsive reflow at 400% zoom.
    -   Fixed: Express List performance:
-   **Version 26.12.32 - February 2026**
    -   Fixed:
        -   Enrich Automation - Extract from Field Info button is not displayed.
        -   Ignore Automation - Automation Details section does not expand after collapse, fields are not displayed \(AIOps Experience\).
        -   Alert Automation - Delay Incident Creation flow is broken because of Condition Builder API change between Z to A.
-   **Version 26.12.11 - January 2026**

    New: AI insights panel - display insights and recommendations generated by the Manage alert autonomously agentic workflow

-   **Version 26.11.0 - December 2025**
    -   New:
        -   Introduce unified HLA admin pages in Service Operations Workspace
        -   Create integration for Azure Event Hubs data input
        -   Create integration for GCP PubSub data input
        -   Create integration for Edge Delta data input
        -   Enhance bulk actions usability in the Express List
    -   Changed:
        -   Replace chart-bar component with a new and accessible component
        -   Add categories to the AIOps 360 dashboard
        -   Use Now Presentation List instead of EM Variant in the Service Operations Workspace Lists module
        -   Adopt force layout in the Link View chart
        -   Update the link to dependency view in the Service Operations Workspace to open the Unified Map
    -   Fixed:
        -   Fix accessibility and performance issues in the Integrations Launchpad
        -   Fix accessibility issues in the Metrics view panel
        -   Fix accessibility issues in the Express List
-   **Version 26.9.2 - November 2025**

    Fix - Express list filtering: Fixed an issue where applying multiple filters in quick succession could result in alerts being shown for the initial filter only.

-   **Version 26.9.1 - October 2025**

    Fixed:

    -   Express List Preview Panel - Fixed an issue where viewing HLA alerts unexpectedly triggered a pop-up login window.
    -   Application Manager - Resolved a naming issue where some applications displayed the plugin name instead of the actual application name.
-   **Version 26.9.0 - August 2025**
    -   New:
        -   New 360 AIOps dashboard available in the Service Operations Workspace.
        -   Support for mixed group criteria in the Link View, Express List, and Alert Form.
        -   Anomaly card embedded in the Express List for Metric Intelligence Anomaly and Health Log Analytics alerts
        -   Auto-resume live list feature in the Express List
        -   Configurable default time range for the Express List
        -   Support for Health Log Analytics alerts in the Link View
        -   New Cribl data input for Health Log Analytics in the Integrations Launchpad
        -   New generic OLTP data input for Health Log Analytics in the Integrations Launchpad
        -   Grouping automations now support grouping alerts with related CIs and matching fields or tags
        -   Enrichment automations now include a test option for CI identification and a checkbox to easily clear the node.
        -   Ignore automations now include a button to enforce running ignore automations before enrichment automations when opening legacy event rules.
    -   Changed:
        -   In response automations, more alert management rules can now be opened from UI16. The fields for parent and maintenance are now optional, and you can also use lower order numbers and matching condition builder fields.
        -   When both the "evt\_mgmt\_admin" and "evt\_team\_operator" roles are assigned to the same user, the permissions and filters of "evt\_mgmt\_admin" take precedence.
    -   Fixed:
        -   Hide the surrounding log from the alert form for virtual HLA alerts
        -   Express list:
            -   Fixed an issue with the Application service filter
            -   Fixed an issue where the Alert Tags column could not be removed from the view
            -   Fixed a problem editing Express List views that had a filter set on the "Source" field
            -   Fixed a problem with the Link View Legend for the Resource toggle
            -   Fixed accessibility issues related to tab and keyboard navigation
-   **Version 26.7.3 - July 2025**

    Fixed: Link view buttons are disabled

-   **Version 26.7.2 - June 2025**
    -   Fixed in Integration Launchpad:
        -   PRB1884316 - Integration Launchpad not working with HLA versions prior to February.
        -   PRB1890903 - Push Connector Instance Deletion Issue Not Created via Integration Launchpad.
        -   PRB1892575 - Integration created for a Dynamic CI service in SRM has a blank "Default CI" field.
-   **Version 26.7.0 - May 2025**
    -   New:
        -   Express List Data Source icons improvements
            -   Adding new icons for HLA alerts and displaying all source icons for Alert Groups on the Express List.Also, for Alert groups, the Preview Panel Alert card displays the source icon for each alert.
        -   Enhancements in the integration launchpad for HLA data inputs and the Overview page:
            -   Link out to Log Viewer in Context
            -   Overview page - Banner adjustment
            -   New Log Analytics push integration for REST API data input
            -   Log Analytics integration for Kafka data input
            -   AWS Firehose Integration for Log Analytics
            -   New integration for Azure Log Analytics data input
            -   New integration for Splunk data input in the integration launchpad
    -   Fixed: Accessibility improvements on the Service Dashboard
-   **Version 26.3.4 - March 2025**

    Fixed: Fixing a bug in the Express list preview panel, for cases where an Alerts Additional info field contains a nested object.

-   **Version 26.3.1 - February 2025**
    -   New:
        -   Added the ability to simulate all grouping types in Alert Automation Grouping Definitions.
        -   Introduced new Health Log Analytics Data Inputs in the Integrations Launchpad.
        -   Added support for the Network Traffic Correlation Group in the Express List and Alert form.
        -   Introduced a new Link View Visualization for the Network Traffic Correlation Group.
        -   Added the "Add Alerts to Group" action in the Express List.
        -   Introduced a new role in Event Management \(evt\_team\_operator\) to support federated teams. Users with this role can:
            -   Create new integrations for their teams.
            -   Create and edit alert automations for their teams.
            -   Access a filtered list of alerts that belong to their teams.
            -   View the on-call schedule of their teams.
    -   Changed:
        -   Made accessibility improvements.
        -   Redesigned the Additional Info field in the Express List.
        -   Added new fields to the CI Info in the Express List preview panel.
-   **Version 25.3.3 - November 2024**
    -   New Features:
        -   Alert Automation - Event Data Mapping: Allows single values from event sources to be directly mapped to standard ServiceNow alert fields within Service Operations Workspace. Note: This feature is only available on the X release.
        -   Group Automation - New Header: Displays grouping efficiency stats, such as total alerts, alert groups, ungrouped alerts, and compression.
        -   Express List - Preview Panel: Shows detailed configuration item \(CI\) information associated with alerts in the preview panel.
        -   Integration Launchpad - New Metric Connectors: Added SCOM and Dynatrace metric connectors as new integration tiles.
    -   Changes:
        -   Platform Enhancements: Improved performance and accessibility.
        -   Automation Active Switches: Active toggle switches across automations \(Ignore, Enrich, Respond, and Group\) are now check boxes.
            -   Enrich &amp; Respond Automation: Added And finally section with two radio buttons:
                -   Run other enrich alert automations continues matching automations.
                -   Don’t run other enrich alert automations halts matching automations after execution, except those by other assignment groups.
        -   Express List - “Select All”: Pausing the Live list by selecting All prevents new alerts from flowing in, allowing focus on selected alerts.
    -   Fixes:
        -   Grouping Automation: Resolved an issue with grouping criteria deletion.
        -   Event Management Connectors:
            -   vRealize events now return the Node field.
            -   Improved Event Time mapping in custom connectors.
            -   Resolved Solarwinds compartment call failures for over 3,000 compartments.
            -   Fixed ICINGA event retrieval issues.
        -   Alert Automation:
            -   Replaced Enrich Automation toggle with check box.
            -   Corrected Abort function in Group Simulation.
            -   Fixed infinite loader in the Identified Issues card in the Alert Overview tab.
            -   Fixed timeframe filter in Tag-Based Alert Clustering.
-   **Version 25.1.15 - August 2024**

    Fixed: Group By functionality in Lists.

-   **Version 24.2.3 - June 2024**
    -   New:
        -   Alert Timeline View
        -   Link View
        -   Free-text search of alerts
        -   Keyboard interactions
        -   Connector health KPIs
    -   Changed:
        -   Restyled the alert panel
        -   Display time format according to user preferences
    -   Fixed: Alert auto-refresh issues
-   **Version 24.1.2 - March 2024**
    -   New:
        -   Add Alert Assist to the Express List - Simplify and enrich with technical analysis using Now Assist
        -   Manage views \(Express List\) - Centralized management of predefined views assigned to users and user groups
        -   Probable root cause in alert preview panel \(Express List\) - Add the Probable Cause tab to the alert preview panel in the Express List
        -   Define assigned teams in connector setup \(Integration Launchpad\) - Add the option to assign a connector to a specific team to achieve ownership and assignment to a team
        -   Customer connector definition - Add the option to map from received events \(Integration Launchpad\)
        -   Add alert trends to the alert preview panel \(Express list\) - Add information on repeated alerts and similar alerts to the alert preview panel in the Express List
    -   Changed: Align Source icons in Express List and Integration Launchpad.
    -   Fixed:
        -   Fixing the loading time of large alert groups
        -   Fixing UI for long filter name
        -   Fixing live list filters when filtering on complex column
-   **Version 23.1.2 - March 2024**
    -   New
        -   Add Alert Assist to the Express List - Simplify and enrich with technical analysis using Now Assist
        -   Manage views \(Express List\) - Centralized management of predefined views assigned to users and user groups
        -   Probable root cause in alert preview panel \(Express List\) - Add the Probable Cause tab to the alert preview panel in the Express List
        -   Define assigned teams in connector setup \(Integration Launchpad\) - Add the option to assign a connector to a specific team to achieve ownership and assignment to a team
        -   Customer connector definition - Add the option to map from received events \(Integration Launchpad\)
        -   Add alert trends to the alert preview panel \(Express list\) - Add information on repeated alerts and similar alerts to the alert preview panel in the Express List
    -   Changed
        -   Align Source icons in Express List and Integration Launchpad
    -   Fixed
        -   Fixing the loading time of large alert groups
        -   Fixing UI for long filter name
        -   Fixing live list filters when filtering on complex column
-   **Version 24.0.4 - December 2023**
    -   Fixed:
        -   Unable to install Service Operations Workspace
        -   Unable to load the playbook tab
-   **Version 23.0.0 - December 2023**
    -   Fixed:
        -   Unable to install Service Operations Workspace
        -   Unable to load the playbook tab
-   **Version 22.2.0 - August 2023**
    -   New: Adding visualization for Tag Cluster groups \(starting in Vancouver\).
    -   Changed: Update translation files.
    -   Fixed: Fixing Playbook experience loading errors.
-   **Version 22.0.0 - May 2023**
    -   New: Adding agent assist to alert so users can search, view, and attach KB articles to alerts.
    -   Changed: Mute multiple components.
    -   Fixed:
        -   The donut data automatically refreshed when the user performs an action on the landing page.
        -   The 'View all' link is disabled when the donut widget has no data on the landing page.
-   **Version 21.6.2 - February 2023**

    All changes are part of Service Operations Workspace Alert Management app.

-   **Version 21.2.3 - November 2022**
    -   Fixed:
        -   Header and sub-header texts
        -   Dynamic CI Group form
        -   Links to tag-based services
        -   Sorting on various cards and related lists
        -   Landing page column order
-   **Version 21.1.3 - September 2022**

    Fixed: Fix on playbook execution table to reduce the number of records

-   **Version 21.1.1 - August 2022**
    -   New: Display related Service Offerings under the impacted services section in the alert overview page
    -   Changed:
        -   Updated service form page layout and related lists
        -   New design for the operator's landing page
        -   Updated design of the alerts in group card on the alert overview page
    -   Fixed:
        -   Remove redundant new buttons from lists and related lists
        -   Remove duplicated close button on alert list
        -   Change 'view more' counts on alert overview cards
        -   Align alerts in group-related list columns to the main alerts list layout
        -   Fix empty state for probable root cause card in alert overview page
        -   Fix identified issue card in Alert overview
        -   Fix dynamic CI group related lists
-   **Version 21.0.0 - June 2022**
    -   Service Operations Workspace gives service desk agents and operations teams a single place to manage work, collaborate, and have shared visibility into issues. It includes a unified user experience for agents and operations teams to work on the same problem at the same time and solve issues faster. This helps reduce downtime, improve customer satisfaction, and increase productivity across multiple groups.
    -   Service Operations Workplace ITOM Applications enable you to streamline IT Operations Management workflows and processes for modern operations. You can effectively manage the lifecycle of alerts, find the root cause and remediate it.


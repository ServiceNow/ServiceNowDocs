---
title: AIOps Experience release notes
description: Version history for the ITOM AIOps Experience application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-experience.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# AIOps Experience release notes

Version history for the ITOM AIOps Experience application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.1.1 - June 2026**
    -   New:
        -   AIOps Supervisor Homepage – A new dedicated homepage for NOC supervisors is now available in the Service Operations Workspace, providing a real-time operational view of AIOps AI Specialist activity, recent alert actions, and team performance.
        -   AIOps Manager Homepage – A new homepage for the AIOps Manager role gives IT operations managers a centralized landing experience tailored to their persona. The AI Supervising tab features on-demand widget refresh, and navigation links open in the correct workspace context.
        -   Onboarding experience for the AIOps AI Specialist \(limited availability\) – A guided onboarding experience is now available for the AIOps AI Specialist role to streamline initial setup and configuration.
        -   Proactive grouping recommendations in the Alert Automation grouping definition – Proactive grouping recommendations are now available within the Alert Automation grouping definition.
    -   Changed: Link View has been enhanced to better support mixed alert groups.
    -   Fixed:
        -   The Express List layout broke when the browser window was resized to certain widths.
        -   An "update available" banner was incorrectly displayed when resuming the live list.
        -   Express List columns were untranslated when viewed in Japanese.\(Backport\)
        -   CJK \(Chinese, Japanese, Korean\) translations in the Express List were displaying vertically instead of horizontally.\(Backport\)
        -   Double scrollbars appeared in the Express List at high zoom levels.
        -   Saving an Alert Management Rule with "Create Incident Advanced" failed in certain scenarios.
        -   Operators with more than 5 assignment groups could not see their created Enrich automations in the Enrich module.
        -   Alerts that were manually removed from a group were automatically re-added. This behavior has been corrected.
        -   A broken documentation link in the alert automation configuration has been fixed.
        -   The Dynatrace Monitor setup instructions in the Launchpad no longer matched the current Dynatrace console. Instructions have been updated.
        -   The "Tags" label in the Launchpad was shared across contexts, causing incorrect translations in some languages.
        -   Two concatenated strings were causing grammatical issues in certain target languages and have been separated to support correct localization.
        -   Launchpad forms at high zoom levels did not match the approved design. Layout has been corrected at 400% zoom.
        -   Dotted connection lines were not appearing in the Link View even when connected CIs were returned correctly from the backend.
        -   The Simulation UI was displaying "MIXED" or "CMDB" labels instead of "This automation" or the saved automation name when the group type was Mixed or CMDB.
        -   The "All Time \(Last 180 days\)" option was not showing as selected in the time range picker and was also not being translated correctly.
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

    See Service Operations Workspace ITOM Apps.

-   **Version 26.12.32 - February 2026**
    -   Fixed:
        -   Enrich Automation - Extract from Field Info button is not displayed.
        -   Ignore Automation - Automation Details section does not expand after collapse, fields are not displayed \(AIOps Experience\).
        -   Alert Automation - Delay Incident Creation flow is broken because of Condition Builder API change between Z to A.
-   **Version 26.12.11 - January 2026**

    AI Insights panel - display the insights and recommendations generated by the Manage alert autonomously agentic workflow

-   **Version 26.11.0 - December 2025**
    -   New:
        -   Introduced unified HLA admin pages in Service Operations Workspace
        -   Created an integration for the Azure Event Hubs data input
        -   Created an integration for the GCP PubSub data input
        -   Created an integration for the Edge Delta data input
        -   Enhanced bulk actions usability in Express List
    -   Changed:
        -   Replaced the chart bar component with a new, accessible component
        -   Added categories to the AIOps 360 dashboard
        -   Adopted the NOW Presentation List instead of the Event Management variant in the Service Operations Workspace Lists module
        -   Adopted force layout in Link View chart
        -   Updated link to dependency view in Service Operations Workspace to open unified map
    -   Fixed:
        -   Fixed accessibility and performance issues in Integrations Launchpad
        -   Fixed accessibility issues in Metrics View panel
        -   Fixed accessibility issues in Express List
-   **Version 26.9.2 - November 2025**

    Fix - Express list filtering: Fixed an issue where applying multiple filters in quick succession could result in alerts being shown for the initial filter only.

-   **Version 26.9.1 - October 2025**
    -   Fixed:
        -   Express List Preview Panel: Fixed an issue where viewing HLA alerts unexpectedly triggered a pop-up login window.
        -   Application Manager: Resolved a naming issue where some applications displayed the plugin name instead of the actual application name.
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
    -   Fixed in Integration Launchpad
        -   PRB1884316 - Integration Launchpad not working with HLA versions prior to February.
        -   PRB1890903 - Push Connector Instance Deletion Issue Not Created via Integration Launchpad.
        -   PRB1892575 - Integration created for a Dynamic CI service in SRM has a blank "Default CI" field.
-   **Version 26.7.0 - May 2025**
    -   New:
        -   Express List Data Source icons improvements
            -   Added new icons for HLA alerts and now display all source icons for alert groups in the Express List.
            -   In the Preview Panel, the alert card for alert groups also shows the source icon for each alert.
        -   Integration Launchpad and Overview Page Enhancements for HLA Data Inputs
            -   Added link to Log Viewer in context
            -   Adjusted banner on the Overview page
            -   New Log Analytics push integration for REST API data input
            -   New Log Analytics integration for Kafka data input
            -   AWS Firehose integration for Log Analytics
            -   New integration for Azure Log Analytics data input
            -   New integration for Splunk data input in the Integration Launchpad
    -   Fixed: Accessibility improvements on the Service Dashboard
-   **Version 26.3.4 - March 2025**

    Fixed: Fixing a bug in the Express list- preview panel, for cases where an Alerts Additional info field contains a nested object.

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
-   **Version 25.1.15 - August 2024**
    -   Fixed:
        -   Disabled the user role option to create an incident using general actions.
        -   SOW: Fixed missing configuration item value in the alert card.
        -   Preview panel timeline: Closed alerts were still shown as open.
-   **Version 24.2.3 - June 2024**
    -   New:
        -   Alert Timeline View
        -   Link View
        -   Free-text search of alerts
        -   Keyboard interactions
        -   Connector health KPIs
    -   Changed:
        -   Restyled alert panel
        -   Display time format according to user preferences
    -   Fixed: Alert auto-refresh issues
-   **Version 24.1.1 - March 2024**
    -   New:
        -   Add Alert Assist to the Express List - simplify and enrich with technical analysis using Now Assist
        -   Manage views \(Express List\) - Centralized place to manage views for users according to their group membership
        -   Probable root cause in Alert preview panel \(Express List\) - Add the Probable Cause tab to the alert preview panel in the Express List
        -   Define assigned teams in connector setup \(Integration Launchpad\) - add the option to assign a connector to a specific team to achieve ownership and assignment to a team.
        -   Customer connector definition - add the option to map from received events \(Integration Launchpad\)
        -   Add alert trends to the Alert preview panel \(Express list\) - Add information on repeated alerts, and similar alerts to the alert preview panel in the Express List.
    -   Changed: Align Source icons in the Express List and the Integration Launchpad
    -   Fixed:
        -   Fixing the loading time of large alert groups
        -   Fixing UI for long filter name
        -   Fixing live list filters when filtering on complex columns
-   **Version 23.1.1 - March 2024**
    -   New
        -   Add Alert Assist to the Express List - simplify and enrich with technical analysis using Now Assist
        -   Manage views \(Express List\) - Centralized place to manage views for users according to their group membership
        -   Probable root cause in Alert preview panel \(Express List\) - Add the Probable Cause tab to the alert preview panel in the Express List
        -   Define assigned teams in connector setup \(Integration Launchpad\) - add the option to assign a connector to a specific team to achieve ownership and assignment to a team.
        -   Customer connector definition - add the option to map from received events \(Integration Launchpad\)
        -   Add alert trends to the Alert preview panel \(Express list\) - Add information on repeated alerts, and similar alerts to the alert preview panel in the Express List.
    -   Changed
        -   Align Source icons in the Express List and the Integration Launchpad
    -   Fixed
        -   Fixing the loading time of large alert groups
        -   Fixing UI for long filter name
        -   Fixing live list filters when filtering on complex columns
-   **Version 24.0.2 - November 2023**
    -   Accessibility updates to comply with WCAG 2.1AA
    -   Fixing multiple issues in the Express List
    -   Adopting the standard record page \(i.e. SRP\) in Service Operations Workspace
-   **Version 23.0.2 - November 2023**

    No changes.

-   **Version 23.0.0 - August 2023**
    -   The AIOps Experience app is a transformative addition to the AIOps product in ServiceNow, revolutionizing the entire ITOM \(IT Operations Management\) Health user experience. This app introduces three powerful capabilities, namely the Express List, Integration Launchpad, and AIOps Dashboards, each delivering unique value, but when combined, they elevate the user experience to a whole new level.
        -   Express List: The Express List is a game-changer for alert management. It provides a consolidated platform where users can efficiently triage, conduct root cause analysis \(RCA\), and remediate alerts seamlessly. With real-time updates, dynamic filtering, and an intuitive preview pane, users can stay on top of their alert workflows and take immediate action with unparalleled ease and speed.
        -   Integration Launchpad: With the Integration Launchpad, users gain access to a hub of seamless connections to various external tools and services. It is also simplifying the onboarding of new data sources. This simplifies the integration process, enabling users to effortlessly leverage their existing ITOM ecosystem within the ServiceNow platform. The Integration Launchpad streamlines data exchange and improves cross-platform collaboration, enhancing efficiency and productivity across the board.
        -   AIOps Dashboards: The AIOps Dashboards offer comprehensive visualizations of critical operational data and insights. Users can monitor key performance indicators \(KPIs\), track service health, and gain valuable context on the overall IT environment. These customizable dashboards empower users with actionable insights, facilitating data-driven decision-making and ensuring proactive responses to potential issues.
    -   When used in tandem, the Express List, Integration Launchpad, and AIOps Dashboards create a unified, seamless, and efficient user experience. The revamped ITOM Health interface empowers IT teams to swiftly identify and resolve alerts, optimize performance, and improve overall operational efficiency. By providing a consolidated platform for alert management, simplifying integrations, and offering data-rich dashboards, the AIOps Experience app truly takes ServiceNow's AIOps product to a new level, helping organizations achieve greater operational excellence and deliver exceptional IT services.

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)


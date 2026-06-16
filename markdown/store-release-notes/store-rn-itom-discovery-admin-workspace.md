---
title: Discovery Admin Workspace release notes
description: Version history for the Discovery Admin Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-discovery-admin-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Discovery Admin Workspace release notes

Version history for the Discovery Admin Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.17.0 - June 2026**
    -   New:
        -   This release delivers a major leap forward in Discovery error intelligence, guided onboarding, and a cleaner, more focused diagnostics experience.
        -   Error Framework Integration
            -   Discovery administrators can now diagnose, understand, and resolve errors in a fraction of the time—without ever leaving the workspace.
            -   Errors tab: The new Diagnostics &gt; Errors tab groups errors by refined error code, severity, and category. Each error card opens a dedicated Error Details page showing the root cause, step-by-step remediation instructions, and every individual error instance.
            -   AI Insights panel:Automaticallyprioritizes errors by business impact and surfaces quick wins scoped to your active domain.
                -   Requires the Now Assist for Error Framework plugin \(com.sn\_ef\_gen\_ai\), which is installed automatically with Now Assist for Platform \(sn\_genai\_platform\).
            -   Top discovery errors on Home: The Home page now includes a Top discovery errors section with a persistent, at-a-glance view of the most critical active errors, so administrators always know what needs attention the moment they open the workspace.
            -   Enabled by default: Error Framework is on by default and controlled by the sn\_disco\_workspace.enable\_error\_framework system property.
    -   Changed
        -   Home - Guided Onboarding
        -   New administrators get a faster path to first discovery. When no IP-based or cloud-based schedules exist, the Home page now displays an Onboarding for Discovery section with a prominent Get started link and ITOM Configuration Console touchpoint showing real-time onboarding progress. Once your first schedule is created, onboarding content is automatically removed to reduce noise.
            -   Before: Administrators landed on the Home page with no guidance on where to begin.
            -   After: A clear onboarding path and progress indicator appear for new setups. Returning administrators with active schedules see no change.
            -   The Home page now guides administrators to the ITOM Configuration Console based on their configuration status. If no IP-based or cloud-based Discovery schedules have been created, the Home page displays an Onboarding for Discovery section with a Get started link and an ITOM Configuration Console touchpoint with onboarding progress. Once a schedule is created, the onboarding content is no longer displayed, and the ITOM Configuration Console appears in the ITOM visibility apps section.
        -   Diagnostics - Simplified, Error Framework-Aligned Layout
            -   The Diagnostics page is now cleaner and more focused when Error Framework is enabled.
                -   Before: Six separate tabs: Anomaly detection, Diagnostics, Case management, Support tools, Logs, Ignored errors.
                -   After: Two tabs: Errors and Anomaly detection. The Errors tab consolidates the most critical diagnostic information with AI-assisted prioritization. The Case management, Support tools, Logs, and Ignored errors tabs have been replaced—reducing navigation overhead and context-switching.
        -   Settings - URL Discovery tab \(conditional display\)
            -   The URL Discovery tab in Settings now only appears when both the Software Asset Management \(SAM\) Platform \(com.snc.samp\) and ITOM URL Discovery \(itom\_url\_disc\)plugins are installed. This reduces noise for customers who do not have URL Discovery configured, making the Settings page cleaner for everyone else.
-   **Version 1.15.0 - May 2026**
    -   New:
        -   Discovery Operations Monitor:
            -   The Discovery Operations Monitor dashboard is now available from the Home page and Insights page in the Discovery Admin Workspace. This dashboard consolidates actionable insights, key metrics, and schedules into a unified view, enabling administrators to monitor discovery health, identify issues proactively, and optimize discovery schedules.
    -   Changed:
        -   Activate Schedule:
            -   The Run settings drop-down list in the Activate Schedule modal now supports all run settings at the time of activation. Previously, only the On Demand option was functional; all other options were visible but not configurable until after the schedule was activated.
    -   Fixed:
        -   Accessibility issues
        -   Display of related lists for existing schedules
        -   Active filter functionality for IP-based schedules on IP-based discovery tab
-   **Version 1.14.0 - April 2026**
    -   URL Discovery Insights:
        -   New: The URL Discovery Insights dashboard is now available from the Insights page in the Discovery Admin Workspace. This dashboard enables administrators to monitor URLs accessed across the organization via a browser extension, with configurable monitoring settings available on the Settings page. Access requires the ITOM URL Discovery plugin \(sn\_itom\_url\_disco\).
    -   Schedules overview:
        -   Fixed: The View discovery status link on the Schedules page now navigates to a list of statuses for all scheduled IP-based and Cloud discoveries.
-   **Version 1.13.0 - March 2026**
    -   IPAM Discovery integration:
        -   New:
            -   Discovery now integrates with IP Address Management \(IPAM\) systems to automate network discovery across both IPv4 and IPv6 address spaces. This integration enables Discovery to query IPAM for network data and automatically generates accurate, up-to-date Discovery schedules with minimal manual effort. The following capabilities outline how Discovery uses IPAM data to automate schedule creation, maintain network accuracy, and streamline ongoing management:
                -   Automated synchronization of IPAM network data \(networks, subnets, and IP addresses\) into Discovery schedules
                -   Automated schedule creation and reuse based on IPAM infrastructure
                -   Support for both IPv4 and IPv6 address families with independent configuration limits
                -   Automatic organization of schedules by tag fetched by IPAM connectors \(cmdb\_key\_value\)
                -   Automatic cleanup of obsolete IP addresses and subnets no longer present in IPAM
                -   Detection and disabling of empty schedules to prevent unnecessary discovery runs
    -   Discovery notifications:
        -   New:
            -   Discovery notiﬁcations enable administrators to receive real-time notifications or daily summaries about Discovery updates through Microsoft Teams and email, directly from Discovery Admin Workspace.
    -   Additional cloud providers:
        -   New:
            -   Discovery Admin Workspace has expanded its cloud coverage, enabling you to create Discovery schedules for the following six cloud providers: Alibaba, IBM, OCI, OpenStack, oVirt, and VMware. This update advances the integration of cloud discovery capabilities into a unified workspace, reducing operational complexity and aligning with the upcoming deprecation of Cloud Discovery Workspace.
    -   Tag Governance Insights dashboard:
        -   New:
            -   The Tag Governance Insights dashboard is now accessible from the Insights page in the Discovery Admin Workspace. This dashboard displays metrics like tag policy coverage, compliance status, and usage trends. Access to this dashboard requires Tag Governance v1.9.0.
-   **Version 1.12.0 - December 2025**
    -   New:
        -   Creates cloud schedules from Discovery Admin Workspace \(AWS, Azure and GCP\)
        -   Allows deep discovery using AWS SSM
        -   Helps with Discovery implementation by allowing users to navigate to Discovery Guided Setup directly form the Discovery Admin Workspace
-   **Version 1.10.0 - August 2025**
    -   Changed:
        -   The 'CAPI to Patterns' and 'Probes to pattern migration' cards are now hidden when the migration process completes successfully.
        -   The cards that display on the ITOM Visibility apps page have been updated.
        -   An 'Actions' button has been added to the Anomaly Detection tab, allowing users to navigate to settings and clear anomalies.
    -   Fixed:
        -   Issues with viewing and editing the Discovery status column have been resolved.
        -   The schedule title now displays correctly on the Discovery status details page.
        -   Anomaly detection now functions properly for cloud schedules.
        -   The 'Export' button is now visible under the Server tab in the Service Operations Workspace.
-   **Version 1.9.0 - June 2025**
    -   New: Added an option to use the event framework for processing Discovery sensors. This has a mainline dependency on Xanadu Patch 9 and Yokohama Patch 4.
    -   Fixed the 'Save' functionality on the Settings page to enable anomaly detection.
-   **Version 1.8.0 - May 2025**
    -   New:
        -   Home \(existing tab\):
            -   'Active Schedules' card to display total number of active IP-based and Cloud Discovery schedules.
            -   'Schedules with Anomalies' card to display number of Discovery schedules with anomalies over the last 'X' days, The 'X' days can be configured on the Settings page by selecting one of the drop-down values for the Time scale property.
        -   Schedules \(existing tab\):
            -   Overview: The dashboard includes an 'Active Schedules' card, scorecards for 'Schedules without Anomalies' and 'Schedules with Anomalies', and a bar chart that categorizes anomalies by type. Additionally, a new trending graph will display completed schedules alongside schedules with various types of anomalies. A timeline view will also be introduced to show system plugin upgrades and store app upgrades, synchronized with the trending graph's timeline.
            -   Discovery Schedules -&gt;Overview: A new section that features scorecards and graphs for Total CIs, Total Errors, and Discovery Duration. Additionally, a timeline and a banner provides information about the most severe anomaly detected for the selected schedule, if any anomalies are detected.
        -   Diagnostics \(existing tab\):
            -   Virtual Agent:
                -   Discovery and MID Server Health Validation
                    -   MID Server Pre-Upgrade Check.
                    -   MID Server Status validation.
                    -   MID Server Mutual Authentication validation.
                -   Discovery Performance Metrics review
                    -   Samples the ECC Queue for a Discovery status and provides average wait times, as well as information about probes and sensors that took the longest time to complete.
                -   Retrieve logs
        -   Support Tools \(existing tab under Diagnostics\):
            -   New tools added:
                -   Missing IPs in schedules
                -   Retrieve Logs
        -   Anomaly detection \(new tab tab under Diagnostics\) - Displays all the Discovery schedules with anomalies detected in the last x days. This time scale can be configured on the Settings page.
        -   Settings \(new tab\) - Enables you to customize and manage high-level Discovery properties so they're tailored to meet your specific needs.
    -   Changed:
        -   Home: Error tasks card is now configured to show counts based on the time scale property in the Settings page \(last 7, 14, or 30 days\).
        -   Schedules -&gt; Discovery Schedules \(existing tab\):
            -   Added 'Quick Discovery' and 'New Discovery' buttons.
            -   Added new cards for Total Discovery Schedules, IP-based Schedules, and Cloud Schedules. Additionally, a new 'Provider' column and filters for Discovery by, Location, and Provider have been introduced in the Discovery Schedules list view, which now includes Cloud Schedules alongside the existing IP-based Schedules.
        -   Schedules -&gt; Discovery Schedules -&gt; \(existing tab\) clicking on any record -&gt; specific schedule details:
            -   Updated schedule header to include anomaly severity information.
            -   Run history: Added icons to indicate Discovery statuses with anomalies.
            -   Run history-&gt; status -&gt; details tab \(existing\): Cloud discovery schedules now display a Total Cloud Resources count and a horizontal bar graph visualization.
        -   Schedules -&gt; Discovery Status -&gt; Added 'Anomaly type' and 'Anomaly description' to the discovery\_status list view.
            -   Status Details:
                -   Header with anomaly severity information for schedule overall and other schedule metadata.
                -   Status header updated with anomaly severity information.
                -   When a status has an anomaly, a banner with detected anomaly details.
    -   Removed: Home: 'Canceled Discoveries' score card with trending graph on Home page.
-   **Version 1.7.0 - February 2025**

    -   Fixed: 
        -   Fixed app update version for Tag Governance app on ITOM Visibility apps page 
        -   Fixed Service mapping workspace access 
        -   Fixed 'Missing SNMP Devices' Script run configuration 
        -   Fixed 'Start Time' field configuration in new schedule creation flow 
        -   Improved load times when viewing logs via the Diagnostics tab of Discovery Admin Workspace 
        -   Fixed cosmetic issues in MID server step in new schedule creation flow 
        -   Fixed SaCmd Manager Card visibility when Service Mapping is not installed. 
        -   Fixed Diagnostics tool 'Missing snmp devices' tool button 'Add to OID data' label 
        -   Fixed records link for Discovery Status and IP address for the Diagnostics tool 'Missing SNMP Devices'. 
        -   Fixed access to 'SaCmdManager' Diagnostic tool 
        -   Fixed IP range set reference field data sorting in new schedule creation flow 
        -   Added 'Schedule Name' data point in Discovery status record page 
        -   Fixed List View for Error Task 
        -   Fixed Case management - Name field selection from the list view 
        -   Added tooltip on discovery details graph to explain the labels 
        -   Fixed Diagnostics -&gt; Errors by category pie chart to be clickable 
        -   Fixed Action button in related errors page. 
        -   Fixed Cancel option for non-active discoveries
        -   Removed: Removed the 'Simplify IP ranges' Tuning check
     

-   **Version 1.5.0 - November 2024**
    -   New:
        -   Improved schedule creation experience for IP-based schedules:
            -   new capability to add range sets
            -   new ability to save IP ranges as range sets
            -   support for customizing discovery schedule chains using node map.
        -   Improved diagnostics support tools:
            -   Pattern customization check
            -   IRE payload explorer
            -   Discovery customization report
            -   Skipped files from store updates" \(admin only\)
            -   Command validation task
            -   Missing SNMP OID data
            -   SaCmdManager
-   **Version 1.3.3 - August 2024**
    -   New:
        -   The Discovery admin workspace assists discovery administrators in configuring Discovery, tracking discovery schedules, and managing errors, with diagnostic tools that provide insights into discovered data. Build upon the content service. Home - a launch pad with quick access to learning modules, Quick Discovery, and ITOM Visibility apps.
        -   Schedule - a single pane of glass to view discovery schedules. Discovery admin can get visibility to schedule details and jobs with insights in to discovery errors.
        -   Diagnostics - control pane for discovery troubleshooting with discovery case management.
        -   Tuning - discovery tuning advice - Scroll of card widgets that show recommendations on tuning advice to fine-tune discovery / MID settings.
        -   Content 360 - ITOM Content service to source.
        -   Insights - dashboards and Insights.
-   **Version 1.2.5 - July 2024**

    Added compatibility with plugins.

-   **Version 1.2.3 - February 2024**
    -   New:
        -   AI-assisted application fingerprints: ML Clustering that performs cluster analysis on running process estate and recommends unique fingerprints. Create application CIs with a single click.
        -   ITOM Content Services: Crowdsource clustered running process data from customer instances with Opt-in. AI Librarians curate application classifiers and SNMP OID content every week and distribute them to all customer instances.
        -   SAM integration outcome create installed software data using process fingerprints.
    -   ITOM Content Service
        -   While Opted-in, use crowdsourced content, including running process fingerprints and SNMP OIDs, to get faster and wider visibility of your applications and technology.
-   **Version 1.0.6 - November 2023**

    This dedicated Workspace for discovery admins allows them a focused overview of Discovery administration tasks, helps them to track and address the status of Application suggestions, and allows them to participate in a Content Service that crowd sources suggestions for application fingerprinting and OIDs.


**Parent Topic:**[ServiceNow Store - ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-visibility-landing.md)


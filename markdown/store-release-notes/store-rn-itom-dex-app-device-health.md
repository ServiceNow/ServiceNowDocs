---
title: DEX Application and Device Health release notes
description: Version history for the DEX Application and Device Health application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-dex-app-device-health.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 17
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# DEX Application and Device Health release notes

Version history for the DEX Application and Device Health application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

See the [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-service-management/store-rn-itsm-now-assist.html) release notes for information on agentic AI in DEX.

-   **Version 4.3.0 - June 2026**
    -   Fixed:
        -   Fixed an issue where Metric Rule alerts generated under the count condition displayed an incorrect impacted user and configuration item. Alerts now resolve and surface the correct user and CI context.
        -   Fixed broken URL redirection on the Advanced setting page, which previously pointed to an invalid ServiceNow documentation link. The link now resolves to the correct documentation target.
        -   Restored column filtering on the device list modal and search in the Action Library, both of which had stopped responding. Admins and IT agents can again filter device lists and search remedial actions.
        -   Fixed Insights Device List filter persistence so applied filters are cleared when a new page is opened. Users no longer see stale filter conditions carry across pages.
        -   Added input validation on the value field of the Query Builder page so invalid entries are caught at edit time. Users now receive clear error feedback instead of silent failures downstream.
        -   Added missing translations across multiple pages where strings had been displaying in English regardless of session language. Non-English users now see consistent localized labels.
        -   Fixed the Create Remedial Action page so that selecting Map to an existing Remedial Action now lists actions for all operating systems instead of only Windows. Admins can map across platforms without a workaround.
        -   Renamed the Application Devices list column heading from Name to Device to better describe its contents. The label change improves clarity for IT agents triaging devices.
        -   Fixed inconsistent invocation of the Zoom call diagnostic data collector tool by AI Agents during call quality investigations. The tool now runs reliably whenever Zoom diagnostics are needed.
        -   Resolved a DEX Investigate display bug where no data appeared when CPU or memory usage was a decimal value below one percent. Sub-one-percent usage values now render correctly in investigate views.
        -   Fixed DEX Investigate so it no longer reports metrics as unavailable when battery health status is Unknown. Investigate now surfaces available metrics for devices in this state.
        -   Localized hardcoded Yes and No strings in Proactive Engagement that previously appeared in English for all locales. These values now translate based on the user's session language.
-   **Version 4.2.1 - May 2026**
    -   Custom reports enhancements
    -   Event rule enhancements
-   **Version 4.1.0 - April 2026**
    -   DEX Application and Device Health Release notes: New Features
        -   Custom Reports
            -   Added the ability to save reports with full backend persistence and a frontend save modal/popup flow.Added ability to open saved reports — system populates the query from saved tables, opens the query view in closed state, displays current results, and highlights the active report in the left navigation.Added ability to name and rename custom reports for easier identification and management.
        -   Insights
            -   Introduced a new Event Report sourced from DEX event log monitoring data, providing operational visibility into event activity.
        -   Sudo Banner
            -   Sudo banner validation now supports a command exclusion list — if a customer is not using a specific tool \(e.g., JAMF\), the corresponding sudo banner is no longer shown.
        -   Agent Dependency
            -   Updated all existing policies to use the DB view in filter conditions, improving query efficiency and consistency across agent dependency checks.
    -   Updates
        -   Fixed a "no content available" flash that appeared before the query builder page fully loaded.
        -   Resolved data mismatch between Metric Analyzer and the Performance page.
        -   Fixed automation test failures in the DEX Wizard flow within the self-remediation framework.
        -   Static location details are now correctly available for SaaS aggregate Clotho metrics.
        -   Addressed query builder defects in Clotho and applied review-driven enhancements.
-   **Version 4.0.0 - March 2026**
    -   Changed:
        -   Intune Integration
        -   New RA action Intune Sync to Device
        -   Application version cardinality
        -   Few Metrics: System Disk available \(for both macOS and Windows\)
        -   JSON Flattening:used in Query Builder
        -   Pending Updates
        -   Logins
        -   User Profiles
        -   Memory
        -   Stability
    -   New:
        -   Enable service desk agents to view and manage the top 10 CPU and memory-consuming processes in the Investigation tab of incident records. Automated snapshots every 30 minutes help you identify processes causing device issues, improving service desk productivity.
        -   View device boot time metrics to assess system startup health and identify potential issues.
        -   View GPU \(Graphics Processing Unit\) utilization metrics to gain deeper visibility into device performance.
        -   Apply remedial actions to multiple devices at once directly from the Insights page to resolve issues faster with bulk remediation.
        -   Monitor system-level events from Windows and macOS devices to gain deeper insight into device health and stability. Configure events of interest and capture event data directly in ServiceNow to support incident investigation and proactive service desk operations.
        -   Monitor application performance by application version to accelerate incident resolution and improve deployment quality. This capability supports the Service desk agent in faster root cause analysis and data-driven deployment decisions.
        -   Use the new remedial action Sync device to Intune, included with the DEX base system.
-   **Version 3.3.1 - January 2026**

    Minor defect fixes.

-   **Version 3.2.4 - December 2025**
    -   Highlights:
        -   Gain deeper visibility into performance with enhanced metrics analysis and non-persistent Virtual Desktop infrastructures \(VDIs\) monitoring, including device, application, and web page insights for faster troubleshooting.
        -   Use the Metrics analyzer to view metrics collected for a given device or application during a specific period.
        -   Monitor non-persistent VDIs with Digital End-User Experience \(DEX\) to track performance issues and troubleshoot efficiently.
        -   Gain insights into Zoom call quality and Zoom rooms performance across your organization with DEX for Zoom.
        -   Enable service desk agents to diagnose and resolve issues on DEX monitored devices directly from the Investigation tab in incident records within the Service Operations Workspace.
    -   New:
        -   Using the DEX Metrics analyzer, explore and analyze various metrics for Configuration Items \(CIs\) through selecting metrics by application, device, location, and OS.
        -   Set up monitoring of non-persistent VDIs to identify performance issues and to troubleshoot.
        -   Monitor a Web application performance at a specific page level and view the collected metrics in the Metrics analyzer.
        -   Service desk agents can diagnose and resolve common issues on DEX monitored devices from the Investigation tab in incident records within the Service Operations Workspace. View the health status of the device and related metrics, review the suggested resolutions, and execute remedial actions or follow self-help instructions to resolve the incident. Monitor the status of actions after they’re completed.
        -   DEX Desktop Assistant administrators can customize the theme for Desktop Assistant by modifying specific CSS variables. You can also customize the logo, add hyperlink cards, and map these cards to sections on the home page.
        -   Admins can view detailed metrics for Zoom calls made by users assigned to this device or who logged in within the past 15 days. The metrics include call quality, network performances, and call details enabling faster troubleshooting and improved end-user experience visibility.
        -   Using DEX for Zoom, admins can monitor Zoom Room performance across their organization, view issues in each room, and analyze root causes to promote consistent meeting experiences.
        -   DEX administrators can now manage all types of proactive rules \(both metric and configuration-based\) within a unified interface, streamlining rule management across the DEX system.
        -   The DEX base system includes the following new remedial actions:
            -   Add a registry key \(Windows\)
            -   Clear Google Chrome browsing data \(macOS and Windows\)
            -   Clear Recycle Bin \(macOS and Windows\)
            -   Configure device power scheme \(macOS and Windows\)
            -   Delete Network Drive \(Windows\)
            -   Delete a file \(Windows\)
            -   Elevate temporary admin access \(macOS and Windows\)
            -   Map Network Drive \(Windows\)
            -   Modify USB storage access: Execute \(Windows\)
            -   Modify USB storage access: Read \(Windows\)
            -   Modify USB storage access: Write \(Windows\)
            -   Modify a registry key value \(Windows\)
            -   Remediate Zscaler connectivity \(macOS and Windows\)
            -   Repair corrupt Outlook files \(macOS and Windows\)
            -   Reset Google Chrome browser settings \(macOS and Windows\)
            -   Restart Audio Services \(Windows\)
            -   Restart Microsoft OneDrive \(macOS and Windows\)
            -   Restart Microsoft Outlook \(Windows\)
            -   Updated the Clear application cache remedial action to enable selecting the Microsoft Teams application, helping improve Teams performance.
    -   Changed: By default, the Desktop Assistant home page now has two sections: My resources and Quick links. My resources includes Device health check and Network test cards, while Quick links includes Employee Center and Outages cards.
-   **Version 3.2.3 - December 2025**
    -   Highlights:
        -   Gain deeper visibility into performance with enhanced metrics analysis and non-persistent Virtual Desktop infrastructures \(VDIs\) monitoring, including device, application, and web page insights for faster troubleshooting.
        -   Use the Metrics analyzer to view metrics collected for a given device or application during a specific period.
        -   Monitor non-persistent VDIs with Digital End-User Experience \(DEX\) to track performance issues and troubleshoot efficiently.
        -   Gain insights into Zoom call quality and Zoom rooms performance across your organization with DEX for Zoom.
        -   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic AI workflow.
        -   Enable service desk agents to diagnose and resolve issues on DEX monitored devices directly from the Investigation tab in incident records within the Service Operations Workspace.
    -   New:
        -   Using the DEX Metrics analyzer, explore and analyze various metrics for Configuration Items \(CIs\) through selecting metrics by application, device, location, and OS.
        -   Set up monitoring of non-persistent VDIs to identify performance issues and to troubleshoot.
        -   Monitor a Web application performance at a specific page level and view the collected metrics in the Metrics analyzer.
        -   Service desk agents can use the DEX diagnosis and resolution agentic AI workflow to resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.
        -   Service desk agents can diagnose and resolve common issues on DEX monitored devices from the Investigation tab in incident records within the Service Operations Workspace. View the health status of the device and related metrics, review the suggested resolutions, and execute remedial actions or follow self-help instructions to resolve the incident. Monitor the status of actions after they’re completed.
        -   DEX Desktop Assistant administrators can customize the theme for Desktop Assistant by modifying specific CSS variables. You can also customize the logo, add hyperlink cards, and map these cards to sections on the home page.
        -   Admins can view detailed metrics for Zoom calls made by users assigned to this device or who logged in within the past 15 days. The metrics include call quality, network performances, and call details enabling faster troubleshooting and improved end-user experience visibility.
        -   Using DEX for Zoom, admins can monitor Zoom Room performance across their organization, view issues in each room, and analyze root causes to promote consistent meeting experiences.
        -   DEX administrators can now manage all types of proactive rules \(both metric and configuration-based\) within a unified interface, streamlining rule management across the DEX system.
        -   The DEX base system includes the following new remedial actions:
            -   Add a registry key \(Windows\)
            -   Clear Google Chrome browsing data \(macOS and Windows\)
            -   Clear Recycle Bin \(macOS and Windows\)
            -   Configure device power scheme \(macOS and Windows\)
            -   Delete Network Drive \(Windows\)
            -   Delete a file \(Windows\)
            -   Elevate temporary admin access \(macOS and Windows\)
            -   Map Network Drive \(Windows\)
            -   Modify USB storage access: Execute \(Windows\)
            -   Modify USB storage access: Read \(Windows\)
            -   Modify USB storage access: Write \(Windows\)
            -   Modify a registry key value \(Windows\)
            -   Remediate Zscaler connectivity \(macOS and Windows\)
            -   Repair corrupt Outlook files \(macOS and Windows\)
            -   Reset Google Chrome browser settings \(macOS and Windows\)
            -   Restart Audio Services \(Windows\)
            -   Restart Microsoft OneDrive \(macOS and Windows\)
            -   Restart Microsoft Outlook \(Windows\)
            -   Updated the Clear application cache remedial action to enable selecting the Microsoft Teams application, helping improve Teams performance.
    -   Changed: By default, the Desktop Assistant home page now has two sections: My resources and Quick links. My resources includes Device health check and Network test cards, while Quick links includes Employee Center and Outages cards.
-   **Version 3.1.2 - October 2025**
    -   Security fixes related to a few commands
    -   Updated app limits and fixed metrics-related issues
-   **Version 3.1.1 - August 2025**
    -   Highlights:
        -   Assess your organization's Green IT maturity with actionable insights to identify improvement areas and reduce unnecessary energy consumption and costs. You can see real time energy consumption metrics on the ESG dashboard.
        -   Track and analyze call performance for a particular user in Microsoft Teams with DEX for Microsoft 365.
        -   View the consolidated alerts related to devices and applications in the Alerts section of the Device health page.
        -   View the new DEX landing page, which includes an updated Devices world map and an improved Impacted devices card.
        -   View real-time data for alerts, change requests, and incidents that are impacting a device in the Device events section of the Device health page.
        -   Create a remedial action from a check definition, or link an existing remedial action to a check definition.
        -   Execute a remedial action for a DEX alert on multiple impacted devices simultaneously.
        -   Manage device and application configurations and monitor key DEX components in the new DEX Administration workspace.
    -   New:
        -   Assign ITIL-related roles to DEX userExercise tighter control over the role management system and role delegation. Control who has access to Express list, Alerts, and Incident records now that the ITIL-related roles have been removed from the dex\_user or dex\_engineer roles.
        -   Monitor Microsoft Teams call qualityView detailed metrics for the Microsoft Teams calls of a particular user, including call quality, network metrics, and session data, with DEX for Microsoft 365.
        -   Create Remedial Action
            -   Access the Create Remedial Action page from the DEX Administration workspace. DEX admins can create a remedial action or link an existing remedial action to a check definition.
            -   To improve the end-user experience, you can also run a remedial action on multiple impacted devices at once. The bulk remedial action can be accessed from the Alerts section.
        -   Device health page
            -   View real-time data from the past 24 hours for alerts, change requests, and incidents impacting a device in the Device events Timeline chart on the Device health page.
    -   UI changes: Coral themeCoral is now the default theme for the new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to improve your user experience. A dark theme option is available for web and mobile experiences.
    -   Enhancements to the Web and installed apps monitoring setupMap a DEX application to an existing service in the Service \(cmdb\_service\_offering\) or Service Instance \(cmdb\_service\_auto\) tables.
    -   Administration cardsManage the DEX device and application configurations efficiently with the new DEX Administration workspace.
    -   Track experience scores of an individual application, Track experience scores of an individual device groupThe Suboptimal devices column has been updated in the following pages:
        -   Application health metrics section of the Application experience overview page.
        -   Device health metrics section of the Device group page.The column now displays links to device lists that have average or poor metric scores, replacing the previous device count.
    -   Changed in this release
        -   Modified Devices page
            -   The device view is now optimized and segregated into two tabs based on the user persona. The All devices tab is for DEX operators, and the Devices by ACC status tab is for DEX operators and DEX admins.
            -   The application performance tab in the Device page has been improved. Filter performance for installed apps and web apps by date and time, and view the performance metrics for the last seven days.
            -   Access the performance page to view the performance and details of both installed and web applications.
            -   Filter the active devices to view only the devices that were active in the last five minutes.
        -   Updated landing page: The world map in the Devices section on the DEX landing page now shows the devices list instead of users list. The Impacted devices card now shows the count of impacted users based on the alerts of both the devices and the applications running on that device.
        -   Updated users link reference: The user link now redirects to Users page in the Service Operations Workspace.
        -   Changed device alerts: View alerts for both your device and its applications in the Alerts section of the Devices page.
    -   Removed in this release:
        -   Removed the Impacted users and Active users cards from the landing page.
        -   Removed the Users page.
        -   Removed the Users list page.
        -   Removed the Users and Devices filters from the Devices page.
-   **Version 3.0.8 - June 2025**
    -   New:
        -   Guided setup for setting up Agent Client Collector \(ACC\) agents
        -   Guided setup for setting up DEX Desktop Assistant
        -   Guided setup for setting up DEX Browser Extension
        -   Revamped DEX Administration page on Service Operations Workspace \(SOW\)
    -   Fixed: Minor fixes to Application registration, Fenix enrichment, and Agent policy.
-   **Version 3.0.2 - May 2025**
    -   New:
    -   1.  Enforcing security policy via Windows registry key monitoring: Once the admin has configured the registry, DEX starts real-time tracking of these registry values across all corporate devices. The outcomes of this feature are listed below:
    -   The DEX admin successfully detects and resolves registry misconfigurations.
    -   IT teams ensure policy enforcement across all endpoints.
    -   The organization reduces security risks and maintains compliance effortlessly.
2.  Automated device scanning via ACC
    -   DEX scans all managed devices for the presence of executables.
    -   DEX performs continuous or scheduled scanning to ensure updated results.
    -   DEX Insights page shows Summary view.
3.  Added a new remedial action for app crashes using JAMF, supporting base system applications such as Teams, Outlook, and Zoom
4.  Added a new metric for app freeze detection and introduced a new remedial action to clear cache for the application on both macOS and Windows devices.
5.  Enable the Device health check capability provided by DEX Self-service to diagnose and resolve device issues. Your end users can access this capability through Desktop Assistant, Employee Center, or Virtual Agent to self-resolve detected issues.
-   **Version 2.5.5 - March 2025**

    Fixed: Minor bug fixes related to Access Control List \(ACL\) and application creation.

-   **Version 2.5.0 - February 2025**
    -   New:
        -   Digital Experience Score: Digital Experience Score measures and consolidates quantitative and qualitative data to provide a holistic view into your organization's digital employee experience. Digital Experience Score analyses three key data sources:
            -   Monitored metrics from end-user devices
            -   User sentiment
            -   Service desk experience
        -   Provision for Digital End-User Experience \(DEX\) service desk agent to take actions on a device:
            -   Supported actions:
                -   Clear application cache
                -   Clear browser cache
                -   Clear DNS cache
                -   End process
                -   Perform disk cleanup
                -   Restart service
        -   Application network experience: Get visibility into application performance across network paths, tracking key metrics such as latency, packet loss, and jitter.
        -   New in metrics monitoring:
            -   System compliance score: A holistic score \(1-100%\) reflecting compliant and non-compliant system attributes and applications.
            -   Enhanced memory monitoring: New charts for virtual memory, pages/sec, page usage, and page file size to gain deeper visibility into memory utilization and paging performance.
            -   User application CPU consumption: Leverage a detailed breakdown of CPU usage by user applications to identify resource-heavy applications and optimize CPU usage.
            -   Disk performance charts metrics: New set of metrics such as Avg. disk sec/read, write and transfer, disk queue length, and disk time % to pinpoint disk bottlenecks and improve storage performance.
            -   Energy consumption for macOS: Energy charts tracking Total energy, CPU/GPU energy, and ANE energy usage to analyze trends, optimize power efficiency, and support sustainability goals.
            -   Additional hardware and OS details: Provides key details such as CPU processor ID, Windows power plans, and OS metrics \(architecture, version, install date, memory statistics\).
    -   Changed:
        -   Web application management: Updates to web application configuration where DEX admins can configure an existing web application for performance monitoring.
-   **Version 2.4.1 - November 2024**
    -   New:
        -   DEX Insights features:
            -   System compliance report: This feature highlights the applications and attributes on devices that are in compliance with the Zero Trust policy. This will provide a comprehensive view of how well the devices comply with customer-defined security measures.
            -   System performance: This capability identifies high-performance devices by monitoring critical metrics such as CPU usage, memory consumption, disk activity, \(Input/Output\) I/O usage read, and I/O usage write. This ensures a clear understanding of how device performance impacts overall system health.
            -   Network performance monitoring: Introducing advanced metrics like jitter, latency, and packet loss with a visual representation of network hops. This will provide real-time insights into network performance to quickly identify bottlenecks and areas for optimization.
    -   Added:
        -   Device metrics: Added new device-level metrics including memory usage, system time, and page file size, among others. These metrics will provide deeper insights into device health and performance.
    -   Changed:
        -   UI improvements: UI improvements were made to enhance usability, simplify navigation, and improve the overall experience.
        -   Proactive Engagement: Introduced proactive notifications and updated content for battery health catalog requests, along with alerts to notify users about important system metrics, such as system time. This will help users take preemptive actions and ensure optimal device performance.
-   **Version 2.3.0 - August 2024**
    -   Changed:
        -   Metric rules integration with Proactive Engagement
        -   Metric UI improvements
        -   Remedial action improvements
        -   DEX Insight reports
        -   Service desk user role
-   **Version 2.2.2 - June 2024**
    -   Fixed:
        -   Metric rule improvements
        -   Performance improvements
-   **Version 2.2.1 - May 2024**
    -   As a component of the Digital End-User Experience \(DEX\) product, IT installs this software on end-user devices to monitor applications, networks, and devices to detect issues before they result in downtime and reduce employee productivity.
    -   Previously, IT organizations reacted to issues only after employees submitted an incident ticket. This challenge has been compounded by the growing use of SaaS solutions for important employee digital services, where IT has even lesser insight into the employee experience. This solution bridges that gap, enabling IT to identify and resolve the issues proactively.
    -   ServiceNow Digital End-User Experience extends technology supervision to the devices that employees use with a focus on everything that makes up the experience, which includes SaaS apps, installed apps, and device metrics. DEX product suite includes Desktop Assistant, which seamlessly connects the employee with resources for self-service and higher levels of support. IT teams can use this feature to share outage notifications or important announcements, while employees can perform their own network tests and diagnostics.


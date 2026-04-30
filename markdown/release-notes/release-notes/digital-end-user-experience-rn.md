---
title: Digital End-User Experience release notes
description: The ServiceNow Digital End-User Experience \(DEX\) application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. The DEX suite helps you resolve device and application issues proactively and provides easy access to self-service options. DEX was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
---

# Digital End-User Experience release notes

The ServiceNow® Digital End-User Experience \(DEX\) application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. The DEX suite helps you resolve device and application issues proactively and provides easy access to self-service options. DEX was enhanced and updated in the Zurich release.

## Digital End-User Experience highlights for the Zurich release

-   Track and analyze call performance for a particular user in Microsoft Teams with DEX for Microsoft 365.
-   View the consolidated alerts related to devices and applications in the Alerts section of the Device health page.
-   View the new DEX landing page, which includes an updated Devices world map and an enhanced Impacted Devices card.
-   View real-time data for alerts, change requests, and incidents that are impacting a device in the Device events section of the Device health page.
-   Create a remedial action from a check definition, link an existing remedial action to a check definition, and execute a remedial action on multiple impacted devices for a DEX alert simultaneously.
-   Manage device and application configurations and monitor key DEX components in the new DEX Administration workspace.
-   Gain deeper visibility into performance with enhanced metrics analysis and non-persistent Virtual Desktop infrastructures \(VDIs\) monitoring, including device, application, and web page insights for faster troubleshooting.
-   Use the Metrics analyzer to view metrics collected for a given device or application during a specific period.
-   Monitor non-persistent VDIs with Digital End-User Experience \(DEX\) to track performance issues and troubleshoot efficiently.
-   Gain insights into Zoom call quality and Zoom rooms performance across your organization with DEX for Zoom.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic AI workflow.
-   Enable service desk agents to diagnose and resolve issues on DEX monitored devices directly from the Investigation tab in incident records within the Service Operations Workspace.

See [Digital End-User Experience](https://www.servicenow.com/docs/access?context=dex-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

**Important:** Digital End-User Experience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Digital End-User Experience to Zurich

For details on DEX data migration, refer to the [DEX data migration to allocated, last logged in user, last logged in location column of Dex device table \[KB2144029\]](https://support.servicenow.com/kb?sys_kb_id=57fcf86d97ed6650dfd73dae2153af59&id=kb_article_view) and [DEX data migration to CI type column of Alert Metadatas table \[KB2141007\]](https://support.servicenow.com/kb?sys_kb_id=269e049147e5aa503b05ff48436d433c&id=kb_article_view) articles in the Now Support Knowledge Base.

## New in the Zurich release

-   **[View collected metrics with Metrics analyzer](https://www.servicenow.com/docs/access?context=view-dex-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Using the DEX Metrics analyzer, explore and analyze various metrics for Configuration Items \(CIs\) through selecting metrics by application, device, location, and OS.

-   **[Monitoring non-persistent VDIs](https://www.servicenow.com/docs/access?context=monitoring-np-vdis&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Set up monitoring of non-persistent VDIs to identify performance issues and to troubleshoot.

-   **[Set up page-level monitoring](https://www.servicenow.com/docs/access?context=set-up-page-level-monitoring&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Monitor a Web application performance at a specific page level and view the collected metrics in the Metrics analyzer.

-   **[Assign ITIL-related roles to DEX users](https://www.servicenow.com/docs/access?context=components-installed-with-dex&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Exercise tighter control over the role management system and role delegation. Control who has access to Express list, Alerts, and Incident records after the ITIL-related roles have been removed from the dex\_user or dex\_engineer roles.

-   **[Monitor Microsoft Teams call quality](https://www.servicenow.com/docs/access?context=monitor-teams-call-quality&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    View detailed metrics for the Microsoft Teams calls of a particular user, including call quality, network metrics, and session data, with DEX for Microsoft 365.

-   **[Create a remedial action](https://www.servicenow.com/docs/access?context=create-remedial-action&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Access the Create Remedial Action page from the DEX Administration workspace. DEX admins can create a remedial action or link to an existing remedial action to a check definition. To enhance the end-user experience, you can also run the remedial action on multiple impacted devices at once.

-   **[Device health page](https://www.servicenow.com/docs/access?context=user-health-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    View real-time data from the past 24 hours for alerts, change requests, and incidents impacting a device in the Device events Timeline chart on the Device health page.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Service desk agents can use the DEX diagnosis and resolution agentic AI workflow to resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[Incident investigation with DEX](https://www.servicenow.com/docs/access?context=dex-diagnostics-guided-resolutions&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Service desk agents can diagnose and resolve common issues on DEX monitored devices from the Investigation tab in incident records within the Service Operations Workspace. View the health status of the device and related metrics, review the suggested resolutions, and execute remedial actions or follow self-help instructions to resolve the incident. Monitor the status of actions after they’re completed.

-   **[Customize themes for Desktop Assistant](https://www.servicenow.com/docs/access?context=customize-da-theme&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), [Customize Desktop Assistant home page](https://www.servicenow.com/docs/access?context=change-home-page-title&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), and [Create a hyperlink card in Desktop Assistant](https://www.servicenow.com/docs/access?context=create-hyperlink-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    DEX Desktop Assistant administrators can customize the theme for Desktop Assistant by modifying specific CSS variables. You can also customize the logo, add hyperlink cards, and map these cards to sections on the home page.

-   **[Monitor Zoom call quality using DEX](https://www.servicenow.com/docs/access?context=monitor-zoom-call-quality-using-dex&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Admins can view detailed metrics for Zoom calls made by users assigned to this device or who logged in within the past 15 days. The metrics include call quality, network performances, and call details enabling faster troubleshooting and improved end-user experience visibility.

-   **[View Zoom room metrics](https://www.servicenow.com/docs/access?context=view-zoom-room-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Using DEX for Zoom, admins can monitor Zoom Room performance across their organization, view issues in each room, and analyze root causes to promote consistent meeting experiences.

-   **[Added new remedial actions](https://www.servicenow.com/docs/access?context=dex-diff-ra&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The DEX base system includes the following new remedial actions:

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
-   **[Enhanced metric rule experience](https://www.servicenow.com/docs/access?context=create-metric-rules&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    DEX administrators can now manage all types of proactive rules \(both metric and configuration-based\) within a unified interface, streamlining rule management across the DEX system.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and knowledge articles to resolve boot performance problems quickly.

-   **[View GPU device metric details](https://www.servicenow.com/docs/access?context=user-device-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Monitor GPU and VRAM \(Video Random Access Memory\) usage on the Device page to assess graphics performance and identify bottlenecks. GPU usage shows the percentage of graphics processing capacity in use, while VRAM usage highlights memory consumption for graphics intensive workloads. These metrics help detect rendering issues, memory intensive applications, and performance degradation enabling faster investigation and resolution of GPU related device problems.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Enhancements to the web and installed apps monitoring setup](https://www.servicenow.com/docs/access?context=admin-new-app-form&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Map a DEX application to an existing service in the Service \[cmdb\_service\_offering\] or Service Instance \[cmdb\_service\_auto\] tables.

-   **[Administration cards](https://www.servicenow.com/docs/access?context=administration-cards&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Manage the DEX device and application configurations efficiently with the new DEX Administration workspace.

-   **[Track experience scores of an individual application](https://www.servicenow.com/docs/access?context=dexscr-track-application-experience&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) and [Track experience scores of an individual device group](https://www.servicenow.com/docs/access?context=dexscr-track-device-group-experience&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The Suboptimal devices column has been updated in the following pages:

    -   Application health metrics section of the application experience overview page.
    -   Device health metrics section of the device group page.
    The column now displays links to device lists that have average or poor metric scores, replacing the previous device count.


## Changed in this release

-   **[Use DEX Desktop Assistant](https://www.servicenow.com/docs/access?context=use-dex-desktop-exp&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    By default, the Desktop Assistant home page now has two sections: My resources and Quick links. My resources includes Device health check and Network test cards, while Quick links includes Employee Center and Outages cards.

-   **[Modified Devices page](https://www.servicenow.com/docs/access?context=dex-workspace-devices-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   The device view is now optimized and segregated into two tabs based on the user persona. The **All devices** tab is for DEX operators, and the **Devices by ACC status** tab is for DEX operators and DEX admins.
    -   The application performance tab in the Device page has been enhanced. Filter performance for installed apps and web apps by date and time, and view the performance metrics for the last seven days.
    -   Access the performance page to view the performance and details of both installed and web applications.
    -   Filter the active devices to view only the devices that were active in the last five minutes.
-   **[Updated landing page](https://www.servicenow.com/docs/access?context=dashboard-cards&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The world map in the **Devices** section on the DEX landing page now shows the devices list instead of users list. The Impacted Devices card now shows the count of impacted users based on the alerts of both the devices and the applications running on that device.

-   **[Updated users link reference](https://www.servicenow.com/docs/access?context=devices-form&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The user link now redirects to Users page in Service Operations Workspace.

-   **[Changed device alerts](https://www.servicenow.com/docs/access?context=user-health-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    View alerts for both your device and its applications in the Alerts section of the Devices page.


## Removed in this release

-   Removed the **Impacted users** and **Active users** cards from the landing page.
-   Removed the **Users** page.
-   Removed the **Users list** page.
-   Removed the **Users** and **Devices** filters from the **Devices** page.

## Activation information

Install Digital End-User Experience by requesting it from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Enable the DEX browser extension to monitor web applications for various operational or performance-based metrics on your system. For more information, see [Enable DEX browser extension](https://www.servicenow.com/docs/access?context=enable-dex-browser-extension&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Localization information

Localization is applicable to DEX in all languages supported by the ServiceNow AI Platform.

## Related ServiceNow applications and features

-   **[Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Use the DEX integration with the Operational Sustainability Management to assess your organization's Green IT maturity, with actionable insights and the ability to identify improvement areas and help reduce unnecessary energy consumption and costs. Pinpoint energy waste across devices, hardware, and IT infrastructure, as well as track the carbon footprint of CO2 emissions. You can see real-time energy consumption metrics on the ESG dashboard.

-   **[DEX for Service Desk agents](https://www.servicenow.com/docs/access?context=features-of-investigation-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As a Service Desk agent, view device metrics from within the platform by navigating to the DEX Device health page. You can access the page from the Core UI incident experience or from the **Investigate** tab Service Operations Workspace \(SOW\).

-   **[Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    From Desktop Assistant, use generative AI to enhance your productivity and efficiency through conversation and proactive experiences.

-   **[ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=itsm-virtual-agent&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The ServiceNow Virtual Agent application enables you to scale your IT organization, where technicians can address more challenging IT-related user requests and incidents.

-   **[ITSM Success Dashboard](https://www.servicenow.com/docs/access?context=success-dashboard-indicator-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The ServiceNow ITSM Success Dashboard enables the leadership team and process owners to gain insights into the performance of their ServiceNow IT Service Management \(ITSM\) implementation using the KPIs defined in the ServiceNow AI Platform®.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)


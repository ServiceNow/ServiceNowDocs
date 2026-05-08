---
title: Digital End-User Experience release notes
description: The ServiceNow Digital End-User Experience application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. Digital End-User Experience was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Digital End-User Experience release notes

The ServiceNow® Digital End-User Experience application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. Digital End-User Experience was enhanced and updated in the Australia release.

## Digital End-User Experience highlights for the Australia release

-   Enable service desk agents to view and manage the top 10 CPU and memory-consuming processes in the **Investigation** tab of incident records, with automated snapshots every 30 minutes to quickly identify and end processes causing device issues, thus improving service desk productivity.
-   Diagnose and resolve Zoom call issues with the new Zoom AI capability, which provides device-level root cause analysis and suggested resolutions.
-   Monitor device boot time and use Now Assist to quickly diagnose startup delays and get actionable resolutions to resolve boot performance issues.
-   View device boot time metrics to assess system startup health and identify potential issues.
-   Gain deeper visibility into device performance with GPU \(Graphics Processing Unit\) utilization metrics.
-   Apply remedial actions to multiple devices at once directly from the Insights page to resolve issues faster with bulk remediation.
-   Monitor system-level events from Windows and macOS devices to gain deeper insight into device health and stability. Configure events of interest and capture event data directly in ServiceNow to support incident investigation and proactive service desk operations.
-   Generate event insights reports from collected event data to analyze device health trends and support incident investigation.
-   Save custom insight reports and access them from the left navigation panel for faster, repeatable analysis.

See Digital End-User Experience for more information.

**Important:** Digital End-User Experience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Reviewing top processes by resource usage in incident investigation with DEX**

    Service desk agents can now view automated snapshots of the top 10 CPU and memory-consuming processes directly in the **Investigation** tab of incident records. The snapshots that are captured every 30 minutes are initially triggered when an incident is created and a configuration item is tagged. You can refresh and filter snapshots over different time ranges and monitor processes causing device issues.

-   **DEX issue diagnosis and resolution agentic workflow**

    Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **Event monitoring with DEX**

    Monitor system events on Windows and macOS devices to track critical system events available with your base system, configure additional events to monitor, and review collected event data stored in your ServiceNow instance.

    Monitor system-level events, such as application crashes, unexpected shutdowns, disk space warnings, failed login attempts, and service failures. The DEX agent captures event data directly from managed endpoints. Activate or deactivate events or add custom events to extend monitoring beyond the base system catalog.

-   ****

    Generate an insights report from event log data collected by the DEX agent.

    Save useful queries as named reports in the Insights reporting area to preserve them for future use. After you save a report, it appears in the left navigation panel for quick access. IT operators, L2 analysts, DEX engineers, and administrators can save, name, and retrieve reports. Role-based access controls restrict save and retrieval operations to the DEX Engineer and Administrator roles.

-   **AI-powered root cause analysis for Zoom call quality issues**

    Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant knowledge articles to help resolve the issue efficiently.

-   **Get AI driven insights for boot time performance**

    Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and knowledge articles to resolve boot performance problems quickly.

-   **View GPU device metric details**

    Monitor GPU and VRAM \(Video Random Access Memory\) usage on the Device page to assess graphics performance and identify bottlenecks. GPU usage shows the percentage of graphics processing capacity in use, while VRAM usage highlights memory consumption for graphics intensive workloads. These metrics help detect rendering issues, memory intensive applications, and performance degradation enabling faster investigation and resolution of GPU related device problems.

-   **Applications**

    Monitor application performance by application version to accelerate incident resolution and improve deployment quality. This enables the Service desk agent in faster root cause analysis and data-driven deployment decisions improving the overall end-user experience.

-   **Bulk Remediation for Impacted Devices**

    Select multiple impacted devices from the Insights page and apply remedial actions in bulk. Service desk agents can now resolve issues across multiple devices simultaneously, improving productivity and reducing manual effort.

-   **Digital End-User Experience Remedial Actions**

    The DEX base system includes the new remedial action Sync device to Intune.


-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Digital End-User Experience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Enable the DEX browser extension to monitor web applications for various operational or performance-based metrics on your system. For more information, see Enable DEX browser extension.

## Localization information

Localization is applicable to DEX in all languages supported by the ServiceNow AI Platform.

## Related ServiceNow applications and features

-   **Operational Sustainability Management \(formerly Environmental, Social, and Governance\)**

    Use the DEX integration with the Operational Sustainability Management to assess your organization's Green IT maturity, with actionable insights and the ability to identify improvement areas and help reduce unnecessary energy consumption and costs. Pinpoint energy waste across devices, hardware, and IT infrastructure, as well as track the carbon footprint of CO2 emissions. You can see real-time energy consumption metrics on the ESG dashboard.

-   **DEX for Service Desk agents**

    As a Service Desk agent, view device metrics from within the platform by navigating to the DEX Device health page. You can access the page from the Core UI incident experience or from the **Investigate** tab Service Operations Workspace \(SOW\).

-   **Now Assist for IT Service Management \(ITSM\)**

    From Desktop Assistant, use generative AI to enhance your productivity and efficiency through conversation and proactive experiences.

-   **ITSM Virtual Agent**

    The ServiceNow Virtual Agent application enables you to scale your IT organization, where technicians can address more challenging IT-related user requests and incidents.

-   **ITSM Success Dashboard**

    The ServiceNow ITSM Success Dashboard enables the leadership team and process owners to gain insights into the performance of their ServiceNow IT Service Management \(ITSM\) implementation using the KPIs defined in the ServiceNow AI Platform®.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)


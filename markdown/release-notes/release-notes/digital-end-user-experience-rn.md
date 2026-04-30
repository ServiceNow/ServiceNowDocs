---
title: Digital End-User Experience release notes
description: The ServiceNow Digital End-User Experience \(DEX\) solution is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. The DEX suite includes Application and Device Health, which helps IT resolve device and application issues proactively, and Desktop Assistant, which provides easy access to self-service options. Digital End-User Experience was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Digital End-User Experience release notes

The ServiceNow® Digital End-User Experience \(DEX\) solution is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. The DEX suite includes Application and Device Health, which helps IT resolve device and application issues proactively, and Desktop Assistant, which provides easy access to self-service options. Digital End-User Experience was enhanced and updated in the Yokohama release.

## Digital End-User Experience highlights for the Yokohama release

-   Monitor whether the devices across your organization are adhering to the established application and policy metric compliance rules using the System compliance report.
-   Identify high-performance devices and learn the correlation between your device performance and overall system health by monitoring critical metrics, such as CPU usage, in the System performance report.
-   Monitor the multiple facets of the end-user network performance, including connection details, connection stability and path metrics, and application network hops.
-   Manage what DEX metrics are collected for a DEX agent policy, turn off collection of a metric, or change the frequency for a metric collection.
-   Set up file management to track and manage executable files on your organization devices.
-   Track and manage the Windows registry keys configured for monitoring on your organization devices.
-   View client health metrics with the Microsoft Configuration Manager \(MCM\) application.
-   Track the impacted device details from the Service Operations Workspace landing page. You can also track the details of all the impacted users and impacted devices from the active alerts.
-   Determine the device location based on the pre-defined custom logic.
-   Diagnose and resolve device issues using the Device health check capability provided by Digital End-user Experience Self-service.
-   Track the digital experience scores of the applications and devices that your employees use with the Digital Experience Score​ dashboard.
-   The Proactive Engagement application is integrated as part of the DEX suite of applications and is installed along with DEX.

See [Digital End-User Experience](https://www.servicenow.com/docs/access?context=dex-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

**Important:**

-   Digital Experience Score​ is supported from the Yokohama release onward. If you see the Digital Experience Score dashboard in Xanadu, you must disable the DEX Score feature. For more information, see the [Disable DEX Score Feature in Xanadu](https://support.servicenow.com/kb?sys_kb_id=5165617f970aaa90f03d739c1253af67&id=kb_article_view) article \[KB2224330\] in the Now Support Knowledge Base.
-   Digital End-User Experience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Digital End-User Experience to Yokohama

To upgrade your DEX Desktop Assistant, do the following:

1.  Install the latest version of the Desktop Assistant in your instance.
2.  With admin rights, reinstall the Desktop Assistant on your local machine even if you have the latest version.

## New in the Yokohama release

-   **[Manage your system compliance report](https://www.servicenow.com/docs/access?context=manage-compliance-report&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Identify vulnerabilities and keep end-user devices secure and efficient by confirming that they meet security policies and regulatory standards. The Compliance report provides a comprehensive view of how well the end-user devices are adhering to the security measures of your organization.

-   **[Monitor system performance](https://www.servicenow.com/docs/access?context=monitor-system-performance&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Identify high-performance devices by monitoring critical metrics, such as CPU usage, memory consumption, disk activity, and input/output \(IO\) reading and writing speeds. Monitoring system performance provides information about how device performance impacts overall system health.

-   **[Check your device's health](https://www.servicenow.com/docs/access?context=exploring-dex-self-service&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Digital End-user Experience Self-service \(DEX Self-service\) enables you to check the performance of your device using a Device health check. You can check the device health on demand and resolve the issues detected by DEX by leveraging the recommended resolutions for the issues. The resolutions can either be remedial actions \(that you can trigger via a button\), self-help instructions, or URL. You can also use Device actions which can be triggered even when no issues are detected on the device.  These actions enable you to maintain good performance of the devices and applications

-   **[Monitor your user apps network](https://www.servicenow.com/docs/access?context=monitor-user-apps-network&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Monitor the advanced metrics like jitter, latency, and packet loss with a visual representation of network hops. These metrics provide real-time insights into network performance, helping to identify bottlenecks and areas for optimization quickly.

-   **[Additional device metrics](https://www.servicenow.com/docs/access?context=user-device-details-pages&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Get insights into device health and performance using the newly added device-level and application metrics. These metrics include memory usage, system time, energy consumption, and page file size. They're available in the following pages under Device health or Advanced app metrics:

    -   Operating system
    -   System compliance metrics
    -   Windows power plan
    -   File management
    -   Windows registry
    -   Microsoft Configuration Manager \(MCM\) application
    -   Application freeze
-   **[Digital Experience Score​](https://www.servicenow.com/docs/access?context=dexscr-digital-experience-score&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Measure and consolidate both quantitative and qualitative data to gain a holistic view of the digital employee experience. The Digital Experience Score​ dashboard \(DEX Score\) provides data-driven insights to improve your employees' digital experience.

    DEX Score compiles health metrics scores, user sentiment scores, and service experience scores for applications and devices to calculate the overall digital experience score.

    Access device lists based on individual device or application health metric scores. Review the list to identify devices with scores below the average for each metric.

-   **[Proactive Engagement](https://www.servicenow.com/docs/access?context=proactive-engagement-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Inform employees by providing any self-help instructions or notifications by Desktop Assistant and email as the two new notification channels along with the existing Virtual Agent option.

    Explore what Proactive Engagement has to offer with new use cases as part of the base system. The new use cases include poor Wi-Fi connectivity, device crash, app crash, app freeze, Jamf execution, and disconnected Zscaler.

    User criteria help in grouping the users based on certain conditions. You can set the user criteria settings through Proactive Engagement.

    Depending on the remedial action chosen from the list while creating a new metric rule, specific input parameters can be configured with advanced settings that will fetch a static input.


## UI changes

-   **[DEX UI enhancements](https://www.servicenow.com/docs/access?context=dex-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Several user interface improvements have been made to help enhance usability and make navigation more intuitive, leading to a better overall user experience.


## Activation information

Install Digital End-User Experience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Enable the DEX browser extension for monitoring Web applications to collect various operational or performance-based metrics on your system. For more information, see [Enable DEX browser extension for monitoring web/SaaS applications](https://www.servicenow.com/docs/access?context=enable-dex-browser-extension&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

## Localization information

Localization is applicable to DEX in all languages supported by the ServiceNow AI Platform.

## Related ServiceNow applications and features

-   **[DEX for Service Desk Agents](https://www.servicenow.com/docs/access?context=enable-dex-browser-extension&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    As a Service Desk agent, view device metrics from within the platform by navigating to the DEX Device health page. You can access the page from the Core UI incident experience or from the **Investigate** tab Service Operations Workspace \(SOW\).

-   **[Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    From Desktop Assistant, use generative AI to enhance your productivity and efficiency through conversation and proactive experiences.

-   **[ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=itsm-virtual-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The ServiceNow Virtual Agent application enables you to scale your IT organization, where technicians can address more challenging IT-related user requests and incidents.

-   **[ITSM Success Dashboard](https://www.servicenow.com/docs/access?context=success-dashboard-indicator-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The ServiceNow ITSM Success Dashboard enables the leadership team and process owners to gain insights into the performance of their ServiceNow IT Service Management \(ITSM\) implementation using the KPIs defined by the ServiceNow AI Platform®.

-   **[Digital Experience Score​](https://www.servicenow.com/docs/access?context=dexscr-digital-experience-score&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Using the DEX Score dashboard, monitor the digital experience scores of the applications and devices that your employees are using. By exploring the individual device and application experience scores, you can identify what is working well for employees and what needs improvement.

-   **[Digital End-user Experience Self-service](https://www.servicenow.com/docs/access?context=dex-self-service&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Using DEX Self-service, you check your device heath, diagnose the issues, and use the resolutions to improve the device health.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)


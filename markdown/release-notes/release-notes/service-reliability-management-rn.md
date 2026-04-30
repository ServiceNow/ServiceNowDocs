---
title: Service Reliability Management release notes
description: The ServiceNow Service Reliability Management \(SRM\) application helps your organization respond, collaborate, track, and self-remediate when working on alerts and incidents. SRM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Service Reliability Management release notes

The ServiceNow® Service Reliability Management \(SRM\) application helps your organization respond, collaborate, track, and self-remediate when working on alerts and incidents. SRM was enhanced and updated in the Zurich release.

## SRM highlights for the Zurich release

-   Auto-generate service level objectives \(SLOs\) to help teams track service reliability in SRM.
-   Starting in version 6.5.0, remove unneeded services from SRM to keep your monitoring data relevant.
-   Starting in version 6.5.0, track real downtime and customer impact with outage-based service level indicators \(SLIs\).
-   Get timely error budget updates that reflect the impact of ongoing, open alerts.
-   Track, manage, and visualize service performance with the Service reliability dashboard.

See [Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** SRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Auto-generate SLOs for SRM services](https://www.servicenow.com/docs/access?context=now-assist-itom-manage-generated-slos&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Use the SLO creator agent to generate SLOs for your SRM services. This capability is available with the AI Agents for SLO \(sn\_ai\_agents\_slo\) plugin. The agent analyzes incidents, alerts, and outage events to automatically create SLOs, helping teams adopt SLOs faster and track service reliability.

-   **[Remove a service from SRM](https://www.servicenow.com/docs/access?context=sr-remove-service&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 6.5.0, remove a service from SRM when you no longer need to track or monitor its reliability. Removing a service clears it from SRM views, including the Service page and Service reliability dashboard. The service remains in the Configuration Management Database \(CMDB\), and you can add it back to SRM at any time.

-   **[Create outage-based SLIs](https://www.servicenow.com/docs/access?context=sr-create-slo-sli&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 6.5.0, add outage-based SLIs to track real downtime and customer impact. Use them with existing alert-based SLIs for a broader view of reliability. The flow for creating service level objectives \(SLOs\), SLIs, and error budget policies is also improved to simplify setup.

-   **[Keep teams informed with notification destinations](https://www.servicenow.com/docs/access?context=create-notification-destination&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Send notifications about error budget policy violations to notification destinations. The first supported destination is Microsoft Teams, which lets you post details in specific channels and link back to SRM for further investigation.

-   **[Monitor service reliability in a dashboard](https://www.servicenow.com/docs/access?context=sr-service-dashboard-visualizations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Use the Service reliability dashboard to monitor and manage service performance. The dashboard offers multiple visualizations to help you track error budgets, monitor SLOs, and identify issues across your services. Starting in version 6.4.1, monitor reliability using interactive charts and a new service level objective \(SLO\) table in the Service reliability dashboard.

-   **[Customize team approval settings](https://www.servicenow.com/docs/access?context=sr-add-approval-teams&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Customize team governance with more flexibility and less manual effort. You can assign different approval teams for new and existing team requests. The customization options are also fully available in the Service Operations Workspace Admin Center and no longer require manual setup in the Catalog Builder.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Work notes for SLOs](https://www.servicenow.com/docs/access?context=sr-view-slo&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.6.1, SLOs include work notes on the Details tab. Posted work notes are visible in the Activity panel, providing a unified view of both manual and automated SLO changes.

-   **[Microsoft Teams notification update](https://www.servicenow.com/docs/access?context=srm-notifications-messages&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.5.0, the error budget policy violation notification in Microsoft Teams now includes a button instead of a text link. The new button makes it easier to open the relevant SLO directly in SRM.

-   **[New service class names](https://www.servicenow.com/docs/access?context=sr-work-services&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.5.0, application service and technical service are now called service instance and technology management service. The terminology update aligns with current naming standards.

-   **[Enhanced SLO table view](https://www.servicenow.com/docs/access?context=sr-work-SLI-SLO&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.5.0, the Service level objectives table on the SRM Reliability metrics tab has a new layout, which improves readability and navigation.

-   **[New navigation for Integrations Launchpad and Alert Automation](https://www.servicenow.com/docs/access?context=sr-work-integrations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.5.0, the icons for Integrations Launchpad and Alert Automation have been removed from the primary navigation. You can now access them under the ITOM Admin Experience icon in the Service Operations Workspace.

-   **[Updated Service reliability dashboard](https://www.servicenow.com/docs/access?context=sr-service-dashboard-visualizations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 6.5.0, the High burn rate chart now links to a chart view instead of a list view. The new link helps you better visualize and explore SLO performance.


## Activation information

Install SRM or ITOM Mobile Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugin is new in Zurich:

    AI Agents for SLO \(sn\_ai\_agents\_slo\): AI agents for SLO can help customers improve service resilience.


## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Use SRM in Service Operations Workspace to manage SLOs alongside other IT Operations Management workflows.

-   **[Alert automation in Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-itom-alert-automation&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Work with alert automation to respond to alerts, improve service reliability, and scale staff resources.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)


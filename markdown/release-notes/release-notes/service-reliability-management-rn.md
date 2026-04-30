---
title: Service Reliability Management release notes
description: The ServiceNow Service Reliability Management \(SRM\) application helps your organization respond, collaborate, track, and self-remediate when working on alerts and incidents. SRM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Service Reliability Management release notes

The ServiceNow® Service Reliability Management \(SRM\) application helps your organization respond, collaborate, track, and self-remediate when working on alerts and incidents. SRM was enhanced and updated in the Yokohama release.

## SRM highlights for the Yokohama release

-   View and assess alerts in one place with Express List.
-   Starting in version 6.3, access SRM features on the go with ITOM Mobile Agent.
-   Starting in version 6.4, inform teams by setting up notification destinations and attaching them to error budget policies.
-   Starting in version 6.4, track, manage, and visualize service performance with the Service reliability dashboard.
-   Starting in version 6.4, get timely error budget updates that reflect the impact of ongoing, open alerts.

See [Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** SRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Enhance monitoring for distributed teams with Express List](https://www.servicenow.com/docs/access?context=express-list&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Improve monitoring with Express List. Express List replaces the **Alerts** tab and helps distributed SRM teams focus on the services, priorities, or alerts that matter to them.

-   **[Track SLO update history](https://www.servicenow.com/docs/access?context=sr-edit-sli-slo&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    View and track SLO update history with new naming conventions. Edited SLOs now receive unique names, such as Uptime \(1\) or Uptime \(2\), instead of keeping their original names. This update improves clarity and helps you distinguish between versions.

-   **[Add SLOs to change approval policies](https://www.servicenow.com/docs/access?context=sr-add-change-approval-slos&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Define change approval policies to approve updates or modifications in your system. You can now add the following policy inputs, helping you integrate critical information into the approval process:

    -   SLO with the lowest percentage of error budget remaining
    -   SLO with the highest burn rate
-   **[Assign teams to TSOs](https://www.servicenow.com/docs/access?context=sr-add-service&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Manage your services effectively by assigning teams to TSOs. TSOs, which are specific components within a parent technical service, can now be used in the SRM service list. Assigning SRM teams to TSOs helps decentralized teams focus on the services they’re responsible for.

-   **[Stay connected and keep services reliable with ITOM Mobile Agent](https://www.servicenow.com/docs/access?context=itom-mobile-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.3, use ITOM Mobile Agent to access SRM features on iOS and Android devices. With ITOM Mobile Agent, you can track alerts, manage incidents, and work on tasks on the go. You can also manage on-call schedules by checking shifts, requesting time off, and filling gaps.

-   **[Create SLIs on configuration items](https://www.servicenow.com/docs/access?context=sr-create-slo-sli&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.3, filter an SLI to a specific configuration item within the parent service hierarchy. This feature lets you monitor the individual components of a service, helping you accurately track service health and identify root causes faster.

-   **[Keep teams informed with notification destinations](https://www.servicenow.com/docs/access?context=create-notification-destination&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.4, send notifications about error budget policy violations to notification destinations. The first supported destination is Microsoft Teams, which lets you post details in specific channels and link back to SRM for further investigation.

-   **[Monitor service reliability in a dashboard](https://www.servicenow.com/docs/access?context=sr-service-dashboard-visualizations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.4, use the Service reliability dashboard to monitor and manage service performance. The dashboard offers multiple visualizations to help you track error budgets, monitor SLOs, and identify issues across your services. Starting in version 6.4.1, you can select charts to access further details and use the new SLO table to monitor reliability.

-   **[Customize team approval settings with more flexibility](https://www.servicenow.com/docs/access?context=sr-add-approval-teams&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.4, customize team governance with more flexibility and less manual effort. You can assign different approval teams for new and existing team requests. The customization options are also fully available in the Service Operations Workspace Admin Center and no longer require manual setup in the Catalog Builder.


## UI changes

-   **[Express List](https://www.servicenow.com/docs/access?context=express-list&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Express List icon \(![Express List icon)](../../product/event-management/image/express-list1.png) is now in the navigation pane.

-   **[Integrations Launchpad](https://www.servicenow.com/docs/access?context=integrations-launchpad&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Integrations Launchpad icon \(![Integrations Launchpad icon](../../product/service-operations-workspace-itom/image/integrations-launchpad.png)\) is now in the navigation pane.

    **Note:** Starting in version 6.3, the custom Integrations Launchpad in SRM was replaced with the official Service Operations Workspace version. This change promotes consistency across applications and gives you immediate access to the latest SOW updates.

-   **[New banner for configuring SLIs](https://www.servicenow.com/docs/access?context=sr-create-slo-sli&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.3, when you set up an SLI, a new information banner shows how many configuration items are associated with your service. To set up an effective SLI for your system, select **View CIs in service map** to see how the service and configuration items relate.

-   **[Service import improvements](https://www.servicenow.com/docs/access?context=sr-add-service&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 6.3, the service import flow includes the following updates:

    -   Services owned by others are selectable options in the UI.
    -   Service suggestions appear in the search box, reducing the need to remember exact service names.

## Removed in this release

The **Alerts** tab has been removed from the Reliability tasks page.

## Activation information

Install SRM or ITOM Mobile Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Use SRM in Service Operations Workspace to manage SLOs alongside other IT Operations Management workflows.

-   **[Alert automation in Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-itom-alert-automation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Work with alert automation to respond to alerts, improve service reliability, and scale staff resources.



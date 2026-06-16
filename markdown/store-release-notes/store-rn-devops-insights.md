---
title: DevOps Insights release notes
description: Version history for the DevOps Insights application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-insights.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Insights release notes

Version history for the DevOps Insights application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.0.0 - June 2026**
    -   Changed:
        -   Jira authentication with 3LO
            -   Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.
        -   Bitbucket Cloud basic authentication using API token with scopes
            -   Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.
-   **Version 6.3.0 - March 2026**
    -   Changed:
        -   Enhanced JFrog integration with DevOps Change Velocity
            -   Gather JFrog evidence seamlessly and create change records automatically using the improved integration with DevOps Change Velocity.
        -   Bearer authentication in JFrog
            -   Connect to JFrog using the more secure bearer token authentication to comply with updated security policies.
        -   HTTP proxy for Docker
            -   Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment.
        -   Auto close without Change Management - State Model \[Legacy\] plugin
            -   Change requests can now be auto-closed without requiring installation of the Change Management - State Model \[Legacy\] plugin.
-   **Version 6.2.0 - December 2025**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in related DevOps applications.

-   **Version 6.1.0 - August 2025**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in related DevOps applications.

-   **Version 6.0.0 - May 2025**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in related DevOps applications.

-   **Version 5.1.0 - February 2025**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in related DevOps applications.

-   **Version 5.0.0 - November 2024**

    Bug fixes.

-   **Version 4.1.0 - August 2024**

    Changed: No code updates were made in this release. The release number has been updated to maintain consistency with changes in the related DevOps applications.

-   **Version 4.0.0 - May 2024**

    Changed: You cannot utilize the Insights dashboard in the DevOps Workspace as part of the Next Experience Dashboard which has all the newer and relevant indicators/widgets such as Deployment success rate and Failed Deployments along with safeguards and better filtering. DevOps Standard Insights on platform has been deprecated for all new DevOps users. In addition, platform \(record producer\) users are now redirected to the workspace to create tools or apps. Release/legacy users can still directly go to the platform URL to create tools or apps in the platform through the "Create New \(legacy\)" and "Create App \(legacy\)" options.

-   **Version 3.1.0 - February 2024**
    -   New: Localization framework improvements
    -   Fixed:
        -   Bug Count Widget not showing data when demo data is installed
        -   Incorrect value in the 'job count' field for base system PA indicators
        -   DevOps Insights filters not showing all apps and repos
-   **Version 3.0.0 - November 2023**
    -   New:
        -   Studio support forDevOps Insights.
        -   Added filter on the task assignments based on role.
    -   Removed:
        -   Removed zero values from line graphs.
        -   Removed duplicate property for DevOps Insights.
-   **Version 2.0.0 - August 2023**
    -   Changed:
        -   Info icons for DevOps Insights widgets.
        -   Better visuals for flow and accelerate metric score widgets.
-   **Version 1.38.0 - May 2023**
    -   Fixed:
        -   User with the DevOps Viewer role cannot access KPI analytics for all Insights widgets in workspace.
        -   Incorrect \# of tests displayed in the Application activity last 30 days widget.
        -   Filtering by Business App does not render data.
-   **Version 1.37.0 - February 2023**
    -   Changed: DevOps Accelerate Metrics - Now also shown in Digital Portfolio Management workspace by business application.
    -   Fixed: DevOps Insights 1.36 application adds ACLs.
-   **Version 1.36.0 - November 2022**

    New: Ability to filter by Business Application.

-   **Version 1.35.0 - August 2022**

    DevOps Insights Module in Workspace:

    -   Flow Metrics that show the value of work being delivered
    -   Cycle Times, Throughput Distribution, Planned to Deploy Flow Time and Work In Progress amounts
    -   New change acceleration metrics that focus on the path to automation
    -   Automated versus manual changes, Change policy decisions applied, ROI
    -   Updated filtering capabilities include Service, Configuration Item, Products, and by-Date
    -   Drill into data collected with a new tabbing design that keeps you in the workspace
-   **Version 1.14.0 - May 2020**
    -   Please note that this version of the app can only be installed on instances running New York or later.
-   **Version 1.10.0 - January 2020**
    -   New: Flow metrics
-   **Version 1.9.0 - December 2019**

    New:

    -   Change Acceleration insights
    -   System Health insights
    -   Development insights
    -   Updates for New York compatibility
-   **Version 1.4.0 - July 2019**

    Deep insights into DevOps practices, processes, and Change Acceleration. Drill into data collected over time and compare data sets.

    -   Change Acceleration insights
    -   System Health insights
    -   Development insights

**Parent Topic:**[ServiceNow Store - DevOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-devops-highlight.md)


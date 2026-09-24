---
title: Impact Guided Setup
description: Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/guided-setup-impact-in-app.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configuring Impact, Impact]
---

# Impact Guided Setup

Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

Automated registration, the preferred method, initiates the connection and the registration to the Impact Delivery Instance provider instance into combined tasks. You will establish and verify your connection between the Impact Store Application and the Impact Delivery Instance \(IDI\) for data synchronization and migration.

Follow the individual step of the Impact Guided setup:

-   User access – Onboard users and assign them to appropriate Impact and Scan Engine groups
-   Scan Engine settings – Configure initial scanning properties and definitions
-   Scan execution – Run initial scans to identify technical debt and platform health issues
-   Data synchronization – Establish automated connection between the Impact Store Application and IDI
-   Data migration – Initiate migration of historical data for value tracking and reporting
-   Agent setup – Configure the ServiceNow Auto Panel and assistant settings to enable AI agents in Impact

You may return to the various steps in the configuration if you don't complete the entire setup at once. As you complete each step successfully, mark the step as complete. For multi-instance configurations, repeat the connection and data synchronization steps for each instance.

**Note:** Regulated and GCC customers are required to perform Manual registration. See [Use manual registration to configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/use_manual_registration_configure_impact_store_application.md).

## Before you begin

Role required: impact app admin, admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup**.

    The Impact Guided Setup overview page displays with additional information about the setup process and Pre-checklist information. For general information, see [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/guided-setup.md).

2.  Select **Get Started**.

    The setup steps are displayed in category sections. You can expand a category to view details and related tasks.

    **Important:** You must mark each section as completed in order to unlock the next task section and continue setup.

    \[Omitted image "guided-setup-steps.png"\] Alt text: The Impact Guided Setup screen with the different activities to select to configure that option.


## What to do next

After completing Guided Setup, you can:

-   Configure additional instance integrations to expand Scan Engine coverage across your environment. See [Configure Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md).
-   Grant temporary instance access to your Impact Squad for support and troubleshooting. See [Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/hop-access-impact-squad.md).
-   Activate Now Assist Skills for Impact to enable AI-powered recommendations and insights. See [Activate Now Assist Skills for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/activate-now-assist-skills-in-now-assist-for-impact.md).
-   Enable data collection for Value Management to track and measure the business impact of technical debt reduction. See [Enable data collection for Value Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/data-collection-toolkit.md).
-   Set up agents to enable AI-powered features such as Success Path, Value Story Builder, and the Health Agent. See [Set up agents for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/set-up-agents-for-impact.md).

-   **[Onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/onboard_users_impact_store_application.md)**  
Assign groups to your users in the Impact Store Application so that you can control their access to the features, capabilities, and data.
-   **[Assign users to Platform Health groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/assign-users-scan-engine-groups.md)**  
In addition to assigning Impact users to groups, Platform Health users must also be part of a group for the Scan Engine feature.
-   **[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-initial-scan-engine-settings.md)**  
Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.
-   **[Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md)**  
Run an initial full instance scan to set a baseline to tune the instance environment to complete future scans quickly and efficiently.
-   **[Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md)**  
The automated registration process in Guided Setup simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
-   **[Set up agents for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/set-up-agents-for-impact.md)**  
Configure the ServiceNow Auto Panel and assistant settings to enable AI agents in Impact. Completing this setup allows agents such as Success Path, Value Story Builder, and the Health Agent to display in the context panel on Impact pages.
-   **[Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/hop-access-impact-squad.md)**  
Familiarize yourself with your ServiceNow Impact Squad, a dedicated team of experts ready to assist in tackling your team's unique transformation challenges. View or grant your Impact squad 30 day read-only access to your instance to support you with Impact features.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Install Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/install-impact-innovation-lab.md)

**Next topic:**[Onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/onboard_users_impact_store_application.md)


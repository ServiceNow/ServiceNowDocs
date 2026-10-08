---
title: Impact Guided Setup \(Legacy\)
description: Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/guided-setup-impact-in-app.html
release: brazil
topic_type: task
last_updated: "2026-10-03"
reading_time_minutes: 4
breadcrumb: [Configuring Impact, Impact]
---

# Impact Guided Setup \(Legacy\)

Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

**Important:** This is the legacy setup path. The Impact Setup Hub is the current way to install and configure the Impact Store Application. See [Use the Impact Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/use-impact-setup-hub.md). This legacy path remains available for a period of time, but it will not receive new features going forward.

Automated registration, the preferred method, initiates the connection and the registration to the Impact Delivery Instance provider instance into combined tasks. You will establish and verify your connection between the Impact Store Application and the Impact Delivery Instance \(IDI\) for data synchronization and migration.

Follow the individual step of the Impact Guided setup:

-   User access – Onboard users and assign them to appropriate Impact and Scan Engine groups
-   Scan Engine settings – Configure scanning properties and definitions
-   Scan execution – Run scans to identify technical debt and platform health issues
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
-   Set up agents to enable AI-powered features such as Success Path, Value Story Builder, and the Health Agent. See .

-   **[Install Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/install-impact-innovation-lab.md)**  
Follow these instructions to install the Impact Store Application.
-   **[Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md)**  
The automated registration process in Guided Setup simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
-   **[Enable data collection for Value Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/data-collection-toolkit.md)**  
The Impact Value Management Data Collection apps are designed to simplify and optimize the value metrics data collection process using Performance Analytics \(PA\). These applications enable you to efficiently gather, track, and analyze critical success metrics, ensuring data-driven decision-making and improved visibility into key performance trends.
-   **[Activate Now Assist Skills for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/activate-now-assist-skills-in-now-assist-for-impact.md)**  
Activate the Now Assist skill before you can use the generative AI capabilities for Impact.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/hop-access-impact-squad.md)

**Next topic:**[Install Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/install-impact-innovation-lab.md)


---
title: Run Impact Guided Setup
description: Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/guided-setup-impact-in-app.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Impact, Impact]
---

# Run Impact Guided Setup

Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

## Before you begin

You will establish and verify your connection between the Impact Store Application and the Impact Delivery Instance IDI for data synchronization and migration.

**Note:** You may return to the various steps in the configuration if you don't complete the entire setup at once. As you complete each step successfully, mark the step as complete. Subsequent tasks are locked until the previous step has been completed.

Role required: impact app admin, admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup**.

    The Impact Guided Setup overview page displays with additional information about the setup process and Pre-checklist information. For general information, see [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/guided-setup.md).

2.  Select **Get Started**.

    The setup steps are displayed in category sections. You can expand a category to view details and related tasks.

    **Important:** You must mark each section as completed in order to unlock the next task section and continue setup.

    \[Omitted image "guided-setup-steps.png"\] Alt text: The Impact Guided Setup screen with the different activities to select to configure that option.


-   **[Use Guided Setup to onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/onboard_users_impact_store_application.md)**  
Onboard new and existing users to the Impact Store Application.
-   **[Assign users to Platform Health groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/assign-users-scan-engine-groups.md)**  
In addition to assigning Impact users to groups, Platform Health users must also be part of a group for the Scan Engine feature.
-   **[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md)**  
Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.
-   **[Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/run-scan-engine.md)**  
An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.
-   **[Use automated registration to connect to the Impact Delivery Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/start-automated-registration-IDI.md)**  
The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
-   **[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/verify-impact-data-connection.md)**  
During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress.
-   **[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-migration-idi.md)**  
After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Install Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/install-impact-innovation-lab.md)

**Next topic:**[Use Guided Setup to onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/onboard_users_impact_store_application.md)


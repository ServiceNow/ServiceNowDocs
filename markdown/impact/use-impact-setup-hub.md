---
title: Use the Impact Setup Hub
description: Use the Impact Setup Hub to install Impact and complete a sequence of tasks that configure it on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/use-impact-setup-hub.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Configuring Impact, Impact]
---

# Use the Impact Setup Hub

Use the Impact Setup Hub to install Impact and complete a sequence of tasks that configure it on your ServiceNow instance.

The setup activities are similar to the Impact Guided Setup \(Legacy\) steps, with a more seamless experience. Installation is included as part of the same flow, instead of a separate step.

## Before you begin

Role required: impact app admin, admin

## Procedure

1.  Navigate to the Impact Setup Hub.

    -   On the ServiceNow landing page, navigate to **Manage Your Products** &gt; **Impact**.
    -   \(Optional\) If Impact is already installed, navigate directly to the Setup Hub by going to **All** &gt; **Impact** &gt; **Impact Setup Hub**. If you use this option, skip to step 3.
2.  Select the Impact tile and install or configure Impact.

    The Impact Product Hub launches:

    1.  If the Configure your product section has the **Configure** button available, then Impact is already installed.

    2.  Review the Apps and plugins sections:

        -   Not installed: If Impact isn't installed select Install and follow the onscreen steps.
        -   Installed: Impact is already installed. Proceed to the **Configure** option.
    The Configuration console opens. The Configuration summary shows the overall setup status, including the steps or tasks under each activity. For instance, the setup section for Platform Health has seven steps, as the progression status displays the count completed.

3.  Select **Get Started** for each setup area to complete Impact configuration.

    -   **Set up users and access**

        [Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/assign-roles.md)

    -   **Set up Platform Health**
        -   [Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/assign-roles.md)
        -   [Create a development team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/create-development-team.md)
        -   [Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-initial-scan-engine-settings.md)
        -   [Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-scan-engine-properties.md) and [Configure real-time scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-real-time-scanning-properties.md)
        -   [Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)
    -   **Register your instance**
        -   [Register and connect to the data provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-registration.md)
        -   [Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/verify-impact-data-connection.md)
    -   **Sync and migrate data**
        -   [Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-migration-idi.md)
        -   [Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/hop-access-impact-squad.md)
    -   **Enable Value Management data**

        [Configure an estimated data definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/value-library/configure-estimated-data-definition.md)

        To configure Value Management data, you need one of these roles: admin, pa\_power\_user, pa\_admin, or pa\_data\_collector.

    **Note:** Some activities are sequential. Unless you complete the previous activity, you can't finish the next one.

    You can return to the Configuration console at any time to complete the remaining activities.


**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configuring-impact-platform.md)

**Previous topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configuring-impact-platform.md)

**Next topic:**[Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/assign-roles.md)


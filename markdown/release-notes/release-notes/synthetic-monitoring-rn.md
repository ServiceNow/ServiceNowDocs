---
title: Synthetic monitoring release notes
description: The ServiceNow synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Synthetic monitoring release notes

The ServiceNow® synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring was enhanced and updated in the Zurich release.

## Synthetic monitoring highlights for the Zurich release

-   Run synthetic monitors from the MID Server.
-   Create monitors without needing to leave SOW to create an HTTP endpoint.
-   Assign a support group to synthetic monitoring alerts for easy investigation.
-   As of 1.4, view alerts associated with monitors and navigate to those alerts.
-   As of 1.4, use tags on a monitor's alerts.
-   As of 1.4, use synthetic monitoring with endpoints that support OAuth credentials.

See [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** Synthetic monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading synthetic monitoring to Zurich

If you want to run monitors using a MID Server as a location, you must restart the MID Server after upgrading.

## New in the Zurich release

-   **[MID Server support for running synthetic monitors](https://www.servicenow.com/docs/access?context=create-synthetic-monitoring-locations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Run synthetic monitors from your MID Server.

-   **[HTTP endpoint creation directly in synthetic monitoring](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Create HTTP endpoints for your monitors without leaving the SOW.

-   **[Support groups for synthetic monitor-based alerts](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Assign a support group to a monitor, and then any raised alerts follow the associated alert automation rules.

-   **[View all monitors with open alerts](https://www.servicenow.com/docs/access?context=identifying-system-issues&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US#section_yll_v5k_fdc)**

    As of 1.4, view all monitors with open alerts.

-   **[View alerts associated with a monitor](https://www.servicenow.com/docs/access?context=view-alerts-for-a-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.4, navigate to a monitor's open alerts.

-   **[Assign tags to a monitor's alerts](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.4, use tag-based clustering to group monitor alerts.

-   **[Use OAuth-based credentials](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.4, OAuth credentials on endpoints are supported.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[New columns in the Synthetic Location table](https://www.servicenow.com/docs/access?context=create-synthetic-monitoring-locations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**
    -   **Type**: Shows whether the location is a MID Server, ACC Collector, or hosted on the platform.
    -   **Number of monitors**: Displays the number of monitors running on the location.
-   **[Configuration tab removed](https://www.servicenow.com/docs/access?context=view-test-details&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 1.4, the **Configuration** tab on the Monitor Details page has been removed. You can access this information from the **Details** tab.

-   **[Landing page updates](https://www.servicenow.com/docs/access?context=view-aggregat-monitor-information&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 1.4, these changes were made to the landing page:

    -   New open alerts filter
    -   New Open alerts column in the Monitors table
-   **[New Alerts tab on the Monitor Details page](https://www.servicenow.com/docs/access?context=view-alerts-for-a-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 1.4, you can view all alerts for a monitor or filter by open alerts.

-   **[New Alert column in the Monitor result history table on the Details tab](https://www.servicenow.com/docs/access?context=view-a-monitor-s-test-results&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 1.4, you can see open alerts for any tests the monitor has run.

-   **[Tag field on the Create Monitor page](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    In version 1.4, you can add tags when configuring alerts for monitors.


## Activation information

Install synthetic monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)


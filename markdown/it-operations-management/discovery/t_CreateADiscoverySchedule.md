---
title: Schedule a horizontal discovery
description: A discovery schedule determines what horizontal discovery searches for, when it runs, and which MID Servers are used. Create a discovery schedule for your local environment or a schedule for discovering the resources in your cloud service account.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Schedule a horizontal discovery

A discovery schedule determines what horizontal discovery searches for, when it runs, and which MID Servers are used. Create a discovery schedule for your local environment or a schedule for discovering the resources in your cloud service account.

## Before you begin

Ensure that your discovery schedule conforms to security best practices, such as limiting the range of discovery targets and using the most secure credentials.

Make sure to [test your credentials](https://www.servicenow.com/docs/access?context=t_CreateCredential&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) before you run a schedule. Bad credentials are a leading cause of failed discoveries.

Roles required: discovery\_admin or admin

## About this task

You can use a discovery schedule to launch horizontal discovery, which uses probes, sensors, and pattern operations to scan your network for CIs. Use this procedure to create a schedule manually from the **Discovery Schedules** form.

Service Mapping also provides a discovery schedule for top-down discovery. See [Schedule a top-down discovery by Service Mapping](../../service-mapping/task/t_CreateDiscoSchedForCITypes.md) for more information.

Use the **Discovery Schedules** module in the Discovery application to:

-   Configure a schedule to discover resources in your cloud service account.
-   Configure a schedule to discover certificates from URL scans.
-   Configure device identification by IP address or other identifiers.
-   Determine if credentials are used in device probes.
-   Name the MID Server to use for a particular type of discovery.
-   Create or disable a schedule that controls when the discovery runs in your network.
-   Configure the use of multiple Shazzam probes for load balancing.
-   Configure the use of multiple MID Servers for load balancing.
-   Run a discovery schedule manually.
-   Run a discovery on a single IP address.

**Note:** To view the run-results of your schedules for both IP-based and Cloud Discovery, use the summaries on the [Discovery Home page](../concept/discovery-home-page.md#). The Home page publishes the details of any errors that might have occurred and displays possible actions to take to remediate problems.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules** to create a new record.

2.  Select the type of schedule to open:

    -   **New**: Creates a new horizontal schedule for discovering components in your network.
    -   **Quick Discovery**: Runs a horizontal discovery on a single IP address without requiring a schedule.
    -   **Create a Cloud Discovery schedule**: Creates a schedule, using the Discovery Manager wizard, for discovering resources in a cloud service account.
3.  Complete the discovery schedule form, using the fields in the table.

    For more information, see [Discovery Schedule form reference](../reference/discovery-schedule-form.md).

4.  Right-click in the header of the record and select **Save** from the context menu.

5.  To create a range of IP addresses to discover, click **Quick Ranges** under **Related Links**.

    **Note:** To improve security, limit the range of discovery targets to exclude unnecessary networks and devices.

6.  Define the frequency of schedule running as described in [Run options for discovery schedules](../../it-operations-management/reference/discovery-schedule-run-options.md).



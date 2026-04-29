---
title: Discovery Quick Start
description: Discovery Quick Start is a wizard that helps you get up and running with Discovery quickly. Use Discovery Quick Start tasks to discover IP ranges, or subnets, in your environment and then to identify the configuration items \(CI\) in those subnets.Subnet discovery finds all the subnets in your environment to determine available IP ranges and to verify that there are MID Servers available to access these ranges.Using the credentials you provide, the Quick Start wizard finds all the configuration items \(CI\) for the IP ranges identified during subnet discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Discovery setup, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Quick Start

Discovery Quick Start is a wizard that helps you get up and running with Discovery quickly. Use Discovery Quick Start tasks to discover IP ranges, or subnets, in your environment and then to identify the configuration items \(CI\) in those subnets.

Before using Discovery Quick Start, install and validate MID Servers. See [MID Server installation](https://www.servicenow.com/docs/access?context=mid-server-installation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for details.

## Configure and schedule subnet discovery

Subnet discovery finds all the subnets in your environment to determine available IP ranges and to verify that there are MID Servers available to access these ranges.

### Before you begin

Role required: discovery\_admin

### About this task

The goal of this phase is to discover all the subnets in your network. To do this, Discovery must have the correct SNMP credentials to identify the routers it encounters. Using the credentials you provide, Discovery begins by reading the router tables of the router connected to the MID Server to identify connected routers. Discovery then moves outward through the network from router to router until it has discovered all the local subnets.

After Discovery identifies the subnets, it automatically assigns the IP ranges of these subnets to qualified MID Servers in preparation for the CI discovery phase.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

    The first time you access Discovery Home, a welcome screen appears. After you have configured subnet discovery and run the schedule, Quick Start shows the subnet results information.

2.  Select **Discovery Quick Start** to begin configuration.

    ![Start Quick Start](../image/QS_Start.png)

    **Note:** If you did not set up a MID Server yet, select **MID Server Guided Setup** when prompted to create the MID Server user, download and install the MID Server, and validate it. Links in Guided Setup return you to Discovery Quick Start to continue configuring subnet discovery. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    ![MID Server setup link](../image/QS_NoMIDFound2.png)

3.  In the **Select MID Servers** tab, select qualified MID Servers for subnet discovery.

    1.  Move the MID Servers you want to use for subnet discovery from the **Available** column to the **Selected** column.

        Available MID Servers must meet these requirements:

        -   Be configured and in an **Up** state.
        -   Be validated.
        -   Have the Discovery application attached or **ALL** applications configured.
        ![MID Server selection screen](../image/QS_SelectMIDServers.png)

    2.  If you want Discovery to use all new MID Servers that meet the setup criteria, select the **Automatically include new MID Servers** option.

    3.  Select **next**.

4.  In the **Add Credentials** tab, add credentials for the routers you're going to discover.

    This tab shows any SNMP credentials that are already configured. Routers that appear in the **Targeted Routers** list are default gateway routers to which the MID Server host is connected.

    **Note:** You can return to this phase after creating a schedule to add credentials.

    ![SNMP credentials for routers](../image/snmp-creds-accelerator.png)

    1.  Select **New** to add SNMP community or SNMP V3 credentials, if necessary.

    2.  If the list of targeted routers does not include all the routers you expect to use, select the plus icon and add the router by IP address.

        ![Add routers](../image/list-of-routers-accelerator.png)

    3.  After you configure all necessary credentials, select **Test Router Access** to verify that Discovery can use your credentials to access routers.

        The gateway routers appear in the **Routers** column, regardless of whether the credentials can access the router. Those routers that the credentials can successfully access appear with a **Success** indicator. The routers that cannot be reached, appear with a **Failed** indicator.

        You can filter the list using the **Search by IP** field or by using the **Reached Routers** or **Unreached Routers** options from the **View** choice list.

    4.  Select **next**.

5.  In the **Create Schedule** tab, create a schedule to run subnet discovery regularly.

    Execution of this schedule performs subnet discovery and triggers IP subnet auto-assignment, in which the discovered subnets are assigned to qualified MID Servers.

    1.  Complete the schedule using the fields from the list.

        ![Discovery schedule for accelerator](../image/schedule-accelerator.png)

        -   **Active**: Enables or disables this schedule.
        -   **Frequency**: Select how often the schedule should run:
            -   **Daily**: Run Discovery at a specified time each day.
            -   **Weekly**: Run Discovery on one designated day of each week.
            -   **Monthly**: Run Discovery on one designated day of the month. If the designated day doesn’t occur in the month, the schedule doesn’t run that month. For example, if you designate day 30, the schedule doesn’t run in February.
            -   **Once**: Run Discovery once on the designated date and time.
            -   **Periodically**: Run Discovery every designated time. Use the **Repeat Interval** field to define the time in days, hours, minutes and seconds. The first discovery runs at the point in time defined in the **Starting** field. The subsequent discoveries run after each **Repeat Interval** period passes.
        -   **Cancel Discovery if longer than**: Terminate the Discovery process if it exceeds the specified duration. Discovery might run for an excessive amount of time based on multiple factors, including the size of your network.

            **Note:** Any MID Server processing taking place when Discovery is canceled is allowed to complete. However, all output records that MID Servers haven’t picked up are canceled.

    2.  Select one of the following options:

        -   **Finish and Run** saves the schedule and runs discovery immediately.
        -   **Finish** saves the schedule. Discovery then runs at the interval specified in the schedule.
6.  View subnet discovery results.

    ![Subnet Discovery results](../image/subnet-discovery-results-accel.png)

    1.  Select each tile for details.

        If subnet Discovery did not yet run, each of these tiles shows **0**.

        -   **Reached Routers**: The number of routers that Discovery was able to access and discover.
        -   **Unreached Routers**: The number of routers that Discovery was not able to access.
        -   **Found Subnets**: The number of subnets that Discovery found.
        -   **Assigned Subnets**: IP subnets that were assigned to at least one MID Server.
        -   **Unassignable Subnets**: IP subnets that were not assigned to any MID Servers.
    2.  Select **Edit Schedule** to return to the **Select MID Servers** tab.

        Resolve any issues with subnet discovery by returning to the Router Access page and making sure each credential is configured correctly. Also test router access for each credential.

    3.  Select **Advanced View** to see the Automation Status Set form.

        This form displays detailed results for both subnet discovery and the automatic assignment of IP ranges.


## Configure and schedule CI discovery

Using the credentials you provide, the Quick Start wizard finds all the configuration items \(CI\) for the IP ranges identified during subnet discovery.

### Before you begin

You should perform this procedure after you complete [Configure and schedule subnet discovery](discovery-quick-start.md#) in the Discovery Quick Start.

Role required: discovery\_admin

### About this task

The goal of this phase is to create the schedules necessary to discover the CIs on each subnet. Discovery Quick Start does that automatically, and then runs these schedules using the credentials you provide. You can add additional credentials at any time. Optionally, you can define locations for each of the subnet routers, and Discovery creates separate schedules for each location.

You must be familiar with the types of credentials that you need for the CIs in your network. Each CI type requires different credentials. For example, if Discovery uses patterns instead of probes, the patterns might require [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Review the requirements for the CI types you intend to discover. See [Data collected by ITOM Visibility](../reference/data-collected-by-itom-visibility.md), and then locate the specific type of device, computer, or application.

### Procedure

1.  From the Subnet Discovery Results page of the Discovery Quick Start, select **Create Discovery schedules**.

    ![Subnet Discovery results](../image/subnet-discovery-results-accel.png)

2.  Create the credentials necessary to discover CIs in your network.

    1.  Select the credential type you want to manage from the **View** drop-down list.

        All the credentials currently configured for that CI type display in individual tiles.![Create credentials for CI Discovery](../image/credentials-ci-disco-accel.png)

    2.  To add a credential, select **New**.

        The Add Credential form displays, enabling you to specify your new credential.

    3.  Select **Next** to go to the **Router Location** phase.

3.  **Optional:** In the **Assign Router Location** tab, assign a location to each router that subnet discovery found.

    When you configure router locations, you have the option of creating a schedule for each location. If you do not assign locations, a single Discovery schedule is created for all your subnets. If you assign a time zone to a location, Discovery creates a schedule that runs in that location's time zone. If you do not assign a time zone to a location, the schedule for that location runs in the user's local time zone.

    **Note:** A subnet can belong to multiple routers. If schedules are created by location, Discovery finds subnets managed by multiple routers using multiple schedules.

    The list of gateway routers shows those devices not currently assigned to a location.

    ![Assign routers to locations](../image/router-locations-accelerator.png)

    1.  Select the check boxes for the routers you want to assign a location.

    2.  Select the location in the **Assign to** list.

    3.  If the location is not already in the list, select **Add New Location** and add the location.

    4.  Verify that the location has a time zone defined.

        Timezones enable you to create a schedule for each location based on the time zone.

    5.  Select **Assign**.

        **Note:** Routers that are unassigned cannot be added to any schedules that are based on location.

    6.  Select **next**.

4.  Create a CI Discovery schedule.

    1.  Complete the schedule using the fields in the list.

        ![Create a CI Discovery schedule](../image/QS_CI_Schedule.png)

        -   **Active**: Enables or disables this schedule.
        -   **Frequency**: Select how often the schedule should run:
            -   **Daily**: Run Discovery at a specified time each day.
            -   **Weekly**: Run Discovery on one designated day of each week.
            -   **Monthly**: Run Discovery on one designated day of the month. If the designated day doesn’t occur in the month, the schedule doesn’t run that month. For example, if you designate day 30, the schedule doesn’t run in February.
            -   **Once**: Run Discovery once on the designated date and time.
            -   **Periodically**: Run Discovery every designated time. Use the **Repeat Interval** field to define the time in days, hours, minutes and seconds. The first discovery runs at the point in time defined in the **Starting** field. The subsequent discoveries run after each **Repeat Interval** period passes.
        -   **Create a separate schedule for each location**: Automatically create schedules for any router locations that you’ve configured. These schedules run on the day and time that you specify, but in their own local time zone. Clear this check box to create a single schedule for all your locations that runs in the user's local time zone. This option is only available if you have configured router locations.
        -   **Cancel Discovery if longer than**: Terminate the Discovery process if it exceeds the specified duration. Discovery might run for an excessive amount of time based on multiple factors, including the size of your network.

            **Note:** Any MID Server processing taking place when Discovery is canceled is allowed to complete. However, all output records that MID Servers haven’t picked up are canceled.

    2.  Select one of the following options:

        -   **Finish and Run** saves the schedule and runs a discovery immediately.
        -   **Finish** saves the schedule. Discovery runs at the interval you specified in the schedule.


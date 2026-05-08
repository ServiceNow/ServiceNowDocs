---
title: Set up the Service Graph Connector for Fortinet schedule
description: Set up and configure the Service Graph Connector for Fortinet SD-WAN. The process includes installation, optional demo data integration, connectivity configuration, and scheduling data collection for seamless Configuration Management Database \(CMDB\) integration.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Set up the Service Graph Connector for Fortinet schedule

Set up and configure the Service Graph Connector for Fortinet SD-WAN. The process includes installation, optional demo data integration, connectivity configuration, and scheduling data collection for seamless Configuration Management Database \(CMDB\) integration.

## Before you begin

Verify the active application scope is Service Graph Connector \(SGC\) for Fortinet.

1.  Select the application picker \(![](../../../reuse/icons/product-icons/globe-outline-24.svg)\) in the header.
2.  Search for **Fortinet**.
3.  Select Service Graph Connector for Fortinet from the list.

Role required: TSOM Visibility admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Fortinet** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  On the Guided setup home page, create and configure the MID Server or skip based on your environment.

    **Note:** For more information on how to activate and configure a MID Server, see Configuring MID Server.

    1.  Select **Get Started**.

    2.  Select **Configure**.

    3.  Follow the on-screen instructions to download and install the appropriate MID Server installer archive for the operating system.

    4.  Select **Mark as Complete** when done.

        Once all MID Server steps are complete, proceed to **Configure Connectivity**.

4.  Enable the Service Graph Connector to reference the Fortinet connection by name, extracting active aliases from the CMDB, and initiate data collection on the associated HTTP connection by creating connection aliases, credentials, and HTTP connections.

    1.  Select **Get Started**.

    2.  Create and configure aliases for the connections and credentials:

        1.  Select **Configure**.
        2.  In the **Name** field, specify the alias name.
        3.  Retain the default values in the rest of the fields.
        4.  Select **Submit** and then select **Mark as Complete**.
    3.  Create the basic credentials to access the FortiManager.

        1.  Select **Configure**.
        2.  In the **Name** field, specify the alias name.
        3.  In the **API Key** field, enter the API key created in the FortiPortal.

            **Note:** Other authentication fields might be required depending on the authentication methods used in your FortiManager instance. By default, use basic authentication credentials as part of the Guided setup. For more information, see Basic authentication credentials.

        4.  Retain the default values in the rest of the fields.
        5.  Select **Submit** and then select **Mark as Complete**.
    4.  Create the HTTP Connection.

        1.  Select **Configure**.
        2.  In the **Name** field, specify the connection name.
        3.  Choose the **Credentials** and **Connection Alias** created earlier.
        4.  Specify the **Connection URL** for FortiManager.
        5.  Select the **Use MID Server** check box and indicate how the MID Server should be selected:
            -   Auto-select: Selects from MID Servers based on MID Server criteria, regardless of whether they are members of a cluster.
            -   Specific MID Server: Automatic reassignment to another MID Server is not supported.
            -   Specific MID Cluster: Automatic reassignment to another MID Server only selects from members of the specified cluster.
        6.  If **Specific MID Server** or **Specific MID Cluster** is selected, select a name in the appropriate field.
        7.  Retain the default values in the rest of the fields.
        8.  Select **Submit** and then select **Mark as Complete**.
5.  Configure the data collection schedule.

    1.  Select **Get Started**.

    2.  Select **Configure**.

    3.  Configure the schedule.

        1.  In the **Name** field, provide a name for the scheduler.
        2.  Select the data source based on whether the schedule should be for bulk discovery or filtered discovery.
            -   To use the bulk discovery data source for all devices in connection alias, select the data source SGC-Fortinet Bulk Discovery.
            -   To set specific filter criteria for each connection alias, select the data source SGC-Fortinet Filtering Discovery.
        3.  Determine whether the schedule should automatically run or you want to have it run it manually.
        4.  -   Select the **Active** check box, to run the schedule automatically based on the values in the **Run** and **Time** fields.
-   Clear the**Active** check box to run the schedule manually.
        5.  From the **Run** drop-down list, select the frequency at which you want the scheduler to run automatically. The available choices are Daily, Weekly, Monthly, Periodically, after Parent Runs, or once.
        6.  In the **Time** field, set the time of day at which the scheduler should run in hours, minutes, and seconds.
        7.  Provide the connection information.
            1.  Select the **Use Connection** check box.
            2.  From the **Connection** drop-down list, select the connection alias. For example, sn\_sgc\_fortinet.Fortinet\_Alias.
    4.  Set specific filter criteria for each connection alias.

        1.  Ensure that the \[FIELD NAME FOR DATA SOURCE\] field is set to the data source SGC-Fortinet Filtering Discovery.
        2.  In the **Connection Alias** field, choose a connection alias.
        3.  Set the filtering parameters.
            -   To filter by IP address, in the **Filtered IPs** field, add IP filters in the desired format.
                -   Single IP: `10.10.10.10`
                -   List: `10.10.10.10, 10.10.10.20`
                -   Ranges: `10.10.10.30-10.10.10.40`
                -   CIDR: `10.10.10.0/24`
                -   Mask: `10.10.10.0:255.255.255.0`
            -   To filter by name, add name filters to search by device name or part of the name.

                You can specify a single string or a list of names.

6.  Select **Submit** and then select **Mark as Complete**.


## Result

Once the setup is complete, a confirmation screen appears indicating all tasks have been completed successfully.

You can access the configured connections, aliases, credentials, and import schedules from the navigation. Navigate to **All** &gt; **Service Graph Connectors** &gt; **Fortinet**.


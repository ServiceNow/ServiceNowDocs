---
title: Set up Nokia Altiplano
description: Learn how to install and configure the Service Graph Connector for Nokia Altiplano, including optional demo data, connectivity setup, and data collection schedules.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure Nokia Altiplano SGC, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Set up Nokia Altiplano

Learn how to install and configure the Service Graph Connector for Nokia Altiplano, including optional demo data, connectivity setup, and data collection schedules.

## Before you begin

Role required: TSOM Visibility admin

## About this task

Confirm you are operating in the Service Graph Connector for the Nokia Altiplano application scope. To switch to the Service Graph Connector for Nokia Altiplano scope:

1.  Select the application picker \(![](../../../reuse/icons/product-icons/globe-outline-24.svg)\) in the header.
2.  Search for **Nokia Altiplano**.
3.  Select Service Graph Connector for Nokia Altiplano from the list.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

    The Guided Setup home page opens in a new tab.

3.  Create and configure MID Server or skip based on your environment.

    1.  Select **Configure** to complete the process.

    2.  Follow the on-screen instructions to download and install.

    3.  Select **Mark as Complete** when done.

        **Note:** For more information on how to install and configure MID Server, see [Configuring MID Server](https://www.servicenow.com/docs/access?context=configure-mid-server&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    4.  Configure or skip the validation step.

    5.  Select **Mark as Complete** when validated.

        Once all MID Server steps are complete, proceed to **Configure Connectivity**.

4.  Create connection aliases, credentials, and HTTP connections to your Nokia Altiplano instance with **Configure Connectivity**

    1.  Select **Get Started**.

    2.  Create and configure aliases for the connections and credentials:

        1.  Select **Configure**.
        2.  In the **Name** field, specify the alias name.
        3.  Leave the rest of the fields as default, select **Submit** and then **Mark as Complete**.
        **Note:** This enables using the connection by name rather than directly, enabling the collector to extract all active aliases from the CMDB and start performing data collection on the HTTP connection bound to it.

    3.  Create the credentials to access the Nokia Altiplano Controller by selecting **Configure**.

        1.  In the **Name** field, specify the alias name.
        2.  In the **User name** field, specify your Nokia Altiplano instance user name.
        3.  In the **Password** field, specify your Nokia Altiplano instance password.

            **Note:** Other authentication fields may be required depending on the authentication methods used in your Nokia Altiplano instance. By default, we use [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) \(as part of the Guided setup\).

        4.  Leave the rest of the fields as default, select **Submit** and then select **Mark as Complete**.
    4.  Create HTTP Connection by selecting **Configure**

        1.  In the **Name** field, specify the connection name.
        2.  Choose the **Credentials** and **Connection Alias** created earlier.
        3.  Specify the **Connection URL** for Nokia Altiplano.
        4.  Check **Use MID Server** and choose either:
            -   Auto-select
            -   Specific MID Server
            -   Specific MID Cluster
        5.  Leave the rest of the fields as default, select **Submit** and then select **Mark as Complete**.
5.  Configure Data Collection Schedule either for bulk discovery or filtered discovery by clicking **Get Started**and then click **Configure**.

<table id="choicetable_h3d_ndy_yfc"><thead><tr><th align="left" id="d27113e347">

To

</th><th align="left" id="d27113e350">

Do the following

</th></tr></thead><tbody><tr><td id="d27113e356">

**Schedule data collection for bulk discovery \(Use bulk discovery data source for all devices in connection alias\)**

</td><td>

-   Provide a **Name** for the scheduler.
-   Ensure the bulk data source SGC-Nokia Altipano Bulk Discovery is selected.
-   Set **Active** the scheduler automatically runs as mentioned in the **Run** and **Time** fields. If inactive, you must manually execute.
-   Select **Use Connection.**
-   In the **Connection** field, select connection alias. For example, sn\_sgc\_altiplano.Atiplano\_Alias.
-   In the **Run** field, select the frequency. Specify when you want this schedule to run: Daily, Weekly, Monthly, Periodically, After Parent Runs, or Once.
-   In the **Time** field, enter the time in hours, minutes, and seconds.


</td></tr><tr><td id="d27113e413">

**Schedule data collection for filtered discovery \(Use Filtering Discovery data source for specific OLT filter criteria for each connection alias\)**

</td><td>

1.  Add Filtering Parameters
    1.  In the **Connection Alias** field, choose a connection alias.
    2.  Optionally, in the **Filtered IPs** field, add IP filters in various formats defined as following:
        -   Single IP: `10.10.10.10`
        -   List: `10.10.10.10, 10.10.10.20`
        -   Ranges: `10.10.10.30-10.10.10.40`
        -   CIDR: `10.10.10.0/24`
        -   Mask: `10.10.10.0:255.255.255.0`
    3.  Optionally, add name filters to search by device name or part of the name. You can specify a single string or a list of names to filter the results.
2.  Schedule filtered Collection
    -   Provide a **Name** for the scheduler.
    -   Ensure the data source SGC-Nokia Altipano Filtering Discovery is selected.
    -   Set **Active** the scheduler automatically runs as mentioned in the **Run** and **Time** fields. If inactive, you must manually execute.
    -   In the **Run** field, select the frequency. Specify when you want this schedule to run: Daily, Weekly, Monthly, Periodically, After Parent Runs, or Once.
    -   In the **Time** field, enter the time in hours, minutes, and seconds.
    -   Select **Use Connection.**.
    -   In the **Connection** field, select connection alias. For example, sn\_sgc\_altiplano.Atiplano\_Alias.


</td></tr></tbody>
</table>6.  Select **Submit** and then select **Mark as Complete**.


## Result

The configured connections, aliases, credentials, and import schedules can also be accessed from the navigation Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano**.

**Related topics**  


[Set up multiple Nokia Altiplano instances](multi-instance-setup.md)

[Configure concurrent import and parallel loading for Nokia Altiplano](configure-concurrent-import-and-parallel-loading.md)

[Mapping Nokia Altiplano CIs and Relationships in CMDB](../concept/data-mapping.md)

[System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md)


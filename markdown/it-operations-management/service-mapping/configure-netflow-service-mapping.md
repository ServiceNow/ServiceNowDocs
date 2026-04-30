---
title: Configure data collection using Netflow
description: Enable Service Mapping to perform discovery based on data collected using the Netflow protocol. This setup results in fully automated data collection flow, where all involved components send, collect, and analyze data automatically.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data collection and discovery using Netflow, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure data collection using Netflow

Enable Service Mapping to perform discovery based on data collected using the Netflow protocol. This setup results in fully automated data collection flow, where all involved components send, collect, and analyze data automatically.

## Before you begin

Learn about [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

Enable the following scheduled job: Flow Discovery Scheduler \[sysauto\_script\_74c676f0dbb0220060ff742eaf9619f2\].

Role required: admin or service\_mapping\_admin

## About this task

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. You can enrich your traffic-based discovery by configuring Service Mapping to use the Netflow protocol. For more information about the way Service Mapping uses Netflow, see [Data collection and discovery using Netflow](../concept/data-collection-netflow-mapping.md).

Configure the ServiceNow Netflow connector to trigger the MID Server to collect the data from the Netflow flows and process them.

## Procedure

1.  Install the nfdump package on a server hosting the MID Server in your organization:

    -   For a Linux server, download, compile, and install the nfdump package. You can download the nfdump package from [https://sourceforge.net/projects/nfdump/](https://sourceforge.net/projects/nfdump/).
    -   For an Ubuntu server, install the nfdump package without predownloading or compiling it. Open the command-line window and run the following command:

        **sudo apt-get install nfdump**

    -   For an Ubuntu server, if the **apt-get** command fails, predownload the nfdump package, save it locally and then install it. Open the command-line window and run the following commands:

        **sudo dpkg -i nfdump\_1.6.15-3\_i386.deb -**

        **sudo apt-get -f install**

        **Note:** The file name for the nfdump package has the following format: nfdump\_&lt;version number&gt; .deb. In this example it is nfdump\_1.6.15-3\_i386.deb.

2.  Configure the Netflow collector to save the nfdump file in the required directory.

    1.  Open the `/etc/init.d/nfdump` file.

    2.  Modify the parameter responsible for saving this file in the required location.

        For example, on an Ubuntu server, specify the location using the **DEAMON\_ARGS** parameter:

        `DATA_BASE_DIR="/var/cache/nfdump"`

        `DAEMON_ARGS="-D -l $DATA_BASE_DIR -P $PIDFILE"`

    For operational information, refer to [https://sourceforge.net/projects/nfdump/](https://sourceforge.net/projects/nfdump/).

3.  Configure the switches to forward their nfdump files to the MID Server.

    The default value for the MID Server is port 9995.

4.  Configure the Netflow collector to save data for one day.

    1.  Open the command-line window on the server hosting the Netflow collector.

    2.  Create a cron job.

        `crontab -e`

    3.  Enter the following command using the correct paths.

        `*/10 * * * * /usr/local/bin/nfexpire -e /data/nfdump -t 1d`

5.  Verify that the Netflow collector is configured correctly and receives the correct data from the network resources.

    1.  Run the following command:

        ```
        nfdump -q -O tstart -R /data/nfdump/ -o extended
        ```

    2.  In the command output, verify that marked fields contain real data:

        ![Verification command output](../image/NetflowVerificationOutput.png)

6.  Configure Service Mapping to receive data collected by the Netflow collector:

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Flow Connectors**.

    2.  Click **New**.

    3.  Click **nfdump install**.

    4.  On the nfdump install page, configure parameters as follows:

        |Field|Description|
        |-----|-----------|
        |**Name**|A descriptive name for the connector.|
        |**MID Server**|The MID Server on which you installed the Netflow collector.|
        |**nfdump data directory**|The data directory where you configured the Netflow collector to save the nfdump files.|

    5.  Click **Submit**.

7.  Verify that Service Mapping collects data using Netflow:

    1.  On the **nfdump install** form, select the newly configured connector and click **Run now** to start the data collection flow and populate the Flow Connection \[sa\_flow\_connection\] table.

    2.  Navigate to **System Definitions** &gt; **Tables**.

    3.  Click the Flow Connection \[sa\_flow\_connection\] table.

    4.  Under **Related Links**, click **Show List**.

    5.  Verify that the table contains data.


**Parent Topic:**[Advanced Service Mapping configuration](../concept/c_ConfigureSM.md)


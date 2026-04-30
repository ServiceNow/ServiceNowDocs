---
title: Configure onetime data import using Netflow for testing purposes
description: Configure and test Service Mapping discovery process based on data collected using the Netflow protocol.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data collection and discovery using Netflow, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure onetime data import using Netflow for testing purposes

Configure and test Service Mapping discovery process based on data collected using the Netflow protocol.

## Before you begin

Learn about [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

Role required: admin or service\_mapping\_admin

## About this task

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. You can enrich your traffic-based discovery by configuring Service Mapping to use the Netflow protocol. For more information about the way Service Mapping to collect Netflow data, see [Data collection and discovery using Netflow](../concept/data-collection-netflow-mapping.md).

For testing purposes, install the Netflow Collector \(nfdump\) on a Unix server inside your organization. In this case, this Unix server should be different from the server hosting the MID Server server.

Configure the ServiceNow connector to trigger MID Server to collect the data from the flow log and processes it.

## Procedure

1.  Download and install the Netflow collector \(nfdump\) on a Unix or Ubuntu server inside your organization.

    -   For a Linux server, download, compile, and install the nfdump package. You can download the nfdump package from [https://sourceforge.net/projects/nfdump/](https://sourceforge.net/projects/nfdump/).
    -   For an Ubuntu server, install the nfdump package without predownloading or compiling it. Open the command-line window and run the following command:

        **sudo apt-get install nfdump**

    -   For an Ubuntu server, if the **apt-get** command fails, predownload the nfdump package, save it locally and then install it. Open the command-line window and run the following commands:

        **sudo dpkg -i nfdump\_1.6.15-3\_i386.deb -**

        **sudo apt-get -f install**

        **Note:** The file name for the nfdump package has the following format: nfdump\_&lt;version number&gt; .deb. In this example it is nfdump\_1.6.15-3\_i386.deb.

2.  Configure the Netflow collector to save data for one day.

    1.  Open the command-line window on the server hosting the Netflow collector.

    2.  Create a cron job.

        `crontab -e`

    3.  Enter the following command using the correct paths.

        `*/10 * * * * /usr/local/bin/nfexpire -e /data/nfdump -t 1d`

3.  Create a file with the nfdump data.

    For example, use the following command:

    nfdump -q -m -R /data/nfdump/ -o extended -t 2016/07/06.07:00:00-2016/07/06.07:10:00 'inet and proto tcp' &gt;&gt; /tmp/my\_file

4.  If the file is very large, you can compress it using the gzip format by using the following command:

    `gzip /tmp/my_file`

5.  Copy the nfdump data file to the MID Server.

6.  Configure Service Mapping to receive data collected by the Netflow collector:

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Flow Connectors**.

    2.  Click **New**.

    3.  Click **ndfdump file**.

    4.  On the dfdump file page, configure parameters as follows:

        |Field|Description|
        |-----|-----------|
        |**Name**|A descriptive name for the connector.|
        |**nfdump data path**|The path to a location on the MID Server to which you saved the nfdump data file in [5](test-netflow-service-mapping.md#CopyNfdumpFile).|
        |**MID Server**|The MID Server, onto which you copied the nfdump file.|
        |**Gzipped file**|If you converted the nfdump file into the gzip format before saving it on the MID Server, set this parameter to true to unzip it.|

    5.  Click **Submit**.

7.  Verify that Service Mapping collects data using Netflow:

    1.  On the **nfdump file** form, select the newly configured connector and click **Run now** to start the data collection flow and populate the Flow Connection \[sa\_flow\_connection\] table.

    2.  Navigate to **System Definitions** &gt; **Tables**.

    3.  Click the Flow Connection \[sa\_flow\_connection\] table.

    4.  Under **Related Links**, click **Show List**.

    5.  Verify that the table contains data.


## What to do next

If you are satisfied with the results of the test, configure Netflow-based data collection as described in [Configure data collection using Netflow](configure-netflow-service-mapping.md).

**Parent Topic:**[Advanced Service Mapping configuration](../concept/c_ConfigureSM.md)


---
title: Configure data inputs \(Rsyslog, Filebeat, or Winlogbeat\)
description: Configure a data input for streaming log messages to your ServiceNow instance using an Rsyslog, Filebeat, or Winlogbeat agent. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure data inputs \(Rsyslog, Filebeat, or Winlogbeat\)

Configure a data input for streaming log messages to your ServiceNow instance using an Rsyslog, Filebeat, or Winlogbeat agent. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the data input type to create from the available data input types described in the table.

    **Note:** The selected data input type complements the passive data input \(listener\). For more information, see [Supported data inputs](../reference/hla-data-input-supported.md).

    |Type|Description|
    |----|-----------|
    |Rsyslog|Streams log messages from UNIX-based servers to the ServiceNow AI engine using the Rsyslog agent.|
    |Linux using Filebeat|Streams system log messages and local files from Linux servers to the instance using the Filebeat agent.|
    |Windows Application Logs using Filebeat|Streams local files from Microsoft Windows devices to the ServiceNow instance using the Filebeat agent.|
    |Windows OS using Winlogbeat|Streams Windows event logs to the ServiceNow instance using the Winlogbeat agent.|

4.  On the **Getting Started** tab, fill in the form.

    For a description of the fields, see [Rsyslog, Filebeat, or Winlogbeat data input configuration fields](../reference/hla-data-input-syslog-beats-ref.md).

    **Note:** When creating a data input for Linux using Filebeat, you can select a content pack from the **Content pack** drop-down. The content pack contains default source types and mapping script templates that save you the time it takes to create them from scratch. For more information, see [Health Log Analytics content packs for quicker time to value](../concept/hla-content-packs.md).

5.  If the agent has not already been installed, download and install it from the **Installation** tab.

    **Note:** Make sure that you’re running the latest version of the agent. Earlier versions will work, but with limited functionality.

6.  On the **Tagging and Binding** tab, assign logs to a service instance in the Configuration Management Database \(CMDB\) to enable the service to correlate the log data and enable the system to do root cause analysis.

    1.  For each source, configure the path and service instance for the logs to be streamed.

        **Note:** By default, only the required fields **Path** and **Service Instance** appear.

        For a description of the fields, see [Rsyslog, Filebeat, or Winlogbeat data input configuration fields](../reference/hla-data-input-syslog-beats-ref.md).

    2.  If you want to ship multiline logs using Filebeat, configure the properties that control how Filebeat handles messages that span multiple lines of text.

        |Field|Description|
        |-----|-----------|
        |Match|Specifies how Filebeat combines matching lines into an event.|
        |Negate|Defines whether the pattern identified in the log lines is negated.|
        |Regex|Specifies the regular expression to match.|

        **Note:** Health Log Analytics currently doesn't support multiline properties for Rsyslog.

    3.  Define additional log paths to enable the data input to stream log types from multiple paths.

        Do the following for each additional log path:

        1.  Insert a new row.
        2.  Configure the log path.
        3.  Choose a service instance.
        4.  \(Optional\) Choose a component and a source type.
        **Note:** This option is not available or necessary when using Winlogbeat, because Health Log Analytics streams the Windows event logs.

7.  On the **Finish** tab, complete the configuration for your data input type.

    -   Rsyslog:
        1.  Download the configuration file and install it on the endpoint device, in the `/etc/rsyslog.d/rsyslog.conf` directory.

            **Note:** If you are using the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), do the following instead:

            1.  On the endpoint device, install the configuration file in the `/etc/rsyslog.d/` directory.
            2.  Create a spool directory by running the `sudo mkdir -p/var/spool/rsyslog` command.
        2.  Validate the configuration by running the `rsyslogd -N1` command and verify the output.
        3.  Restart Rsyslog by running the `sudo systemctl restart rsyslog` command.
        4.  Verify the output. If it contains errors, check the `/var/log/messages` system log file for error messages and fix the errors.
    -   Linux using Filebeat:
        1.  Download the configuration file and install it on the endpoint device, in the `/etc/filebeat/` directory.
        2.  Start the agent service by running the `sudo service filebeat start` command.

            **Note:** The generated configuration ignores files that were last changed more than six hours ago. If needed, you can change this setting in the configuration.

        3.  Restart the agent service by running the appropriate command.
    -   Windows using Beats \(Filebeat or Winlogbeat\):
        1.  Download the configuration file and install it on the endpoint device, in the `C:\Program Files\` directory.
        2.  Start the agent service by running the appropriate command in PowerShell.

            -   Filebeat: `PS > Start-Service filebeat`
            -   Winlogbeat: `PS > Start-Service winlogbeat`
            **Note:** The generated configuration ignores files that were last changed more than six hours ago. If needed, you can change this setting in the configuration.

        3.  Restart the agent service by running the appropriate command.
8.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

9.  Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. This field displays only when a streaming error has occurred.

        Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

10. Select **Publish** to publish the data input to the MID Server.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data to your ServiceNow instance.

**Note:** The configuration file Health Log Analytics generates for new Filebeat data inputs is compatible with Filebeat version 7.14 and above. The minimum Filebeat version that Elasticsearch currently supports is 7.17, which is nearing its end of life \(EOL\).

Existing Filebeat data input configuration files in HLA are compatible with Filebeat versions up to 8.x. For Filebeat version 9.0 and above, either migrate from log input to filestream input or generate a new configuration file. For more information on the migration process, refer to the [Filebeat documentation](https://www.elastic.co/docs/reference/beats/filebeat/migrate-to-filestream).

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

-   **[Rsyslog, Filebeat, or Winlogbeat data input configuration fields](../reference/hla-data-input-syslog-beats-ref.md)**  
Description of the fields on the Rsyslog, Filebeat, and Winlogbeat data input configuration forms.

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

**Related topics**  


[Configure advanced settings for Rsyslog, Splunk, or TCP data inputs](hla-data-input-adv-rsyslog-splunk.md)

[Configure advanced settings for Beats data inputs](hla-data-input-adv-beats.md)


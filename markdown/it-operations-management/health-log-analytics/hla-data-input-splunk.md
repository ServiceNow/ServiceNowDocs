---
title: Configure Splunk data inputs
description: Configure a data input for streaming log messages to your ServiceNow instance using a Splunk heavy forwarder.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure Splunk data inputs

Configure a data input for streaming log messages to your ServiceNow instance using a Splunk heavy forwarder.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

-   Configure Splunk to forward logs to your ServiceNow instance using Syslog.
-   The configuration of this data input assumes the existence of an environment variable named $SPLUNK\_HOME. In Unix-like environments, this variable typically points to `/opt/splunk`.

    **Note:** The Windows environment uses the same directory structure, but with backslashes \(\\\).


Role required: evt\_mgmt\_admin

## About this task

This setup procedure is for streaming logs to your instance using a Splunk heavy forwarder. If you can't use a heavy forwarder, you can use a Splunk Universal Forwarder instead. For more information, see the [Splunk Universal Forwarder as a Shipping method \[KB0961378\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0961378) article in the Now Support Knowledge Base.

Starting in the Yokohama family release, you can use new Splunk data inputs to ingest data in the preprocessed \("cooked"\) log-forwarding format that Splunk uses by default. In cooked mode, the Splunk forwarder embeds configuration details, such as host, source type, source, and other settings into the log data. Ingesting the data into HLA in this format ensures that each log line retains all the relevant contextual information. If you are using the cooked data option in HLA, there is no need to edit the `props.conf` and `transforms.conf` files during Splunk data input configuration.

**Note:** All Splunk configuration files are located in the `$SPLUNK_HOME/etc/system/local/` folder. If a configuration file that you need to modify doesn't exist, create it and save it to this folder.

**Note:** A MID Server that is down can cause a blockage in your Splunk pipeline. A full processing queue does not affect the pipeline.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Splunk data input for streaming logs via a Splunk heavy forwarder or universal forwarder.

4.  On the **Getting Started** tab, fill in the form fields.

    For a description of the fields, see [Splunk data input configuration fields](../reference/hla-data-input-splunk-ref.md).

5.  On the **Outputs.conf** tab, add the following stanzas to the `outputs.conf` file to make the shipper forward log data over the selected transport protocol on the selected port, and then select **Next**.

    **Note:** If you have already configured outputs, merge these lines with your existing configuration.

    -   Forwarding over TCP:

        **Note:** Use the first stanza only if you have not already configured a tcpout stanza. The second stanza is required for forwarding to Health Log Analytics over TCP.

        ```
        
        [tcpout]
        indexAndForward = 1
        defaultGroup = nothing
        
        [tcpout:health_log_analytics]
        server = ip-172-31-17-121.us-east-2.compute.internal:5000
        sendCookedData = false
        compressed = false
        
        ```

    -   Forwarding over UDP:

        **Note:** Use the first stanza only if you have not already configured a syslog stanza. The second stanza is required for forwarding to Health Log Analytics over UDP.

        ```
        
        [syslog]defaultGroup = nothing
        
        [syslog:health_log_analytics]
        server = ip-172-31-17-121.us-east-2.compute.internal:5000
        
        ```

6.  On the **Props.conf** tab, edit the `props.conf` file, and then select **Next**.

    **Note:** If you selected the **Use Cooked Data** option on the **Getting Started** tab, there is no need to edit the `props.conf` file.

    1.  Modify existing stanzas or add stanzas to mark source types, service instances, and hosts for forwarding to Health Log Analytics.

        **Note:** For best results, mark only source types for forwarding.

        When adding stanzas, use the following name formats:

        -   Source types: \[&lt;source type&gt;\]. For example: \[syslog\]
        -   Sources \(not recommended\): \[source::&lt;source&gt;\]. For example, \[source::myApp\]
        -   Hosts \(not recommended\): \[host::&lt;host&gt;\]. For example, \[host::10.9.8.7\]
    2.  Add the following line to the end of each stanza that you want to forward to Health Log Analytics over either TCP or UDP.

        -   Forwarding over TCP:

            ```
            TRANSFORMS-cloned_data = clone_for_hla_store_sourcetype, clone_for_hla
            ```

        -   Forwarding over UDP:

            ```
            TRANSFORMS-cloned_data = clone_for_hla_store_sourcetype, clone_for_hla_udp
            ```

            This line applies the CLONE\_SOURCETYPE transform on the data to prevent manipulation needed for Health Log Analytics processing from affecting your existing data pipeline. For example, to send all logs from the source type "syslog" to Health Log Analytics:

            ```
            [syslog]
                                                #existing configuration goes here
                                                TRANSFORMS-cloned_data = clone_for_hla_store_sourcetype, clone_for_hla_udp
            ```

    3.  Add the following stanza to apply all the relevant transforms needed for Health Log Analytics processing.

        **Note:** Splunk enables you to anonymize sensitive data on the cloned source type for the selected protocol. For more information, see the "Anonymize data" section in the [Splunk documentation](https://docs.splunk.com/Documentation).

        -   Forwarding over TCP:

            ```
            [send_to_hla_tcp]
            TRANSFORMS-health_log_analytics = health_log_analytics_add_sourcetype, health_log_analytics_add_host, health_log_analytics_add_source, health_log_analytics_add_syslog5424, health_log_analytics_add_index, health_log_analytics_add_syslogHost, health_log_analytics_add_time
            ```

        -   Forwarding over UDP:

            ```
            [send_to_hla_udp]
            TRANSFORMS-health_log_analytics = health_log_analytics_add_sourcetype, health_log_analytics_add_host, health_log_analytics_add_source, health_log_analytics_add_syslog5424, health_log_analytics_add_index, health_log_analytics_add_syslogHost, health_log_analytics_add_time
            ```

7.  On the **Transforms.conf** tab, add the following stanzas to the `transforms.conf` file, and then select **Next**.

    **Note:** If you selected the **Use Cooked Data** option on the **Getting Started** tab, there is no need to edit the `transforms.conf` file.

    The third stanza clones the logs for further manipulation without affecting your existing indexing. The remaining stanzas add the information needed to enable correct Health Log Analytics processing.

    **Note:** You can obfuscate sensitive data by adding a transform here and then modifying the stanza of the cloned source type in the `props.conf` file.

    ```
    [accepted_keys]
    #Custom field for preserving sourcetype
    hla_sourcetype_preservation=_hla_sourcetype
    
    #Store sourcetype in a custom field, since CLONE_SOURCETYPE overwrites it
    [clone_for_hla_store_sourcetype]
    SOURCE_KEY = MetaData:Sourcetype
    REGEX = ^sourcetype::(.+)$
    FORMAT = hla_sourcetype::$1
    DEST_KEY = _hla_sourcetype
    
    [clone_for_hla]
    REGEX=.
    DEST_KEY = _TCP_ROUTING
    FORMAT = health_log_analytics
    CLONE_SOURCETYPE=send_to_hla_tcp
    
    #Only used in case of UDP forwarding
    [clone_for_hla_udp]
    REGEX=.
    DEST_KEY = _SYSLOG_ROUTING
    FORMAT = health_log_analytics
    CLONE_SOURCETYPE=send_to_hla_udp
    
    #Add metadata to the log message, since metadata is lost when forwarding externally
    [health_log_analytics_add_sourcetype]
    SOURCE_KEY = _hla_sourcetype
    REGEX = ^hla_sourcetype::(.+)$
    FORMAT = sourcetype="$1"] $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_host]
    SOURCE_KEY = MetaData:Host
    REGEX = ^host::(.+)$
    FORMAT = host="$1" $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_source]
    SOURCE_KEY = MetaData:Source
    REGEX = ^source::(.+)$
    FORMAT = source="$1" $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_syslog5424]
    REGEX=.
    FORMAT = - - [sdid@1234 $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_index]
    SOURCE_KEY = _MetaData:Index
    REGEX = ^(.+)$
    FORMAT = $1 $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_syslogHost]
    SOURCE_KEY = MetaData:Host
    REGEX = ^host::(.+)$
    FORMAT = $1 $0
    DEST_KEY = _raw
    
    [health_log_analytics_add_time]
    SOURCE_KEY = _time
    REGEX = ^(.+)$
    FORMAT = <182>1 $1 $0
    DEST_KEY = _raw
    ```

8.  On the **Finish.conf** tab, restart Splunk by running the `$SPLUNK_HOME/bin/splunk restart splunkd` command.

9.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

10. Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. This field displays only when a streaming error has occurred.

        Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

11. Select **Publish** to publish the data input to the MID Server.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data to your ServiceNow instance using a Splunk shipper.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

**Related topics**  


[Configure advanced settings for Rsyslog, Splunk, or TCP data inputs](hla-data-input-adv-rsyslog-splunk.md)


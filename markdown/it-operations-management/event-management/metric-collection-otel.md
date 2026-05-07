---
title: Metric collection from OpenTelemetry \(Otel\) metrics
description: The MID WebService metric Collector enables you to collect JSON and protobuf formatted metrics sent from OpenTelemetry \(Otel\).
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 5
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Metric collection from OpenTelemetry \(Otel\) metrics

The MID WebService metric Collector enables you to collect JSON and protobuf formatted metrics sent from OpenTelemetry \(Otel\).

## Before you begin

Ensure that you have installed the Event Management Connectors \(sn\_em\_connector\) plugin on the ServiceNow AI Platform instance and the ServiceNow version is Australia or above.

Ensure that you:

-   Deploy and start the MID Server. See [MID Server configuration](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   Configure and start the MID Web Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md).
-   To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in Started mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).
-   Enable the rest listener.

Role required: evt\_mgmt\_admin

## About this task

Protobuf and JSON formatted metrics are sent from Opentelemetry. The MID Server transforms the collected metrics by parsing them using the**TransformMetrics\_MidOpenTelemetry** script include, located at **Event Management** &gt; **Integrations** &gt; **PushConnectors**. In the Push Connectors page, select **OpenTelemetry**.

The default format of the URL to push event messages from the GCP to the MID Server is: `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/sa/inbound_metrics?transform=TransformMetrics_MidOpenTelemetry`

|Variable|Description|
|--------|-----------|
|MID\_Server\_IP|IP address of the MID Web Server Extension.|
|MID\_Web\_Server\_Port|Listening port of the MID Web Server Extension.|
|MID\_Web\_Server\_User|Username for the MID Web Server Extension.|
|MID\_Web\_Server\_Password|Password of the user of the MID Web Server.|

## Procedure

1.  CONFIGURE RECEIVERS: HOSTMETRICS RECEIVER - SYSTEM METRICS COLLECTION

    Add the following hostmetrics receiver under the "receivers:" section to collect system metrics:

    ```
    receivers:
      hostmetrics:
        collection_interval: 10s
        scrapers:
          cpu:
          memory:
          disk:
          filesystem:
          network:
          processes:
          paging:
    
    ```

    **Note:**

    -   Collection\_interval set to 10 seconds for frequent metric updates.
    -   Adjust the interval based on your monitoring requirements \(higher values reduce overhead\).
    -   Enable only the scrapers you need to minimize resource usage.
2.  CONFIGURE PROCESSORS

    TRANSFORM PROCESSOR - REMOVE UNNECESSARY FIELDS

    1.  Add the following transform processor under the "processors:" section to remove unnecessary fields from the payload:

        ```
        transform:
          metric_statements:
            - context: scope
              statements:
                - set(name, "")
                - set(version, "")
        
        ```

    2.  MEMORY LIMITER PROCESSOR - PREVENT MEMORY ISSUES

        Add the following memory\_limiter processor under the "processors:" section to prevent out-of-memory errors:

        ```
        memory_limiter:
          limit_mib: 5
          spike_limit_mib: 1
        
        ```

        **Note:**

        -   limit\_mib set to 5 MB of memory usage
        -   spike\_limit\_mib adjusted to 1 MB to handle temporary spikes
        -   Adjust these values based on your system's available memory
    3.  FILTER PROCESSOR - SELECT SPECIFIC METRICS

        Add the following filter processor under the "processors:" section to include only selected metrics:

        ```
        filter/minimal:
          metrics:
            include:
              match_type: strict
              metric_names:
                # CPU Metrics
                - system.cpu.time
                - system.cpu.load_average.1m
                - system.cpu.load_average.5m
                - system.cpu.load_average.15m
                # Memory Metrics
                - system.memory.usage
                - system.paging.usage
                # Disk Metrics
                - system.filesystem.usage
                - system.disk.io
                - system.disk.io_time
                # Process Metrics
                - system.processes.count
                - system.processes.created
                # Paging Metrics
                - system.paging.operations
                # Network Metrics
                - system.network.io
                - system.network.packets
                - system.network.errors
                - system.network.dropped
                - system.network.connections
                # MySQL Metrics
                - mysql.operations
                - mysql.locks
                - mysql.uptime
                - mysql.threads
                # HTTP Check Metrics
                - httpcheck.duration
                - httpcheck.status
                - httpcheck.error
                # Prometheus node_exporter Metrics
                - node_cpu_seconds_total
                - node_memory_MemTotal_bytes
                - node_memory_MemAvailable_bytes
                - node_disk_read_bytes_total
                - node_disk_written_bytes_total
                - node_disk_io_time_seconds_total
                - node_network_receive_bytes_total
                - node_network_transmit_bytes_total
        
        ```

        **Note:** Histogram metrics are not supported by ServiceNow MID Server.

        Even if histogram metrics are sent to the MID Server, the ServiceNow transform script will automatically ignore them. However, as a best practice, it is recommended to filter out histogram metrics at the collector level to optimize network bandwidth and reduce unnecessary data transmission.

        To exclude histogram metrics, add the following filter:

        ```
        filter/drop_histograms:
            metrics:
              metric:
                - 'type == METRIC_DATA_TYPE_HISTOGRAM'
        ```

3.  CONFIGURE EXPORTERS

    Choose one of the following authentication methods based on your requirements:

    1.  OPTION A: API KEY AUTHENTICATION

        Add the following exporter under the "exporters:" section:

        ```
        otlphttp/opentelemetry:
          metrics_endpoint: "http://{mid_server_ip}:{port}/api/mid/sa/inbound_metrics?transform=TransformMetrics_MidOpenTelemetry"
          headers:
            Authorization: "Key {api_key}"
          timeout: 30s
          compression: none
          tls:
            insecure: true
          sending_queue:
            enabled: true
            num_consumers: 4
            queue_size: 100
          retry_on_failure:
            enabled: true
            initial_interval: 5s
            max_interval: 30s
        
        ```

        **Note:** Compression:gzip is not supported. Replace \{mid\_server\_ip\}, \{port\}, and \{api\_key\} with your actual values.

    2.  OPTION B: BASIC AUTHENTICATION

        For Basic Authentication, you need to configure both an extension and an exporter.

        1.  Configure Basic Auth Extension

            Add the following under the "extensions:" section:

            ```
            extensions:
              basicauth/mid:
                client_auth:
                  username: "otel"
                  password: "Otel@123"
            
            ```

            **Note:** Replace username and password with your actual credentials.

        2.  Configure Basic Auth Exporter

            Add the following under the "exporters:" section:

            ```
            otlphttp/opentelemetryBasic:
              metrics_endpoint: "http://{mid_server_ip}:{port}/api/mid/sa/inbound_metrics?transform=TransformMetrics_MidOpenTelemetry"
              auth:
                authenticator: basicauth/mid
              timeout: 30s
              compression: none
              tls:
                insecure: true
              sending_queue:
                enabled: true
                num_consumers: 4
                queue_size: 100
              retry_on_failure:
                enabled: true
                initial_interval: 5s
                max_interval: 30s
            
            ```

            **Note:** Compression:gzip is not supported. Replace \{mid\_server\_ip\} and \{port\} with your actual values.

4.  CONFIGURE SERVICE PIPELINE

    Add the configured processors and exporters to the metrics pipeline under the "service:" section:

    ```
    service:
      pipelines:
        metrics:
          receivers: [<your_configured_receivers>]
          processors: [memory_limiter, transform, filter/minimal]
          exporters: [otlphttp/opentelemetry, otlphttp/opentelemetryBasic]
    
    ```

    **Note:**

    -   Replace &lt;your\_configured\_receivers&gt; with your actual receiver names \(e.g., hostmetrics\).
    -   Include only the exporters you have configured \(API Key or Basic Auth, or both\).
    -   Processor order matters: memory\_limiter should be first, followed by transform and filter.
    -   Ensure the processor names match those defined in Step 2.
    -   If using histogram filtering, add filter/drop\_histograms after filter/minimal.
5.  ADDITIONAL CONFIGURATION OPTIONS

    By default, OpenTelemetry sends data in Protocol Buffers \(protobuf\) format.

    To send data in JSON format instead, add the following header to your exporter configuration:

    ```
    headers:
      Content-Type: "application/json"
    
    ```

    COMPLETE CONFIGURATION EXAMPLE.

    Below is a complete example configuration file combining all components:

    ```
    receivers:
      hostmetrics:
        collection_interval: 10s
        scrapers:
          cpu:
          memory:
          disk:
          filesystem:
          network:
          processes:
          paging:
     
    processors:
      memory_limiter:
        limit_mib: 5
        spike_limit_mib: 1
      
      transform:
        metric_statements:
          - context: scope
            statements:
              - set(name, "")
              - set(version, "")
      
      filter/minimal:
        metrics:
          include:
            match_type: strict
            metric_names:
              - system.cpu.time
              - system.cpu.load_average.1m
              - system.memory.usage
              - system.network.io
      
      filter/drop_histograms:
        metrics:
          include:
            metric:
              - 'type != METRIC_DATA_TYPE_HISTOGRAM'
     
    extensions:
      basicauth/mid:
        client_auth:
          username: "otel"
          password: "Otel@123"
     
    exporters:
      otlphttp/opentelemetry:
        metrics_endpoint: "https://10.0.0.100:8443/api/mid/sa/inbound_metrics?transform=TransformMetrics_MidOpenTelemetry"
        headers:
          Authorization: "Key your_api_key_here"
        timeout: 30s
        compression: none
        tls:
          insecure: false
        sending_queue:
          enabled: true
          num_consumers: 4
          queue_size: 100
        retry_on_failure:
          enabled: true
          initial_interval: 5s
          max_interval: 30s
     
    service:
      extensions: [basicauth/mid]
      pipelines:
        metrics:
          receivers: [hostmetrics]
          processors: [memory_limiter, transform, filter/minimal, filter/drop_histograms]
          exporters: [otlphttp/opentelemetry]
    
      
    ```


**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)


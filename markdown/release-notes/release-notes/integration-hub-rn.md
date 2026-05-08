---
title: Integration Hub release notes
description: The ServiceNow Integration Hub application extends the ServiceNow Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Integration Hub release notes

The ServiceNow® Integration Hub application extends the ServiceNow® Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Australia release.

## Integration Hub highlights for the Australia release

-   Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka.
-   Simplify topic management in Stream Connect with topic aliases. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic.
-   View detailed statistics and monitor the health of your Integration Hub Remote Process Sync \(RPS\) integrations with the Remote Process Sync Dashboard.

See Integration Hub for more information.

## New in the Australia release

-   **Use Direct Kafka to integrate your on-premise ServiceNow instance with your local Kafka environment**

    Configure a custom Kafka connection to enable your on-premise instance to connect directly to your local Kafka environment.

-   **Create topic aliases for Stream Connect topics**

    Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and, wherever they’re moved, connected to an underlying topic.

-   **Stream Connect Dashboard updates**
    -   The Topics menu displays topic aliases, Hermes topics, and Direct Kafka topics.
    -   The **Data usage** tab shows data for the Hermes cluster or the Direct Kafka cluster. Use the **Kafka Cluster** list to select which cluster data to display.
    -   The Consumers and Producers menus reference topic aliases instead of Hermes topics.
-   **View the Remote Process Sync Dashboard**

    View detailed statistics and monitor the health of your Remote Process Sync \(RPS\) integrations. The Remote Process Sync Dashboard provides real-time visibility into key metrics, including records processed, queue sizes, processing times, and system status. Use this dashboard to identify issues, track performance trends, and promote smooth operation of your RPS integrations.

-   **Produce messages to Hermes via a MID Server**

    Send message payloads to Hermes with MID script includes.

-   **View usage metrics for Direct Kafka**

    Track data usage between your instance and Direct Kafka systems. The Direct Kafka Usage metrics table provides administrators with visibility into data transfer volumes for bytes produced and consumed. View metrics aggregated by hour, day, or month at the cluster and topic level. Usage records are automatically retained for 13 months.

-   **Use the read-only role for Stream Connect**

    Use the new read-only role for Stream Connect to grant users view-only access to Stream Connect resources. Users with this role can view Stream Connect configurations and runtime statistics across all related modules, but can’t create, modify, or delete any Stream Connect settings.

-   **View logs for Stream Connect producers**

    Get detailed log information for producers in the Stream Connect logs. Use the **glide.ih.kafka.producer.message\_bytes\_to\_log** property to specify how much of the message to display in the logs.

-   **Configure alert thresholds for undelivered messages in Stream Connect**

    Set alert thresholds for undelivered messages based on how long a topic has gone without receiving new messages. Use this configuration to trigger INFO, WARNING, or CRITICAL alerts when message delivery stops for a specified period.

-   **Configure alert thresholds for unprocessed messages in Stream Connect**

    Set alert thresholds for messages that remain unprocessed in a topic. You can trigger alerts based on how long messages sit in a topic without being consumed, helping to identify lagging or failing consumers.

-   **Get metadata information for Stream Connect consumers**

    View the partition, offset, datacenter ID, and timestamp epoch for the script consumer and Kafka Message trigger.

-   **View message timestamps in the Stream Connect script consumer**

    Get the message timestamp in the script consumer as a UTC time-zone string. You can use the UTC time-zone string to convert the timestamp to a **GlideDateTime** object.

-   **Use an error subflow template to create your own error subflows in Remote Process Sync**

    Copy and modify the RPS Error Subflow Template to create error subflows. The template enables you to select notification methods for when the Inbound and Outbound States are errored.

-   **Specify attachment details in Remote Process Sync actions**

    Specify the max attachment size and allowed attachment extensions in the Identify New Attachments action and the Get Attachment Metadata for Local Record action.

-   **Use a new retry policy for Remote Process Sync actions**

    Retry failed requests at specified intervals with the RPS Push Attachment Policy. This policy works with the Identify New Attachments action and the Get Attachment Metadata for Local Record action.

-   **SASL authentication support for Apache Kafka connections**

    Configure SASL authentication for your Apache Kafka connections with support for SASL\_SSL and SASL\_PLAINTEXT security protocols. Kafka credentials now support multiple SASL mechanisms: PLAIN- SCRAM-SHA-256, SCRAM-SHA-512.


## Activation information

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   ServiceNow Stream Connect common core \(com.glide.hub.stream\_connect.common.core\): Provides the general Stream Connect capabilities across Hermes and Direct Kafka.
    -   ServiceNow Stream Connect Direct Kafka \(com.glide.hub.stream\_connect.direct\_kafka\): Adds the capability to connect the ServiceNow instance to Apache Kafka directly \(not using Hermes Messaging Service\).
    -   ServiceNow Stream Connect Hermes \(com.glide.hub.stream\_connect.hermes\): Adds the capability for Stream Connect to connect to the Hermes Messaging Service.
    -   ServiceNow Stream Connect Installer \(Direct Kafka\) \(com.glide.hub.stream\_connect.onprem\_installer\): The installer that installs the required plugins for Direct Kafka.
    -   ServiceNow Stream Connect Kafka Connection \(com.glide.hub.stream\_connect.kafka\_connection\): Adds the ability to use Kafka credentials for Direct Kafka and Message Replication.
    -   ServiceNow Stream Connect Replication Certificates \(com.sn\_stream\_connect.replication.cert\): Adds the capability to handle certificates to connect to the Hermes Messaging Service from the MID Server.
    -   ServiceNow Stream Connect Replication Core \(com.glide.hub.stream\_connect.replication.core\): Adds capabilities to replicate data between a topic in the Hermes Messaging Service and a topic in a local Apache Kafka environment.
    -   Stream Connect MID Hermes API \(com.glide.mid.hermes\_api\): Provides the capability to produce messages from the MID Server to a topic in the Hermes Messaging Service.

## Related ServiceNow applications and features

-   **Workflow Studio**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results that they produce.

-   **MID Server**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **RPA Hub**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **Connections and Credentials**

    Credentials and connection information are required to gain access to a computer or network device for ServiceNow® Discovery, ServiceNow® Service Mapping, and ServiceNow® Cloud Management, or to perform work using ServiceNow® Orchestration. When adding content to share on the ServiceNow® Developer Site or the ServiceNow® Store, you can configure connections and credentials relevant to your environment without modifying the built content.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)


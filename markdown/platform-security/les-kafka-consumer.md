---
title: Kafka consumer
description: Use guided setup to step through the initial configuration of LES. Guided setup assists you with planning the roll-out of the product and performing the basic configuration to go live.Implement the following steps for a complete guided setup for Kafka consumers.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Log Export Service \(LES\), Platform Security]
---

# Kafka consumer

Use guided setup to step through the initial configuration of LES. Guided setup assists you with planning the roll-out of the product and performing the basic configuration to go live.

Guided setup organizes configuration activities into categories. Each category provides information, such as planning guidance, pre-setup steps, and links to useful help content. Categories also provide a set of links to the pages in your instance where you perform the configuration. The guided setup process keeps track of what you have completed, so you can stop and start again where you left off.

## Guided setup home page

The home page for guided setup contains an overview of configuration types for your guided setup. You can select your guided setup type and select **Continue** to open the guided setup steps and begin configuration.

![](../image/les-kafka-setup.png)

All three setups on this page, Quick Start/Best Experience/Custom provide the same tasks and functionality. It is required that to coordinate the integration between the ServiceNow instance and the destination log analytic tool with the respective administrator. The log analytic administrator must configure their tool to connect to the ServiceNow instance securely. It is recommended to share the [Set up a secure connection to the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=set-up-secure-connection-to-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) document with the log analytic administrator ahead of time. Even if you have marked a task as completed, you can go back and uncheck it back to in progress. To do so, first click on the **Edit** box in the upper right corner for the category. Then click on the **Edit** box for the task you want to uncheck. The **Mark as complete** box will no longer be marked.

## Guided setup categories page

The categories page contains an overview and descriptions of the categories and associated tasks. You can click either the drop down arrow to view information about the category or the Start button to open the guided setup steps and begin configuration.

![](../image/les-kafka-categories.png)

Complete the tasks under each category by following the setup instructions.

**Parent Topic:**[Log Export Service \(LES\)](les-landing-page.md)

## Guided setup for Kafka consumers

Implement the following steps for a complete guided setup for Kafka consumers.

### Before you begin

Navigate to **Log Export Service \(LES\)** &gt; **Kafka Consumer** &gt; **Guided Setup**. Select the type of setup you wish to configure and click **Continue**.

**Note:** During the Log Export Service application installation, ServiceNow will provision the underlying Hermes Messaging Service infrastructure. Be aware that this process can take up to a couple of hours to complete from the time you request the Log Export Service application installation.

Role required: admin

### Procedure

1.  Review Hermes Messaging Service Diagnostics.

    It is recommended that you verify that the Hermes Messaging Service is up and running with the Hermes diagnostic tool, which displays on screen during this step. If you see a "Page not found" error on this page, Hermes is not installed and you should contact your system admin.

    -   Setup information: The following bootstrap information is used to connect to the Hermes Messaging Service. The "Producer Bootstrap" is the connection used to send messages into Hermes and "Consumer Bootstrap 1 &amp; 2" are used to retrieve messages from Hermes.
        -   Producer Bootstrap
        -   Consumer Bootstrap 1
        -   Consumer Bootstrap 2
    -   Instance PKI: The Instance Public Key Infrastructure \(PKI\) component allows a ServiceNow instance to act as an issuer in a X.509 trust hierarchy.
    -   Bootstrap Connectivity: Click **Run Test** to confirm external client is able to connect to the defined instance ports \(producer and consumer\).

        **Note:** Work with your network administrator to ensure that the following port ranges are open before you begin:

        -   Consumer1: 4100-4150
        -   Consumer2: 4200-4250
    -   Instance Connectivity: Click **Run Test** to confirm the instance is able to send and receive messages.
    -   View Topics: Click the listed topic to retrieve the timestamp of the last known message.
    **Note:** You can access Hermes Diagnostics in the future to troubleshoot potential connectivity issues by returning to this step of the guided setup or by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Diagnostics**.

2.  Generate certificates for a secure connection to Hermes Messaging Service and pull log events from it.

    You are going to use these certificates when connecting your external system.

    Setup secure connection to Hermes Messaging Service. See [Set up a secure connection to the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=set-up-secure-connection-to-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information. You will need these certificates for authentication and authorization in the client which will pull the logs from Hermes.

    **Note:** admin or Hermes\_admin roles are required for this step.

3.  Configure Log Producer: Choose log sources to export and configure their filters.

    Complete the following tasks to configure the Log Producer.

    -   Configure log sources to export: Create one Source record for each of the log sources that you want to export.

        **Note:** admin or sn\_logstoanalytics.admin roles are required to complete this step

        1.  Click **New** at the top right corner
        2.  Select a Source Type
        3.  Select the appropriate filters for the selected source type

            **Note:** Filters are different depending on the selected source type

        4.  Click Update
        When successfully created, it will display the name of the Hermes topic to which that log source will be exported to. Write down the topic name, you will need it later when configuring your log consumer system. The Active field controls whether or not that log source is going to be exported or not. If you see errors, please go back to task “Check Hermes Diagnostics” and verify Hermes status.

    -   Validate Log Producer: Once you have created a Source to produce logs from, you can see live log records in the topic using **Hermes Messaging Service** &gt; **Hermes Topic Inspector**.
        1.  Select External Topics
        2.  Click List Topics
        3.  Select row with your topic from previous step \(listed in Sources\)
        4.  Adjust message start date if necessary
        5.  Click **View** to see a log message that was exported to the topic
4.  Connect Kafka consumer: Follow these tasks to connect your chosen Kafka consumer to pull log events from the Hermes.

    -   Identify Kafka consumer: You have two options based on your log analytics architecture.

        -   If you have your own Kafka system and choose that for log aggregation, you can connect directly to the Hermes Messaging Service via the native Kafka protocol.
        -   If you choose to have your log analytics tool connect directly to the Hermes Messaging Service then you need to deploy a Kafka connector supported by your log analytics system \(i.e. Splunk Connect for Kafka\).
        **Note:** In either case, you will need to work with the Administrator for those systems to coordinate the connection with the Hermes Messaging Service.

    -   Import Hermes certificates to Kafka consumer system: Log into your Kafka consumer system and make sure you have appropriate admin entitlements to configure it and connect it to an external system. Import the certificates generated in “Set up secure connection to Hermes Messaging Service” task into your Kafka connector or Kafka server. Follow the instructions in the documentation for your chosen Kafka consumer.
    -   Configure Kafka processes: The Hermes Messaging Service is designed for high availability. Two processes are required to consume messages from Hermes. Two processes are required because Hermes uses a pair of Kafka clusters for failover purposes. If one cluster goes down, data is produced to the other Hermes Kafka cluster.

        In your Kafka consumer system, you will need to create two separate consumer processes to connect to both Hermes Kafka clusters. For both processes you will specify the same Hermes Kafka topic but you will need to configure two separate bootstrap addresses:

        -   &lt;instance\_name&gt;.service-now.com:4100,&lt;instance\_name&gt;.service-now.com:4101,&lt;instance\_name&gt;.service-now.com:4102,&lt;instance\_name&gt;.service-now.com:4103
        -   &lt;instance\_name&gt;.service-now.com:4200,&lt;instance\_name&gt;.service-now.com:4201,&lt;instance\_name&gt;.service-now.com:4202,&lt;instance\_name&gt;.service-now.com:4203
        Important notes:

        -   When accessing the Kafka topic from external systems, you must prepend “snc.&lt;instance name&gt;.” to the topic that the logs are being forwarded to.
        -   Configure each consumer with the same Kafka Consumer Group ID.
        -   Install your keystore and truststore files in a location where your consumers can access them.
        -   If your consumers require it, specify the Kafka JSON Converters properties to disable schemas: “key.converter.schemas.enable=false”, “value.converter.schemas.enable=false”
    -   Verify Kafka consumer pulling logs from Hermes: Verify in your chosen Kakfa consumer that you can pull log events from the Hermes Messaging Service.


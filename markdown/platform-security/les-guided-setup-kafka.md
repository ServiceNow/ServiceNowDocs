---
title: Guided setup for Kafka consumers
description: Implement the following steps for a complete guided setup for Kafka consumers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-guided-setup-kafka.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Kafka consumer, Configure, Log Export Service \(LES\), Platform Security]
---

# Guided setup for Kafka consumers

Implement the following steps for a complete guided setup for Kafka consumers.

## Before you begin

Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Kafka Consumer** &gt; **Guided Setup**.

Role required: admin

**Note:** During the Log Export Service application installation, ServiceNow will provision the underlying Hermes Messaging Service infrastructure. Be aware that this process can take up to a couple of hours to complete from the time you request the Log Export Service application installation.

## Procedure

1.  Review Hermes Messaging Service Diagnostics.

    It is recommended that you verify that the Hermes Messaging Service is up and running with the Hermes diagnostic tool, which displays on screen during this step. If you see a "Page not found" error on this page, Hermes is not installed and you should contact your system admin. For more information, see [Exploring Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/exploring-hermes-messaging-service.md).

    1.  Select **Start** to begin.
    2.  Review the following diagnostics:
        -   Setup information: The following bootstrap information is used to connect to the Hermes Messaging Service. The "Producer Bootstrap" is the connection used to send messages into Hermes and "Consumer Bootstrap 1 &amp; 2" are used to retrieve messages from Hermes.
            -   Producer Bootstrap
            -   Consumer Bootstrap 1
            -   Consumer Bootstrap 2
        -   Instance PKI: The Instance Public Key Infrastructure \(PKI\) component allows a ServiceNow instance to act as an issuer in a X.509 trust hierarchy.
        -   Bootstrap Connectivity: Select **Run Test** to confirm external client is able to connect to the defined instance ports \(producer and consumer\).
        -   Instance Connectivity: Select **Run Test** to confirm the instance is able to send and receive messages.
        -   View Topics: Select **Get Topic List** to view and retrieve the timestamp of the last known message.
    3.  Select **Mark as complete** to proceed once done.
    **Note:** You can access Hermes Diagnostics in the future to troubleshoot potential connectivity issues by returning to this step of the guided setup or by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Diagnostics**.

2.  Generate certificates for a secure connection to Hermes Messaging Service and pull log events from it.

    You are going to use these certificates when connecting your external system.

    Set up a secure connection to Hermes Messaging Service. See [Set up a secure connection to the Hermes Messaging Service for LES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-hermes-cert.md) for more information. You will need these certificates for authentication and authorization in the client which will pull the logs from Hermes.

    **Note:** admin or Hermes\_admin roles are required for this step.

    Select **Mark as complete** to proceed once done.

3.  Configure Log Producer: Choose log sources to export and configure their filters.

    Complete the following tasks to configure the Log Producer.

    -   Configure log sources to export: Create one Source record for each of the log sources that you want to export.

        **Note:** admin or sn\_logstoanalytics.admin roles are required to complete this step.

        1.  Select **New** to create a new source configuration. The Source form shows up.

            **Note:** You can also select an existing source configuration if you want to modify it.

        2.  On the form, fill in the fields:
            -   **Source Type**: Types of log sources \(Node Log or Table\). See [Log sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md) for more information.
            -   **Log Level**: A set of standard logging levels that can be used to control logging output. Following convention, each level forwards logs of equal or greater severity. This field is visible when you select Node Log as the Source Type, or when you select Table as the Source Type and the table is syslog.
            -   **Table**: Selection of table for exporting table type logs. For more information on supported tables, see [Log Sources.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md)
            -   **Filter Type**: Conditions to forward logs selectively. This field is visible only if you select syslog, sys\_audit, sys\_audit\_delete, or sys\_audit\_relation as the table.
            -   **Topic**: Select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, see [Create source type and multiple topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).
            -   **Accepts**: Specifies the format in which the logs are forwarded to Hermes. They can either be sent as JSON or as plain text.
            -   **Active**: Indicates whether the Source log is active.
        3.  Complete the flow that matches the table you selected.
            -   **Standard source**

                Select **Submit** to save the source configuration. The source details appear in the Sources list, where you can review its source type, table, topic, and active status.

                **Note:**

                -   Applies when you select Source type as Node Log and any table other than the syslog and sys\_audit tables.
                -   The configuration is complete. Skip the remaining steps.
            -   **syslog table**

                When you select **Source type** as Table and syslog in the **Table** field:

                **Note:** You can create multiple source topics for this selection.

                1.  Select the **Log level**.
                2.  Select **Submit**. The **Source topics** related list appears, and the log export filters become available.
                3.  Select **New** to create a new source topic.
                4.  In the **Filter** field, select a value from the dropdown list.
                    -   **All**: No additional field appears.
                    -   **Application Family**, **Package**, or **Scope**: A corresponding lookup field appears. Select the lookup icon to select a value.
                5.  In the **Topic** field, select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, refer [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).
                6.  Select **Submit**, and then review the source topics that you created.
            -   **sys\_audit table with the Log table filter**

                When you select the **Table** as sys\_audit and **Filter type** as Log table:

                **Note:** You can create multiple source topics for this selection.

                1.  The **Source topics** related list appears, and the log export filters become available.
                2.  Select **New** to create a new source topic.
                3.  Select the required table in the **Log table** field using the lookup icon.
                4.  In the **Topic** field, select an existing topic, or create a topic through the lookup icon. For more information on creating a topic, refer [Create source type and multi topics in the LES source table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-multi-topics-v2.md).
                5.  Select **Submit**, and then review the source topics that you created.
        When successfully created, it will display the name of the Hermes topic to which that log source will be exported to. Write down the topic name, you will need it later when configuring your log consumer system.

        The Active field controls whether or not that log source is going to be exported. If you see errors, go back to the Check Hermes Diagnostics task and verify Hermes status.

    -   Validate Log Producer: Once you have created a Source to produce logs from, you can see live log records in the topic using **Hermes Messaging Service** &gt; **Hermes Topic Inspector**.
        1.  Select External Topics
        2.  Select List Topics
        3.  Select row with your topic from previous step \(listed in Sources\)
        4.  Adjust message start date if necessary
        5.  Select **View** to see a log message that was exported to the topic
    Select **Mark as complete** once done.

4.  Connect Kafka consumer: Follow these tasks to connect your chosen Kafka consumer to pull log events from the Hermes.

    -   Identify Kafka consumer: You have two options based on your log analytics architecture.

        -   If you have your own Kafka system and choose that for log aggregation, you can connect directly to the Hermes Messaging Service via the native Kafka protocol. For more information, see [Apache Kafka](https://kafka.apache.org/).
        -   If you choose to have your log analytics tool connect directly to the Hermes Messaging Service, you need to deploy a Kafka connector. Deploy a connector supported by your log analytics system, for example, Splunk Connect for Kafka. For more information, see [Splunk Connect for Kafka](https://splunkbase.splunk.com/app/3862).
        **Note:** In either case, you will need to work with the Administrator for those systems to coordinate the connection with the Hermes Messaging Service.

        Select **Next** to proceed.

    -   Import Hermes certificates to Kafka consumer system: Log into your Kafka consumer system and make sure you have appropriate admin entitlements to configure it and connect it to an external system. Import the certificates generated in “Set up secure connection to Hermes Messaging Service” task into your Kafka connector or Kafka server. Follow the instructions in the documentation for your chosen Kafka consumer.

        Select **Next** to proceed.

    -   Configure Kafka processes: The Hermes Messaging Service is designed for high availability. Two processes are required to consume messages from Hermes. Two processes are required because Hermes uses a pair of Kafka clusters for failover purposes. If one cluster goes down, data is produced to the other Hermes Kafka cluster.

        In your Kafka consumer system, you will need to create two separate consumer processes to connect to both Hermes Kafka clusters. For both processes you will specify the same Hermes Kafka topic but you will need to configure two separate bootstrap addresses:

        -   &lt;instance\_name&gt;.service-now.com:4100,&lt;instance\_name&gt;.service-now.com:4101,&lt;instance\_name&gt;.service-now.com:4102,&lt;instance\_name&gt;.service-now.com:4103
        -   &lt;instance\_name&gt;.service-now.com:4200,&lt;instance\_name&gt;.service-now.com:4201,&lt;instance\_name&gt;.service-now.com:4202,&lt;instance\_name&gt;.service-now.com:4203
        **Note:** Work with your network administrator to ensure that the following port ranges are open before you begin:

        -   Consumer1: 4100-4150
        -   Consumer2: 4200-4250
        Important notes:

        -   When accessing the Kafka topic from external systems, you must prepend “snc.&lt;instance name&gt;.” to the topic that the logs are being forwarded to.
        -   Configure each consumer with the same Kafka Consumer Group ID.
        -   Install your keystore and truststore files in a location where your consumers can access them.
        -   If your consumers require it, specify the Kafka JSON Converters properties to disable schemas: “key.converter.schemas.enable=false”, “value.converter.schemas.enable=false”
    -   Verify Kafka consumer pulling logs from Hermes: Verify in your chosen Kakfa consumer that you can pull log events from the Hermes Messaging Service.
    Select **Mark as complete** once done.


**Parent Topic:**[Kafka consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-kafka-consumer.md)


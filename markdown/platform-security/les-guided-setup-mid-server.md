---
title: Guided setup for MID Server consumers
description: Implement the following steps for a complete guided setup for MID Server consumers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-guided-setup-mid-server.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [MID server consumer, Configure, Log Export Service \(LES\), Platform Security]
---

# Guided setup for MID Server consumers

Implement the following steps for a complete guided setup for MID Server consumers.

## Before you begin

Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **MID Server Consumer Guided Setup**.

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
    3.  Select **Mark as Complete** to proceed once done.
    **Note:** You can access Hermes Diagnostics in the future to troubleshoot potential connectivity issues by returning to this step of the guided setup or by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Diagnostics**.

2.  Generate certificates for a secure connection to Hermes Messaging Service and pull log events from it.

    You are going to use these certificates when connecting your external system.

    Set up a secure connection to Hermes Messaging Service. See [Set up a secure connection to the Hermes Messaging Service for LES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-hermes-cert.md) for more information. You will need these certificates for authentication and authorization in the client which will pull the logs from Hermes.

    **Note:** admin or Hermes\_admin roles are required for this step.

    Select **Mark as Complete** to proceed once done.

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

4.  Configure Log REST Push Destination: Setup the MID Server to be able to push logs to your log analytics system \(such as Splunk\).

    Complete the following tasks to configure log REST push destination.

    -   Add MID Properties: You must add MID Server properties so that it’s able to connect to Hermes. Navigate to **MID Server** &gt;**Properties** and set the appropriate values for each of the properties listed below.

        |Name|Value|
        |----|-----|
        |mid.les.kafka.ssl.truststore.password|&lt;password&gt;|
        |mid.les.kafka.ssl.keystore.password|&lt;password&gt;|
        |mid.les.kafka.ssl.key.password|&lt;password&gt;|
        |mid.les.kafka.ssl.truststore.location|&lt;your\_path&gt;/&lt;truststore&gt;.p12|
        |mid.les.kafka.ssl.keystore.location|&lt;your\_path&gt;/&lt;keystore&gt;.p12|
        |mid.les.kafka.ssl.truststore.type|PKCS12|
        |mid.les.kafka.ssl.keystore.type|PKCS12|
        |mid.les.kafka.client.id|&lt;instance\_name&gt;|
        |mid.les.kafka.group.id|snc.&lt;instance\_name&gt;.group1|
        |mid.les.kafka.bootstrap.servers|&lt;instance\_name&gt;.servicenow.com:4100,&lt;instance\_name&gt;.servicenow.com:4101,&lt;instance\_name&gt;.servicenow.com:4102,&lt;instance\_name&gt;.servicenow.com:4103|
        |mid.les.kafka.set2.bootstrap.servers|&lt;instance\_name&gt;.servicenow.com:4200,&lt;instance\_name&gt;.servicenow.com:4201,&lt;instance\_name&gt;.servicenow.com:4202,&lt;instance\_name&gt;.servicenow.com:4203|
        |mid.les.consumer.threads.count|4|
        |mid.les.kafka.security.protocol|SSL|

        Follow these notes on how to obtain some of the above values

        -   &lt;password&gt; is the password you set for the keystore and truststore
        -   &lt;your\_path&gt; is the file path to the directory where you keep the keystore and truststore files you downloaded. The certificates need to be on the server where you are running MID
        -   &lt;instance\_name&gt; is the name of your ServiceNow instance. If you are not sure, you can find it in the sys\_properties table
        -   You can obtain the values for both mid.les.kafka.bootstrap.servers and mid.les.kafka.set2.bootstrap.servers from the Hermes Diagnostics page. Navigate to **Hermes Messaging Service** &gt; **Diagnostics** and copy the strings under Consumer Bootstrap 1 and Consumer Bootstrap 2 respectively.
    -   Configure Destination: Create a new Destination Configuration record, which defines the REST endpoint that this Extension will forward logs to.

        **Note:** admin or sn\_logstoanalytics.admin roles are required to complete this step.

        1.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Destination Configurations** 
        2.  Select **New** at the right hand corner.
        3.  On the form, fill in the fields:
            -   **Name**: Name of the destination configuration.
            -   **Destination URL**: The URL for your desired endpoint for the exported log sources.
            -   **Destination Credentials**: Search for or create the credentials to connect to your endpoint. Only Basic Auth and OAuth credential types are valid with LES.
            -   **Transform Script**: Search for or create a script that specifies how to transform logs into a suitable format for the destination. A predefined script named **SplunkTransform** is provided for Splunk endpoints, which you can use and edit as needed.
        4.  Select **Submit**.
5.  Configure LOG Consumer: Follow these tasks to configure your MID Server Extension for Log Export Service purposes.

    -   Configure LES Consumer Context: In this step, you will update the LES Consumer record to execute on the dedicated MID server you just installed for the Log Export Service. Update the LES Consumer record by setting the following fields:

        1.  Navigate to **MID Server** &gt; **Extensions** &gt; **LES Consumer Context**.
        2.  Select on 'LES Consumer' to open the MID Server context record
        3.  Select Specific MID Server for the "Execute on" field
        4.  Enter the name of the MID you validated in the previous step for the “MID Server” field
        5.  Select **Update**.
        **Note:**

        -   Each Consumer is designed to process data from a single Hermes topic using its own Consumer Context.
        -   Each Consumer Context runs on a dedicated MID Server to ensure optimal performance.
        -   We recommend configuring a separate MID Server for each Consumer Context you create.
    -   Configure Consumer: Create a new Consumer record, which represents the process that’s part of the Log Export Service MID Server Extension.
        1.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Consumers**.
        2.  Select **New** to create a new Consumer record.
        3.  On the form, fill in the fields:
            -   **Name**: Name of the consumer.
            -   **Topic**: Active topic to retrieve log messages from. Select a topic from the ones available in the Sources table. If the Topic dropdown is empty, navigate to the Sources table and make sure at least one active log source is configured before you create a consumer.
            -   **Destination Configuration**: Destination to send the retrieved logs to.
            -   **Consumer Context**: Unique LES Consumer Context record to link to this consumer. Attach the corresponding consumer context when you create the consumer.
        4.  Select **Submit**.
    -   Test MID Connection: Verify connectivity from the MID Server environment to the Hermes cluster before starting the Consumer.

        **Note:** Role required: admin or sn\_logstoanalytics.admin

        Navigate to **Log Export Service \(LES\)** &gt; **Consumers** and test the connection:

        1.  Open the existing Consumer record.
        2.  Click the **Test MID Connection** UI Action
            1.  This validates connectivity between the MID Server environment and the Hermes cluster
            2.  The Status field will change to “Checking Kafka Network Connectivity”
        3.  Wait for the test to complete, then refresh the page
        4.  Review the Status and Status Detail fields
        5.  If successful: Network connectivity is confirmed. Refresh the page and verify the Status and Status Detail fields reflect success.

            Start the consumer.

        6.  If unsuccessful: Please pause before proceeding. Review the MID Server agent logs to understand the cause. Common areas to verify include:
            1.  MID Server properties are correctly configured
            2.  Network connectivity is available between the MID Server and the Hermes cluster
        **Note:** The Test MID Connection must succeed before starting the Consumer.

    -   Verify MID Server integration:

        1.  Navigate to  **All** &gt; **Log Export Service \(LES\)** &gt; **Consumer Status** to view the  'Status' and 'Status Detail' fields of the record defined.

            The information in these fields reports the current state of the process running on the MID server, including any errors that may have been encountered while relaying messages to the REST endpoint. This is a status view page only.

        2.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Consumers** if you want to create a new consumer record.  If the Consumer status indicates that the process has started, you should be able to inspect your endpoint to view the logs that have been relayed to it.  Additionally, you can view the logs on the MID Server to see if there are additional details about any errors that might be encountered. You can also enable Debug logging on the MID Server to get additional information if needed.
        3.  Select **Mark as complete** once done.
        **Note:** If you make any change in one of the Consumer records, it shows up on the Consumer Status view page. If you select a consumer record name on the Consumer Status list, the Consumer form for the selected record opens. You can then update the Name and Destination Configuration of the selected record.


**Parent Topic:**[MID server consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-mid-server-consumer.md)


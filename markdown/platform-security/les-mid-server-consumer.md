---
title: MID server consumer
description: Use guided setup to step through the initial configuration of LES for MID server consumer.Implement the following steps for a complete guided setup for MID Server consumers.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Configuring Log Export Service \(LES\), Log Export Service \(LES\), Platform Security]
---

# MID server consumer

Use guided setup to step through the initial configuration of LES for MID server consumer.

## Guided setup home page

The home page for guided setup contains an overview of configuration types for your guided setup. You can select your guided setup type and select **Continue** to open the guided setup steps and begin configuration.

![LES Guided setup for MID server consumer](../image/les-mid-server-setup.png)

All three setups on this page, Quick Start/Best Experience/Custom provide the same tasks and functionality. A dedicated MID Server is required to continuously stream logs from your instance to your log analytic system. The MID Server needs a one-time setup to establish a secure connection to the Hermes Messaging Service. Even if you have marked a task as completed, you can go back and uncheck it back to in-progress. To do so, first click on the **Edit** box on the upper right corner for the category. Then click on the **Edit** box for the task you want to uncheck. The **Mark as complete** box will be no longer marked.

## Guided setup categories page

The categories page contains an overview and descriptions of the categories and associated tasks. You can click either the drop down arrow to view information about the category or click **Start** to open the guided setup steps and begin configuration.

![Categories page for LES Guided setup](../image/les-mid-server-categories.png)

Complete the tasks under each category by following the setup instructions.

**Parent Topic:**[Configuring Log Export Service \(LES\)](les-configure.md)

**Related topics**  


[Kafka consumer](les-kafka-consumer.md#)

[Set up a secure connection to the Hermes Messaging Service for LES](../task/les-hermes-cert.md)

## Guided setup for MID Server consumers

Implement the following steps for a complete guided setup for MID Server consumers.

### Before you begin

Navigate to **Log Export Service \(LES\)** &gt; **MID Server Consumer** &gt; **Guided Setup**. Select the type of setup you wish to configure and click **Continue**.

**Note:** During the Log Export Service application installation, ServiceNow will provision the underlying Hermes Messaging Service infrastructure. Be aware that this process can take up to a couple of hours to complete from the time you request the Log Export Service application installation.

**Note:** Currently only one MID server consumer is supported.

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
    -   Instance Connectivity: Click **Run Test** to confirm the instance is able to send and receive messages.
    -   View Topics: Click the listed topic to retrieve the timestamp of the last known message.
    **Note:** You can access Hermes Diagnostics in the future to troubleshoot potential connectivity issues by returning to this step of the guided setup or by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Diagnostics**.

2.  Generate certificates for a secure connection to Hermes Messaging Service and pull log events from it.

    Setup secure connection to Hermes Messaging Service. See [Set up a secure connection to the Hermes Messaging Service for LES](../task/les-hermes-cert.md) for more information. You will need these certificates for authentication and authorization in the client which will pull the logs from Hermes.

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
        When successfully created, it will display the name of the Hermes topic to which that log source will be exported to. Write down the topic name, you will need it later when configuring your log consumer system. The Active field controls whether or not that log source is going to be exported or not. If you see errors, go back to the Check Hermes Diagnostics task and verify Hermes status.

    -   Validate Log Producer: Once you have created a Source to produce logs from, you can see live log records in the topic using **Hermes Messaging Service** &gt; **Hermes Topic Inspector**.
        1.  Select External Topics
        2.  Click List Topics
        3.  Select row with your topic from previous step \(listed in Sources\)
        4.  Adjust message start date if necessary
        5.  Click **View** to see a log message that was exported to the topic
4.  Install MID Server: You must install and configure a dedicated MID Server running Vancouver or later.

    Complete the following tasks to install the MID Server.

    -   Install dedicated MID Server: The MID Server that Log Export Service uses should be dedicated for only this purpose and should not be expected to run other processes. This is important to ensure timely delivery of exported log messages to your REST endpoint. You can install the new MID Server either by using the [Use MID Server guided setup](https://www.servicenow.com/docs/access?context=use-mid-server-guidedsetup&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) or by installing it manually. For the manual installation, follow the [Configure MID Server network connectivity](https://www.servicenow.com/docs/access?context=c_MIDServerConnectionPrerequisites&version=yokohama&pubname=yokohama-servicenow-platform&section=t_ConfigMIDSvrConnecPrereq&ft:locale=en-US) documentation first and then the [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) documentation after that.
    -   Validate MID Server: You must manually validate the MID Server after it is installed to enable it to execute automation tasks. To validate the MID Server you are dedicating for LES, see [Validate the MID Server](https://www.servicenow.com/docs/access?context=t_ValidateAMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
5.  Configure Log REST Push Destination: Setup the MID Server to be able to push logs to your log analytics system \(such as Splunk\).

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

        Follow these notes on how to obtain some of the above values

        -   &lt;password&gt; is the password you set for the keystore and truststore
        -   &lt;your\_path&gt; is the file path to the directory where you keep the keystore and truststore files you downloaded. The certificates need to be on the server where you are running MID
        -   &lt;instance\_name&gt; is the name of your ServiceNow instance. If you are not sure, you can find it in the sys\_properties table
        -   You can obtain the values for both mid.les.kafka.bootstrap.servers and mid.les.kafka.set2.bootstrap.servers from the Hermes Diagnostics page. Navigate to **Hermes Messaging Service** &gt; **Diagnostics** and copy the strings under Consumer Bootstrap 1 and Consumer Bootstrap 2 respectively.
    -   Configure Destination: Create a new Destination Configuration record, which defines the REST endpoint that this Extension will forward logs to.

        **Note:** admin or sn\_logstoanalytics.admin roles are required to complete this step.

        1.  Navigate to **Log Export Service \(LES\)** &gt; **Destination Configurations** 
        2.  Create a new configuration record
        3.  Specify the URL for your desired endpoint for the exported log sources
        4.  Search for or create new credentials to connect to your endpoint. When creating credentials for your endpoint, note that only the following credential types are valid with LES: Basic Auth and OAuth
        5.  Search for or create a new transform script. We ship with the prewritten script, **SplunkTransform** for Splunk
6.  Configure LOG Consumer: Follow these tasks to configure your MID Server Extension for Log Export Service purposes.

    -   Configure LES Consumer Context: In this step, you will update the LES Consumer record to execute on the dedicated MID server you just installed for the Log Export Service. Navigate to **MID Server** &gt; **Extensions** &gt; **LES Consumer Context** and update the LES Consumer record by setting the following fields:

        -   Click on 'LES Consumer' to open the MID Server context record
        -   Select Specific MID Server for the "Execute on" field
        -   Enter the name of the MID you validated in the previous step for the “MID Server” field
        Click **Update** to save.

        **Note:** We ship with a prebuilt context. Don't create a second one. This can have unintended consequences.

    -   Configure Consumer: Create a new Consumer record, which represents the process that’s part of the Log Export Service MID Server Extension. Navigate to **Log Export Service \(LES\)** &gt; **Consumers** and create a new configuration record specifying the Hermes topic to retrieve log messages from and the Destination to relay them to. When you select the **Consumers** module, it shows information about the consumer name and the destination configuration.
        1.  Create new Consumer record
        2.  Choose a source topic from the dropdown
        3.  Choose destination configuration
        4.  Start Consumer
    -   Verify MID Server integration: Navigate to  **Log Export Service \(LES\)** &gt; **Consumer Status** and view the  Status and Status Details fields of the record defined. The information in these fields reports the current state of the process running on the MID server, including any errors that may have been encountered while relaying messages to the REST endpoint. This is a status view page only. Navigate to **Log Export Service \(LES\)** &gt; **Consumers** if you want to create a new consumer record.  If the Consumer status indicates that the process has started, you should be able to inspect your endpoint to view the logs that have been relayed to it.  Additionally, you can view the logs on the MID Server to see if there are additional details about any errors that might be encountered. You can also enable Debug logging on the MID Server to get additional information if needed.

        **Note:** If you make any change in one of the Consumer records, it shows up on the Consumer Status view page. If you select a consumer record name on the Consumer Status list, the Consumer form for the selected record opens. You can then update the Name and Destination Configuration of the selected record.



---
title: Setting up a secure connection to Hermes
description: Configure SSL encryption for your Kafka consumers by generating an instance-signed certificate and configuring your Kafka client with SSL to securely connect to the managed Hermes cluster and consume data export results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/usage-insights/data-export-setup-hermes.html
release: zurich
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Bulk export of Usage Insights data via REST API, Use, Usage Insights, Platform Analytics]
---

# Setting up a secure connection to Hermes

Configure SSL encryption for your Kafka consumers by generating an instance-signed certificate and configuring your Kafka client with SSL to securely connect to the managed Hermes cluster and consume data export results.

## Before you begin

Role required: sn\_uxa\_data\_export.user assigned to the user or integration account that calls the API.

Verify network connectivity to Hermes and confirm you have a Kafka consumer environment that can connect to your managed Hermes cluster, with required network ports \(4100–4150 and 4200–4250\) open.

## Procedure

1.  Confirm that your Kafka consumer environment can reach the Hermes bootstrap servers on the required ports:

    Hermes uses two Kafka clusters for high availability:

    |Cluster|Bootstrap Servers|
    |-------|-----------------|
    |Cluster 1|`<instance>.service-now.com:4100,4101,4102,4103`|
    |Cluster 2|`<instance>.service-now.com:4200,4201,4202,4203`|

    Ask your network administrator to confirm that your firewall rules permit outbound connections to both port ranges \(4100–4150 and 4200–4250\).

2.  Generate the instance certificate

    1.  Open your ServiceNow® instance in a browser.

    2.  Use the search box or navigator to access &gt; &gt; **All** &gt; **Certificate Generator** &gt; **Instance PKI Certificate Generator**.

        The Instance PKI Certificate Generator page opens.

3.  Enter the following:

    1.  In the **Keystore password** field, enter a strong password that will be used for the certificates in your Kafka consumer.

    2.  Select **Generate**.

    The system generates a Keystore and Truststore file pair for your instance. Certificate generation may take a moment.

4.  Download the certificate files.

    After generation completes, the system provides download links for two files:

    -   Keystore file: Contains your instance's private key and certificate. Used to authenticate with Hermes.
    -   Truststore file: Contains the CA certificates needed to validate Hermes server certificate.
    Download both files and save them to a secure location on your local machine.

5.  Copy the certificate files to your Kafka consumer environment that will connect to Hermes.

    Transfer the keystore and truststore files from your local machine to each Kafka consumer client. For the full setup procedure and ACL configuration, see [Set up a secure connection to the Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/set-up-secure-connection-to-hermes.md).

    To learn more about Hermes messaging service, see [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/hermes-messaging-service.md).

    Example \(using SCP\):

    ```
    
    scp keystore.jks <user>@<consumer_host>:/path/to/certificates/
    scp truststore.jks <user>@<consumer_host>:/path/to/certificates/
              
    ```

    Record the full file paths; you will need them in the next step.

6.  Configure your Kafka consumer with SSL properties.

7.  Test the connection.

    Verify that your Kafka consumer can reach both Hermes clusters. Use a simple test consumer to connect to the bootstrap servers:

    ```
    
    kafka-console-consumer.sh \
      --bootstrap-servers <instance>.service-now.com:4100,4101,4102,4103 \
      --topic test \
      --consumer.config consumer.properties \
      --timeout-ms 5000
              
    ```

    Replace `<instance>` with your ServiceNow instance name. If the connection succeeds, the consumer establishes an SSL connection to Cluster 1.

    **Important:**

    If the connection fails, verify the following:

    -   The keystore and truststore files are in the correct paths on the consumer host.
    -   The keystore password is correct.
    -   Ports 4100–4150 and 4200–4250 are open on your firewall.
    -   The SSL properties in your consumer configuration are spelled correctly.
8.  Configure dual consumers for high availability.

    Since Hermes uses two clusters, create two consumer processes:

    1.  Consumer Process 1: Connects to bootstrap servers for Cluster 1 \(`<instance>.service-now.com:4100,4101,4102,4103`\)
    2.  Consumer Process 2: Connects to bootstrap servers for Cluster 2 \(`<instance>.service-now.com:4200,4201,4202,4203`\)
    Both processes must use the same Consumer Group ID. This confirms that messages are distributed across the two processes without duplication.

    Example configuration for Consumer Process 1:

    ```
    
    group.id=my_export_consumer
    bootstrap.servers=<instance>.service-now.com:4100,4101,4102,4103
    security.protocol=SSL
    ssl.truststore.location=/path/to/truststore.jks
    ssl.truststore.password=<keystore_password>
    ssl.keystore.location=/path/to/keystore.jks
    ssl.keystore.password=<keystore_password>
    ssl.key.password=<keystore_password>
              
    ```

    Example configuration for Consumer Process 2:

    ```
    
    group.id=my_export_consumer
    bootstrap.servers=<instance>.service-now.com:4200,4201,4202,4203
    security.protocol=SSL
    ssl.truststore.location=/path/to/truststore.jks
    ssl.truststore.password=<keystore_password>
    ssl.keystore.location=/path/to/keystore.jks
    ssl.keystore.password=<keystore_password>
    ssl.key.password=<keystore_password>
              
    ```

    **Note:** Both configurations use the same `group.id` value. This is intentional and required for high availability.

9.  Start consuming data export results as described in [Consuming data export results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/consuming-data-export-results.md).


## What to do next

Submit data export requests and consume results from the Kafka topic. See [Consuming data export results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/consuming-data-export-results.md) to learn more.

**Parent Topic:**[Bulk export of Usage Insights data via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/data-export-restapi.md)


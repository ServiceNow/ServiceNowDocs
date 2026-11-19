---
title: Set up the Docker spoke
description: Integrate the ServiceNow instance and Docker spoke by using the Docker Connection and Credential alias to authenticate ServiceNow requests.Add and configure a Docker connection to authenticate ServiceNow requests in Docker spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-docker-spoke.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Docker Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Docker spoke

Integrate the ServiceNow instance and Docker spoke by using the Docker Connection and Credential alias to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Docker spoke.
-   Role required: admin.

## Configure a connection for Docker spoke

Add and configure a Docker connection to authenticate ServiceNow requests in Docker spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **Docker** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Docker spoke, click **View Details**.

        \[Omitted image "docker-conn-template.png"\] Alt text: Connection template for Docker spoke

    -   To manage more than one Docker spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "config-docker-conn.png"\] Alt text: Configure connection for Docker spoke

5.  On the Configure Connection form, fill in the fields.

    | | |
    |---|---|
    |Connection Name|Name to uniquely identify the connection record. For example, `Docker connection`.|
    |Connection URL|IP address and port of the host server where Docker is installed. The format of the URL should be: `https://<ip_address>:<port_number>` or `https://<provider-domain-name>.com`.|
    |Repository Name|Name of the repository.|
    |User name|User name of your Docker account.|
    |Email|Email address used in your Docker account.|
    |Repository Type|Type of the Docker repository.|
    |Password|Password of your Docker account.|
    |Server Address|IP address of the host server where Docker is installed.|

    \[Omitted image "docker-spk-conf-temp.png"\] Alt text: Configure a connection for Docker spoke.

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.


---
title: Set up the Jenkins spoke
description: Integrate the ServiceNow instance and Jenkins using basic authentication to authenticate ServiceNow requests.Add and configure a Jenkins v2 connection to authenticate ServiceNow requests in Jenkins v2 spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Jenkins v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Jenkins spoke

Integrate the ServiceNow instance and Jenkins using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jenkins spoke.
-   Role required: admin.

## Configure a connection for Jenkins v2 spoke

Add and configure a Jenkins v2 connection to authenticate ServiceNow requests in Jenkins v2 spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Jenkins\_v2** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jenkins v2 spoke, click **View Details**.

        ![Connection template for Jenkins V2](../image/jenkins-v2-conn-template.png)

    -   To manage more than oneJenkins v2 spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Jenkins v2 connection configuration](../image/jenkins-v2-conn-config.png)

5.  On the Connection form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Jenkins v2 connection`.|
    |Connection URL|Base URL to connect to Jenkins. The format of URL should be: http://&lt;host\_ip\_address&gt;:&lt;port&gt;. For example, `http://198.51.100.24:8080`.|
    |User name|User name of your Jenkins account.|
    |Password|API token of your Jenkins account.|

    ![Configure connection for the Jenkins v2 spoke.](../image/jenkinsv2-conf-template.png)

6.  Click **Create Connection**.

7.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections**.

8.  Open the newly created connection record for Jenkins v2 spoke.

9.  From the **Advanced MID Server Configuration** tab, specify the MID Server settings.


### Result

The spoke connection is configured and ready to be used.


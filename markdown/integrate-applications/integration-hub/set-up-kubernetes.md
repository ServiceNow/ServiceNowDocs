---
title: Set up the Kubernetes spoke
description: Integrate the ServiceNow instance and Kubernetes using an API key and certificate to authenticate ServiceNow requests.Generate an access token and a certificate from your Kubernetes account for API key authentication.Upload the Kubernetes client certificate to your ServiceNow instance to authenticate API requests to the Kubernetes host machine.Add and configure the Kubernetes connection to authenticate ServiceNow requests in Kubernetes spoke.A system property prevents the Kubernetes spoke from processing Kubernetes responses. Set the com.glide.communications.httpclient.verify\_hostname system property to false to enable the integration.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Kubernetes Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Kubernetes spoke

Integrate the ServiceNow instance and Kubernetes using an API key and certificate to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Kubernetes spoke.
-   Role required: admin.

## Generate Kubernetes API token and certificate

Generate an access token and a certificate from your Kubernetes account for API key authentication.

### Before you begin

Kubernetes requirements:

-   Kubernetes account.
-   Role required: administrator with credentials on the host machine where Kubernetes is installed.

### About this task

Complete these steps from your Kubernetes host machine. See [Kubernetes documentation](https://kubernetes.io/docs) for instructions on generating your API token and client certificate.

### Procedure

1.  From your Kubernetes host machine, generate an access token to interact with Kubernetes APIs.

    This token does not expire.

2.  Copy and record the access token to create Credential records on your ServiceNow instance.

3.  Generate a client certificate to upload to your ServiceNow instance.


## Upload Kubernetes client certificate

Upload the Kubernetes client certificate to your ServiceNow instance to authenticate API requests to the Kubernetes host machine.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **Certificates**.

2.  Click **New**.

3.  Complete the form and enter the certificate in the **PEM Certificate** field.

    For more information about uploading certificates, see [Upload a certificate to an instance](https://www.servicenow.com/docs/access?context=t_UploadACertificateToAnInstance&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

4.  Click **Submit**.


## Configure a connection for the Kubernetes spoke

Add and configure the Kubernetes connection to authenticate ServiceNow requests in Kubernetes spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Kubernetes** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Kubernetes spoke, click **View Details**.

        ![Connection for the Kubernetes spoke.](../image/kubernetes-conf-temp.png)

    -   To manage more than one Kubernetes spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![First-time connection configuration.](../image/kubernetes-configure-temp.png)

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the Kubernetes connection alias record.|
    |Connection URL|IP address and port of the host machine where Kubernetes is installed.|
    |API Key|Token you obtained from Kubernetes in this format: `Bearer {access token}`.|

    ![Configure a connection for the Kubernetes spoke.](../image/kubernetes-temp.png)

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

## Turn off remote SSL host verification

A system property prevents the Kubernetes spoke from processing Kubernetes responses. Set the **com.glide.communications.httpclient.verify\_hostname** system property to false to enable the integration.

### Before you begin

Role required: admin.

### Procedure

1.  Enter `sys_properties.list` in the application navigator.

    The System Properties \[sys\_properties\] table opens.

2.  Search for the **com.glide.communications.httpclient.verify\_hostname** system property.

3.  Set the value to false.



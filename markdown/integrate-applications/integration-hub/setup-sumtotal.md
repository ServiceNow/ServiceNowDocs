---
title: Set up the SumTotal spoke
description: Integrate your ServiceNow instance with the SumTotal application host so the SumTotal spoke can perform actions on the SumTotal server.Integrate your ServiceNow instance with the SumTotal host by setting up the connection and credential record.Configure a connection to your SumTotal account. The SumTotal spoke connection and credential aliases use these connections to perform actions in the SumTotal application.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SumTotal Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SumTotal spoke

Integrate your ServiceNow instance with the SumTotal application host so the SumTotal spoke can perform actions on the SumTotal server.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SumTotal spoke.
-   Ensure that the SumTotal configuration template is selected in the SumTotal alias page.
-   Role required: admin.

## About this task

This task enables you to set up a connection and credential record so that your ServiceNow instance can integrate with the SumTotal host. The connection and credential alias record is a form that contains the SumTotal spoke configuration template and the connection and credential details to connect to the SumTotal host.

## Set up SumTotal spoke connection and credential record

Integrate your ServiceNow instance with the SumTotal host by setting up the connection and credential record.

### Before you begin

-   Role required: admin

### About this task

The image provides the flow of creating a connection and credential record.

![Flow to set up SumTotal connection and credential record.](../image/sumtotal-flow.png)

### Procedure

1.  Log in to the SumTotal host.

2.  Navigate to **ADMINISTRATION** &gt; **System** &gt; **Configuration** &gt; **Technical Configuration** &gt; **OAuth Configuration** &gt; **.**

3.  On the OAUTH CLIENTS page, click **+Add**.![Add button to add OAuth client in SumTotal.](../image/sumtotal-add.png)

4.  In the EDIT page, enter the details.![SumTotal OAuth client setup page.](../image/sumtotal-edit.png)

<table id="table_qj1_cxj_qwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Client Name

</td><td>

Custom name of the OAuth client.

</td></tr><tr><td>

Client Id

</td><td>

Unique ID of the OAuth client. You need it when setting up the connection and credential record in the ServiceNow instance.**Tip:** To copy the ID, click **COPY**.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret to set up the connection and credential record in the ServiceNow instance.**Tip:** To copy the ID, click **COPY**.

</td></tr><tr><td>

Allowed Grant Types

</td><td>

Select **Client Credentials**.

</td></tr><tr><td>

Settings

</td><td>

Select **Enabled**.

</td></tr><tr><td>

Access Token Lifetime \(minutes\)

</td><td>

The duration of the access token.

</td></tr><tr><td>

Scopes

</td><td>

Select **allapis**.

</td></tr><tr><td>

Redirect URI

</td><td>

URL of the location after the app is successfully authorized and granted an access token.

</td></tr></tbody>
</table>5.  Select **Submit**.


### Result

The SumTotal OAuth client is created.

## Configure a SumTotal spoke connection

Configure a connection to your SumTotal account. The SumTotal spoke connection and credential aliases use these connections to perform actions in the SumTotal application.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **SumTotal** and select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the SumTotal spoke, select**View Details**.

        ![Connection for the SumTotal spoke](../image/sumtotal-spoke-tile.png)

    -   To manage more than one Sumtotal spoke connection records, you should create child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you're configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

    ![Initial connection configuration](../image/sumtotal-spoke-configure.png)

5.  In the form, fill these details.

<table id="table_ory_gzd_w3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** The name is read-only.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to the SumTotal host.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Custom name of the OAuth entity.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID generated and copied from the SumTotal host.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret generated and copied from the SumTotal host.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth callback endpoint in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>    ![Configure a connection for the SumTotal spoke](../image/sumtotal-spoke-conf-connection.png)

6.  Select **Save and Get OAuth Token**.



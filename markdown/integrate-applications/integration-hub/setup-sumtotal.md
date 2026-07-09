---
title: Set up the SumTotal spoke
description: Integrate your ServiceNow instance with the SumTotal application host so the SumTotal spoke can perform actions on the SumTotal server.Integrate your ServiceNow instance with the SumTotal host by setting up the connection and credential record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-sumtotal.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
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

\[Omitted image "sumtotal-flow.png"\] Alt text: Flow to set up SumTotal connection and credential record.

### Procedure

1.  Log in to the SumTotal host.

2.  Navigate to **ADMINISTRATION** &gt; **System** &gt; **Configuration** &gt; **Technical Configuration** &gt; **OAuth Configuration** &gt; **.**

3.  On the OAUTH CLIENTS page, click **+Add**.\[Omitted image "sumtotal-add.png"\] Alt text: Add button to add OAuth client in SumTotal.

4.  In the EDIT page, enter the details.\[Omitted image "sumtotal-edit.png"\] Alt text: SumTotal OAuth client setup page.

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


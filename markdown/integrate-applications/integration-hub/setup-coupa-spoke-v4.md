---
title: Set up the Coupa spoke
description: Integrate the ServiceNow instance and Coupa by creating a custom OAuth application in Coupa to authenticate ServiceNow requests.Add and configure a Coupa connection to authenticate ServiceNow requests in Coupa spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/setup-coupa-spoke-v4.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Coupa Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Coupa spoke

Integrate the ServiceNow instance and Coupa by creating a custom OAuth application in Coupa to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Coupa spoke.

    **Note:** If you are upgrading to version 4.0.0 from the previous versions \(3.0.3 and earlier\) of the spoke, see this KB article: [KB0550471](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB1124171).

-   Role required: admin.

## Configure a connection for the Coupa spoke

Add and configure a Coupa connection to authenticate ServiceNow requests in Coupa spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **Coupa OAuth** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Coupa spoke, click **View Details**.

        \[Omitted image "coupa-con-config-template.png"\] Alt text: Connection alias for Coupa OAuth

    -   To manage more than one Coupa spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "coupa-conn-alias-config.png"\] Alt text: Coupa OAuth connection alias configuration

5.  On the form, fill in these fields:

<table id="table_tfv_3d5_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Name

</td><td>

Name to uniquely identify the connection. For example, `Coupa spoke connection`.

</td></tr><tr><td>

Connection URL

</td><td>

URL to make a connection to Coupa. -   For customer instances, use this format: `https://{organization_name}.coupahost.com`
-   For partner and demo instances, use this format: `https://{organization_name}.coupacloud.com`


</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

Name

</td><td>

Name to uniquely identify the credential. For example, `Coupa spoke credential`.

</td></tr><tr><td>

Token URL

</td><td>

URL used to generate OAuth token. Use this format: `https://<connection_url>/oauth2/token`

</td></tr><tr><td>

OAuth Client ID

</td><td>

Identifier \(Client ID\) generated in Coupa.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret \(Client Secret\) generated in Coupa.

</td></tr></tbody>
</table>    \[Omitted image "coupa-conf-temp.png"\] Alt text: Configure a connection for the Coupa spoke

6.  Click **Save and Get OAuth Token**.


### Result

The spoke connection is configured and ready to be used.


---
title: Set up the Coupa spoke
description: Integrate the ServiceNow instance and Coupa by creating a custom OAuth application in Coupa to authenticate ServiceNow requests.Add and configure a Coupa connection to authenticate ServiceNow requests in Coupa spoke.
locale: en-US
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

## Configure a connection for Coupa spoke

Add and configure a Coupa connection to authenticate ServiceNow requests in Coupa spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Locate the **Coupa OAuth** connection alias and click **View Details**.

    **Note:** Don't click **Add Connection**.

    ![Connection alias for Coupa OAuth](../image/coupa-con-config-template.png)

4.  Click **Edit** or if you are configuring the spoke for the first time, click **Configure**.

    ![Coupa OAuth connection alias configuration](../image/coupa-conn-alias-config.png)

5.  On the form, fill in the fields.

<table id="table_tfv_3d5_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \(Connection\)

</td><td>

Name to uniquely identify the connection. For example, `Coupa spoke connnection`.

</td></tr><tr><td>

Connection URL

</td><td>

URL to make a connection to Coupa. -   For customer instances, use this format: `https://{organization_name}.coupahost.com`
-   For partner and demo instances, use this format: `https://{organization_name}.coupacloud.com`


</td></tr><tr><td>

Name \(Credential\)

</td><td>

Name to uniquely identify the credential. For example, `Coupa spoke credential`.

</td></tr><tr><td>

Token URL

</td><td>

URL used to generate OAuth token. Use this format:`https://<connection_url>/oauth2/token`

</td></tr><tr><td>

OAuth Client ID

</td><td>

Identifier \(Client ID\) generated in Coupa.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret \(Client Secret\) generated in Coupa.

</td></tr></tbody>
</table>6.  Click **Configure and Get OAuth Token**.


### Result

The spoke connection is configured and ready to be used.


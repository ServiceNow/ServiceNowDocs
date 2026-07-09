---
title: Configure a connection for the UKG spoke
description: Add and configure a connection using the UKG spoke connection template in Flow Designer to authenticate ServiceNow requests to your UKG instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/configure-connection-ukg-spoke.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [UKG Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the UKG spoke

Add and configure a connection using the UKG spoke connection template in Flow Designer to authenticate ServiceNow requests to your UKG instance.

## Before you begin

Request an Integration Hub subscription.

Activate the UKG Spoke.

Role required: admin

**Note:** If you're updating from a previous version \(before version 3.3.0\) of the spoke, first you must remove the current connection record, credentials record, and Kronos user credentials. Then, you can set up the connection.

UKG has updated its authentication mechanism from legacy Auth to AuthN. If you're setting up the spoke for the first time, use AuthN to configure the spoke. If you have previously configured the spoke using the legacy Auth, you can continue using your existing configuration or migrate to AuthN.

**Note:** Verify that the application registry, connections, and credentials are within the application scope.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  Locate the **UKG connection** alias and select **View Details**.

    **Note:** Don't select **Add Connection**.

    \[Omitted image "ukg-spoke-conn-template.png"\] Alt text: Connection template for UKG spoke.

4.  Select **Edit**.

    If you're configuring the spoke for the first time, select **Configure**.\[Omitted image "ukg-spoke-config-conn.png"\] Alt text: Configure a connection for the UKG spoke

5.  On the form, fill in the fields.

<table id="table_olv_1my_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection record. For example, enter Kronos Conn.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the Kronos instance.

</td></tr><tr><td>

Realm

</td><td>

Realm of the Kronos instance.

</td></tr><tr><td>

Username

</td><td>

Username to log in to the user's account in Kronos.

</td></tr><tr><td>

Password

</td><td>

Password of the Kronos user account.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Unique name to identify the OAuth entity profile of the UKG spoke. For example, select `UKG OAuth entity`

.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID created during the application configuration in Kronos.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret created during the application configuration in Kronos.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. For example, `https://<Kronos-Instance>.com/api/authentication/access_token`.**Note:** If you're using the AuthN mechanism,enter `https://welcome-eval.ukg.net/oauth/token`.

</td></tr></tbody>
</table>6.  Select **Configure and Get OAuth Token**.

    A modal page displays to enter your Kronos credentials.

7.  Enter your Kronos username and password and select **Get OAuth Token**.

8.  If you're using the legacy Auth mechanism, you must provide user credentials.

    For more information, see [Provide Kronos user credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/create-user-cred-kronos.md).

9.  If you're using the legacy Auth mechanism, you must set the refresh token lifespan.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    2.  Open the record for the Kronos spoke.

    3.  On the form, navigate to the **Refresh Token Lifespan** field.

    4.  Enter `28800`.


## Result

Once your OAuth token has been successfully fetched, you can begin using your UKG spoke connection.


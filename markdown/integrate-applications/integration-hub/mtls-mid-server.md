---
title: Using the mTLS protocol with a MID Server
description: Make outbound REST and SOAP calls through a MID Server using mTLS. Store mTLS credential and certificate information on the instance, in a configuration file, or in an external vault. The MID Server retrieves the credential and certificate information and makes outbound REST and SOAP calls using the mTLS protocol.A MID Protocol Profile enables you to use the mTLS protocol with a MID Server. With a MID Protocol Profile, you can save your mTLS password and certificate information directly on the instance, in a configuration file, or in an external vault. The MID Server uses this information to make outbound REST and SOAP calls using mTLS.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage connections, Integration Hub, Workflow Data Fabric]
---

# Using the mTLS protocol with a MID Server

Make outbound REST and SOAP calls through a MID Server using mTLS. Store mTLS credential and certificate information on the instance, in a configuration file, or in an external vault. The MID Server retrieves the credential and certificate information and makes outbound REST and SOAP calls using the mTLS protocol.

Mutual authentication using the Transport Layer Security protocol \(mTLS\) is a secure, certificate-based, authentication scheme where the server and the client authenticate each other. With mTLS, the client presents a certificate or certificate chain to the server, and the server authenticates the client in the same way that the client authenticates the server \(mutual authentication\).

You can use mTLS with a MID Server by defining a MID Protocol Profile for connections that use mutual authentication. The MID Protocol Profile specifies the mTLS credential and certificate information required for the connection. The MID Server uses the information in the MID Protocol profile to retrieve the keystore, register protocols with the HTTP Client, and make outbound calls with mTLS.

**Note:** This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Create a MID Protocol Profile to use mTLS on a MID Server

A MID Protocol Profile enables you to use the mTLS protocol with a MID Server. With a MID Protocol Profile, you can save your mTLS password and certificate information directly on the instance, in a configuration file, or in an external vault. The MID Server uses this information to make outbound REST and SOAP calls using mTLS.

### Before you begin

-   Role required: admin or action\_designer.
-   Configure and start a MID Server. For more information, see [Configuring MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerConfiguration.md).

### About this task

This task is divided into four steps.

1.  Create a Connection &amp; Credential Alias. This task shows you how to create a basic Connection &amp; Credential alias. For detailed information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).
2.  Create a connection. This task shows you how to create a basic HTTP\(s\) connection. For more details, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).
3.  Create a MID Protocol Profile. The mTLS keystore and password may be stored on the instance \(in the MID Protocol Profile\), off the instance \(in the MID Server's `config.xml` file\), or in an external vault. ServiceNow supports CyberArk Password Vault for vault storage.
    -   If you're storing them on the instance, the keystore and password must also be on the MID Server.
    -   If you're storing them in the config.xml file, make sure you add the mTLS protocol parameters to the file before you configure the MID Protocol Profile. The `config.xml` is in the `/agent` directory, in the MID Server installation directory. See [MID Server parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-parameters.md).
    -   If you’re storing them in an external vault, make sure you set up your [CyberArk integration configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_CyberArkIntegrationConfiguration.md) before creating a MID Protocol Profile.
4.  Test your connection with a [REST step](../../flow-designer/reference/rest-request-action-designer.md). This step is optional.

### Procedure

1.  Create a Connection &amp; Credential alias.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credential Alias** and select **New**.

    2.  On the Connection &amp; Credential Aliases form, enter a name in the **Name** field, and confirm that **Connection type** is set to **HTTP**.

    3.  Select **Save**.

2.  Create a connection.

    1.  On the Connection &amp; Credential Aliases form, in the Connections tab, select **New**.

    2.  On the HTTP\(s\) Connection form, enter a **Name**.

    3.  Select **URL builder**, **Mutual authentication**, and **Use MID server**.

    4.  In the **MID protocol profile** field, use the magnifying glass icon to open the MID Protocol Profiles form and select **New**.

3.  Create a MID Protocol Profile.

    1.  On the form, fill in the fields.

<table id="table_yts_qtz_tbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protocol

</td><td>

Name for the protocol profile.

</td></tr><tr><td>

Keystore path

</td><td>

Path to the keystore on the MID host. The path can be absolute or relative.

 If you're storing mTLS credential information on the instance, enter your keystore path in this field. The keystore must also be on the MID Server.

 If you're storing mTLS credential information in the `config.xml` file for the MID Server, leave this field empty. Make sure you have added the mTLS protocol parameters to the `config.xml` file.

</td></tr><tr><td>

Applies to

</td><td>

Determines whether this credential applies to all MID Servers or only select ones. Select one of the following.-   **All MID servers**
-   **Specific MID servers**


</td></tr><tr><td>

MID servers

</td><td>

MID Servers this credential applies to.

 This field is only available when **Applies to** is **Specific MID servers**.

</td></tr><tr><td>

Default port

</td><td>

Default port for the protocol. Default value is 443.

</td></tr><tr><td>

External credential store

</td><td>

Option to use an external credential storage system.

 Select this option only if you’re using CyberArk to store your credential information.

 You may need to [configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md) to view this option.

</td></tr><tr><td>

Password

</td><td>

Password for the mTLS protocol. Stored in the database in encrypted form.If you're storing mTLS credential information on the instance, enter your password in this field. The password must also be on the MID Server.

If you're storing mTLS credential information in the `config.xml` file for the MID Server, leave this field empty. Make sure you have added the mTLS protocol parameters to the `config.xml` file.

If you’re storing mTLS credential information in CyberArk, enter the CyberArk ID for the credential.

</td></tr></tbody>
</table>    2.  Select **Submit**.

    3.  On the HTTP\(s\) Connection form, enter the target host for the connection in the **Host** field and **Save** the Connection form.

        On the HTTP\(s\) Connection form, the **Connection URL** field is filled in with the connection URL.

4.  Test your connection with a REST step.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  On the Workflow Studio landing page, select **New** &gt; **Action**.

    3.  Give your action a name in the **Action name** field and select **Build action**.

    4.  In the Action Outline section, select **REST**.

    5.  In the REST step, in the **Connection** field, select **Use Connection Alias** and in the **Connection Alias** field, select the connection alias you created.

        The **Base URL** field should be filled in with the connection URL created in step 2.

    6.  **Save** the REST step and select **Test**.

    7.  In the pop-up window, select **Run Test**.

        After the test runs, the EXECUTION DETAILS page displays. In the ACTION section, expand the steps section. Scroll down to the Step Output Data section to view the Status Code. It should be **200**, showing that you were able to make a successful call to the MID using mTLS.



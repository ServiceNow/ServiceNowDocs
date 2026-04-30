---
title: Create and test your credentials
description: Create and test the credentials that Discovery, Service Mapping, Cloud Management, and Orchestration require to access hardware and software in your network.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Create and test your credentials

Create and test the credentials that Discovery, Service Mapping, Cloud Management, and Orchestration require to access hardware and software in your network.

## Before you begin

Role required: admin

Review your security policy and options with your organization's security team.

## About this task

This task contains general procedures for creating credentials. Refer to the documentation for your credential type for details on specific fields and requirements.

<table id="table_sbq_p4k_1cb"><tbody><tr><td>

[Applicative credentials](../reference/applicative-creds.md)

</td><td>

[Basic authentication credentials](../reference/r_BasicAuthCredentialsForm.md)

</td><td>

[Chef server credentials](../reference/chef-server-creds.md)

</td></tr><tr><td>

[CIM credentials](../reference/r_CIMCredentialsForm.md#)

</td><td>

[Cloud credentials](../reference/r_CloudManagementCredentialsForm.md)

</td><td>

[Container image repository credentials](../reference/container-image-repo-credential.md)

</td></tr><tr><td>

[Infoblox credentials](../reference/infoblox-creds.md)

</td><td>

[JDBC credentials](../reference/r_JDBCCredentialsForm.md)

</td><td>

[JMS credentials](../reference/r_JMSCredentialsForm.md)

</td></tr><tr><td>

[OAuth 2.0 credentials](../reference/oauth-2-credentials.md)

</td><td>

[SAP credentials](../reference/r_SAPCredentials.md)

</td><td>

[SNMP credentials](../concept/c_SNMPCredentials.md#)

</td></tr><tr><td>

[SSH credentials](../reference/r_SSHCredentialsForm.md)

</td><td>

[VMware credentials](../reference/r_VMwareCredentialsForm.md)

</td><td>

[Windows credentials](../reference/r_WindowsCredentialsForm.md#)

</td></tr></tbody>
</table>**Note:** To improve security, limit the scope of credentials to a specific MID Server or schedule to avoid unnecessary credentials.

## Procedure

1.  Navigate to one of these modules:

    -   **Discovery** &gt; **Credentials**
    -   **Service Mapping** &gt; **Credentials**
    -   **Orchestration** &gt; **Credentials**
2.  Click **New**.

3.  On the Credentials page, click a link for the credential type and complete the form.

    Refer to the documentation for the credential type you selected for details.

    You can submit a credential record first and then test it later, or test the credential immediately before saving it.

    Credential testing is supported for these credential types:

    -   SSH private keys
    -   Windows
    -   SNMP v3
    -   VMware
    -   JDBC
    -   JMS
4.  Under **Related Links**, click **Test credential**.

    **Note:** Credentials are encrypted at all times during the test.

5.  Complete the fields in the Test Credential dialog box.

    ![Test credentials dialog box](../image/TestCredentials.png "Test credentials dialog box")

<table id="table_uxn_qln_25"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Credential type

</th></tr></thead><tbody><tr><td>

Target

</td><td>

Target host on which these credentials are run. This value must be an IP address for all credential types except VMware, which can be the host URL. You can not target any MID servers.**Note:** For JMS, this is the provider URL. The information in this URL tells JNDI how to find and access the JMS Provider. An example value for connecting to ActiveMQ V5.1, is `tcp://ipAddressOrHostName:61616`.

</td><td>

All

</td></tr><tr><td>

Port

</td><td>

Port on the target to use for this test. The system pre-populates this field with the default port for the selected credential type.

</td><td>

All

</td></tr><tr><td>

MID Server

</td><td>

MID Server to use for this test. You must use a Windows MID Server to test Windows credentials. Only **Up** and **Validated** MID Servers are available.

</td><td>

All

</td></tr><tr><td>

DB Type

</td><td>

Type of database on which to test these credentials.

</td><td>

JDBC

</td></tr><tr><td>

DB Name

</td><td>

Name of the database on which to test these credentials.

</td><td>

JDBC

</td></tr><tr><td>

Initial Context Factory

</td><td>

Name of the JNDI class that is used to create the InitialContext. Using this **Initial Context Factory**, various JMS objects, such as JMS Connection, are created. For example, to connect to ActiveMQ V5.10, \(JMS Provider\), the value in this field would be `org.apache.activemq.jndi.ActiveMQInitialContextFactory`

</td><td>

JMS

</td></tr></tbody>
</table>6.  Click **OK** to begin the test.

    An indicator appears, showing that the system is attempting to contact the target using the credentials you have provided. When the instance connects to the target it displays a success message. If the instance encounters a problem with the test inputs you have provided, it displays the appropriate error message. The following are some common error messages.

    -   Incorrect target or port number:

        ![TCP connection failure](../image/TestCredentialsTCPError.png "TCP connection failure")

    -   Incorrect user name or password:

        ![Authentication failure](../image/TestCredentialsPasswordError.png "Authentication failure")

    -   Incorrect MID Server for Windows credentials:

        ![MID Server error](../image/TestCredentialsWrongMID.png "MID Server error")

7.  Click **Retry** to open the test Credential dialog box and correct the input error.

8.  When your credentials test is successful, click **Submit** to save the record.

    **Important:** Testing credentials does not ensure that the credentials have the necessary privileges required for the intended Discovery or Orchestration workflow tasks.



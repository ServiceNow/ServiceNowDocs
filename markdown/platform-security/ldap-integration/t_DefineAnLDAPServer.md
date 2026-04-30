---
title: Define an LDAP server
description: Create a new LDAP server record in the instance.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Define an LDAP server

Create a new LDAP server record in the instance.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **Create New Server**.

2.  Fill in the form fields.

    ![Create a new LDAP server record](../image/CreateLDAPServer.png)

    In the **Server URL** field, the valid URLs of all servers appear separated by a space. Servers are first ordered by operational status, with servers that are **Up** listed first, then ordered by the **Order** value that you specify. The first server listed is the primary LDAP server. The others are redundant servers.

    **Note:** There is a slight delay between the change in the actual operational status and the display.

    Alternatively, you can add a redundant LDAP server by navigating to an existing LDAP server record and inserting a row in the LDAP Server URLs embedded list.

3.  Click **Submit**.

    **Note:** You can also modify an existing LDAP server record by navigating to **System LDAP** &gt; **LDAP Servers** and making the needed changes.

4.  Make changes to the fields as necessary.

    ![LDAP server form](../image/LDAP-ServerForm.png "LDAP server form")

<table id="table_LDAPConnectionProperties"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the server.

</td></tr><tr><td>

Active

</td><td>

Select this check box if the server is active.

</td></tr><tr><td>

LDAP Server URLs

</td><td>

Enter the URLs of the primary and backup LDAP servers. Servers are first ordered by operational status, with servers that are Up listed first, then ordered by the Order value that you specify. The first server listed is the primary LDAP server. The others are redundant servers.

</td></tr><tr><td>

Server URL

</td><td>

Enter the URL of the server. Configure the form to add this field if necessary. It is a calculated read-only field that shows the list of LDAP servers that you can also see in the **LDAP Server URLs** field, separated by a space, and ordered by operational status and the order values of the URLs.

</td></tr><tr><td>

Login distinguished name

</td><td>

Enter the distinguished name \(DN\) of the user authenticating the LDAP connection.To access an LDAP directory server, the username must be in the full distinguished name format: `servicenow@service-now.com`

</td></tr><tr><td>

Login password

</td><td>

Enter the server's password.

</td></tr><tr><td>

Starting search directory

</td><td>

Enter the relative distinguished name \(RDN\) of the default search directory. All queries to this LDAP server will start from this RDN.

</td></tr><tr><td>

MID Server

</td><td>

Select the MID Server you want to use to connect to the LDAP server. Using a MID Server to establish an LDAP connection prevents you from having to expose the LDAP server to external network traffic. It also eliminates the need to establish a VPN tunnel between your LDAP server and ServiceNow data centers.

 **Note:**

-   The MID Server user must have the user\_admin role in order to be able to read LDAP server configuration records.
-   The following are not available with the MID Server:
    -   LDAP authentication
    -   SSL connection


</td></tr><tr><td>

Connect timeout

</td><td>

If a MID Server is configured, the connection times out after 10 seconds, regardless of this setting. This setting is hard-coded and cannot be altered.

</td></tr><tr><td>

Read timeout

</td><td>

Specify the number of seconds the integration has to read LDAP data. The integration stops reading LDAP data after the connection exceeds the read timeout. If you enable an SSL connection, you can also set a read timeout value with the**com.glide.ssl.read.timeout**system property. If you enter timeout values for both this field and the system property, the lowest timeout value takes precedence.

</td></tr><tr><td>

SSL

</td><td>

Select this check box to require the LDAP server to make an SSL-encrypted connection. If you selected a MID Server, this field is not available.

 If you use an LDAPS integration and the default SSL port is 636, no further configuration is necessary; SSL is automatically enabled. If the LDAPS integration uses another SSL port, define the alternate SSL connection properties.

 **Note:**

Be sure a network administrator configures the local firewall to allow the application server to access the LDAP server. If the LDAP server is located within an internal network, the firewall forwards \(or NATs\) the application server's IP address through the firewall on the correct port.

</td></tr><tr><td>

Listener

</td><td>

Select this check box to enable the integration to periodically poll Microsoft Active Directory servers or LDAP servers that support persistent search request control. Additionally, if you selected a MID Server, the listener functionality is available for that MID Server. See [Enable an LDAP listener and set system properties](t_EnableAListener.md) for more information.

</td></tr><tr><td>

Listen interval \(timeout value\)

</td><td>

Specify the listener timeout value in the number of minutes that the integration listens for LDAP data with every connection. The integration stops listening for LDAP data after the connection exceeds the listen interval.

</td></tr><tr><td>

Paging

</td><td>

Select this check box to have the LDAP server split up LDAP attribute data into multiple result sets rather than submit multiple queries.

</td></tr></tbody>
</table>    **Note:** If you provide an LDAP password, the integration performs a Simple Bind operation. If you do not provide an LDAP password, the LDAP server must allow anonymous login or the integration cannot bind to the LDAP server.


## Result

When an LDAP Server record is set to active, the system automatically tests every connection to validate it.

Validations include:

-   The LDAP server is accessible at the provided URL and port
-   The LDAP server URL is properly formatted
-   The login credentials are valid

Starting with the Fuji release, the system displays colored dots next to each server URL:

|Color|Description|
|-----|-----------|
|Green|The server if active and operational.|
|Gray|The server is neither active nor operational.|
|Red|The server is active but not operational.|

![](../image/Ldap_server_validations_dots.png "LDAP server connection status")


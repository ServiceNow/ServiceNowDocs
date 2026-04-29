---
title: Applicative credentials
description: Some applications require credentials in addition to the credentials the that host machine requires. Credentials required to access these applications are referred to as applicative credentials.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# Applicative credentials

Some applications require credentials in addition to the credentials the that host machine requires. Credentials required to access these applications are referred to as applicative credentials.

A typical credential contains a user name and a password for logging in to a device or application. While most applications require only one credential for accessing them, sometimes hosts and applications have separate credentials for extra security. For example, ABAP SAP Central Services \(ASCS\) requires applicative credentials in addition to the SSH or Windows host credentials for the server that hosts ASCS.

**Note:** ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

As with host credentials, you assign applicative credentials to MID Servers.

You create applicative credentials per CI type, for example, the CI type for ASCS is SAP ASCS Application \[cmdb\_ci\_appl\_sap\_ascs\]. The preconfigured pattern for discovering CIs belonging to this CI type contains commands that require a MID Server to use the applicative credential for this CI type. If there’s more than one credential configured for this CI type, the MID Server tries using these credentials in the order you define until it finds the credential that fits.

Check the Discovery requirements information in the ServiceNow documentation to determine if you need to configure applicative credentials for specific application CIs. There’s no need to configure applicative credentials, if Discovery prerequisites don’t mention it.

<table id="table_glz_wgm_ht"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Name of the credential. Use a descriptive name like Oracle DB or London Oracle DB \(for an Oracle database\). Don’t use spaces or special characters for the credential name.

</td></tr><tr><td>

**Active**

</td><td>

Select the check box to use the credential.

</td></tr><tr><td>

**User name**

</td><td>

Enter the actual user name of the applicative credential.

</td></tr><tr><td>

**Password**

</td><td>

Enter the actual password of the applicative credential. Don’t use spaces or special characters for the credential name.

</td></tr><tr><td>

**CI type**

</td><td>

Select a CI type to which the CI belongs.

</td></tr><tr><td>

Credential Alias

</td><td>

Create an alias to assign specific credentials for specific discovery schedules. When assigning an alias, you must identify the table name for the CI type whose applicative credentials the application uses. Applications may use applicative credentials of a CI type different from their own. For a specific application, see the list for the appropriate table:-   ABAP SAP Central Services \(ASCS\): cmdb\_ci\_appl\_sap\_ascs
-   IBM Security Access Manager appliance: cmdb\_ci\_app\_server\_webseal
-   SAP Central Instance: cmdb\_ci\_appl\_sap\_ascs
-   SAP Central Services \(SCS\): cmdb\_ci\_appl\_sap\_ascs
-   SAP Evaluated Receipt Settlement \(ERS\): cmdb\_ci\_appl\_sap\_ascs
-   SAP Java Cluster: cmdb\_ci\_appl\_sap\_ascs
-   SAP NetWeaver Dialog Instance: cmdb\_ci\_appl\_sap\_ascs
-   Microsoft Exchange Mailbox \(for Microsoft Exchange\): cmdb\_ci\_exchange\_mailbox
-   Microsoft SQL Database: cmdb\_ci\_db\_mssql\_instance
-   MySQL Server: cmdb\_ci\_db\_mysql\_instance
-   Oracle Advanced Queue Queue: cmdb\_ci\_db\_ora\_instance
-   Oracle Database: cmdb\_ci\_db\_ora\_instance
-   Oracle E-Business Suite: cmdb\_ci\_db\_ora\_instance
-   Oracle WebLogic Module: cmdb\_ci\_app\_server\_weblogic
-   Tibco Enterprise Message Service \(EMS\): cmdb\_ci\_appl\_tibco\_message

</td></tr><tr><td>

**Applies to**

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

**Order**

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>
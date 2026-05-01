---
title: Explore credentials, connections, and aliases
description: All application integrations in the ServiceNow AI Platform use connections, credentials, and aliases to enable applications to access resources.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 4
breadcrumb: [Connections and Credentials, Access Management]
---

# Explore credentials, connections, and aliases

All application integrations in the ServiceNow AI Platform use connections, credentials, and aliases to enable applications to access resources.

Before you can execute an application integration in the ServiceNow AI Platform, you must create and configure connection information, corresponding credentials, and add an alias. To understand how ServiceNow defines these terms:

-   **Connection**

    A connection is an integration with a system, such as an IP address or endpoint with protocols. It contains specific details, such as database particulars, when integrating with a database.

-   **Credential**

    A credential is the authentication data required to make the connection, such as an ID and password.

-   **Alias**

    An alias is a naming convention, or tag, that ties to a set of connections or credentials on your instance. An alias contains the necessary connection and credential information to make an application integration. Rather than enter that information every time you integrate, you can use an alias. For example, you can designate an alias to house your QA, development, and production credentials for the same application integration. The alias resolves the application integration for each environment.

    The ServiceNow AI Platform distinguishes different types of aliases:

    -   **Credential Alias**

        This alias associates to credential data only, and resolves during runtime.

    -   **Connection and Credential Alias**

        This alias associates to connection information and the credential data required to complete the integration, and resolves during runtime.


Within connection and credential aliases, you can also create additional aliases called child aliases. Child aliases allow you to create multiple connections within the same application integration. When you create a child alias, the alias you created it under becomes a parent alias. While child aliases inherit properties from their parent alias, child aliases carry their own connection and credential information.

## Benefits to using Connections, Credentials, and Aliases

-   Central location to store and manage credentials to an external service
-   Define once and reuse for multiple platform features
-   Minimize configuration of other platform features
-   Allow non-administrators to use predefined connections and credentials
-   Increased security

## Features using Connections, Credentials, and Aliases

The following features use connections, credentials, and aliases:

-   Flow Designer
-   IntegrationHub
-   Cloud Management
-   Discovery
-   Orchestration
-   Service Mapping

You can set up aliases on the ServiceNow AI Platform in one of two ways:

-   Using the Connections and Credentials module. See [Create a Connection &amp; Credential alias](../task/connection-alias.md).
-   In the Connections dashboard of Integration Hub. See [Add a connection](https://www.servicenow.com/docs/access?context=dashboard-add-connection&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

    **Note:** Integration Hub requires a separate subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).


## Credential synchronization on MID Servers

Each MID Serverin your network synchronized with the instance keeps a copy of every credential that you create. The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services. This synchronization speeds up the reading of credentials when applications like Discovery or Service Mapping need to access multiple devices on the network. The MID Servers synchronize when they find a **credentials\_reload** job in the ECC Queue. The reload job instructs the MID Server to make a SOAP call to the instance to get the entire list of credentials in the Credentials \[discovery\_credentials\] table, including all the field values. To learn more, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The SOAP response that your instance sends to each MID Server also includes custom fields that you added to any credential form that you customized. If you added reference fields, the data in the referenced table is also sent as part of the SOAP response. This can lead to performance issues when credential synchronization occurs with multiple MID Servers. To control this, manually add these properties to the System Properties \[sys\_properties\] table:

**Note:** To change the values in these properties, add them to the System Properties \[sys\_properties\] table. If you do not add them, the system uses the default value.

<table id="table_swn_mwj_4db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`com.snc.credentials_user_fields`

</td><td>

Includes all customized fields in credential sync. Set this property to false if you do not want to include the fields that you added to credential forms.-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

`com.snc.credentials_recursion_depth`

</td><td>

Defines the number of tables to traverse when the credential-sync mechanism collects fields from reference tables. Lower this number if you are experiencing performance issues and you have customized credential forms that include reference fields to tables that also have reference fields.-   **Type**: integer
-   **Default value**: 3

</td></tr></tbody>
</table>-   **[Scope protections for Credentials and Connections](scope-protections-connections-credentials.md)**  
You can classify certain types of Connection &amp; Credential records as belonging to a scope, and extend scope protections to them. These scope policies protect records you create in a table, and prevent interactions with records that are private to another scope.
-   **[Domain separation and Credentials and Connections](domain-separation-credentials_conn.md)**  
Domain separation is supported in Credentials and Connections. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Connection &amp; Credential configuration templates](spoke-configuration-template.md)**  
Enable users with the admin and flow\_designer roles to set up spoke integrations with third-party systems using a single, customizable form.

**Parent Topic:**[Connections and Credentials](../reference/r-credentials.md)


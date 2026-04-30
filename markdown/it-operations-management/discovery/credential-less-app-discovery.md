---
title: Credential-less Application Discovery
description: Credential-less Application Discovery attempts to identify an application service actively listening on a specific port at a given IP address.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Credential-less Discovery with Nmap, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Credential-less Application Discovery

Credential-less Application Discovery attempts to identify an application service actively listening on a specific port at a given IP address.

## The application discovery pattern

Service Mapping launches the Credentialless Discovery Application pattern when all credential-based port classification steps fail. The pattern executes an Nmap command on a Windows MID Server with Nmap installed, that is configured to perform application/version detection against a specific remote host IP address and port. If the port being scanned by Nmap is open, the pattern executes the CredentialLessApplicationClassNameMapper MID Server script include, which maps the service product, service name, and any extra information supplied by Nmap to a supported ServiceNow application table. If the script can map the returned product to an appropriate table derived from the base Application \[cmdb\_ci\_appl\] table, the script passes this information to the pattern. The pattern passes the match to the Discovery identifier for eventual CI creation or reconciliation. If the information returned by Nmap does not match any derived table, then the instance uses the base Application \[cmdb\_ci\_appl\] table to create the CI.

**Important:** To allow the Credentialless Discovery Application pattern to launch, ensure that the **mid.discovery.credentialless.enable** system property is set to **true**. To disable, ensure this property is set to **false**.

## Example scan

This information was returned by an Nmap Application/Version Detection port scan on a Linux test system and illustrates the type of application data Nmap scans can return.

|Information|Port|
|-----------|----|
|Port state|open|
|Service name|ssh|
|Service product|OpenSSH|
|Extra service information|Protocol 2.0|

## Default application mappings

The CredentialLessApplicationClassNameMapper MID Server script include is configured with a subset of the most common application tables available for Discovery and Service Mapping. A user with the agent\_admin role can edit this script include to add additional CI tables that credential-less application Discovery can use for mapping to a derived application CI class.

Shown in this table are examples of close matches returned by Nmap on a test system that [CMDB Identification and Reconciliation](https://www.servicenow.com/docs/access?context=c_CMDBIdentifyandReconcile&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) was able to resolve into defined products. In many cases, the service name returned by Nmap was not needed to determine a match. Service names that appear in the table were required to determine a match.

Products returned by Nmap that cannot be resolved into defined Discovery products use the following naming format: **&lt;serviceProduct&gt;:&lt;serviceExtrainfo&gt;:&lt;serviceName&gt;**. If any value in this string is null, it is dropped from the name.

-   **serviceProduct**: Service product information returned by Nmap.
-   **serviceExtrainfo**: Any additional information that Nmap returns about the application that might help identify it, such as protocol information.
-   **serviceName**: The installed name of the service or daemon of the product.

|Nmap response|Script response - Identifier input|
|Service product|Service name|Service extra information|Discovered product|CI application table|
|-------------|----------------------------------|
|---------------|------------|-------------------------|------------------|--------------------|
|Apache Tomcat/Coyote JSP engine 1.1|N/A|NULL|Tomcat|cmdb\_ci\_app\_server\_tomcat|
|Apache httpd 2.2.10 \(\(Linux/SUSE\)\)|N/A|NULL|Apache Web Server|cmdb\_ci\_apache\_web\_server|
|IBM HTTP Server|N/A|Derived from Apache|Apache Web Server|cmdb\_ci\_apache\_web\_server|
|IBM DB2 Database Server \(QDB2/LINUX\)|N/A|NULL|DB2 Instance|cmdb\_ci\_db\_db2\_instance|
|Microsoft Exchange smtpd|smtp|NULL|Exchange Client Access Server|cmdb\_ci\_exchange\_cas|
|Microsoft Exchange 2010 log copier|msexchange-logcopier|NULL|Exchange Mailbox|cmdb\_ci\_exchange\_mailbox\_server|
|JBoss service httpd|N/A|NULL|JBoss|cmdb\_ci\_app\_server\_jboss|
|Microsoft IIS httpd 6.0|N/A|NULL|Microsoft iis Web Server|cmdb\_ci\_microsoft\_iis\_web\_server|
|Microsoft SQL Server 2005 9.00.4035; SP3|N/A|NULL|Microsoft SQL Server|cmdb\_ci\_db\_mssql\_instance|
|MongoDB 2.5.1|N/A|NULL|MongoDB Instance|cmdb\_ci\_db\_mongodb\_instance|
|MySQL 5.5.51|N/A|NULL|MySQL Instance|cmdb\_ci\_db\_mysql\_instance|
|nginx 1.4.6 \(Ubuntu\)|N/A|NULL|Nginx Web Server|cmdb\_ci\_nginx\_web\_server|
|PostgreSQL DB|N/A|NULL|PostgreSQL Instance|cmdb\_ci\_db\_postgresql\_instance|
|Oracle WebLogic Server|N/A|NULL|Weblogic|cmdb\_ci\_app\_server\_weblogic|
|IBM WebSphere MQ 6.0|N/A|NULL|IBM WebSphere MQ|cmdb\_ci\_appl\_ibm\_wmq|
|IBM WebSphere Application Server 6.1|N/A|NULL|IBM Websphere|cmdb\_ci\_app\_server\_websphere|
|OpenSSH : ssh|N/A|NULL|OpenSSH|cmdb\_ci\_appl|
|Oracle Instance|N/A|NULL|Oracle Database|cmdb\_ci\_db\_ora\_instance|
|Oracle Instance|N/A|NULL|Oracle TNS Listener|cmdb\_ci\_db\_ora\_instance|
|product-A|service-B|NULL|product-A:service-B|cmdb\_ci\_appl|
|product-A|service-B|extrainfo-C|product-A:extrainfo-C:service-B|cmdb\_ci\_appl|

## Examples of applications not uniquely matched

In this example, the information returned by Nmap does not match any derived table, and the instance must use the base Application \[cmdb\_ci\_appl\] table to create the CI.

<table id="table_zpv_rzn_5bb"><thead><tr><th rowspan="2" align="center">

Scanned application

</th><th colspan="3" align="center">

Nmap response

</th><th colspan="2" align="center">

Script response - identifier input

</th></tr><tr><th>

Service product

</th><th>

Service name

</th><th>

Service extra information

</th><th>

Discovered product

</th><th>

CI application table

</th></tr></thead><tbody><tr><td>

ExchangeHub

</td><td>

Microsoft Windows RPC

</td><td>

msrpc

</td><td>

null

</td><td>

Microsoft Windows RPC:msrpc

</td><td>

cmdb\_ci\_appl

</td></tr><tr><td>

HAProxy Load Balancer

</td><td>

IBM HTTP Server \(Derived from Apache\)

</td><td>

http

</td><td>

null

</td><td>

IBM HTTP Server \(Derived from Apache\):http

</td><td>

cmdb\_ci\_appl

</td></tr><tr><td>

SharePoint

</td><td>

Oracle Database

</td><td>

http

</td><td>

null

</td><td>

Oracle Database:http

</td><td>

cmdb\_ci\_appl

</td></tr><tr><td>

SharePoint

</td><td>

Oracle Instance

</td><td>

N/A

</td><td>

null

</td><td>

Oracle Database

</td><td>

cmdb\_ci\_appl

</td></tr></tbody>
</table>## Application identification

The Discovery - IP Based \[com.snc.discovery.ip\_based\] plugin adds an identifier to the Application Rule for the Application \[cmdb\_ci\_appl\] table that matches on sys\_class\_name and cl\_port for Nmap scans.

![Nmap identifier for the Application Rule](../image/NmapIdentifier.png "Nmap identifier for the Application Rule")

**Parent Topic:**[Credential-less Discovery with Nmap](../concept/nmap-credential-less-discovery.md)


---
title: Entry point attributes
description: Service Mapping comes with a wide range of preconfigured entry point types that cover many commonly used applications. Check attribute definitions to correctly add entry points to your application services.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Entry point attributes

Service Mapping comes with a wide range of preconfigured entry point types that cover many commonly used applications. Check attribute definitions to correctly add entry points to your application services.

An entry point is a point where clients access a service instance. Entry points are stored as records in the Endpoint \[cmdb\_ci\_endpoint\] tables.

There are some general attributes shared by almost all entry point types as described in the following table:

<table id="table_wp1_4jd_tt"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Host/Hostname/Host Name

</td><td>

The value of the target server on which the service is running. This value can contain a real host name, alias, IP, or VIP.**Important:** Do not use a localhost or loopback address \(127.0.0.1\) for discovery and mapping.

</td></tr><tr><td>

Port

</td><td>

The port number of the service that you want to discover.

</td></tr><tr><td>

Name

</td><td>

The name of the service that you want to discover.

</td></tr><tr><td>

URL

</td><td>

The URL of the service that you want to discover in the following format: http\(s\)://\(address\):\(port\). If you do not provide the port, the system uses the default port 443.

</td></tr><tr><td>

Network location

</td><td>

The location of the applicable subnetwork.**Note:** This field is optional and visible only if Network location is enabled.

</td></tr></tbody>
</table>To configure entry points for subnetworks, see [Fine-tune Service Mapping with MID affinity and IP reuse](../concept/network-location-mid-affinity-td-discovery.md).

There are some attributes which you configure differently depending on what entry point they relate to, as described in the following table:

|Entry point type|Attribute|Description|
|----------------|---------|-----------|
|Active Directory Domain to Domain Controllers Endpoint|Domain name|The AD domain name.|
|Forest name|The AD forest name.|
|Domain controller distinguished name|The distinguished name of the AD domain controller. Usually it is a compilation of the domain controller name and the hostname.|
|Domain Controller Name|The AD Domain Controller name.|
|Active Directory Forest Endpoint|Forest name|The AD Forest name.|
|AWS Resource Name Endpoint|ARN|The Amazon Resource name.|
|Application to Storage Endpoint|File in use by application|The path to the file used by an application. For example, mssql uses c:\\applications\\mssql\\users.db. Service Mapping populates this attribute using patterns.|
|File system name|The file system containing the file used by an application. For example, if a mssql uses c:\\applications\\mssql\\users.db, the value is "c:".|
|Connected array ids|N/A|
|Advanced Queue|Scheme|The name of the Oracle DB table where the Queue is defined.|
|Instance|The name of the Oracle instance.|
|Queue|The name of the queue.|
|BizTalk Connection|Adapter address|The connect string to the Biztalk adapter. It can be a path, URL, host, or port.|
|Transport Type|The type of the Biztalk adapter. For example a URL, file SOAP, or FTP.|
|CRM Component|Role|The role of the CRM. Leave empty if unknown.|
|DB2 UDB|Instance|The name of the DB2 instance.|
|DCTM Connection to broker|Repository|The name of documentation repository.|
|DCTM Index Agent Connection|Instance Name|The name of the instance of Documentation Index Agent.|
|Repository|The name of the documentation repository.|
|DCTM Job Processor|Repository|The name of documentation repository.|
|Citrix Delivery Controller|Farm Type|The type of the Delivery Controller.|
|Controller Name|The name of the Citrix Controller.|
|DocBase Connection|Repository|The name of the documentation repository.|
|EJB|JNDI Name|The jndi name of target EJB.|
|EMS|Queue|The name of Tibco EMS queue.|
|EMS JNDI|JNDI Name|The jndi name of Tibco EMS connection.|
|F5 Mirror|Origin IP|The IP address of the second pair F5 device.|
|Origin host|The hostname of the second pair F5 device.|
|Fast Search|Repository|The name of repository of fast search.|
|ITAM Asset Center|Folder|The path to configuration folder.|
|JMS Flow|JMS project|The name of Tibco project.|
|JMS Flow|Queue Name|The name of Tibco EMS queue.|
|JMS Server|Queue Name|The name of the queue defined on JMS server.|
|HTTP Listener to WMB Dependency|Directory|The path to the WMB installation directory.|
|LDAP|Protocol|The protocol name: `ldap`.|
|Type|The LDAP query type. This attribute is not supported. Leave empty.|
|MQ|Queue Name|The name of the IBM MQ Queue.|
|MQ Flow|Source IP|The IP of the source IP create connection to MQ.|
|Queue Name|The name of IBM MQ Queue.|
|MQ Cross-memory|Command line|The command line of MQ.|
|Queue Name|The name of IBM MQ Queue.|
|MSMQ Flow|Queue Name|The name of MS MQ queue.|
|MS SQL Server|Instance|The name of MSSQL instance.|
|MySQL Cluster Data Node|Node ID|The ID of MySQL instance.|
|Node group|The group of MySQL instance|
|MySQL Cluster MGM|Node ID|The ID of MySQL instance.|
|MySQL Secondary Server|Config IP|The IP of the MySQL Config server.|
|Config Port|The port of the MySQL Config server.|
|Oracle DB|Schema|The name of table on the Oracle instance.|
|Instance|The name of oracle instance.|
|Oracle ESB Connection|Adapter data|The content of the adapter.|
|Adapter Type|The type of the adapter.|
|Oracle RAC DB|Service Name|The name of the Oracle RAC service.|
|PostgreSQL DB|Instance|The name of the PostgreSQL DB.|
|Remote TCP Cross-memory|Source\_ IP|The IP of the source host process.|
|Source Port|The port of source process.|
|SAP APP EP|SID|The SAP instance SID name.|
|Instance|The instance name.|
|SAP BO Servers|Server name|The name of the BO server.|
|Sharepoint connection|Origin URL|The URL of the IIS.|
|SSAS|Project|The name of the SSAS project \(can be empty\).|
|SSAS for MSSQL|Instance|The name of the MSSQL instance.|
|Client Type|The type of the client connected.|
|SSIS|Job|The name of SSIS job can be empty.|
|SSIS file|Package file name|The name of the package file.|
|SSIS for MSSQL|Instance|The name of the MSSQL instance.|
|Client Type|The type of the client connected.|
|StoreParameters Components|Front|The parameters of the Citrix application.|
|Farm|The farm host the Citrix application.|
|Application name|The Citrix application name.|
|XenApp or Presentation Server|Type|The type of the Citrix application.|
|Farm|The farm host the Citrix application.|
|Icon path|The logic path of the Citrix application.|
|Argument|The parameters of Citrix application.|
|Path|The logic path of the Citrix application.|
|Exec|The EXE name of Citrix application.|
|IP Address|The IP of host is member of Citrix farm.|
|Sybase|Instance|The name of Sybase instance.|
|Tibco Conf File|Configuration File|The path to Tibco BW project.|
|Process Name|The name of Tibco BW main process.|
|Queue Port|The port of the queue used by the Tibco process.|
|Config IP|The IP of the source of the queue.|
|Tibco BW|Process name|The name of Tibco BW main process.|
|Tibco File Listener|File|The path of the file is used by Tibco BW for integration.|
|Tibco Hawk|Configuration directory|The path to Tibco Hawk Configuration folder.|
|WMB Dependency|Command line|The command line of the WMB.|
|XenApp or Presentation Server Components|Farm|The farm host the Citrix application.|
|Icon path|The logic path of the Citrix application.|

**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

**Related topics**  


[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

[Create entry point types for Service Mapping](../task/t_CreateEntryPoint.md)


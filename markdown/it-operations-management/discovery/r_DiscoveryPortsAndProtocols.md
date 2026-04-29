---
title: Shazzam probe, port probes, and protocols
description: Port scanning is the first step in the discovery process. The Shazzam probe performs port scanning, regardless of whether you use patterns for horizontal discovery. The following table lists the known ports and protocols used by Discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Port probes, List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Shazzam probe, port probes, and protocols

Port scanning is the first step in the discovery process. The Shazzam probe performs port scanning, regardless of whether you use patterns for horizontal discovery. The following table lists the known ports and protocols used by Discovery.

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.

Several port probes are available in the base system. Each port probe uses an IP Service, which is a record that tells Discovery which port to use for a specific protocol. Review this table before you block any ports with a firewall.

**Important:** Make sure that you do not block any ports that Discovery needs.

<table id="table_eqr_tv5_d2b"><thead><tr><th>

Default port probe name

</th><th>

Default classification

</th><th>

Default IP Service and port

</th></tr></thead><tbody><tr><td>

dns

</td><td>

Process Classification \[discovery\_classy\_proc\]

</td><td>

dns \(port 53\)

</td></tr><tr><td>

http

</td><td>

HTTP Classification \[discovery\_classy\_http\]

</td><td>

http \(port 80\) and https \(port 443\)

</td></tr><tr><td>

ip\_phone

</td><td>

SNMP Classification \[discovery\_classy\_snmp\]

</td><td>

sip \(port 5060\)

</td></tr><tr><td>

osx

</td><td>

Scan Results Application Classifier \[discovery\_classy\_scan\_app\]

</td><td>

afp \(port 548\)

</td></tr><tr><td>

printer

</td><td>

Scan Results Application Classifier \[discovery\_classy\_scan\_app\]

</td><td>

hp-pdl-datastr \(port 9100\) and printer \(port 515\)

</td></tr><tr><td>

slp

</td><td>

Process Classification \[discovery\_classy\_proc\]

</td><td>

slp \(port 427\)

</td></tr><tr><td>

snmp

</td><td>

SNMP Classification \[discovery\_classy\_snmp\]

</td><td>

snmp \(port 161\)

</td></tr><tr><td>

ssh

</td><td>

UNIX Classification \[discovery\_classy\_unix\]

</td><td>

ssh \(port 22\)

</td></tr><tr><td>

tls\_ssl\_certs

</td><td>

 

</td><td>

tls\_ssl\_certs-   SSL ports: 443, 8443, 9443, 636 \(ldaps\), 993 \(imaps\), 995 \(popssl\), 989, 990
-   StartTLS ports: 25 \(smtp\), 110, 143, 389, 21, 587 \(smtp\)

</td></tr><tr><td>

vmapp

</td><td>

Application Classification \[discovery\_classy\_appl\]

</td><td>

vmapp\_https \(port 5480\) and vmapp6\_https \(port 9443\)

</td></tr><tr><td>

wbem

</td><td>

CIM Classification \[discovery\_classy\_cim\]

</td><td>

wbem\_https \(port 5989\)

</td></tr><tr><td>

winrm

</td><td>

Windows Classification \[discovery\_classy\_windows\]

</td><td>

winrm \(port 5985\) and winrm\_ssl \(port 5986\)

</td></tr><tr><td>

wins

</td><td>

Process Classification \[discovery\_classy\_proc\]

</td><td>

ms-nb-ns \(port 137\)

</td></tr><tr><td>

wmi

</td><td>

Windows Classification \[discovery\_classy\_windows\]

</td><td>

epmap \(port 135\)

</td></tr></tbody>
</table>This table shows you other common ports and protocols that Discovery uses.

|Name|Service name|Port|Details|Creates|Protocol|
|----|------------|----|-------|-------|--------|
|afp|Apple File Protocol|548| | |TCP|
|BEA Weblogic| |7001| |cmdb\_ci\_app\_server|TCP|
|dns|Domain Name Service|53|To resolve the name of each IP Address| |TCP/UDP|
|epmap|Microsoft RPC \(WMI, DCOM\)|135|Windows Systems| |TCP|
|ftp| |21| | |TCP|
|hp-pdl-datastr|Printer PDL Data Stream|9100|HP Printers| |TCP|
|http|HyperText Transfer Protocol|80|Web Servers|cmdb\_ci\_web\_server|TCP|
|https|HyperText Transfer Protocol over Secure Socket|443|Secure Web Servers|cmdb\_ci\_web\_server|TCP|
|IBM DB2| |50000| | |TCP|
|IBM MQSeries| |1414| | |TCP|
|IBM Websphere| |9080| | |TCP|
|IBM Web sphere SSL| |9443| | |TCP|
|IMAPS| |993| | |TCP|
|pip \(Internet Print Protocol\)|IP Phone/ Session Initiation Protocol|5060| | |TCP|
|LDAP| |389| | |TCP|
|LDAPs| |636| | |TCP|
|Microsoft netbios| |139| | |TCP|
|Microsoft-ds| |445| | |TCP|
|ms-nb-ns| |137| | |UDP|
|Microsoft SQL server| |1433| | |TCP|
|MySQL| |3306| | |TCP|
|Nagios NRPE| |5666| | |TCP|
|nfs| |2049| | |TCP/UDP|
|Oracle TNS| |1521| | |TCP|
|POP3| |110| | |TCP|
|postgresql| |5432| |cmdb\_ci\_database|TCP|
|printer|Printer|515|Printers| |TCP|
|sip|SIP \(Session Initiation Protocol\)|5060| | |TCP|
|slp|Service Location Protocol \(SLP\)|427| | |TCP/UDP|
|smtp|TCP|25| | | |
|smux \(SNMP multiplexing\)| |199| | | |
|snmp|Simple Network Management Protocol|161|Network Devices| |UDP|
|snmptrap| |162| | |UDP|
|ssh|Secure Shell Service|22|Unix Systems| |TCP|
|sunrpc| |111| | |TCP|
|telnet| |23| | |TCP|
|TIBCO Rendezvous| |7500| | |TCP|
|Tomcat HTTP| |8080| | |TCP|
|vmapp6\_https| |9443| | |TCP|
|vmapp\_https|vCenter Server Appliance Web Interface using https|5480| | |TCP|
|wbem\_https|CIM-XML via HTTPS\(WBEM\)|5989|CIM Classification| |TCP|
|wins|Windows Internet Name Service|137|NetBIOS Name Resolver| |UDP|

## Windows and dynamic ports

Supported Windows machines can have dynamic ports ranges: 49152-65535 for both TCP and UDP.

**Parent Topic:**[Port probes](r_PortProbes.md)

